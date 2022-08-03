<template>
    <li class="feature-preview flex flex-column">
        <div>
            <img :src="feature.imgUrl" alt="">
        </div>
        <h4>{{ feature.title }}</h4>
        <p>{{ feature.details }}</p>
    </li>
</template>

<script>
export default {
    name: 'featurePreview',
    props: {
        feature: Object
    },
}
</script>