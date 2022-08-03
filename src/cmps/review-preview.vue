<template>
    <li class="review-preview flex flex-column">
        <p>{{review.content}}</p>
        <user-preview :user="review.byUser" />
    </li>
</template>

<script>
import userPreview from './user-preview.vue'

export default {
    name: 'reviewPreview',
    props: {
        review: Object
    },
    components:{
      userPreview
    }
}
</script>