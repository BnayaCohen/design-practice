<template>
    <ul class="features-container clean-list flex flex-wrap">
        <feature-preview v-for="(feature, i) in features" :key="i" :feature="feature" />
    </ul>
</template>

<script>
import featurePreview from './feature-preview.vue'

export default {
    name: 'featureList',
    data() {
        return {
            features: [
                {
                    imgUrl: 'src/assets/img/icon-access-anywhere.svg',
                    title: 'Access your files, anywhere',
                    details: 'The ability to use a smartphone, tablet, or computer to access your account means your files follow you everywhere.',
                },
                {
                    imgUrl: 'src/assets/img/icon-security.svg',
                    title: 'Security you can trust',
                    details: '2-factor authentication and user-controlled encryption are just a couple of the security features we allow to help secure your files.',
                },
                {
                    imgUrl: 'src/assets/img/icon-collaboration.svg',
                    title: 'Real-time collaboration',
                    details: 'Securely share files and folders with friends, family and colleagues for live collaboration. No email attachments required.',
                },
                {
                    imgUrl: 'src/assets/img/icon-any-file.svg',
                    title: 'Store any type of file',
                    details: 'Whether you\'re sharing holidays photos or work documents, Fylo has you covered allowing for all file types to be securely stored and shared.',
                },
             ]
        }
    },
    components: {
        featurePreview
    }
}
</script>