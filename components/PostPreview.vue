<template>
    <NuxtLink :to="`/posts/${id}`">
        <h2>{{ title }}</h2>
    </NuxtLink>
</template>

<script>
export default {
    props: {
        id: { type: Number, required: true },
        title: { type: String, required: true }
    }
}
</script>

<style>
a {
    h2 {
        color:
            #000;
        width: max-content;
        position: relative;
        margin: 1rem 0;
    }

    h2:before {
        content: '';
        background-color: #2d6cea;
        width: 105%;
        height: 30%;
        position: absolute;
        bottom: 1px;
        left: 50%;
        transform: translatex(-50%);
        z-index: -1;
        transition: height 0.1s linear;
        opacity: 0.4;
    }

    h2:hover:before {
        height: 100%;
    }
}
</style>