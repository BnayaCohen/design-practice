<template>
    <div class="user-preview flex">
        <div class="user-img" :style="{ background: `url(${user.imgUrl}) no-repeat center center/cover` }"></div>
        <div class="flex flex-column">
            <h5>{{ user.fullname }}</h5>
            <p>{{ user.profession }}</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'userPreview',
    props: {
        user: Object
    },
}
</script>