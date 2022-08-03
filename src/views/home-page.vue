<template>
    <main class="home-page main-layout">
        <article class="hero-container flex flex-column">
            <img src="../assets/img/illustration-intro.png" alt="hero">

            <div class="page-background"></div>

            <h2 class="hero-title">All your files in one secure location, accessible anywhere.</h2>
            <p>Fylo stores all your most important files in one secure location. Access them wherever you need, share
                and collaborate with friends family, and co-workers.</p>
            <button class="btn">Get Started</button>
        </article>

        <feature-list />

        <article class="more-details-container flex flex-wrap align-center">
            <div>
                <img src="../assets/img/illustration-stay-productive.png" alt="">
            </div>
            <div class="flex flex-column" style="max-width:500px;">
                <h2>Stay productive, wherever you are</h2>
                <p>Never let location be an issue when accessing your files. Fylo has you covered for all of your file
                    storage needs.</p>
                <p>Securely share files and folders with friends, family and colleagues for live collaboration. No email
                    attachments required.</p>
                <a href="#">See how Fylo works <svg width="16" height="16" xmlns="http://www.w3.org/2000/svg"
                        xmlns:xlink="http://www.w3.org/1999/xlink">
                        <defs>
                            <circle id="b" cx="6" cy="6" r="6" />
                            <filter x="-25%" y="-25%" width="150%" height="150%" filterUnits="objectBoundingBox" id="a">
                                <feOffset in="SourceAlpha" result="shadowOffsetOuter1" />
                                <feGaussianBlur stdDeviation="1" in="shadowOffsetOuter1" result="shadowBlurOuter1" />
                                <feColorMatrix
                                    values="0 0 0 0 0.384313725 0 0 0 0 0.878431373 0 0 0 0 0.850980392 0 0 0 0.811141304 0"
                                    in="shadowBlurOuter1" />
                            </filter>
                        </defs>
                        <g fill="none" fill-rule="evenodd">
                            <g transform="translate(2 2)">
                                <use fill="#000" filter="url(#a)" xlink:href="#b" />
                                <use fill="#62E0D9" xlink:href="#b" />
                            </g>
                            <path d="M8.582 6l-.363.35 1.452 1.4H5.333v.5h4.338L8.22 9.65l.363.35 2.074-2z"
                                fill="#1B2330" />
                        </g>
                    </svg></a>
            </div>
        </article>

        <section class="reviews-container">
            <ul class="clean-list flex flex-wrap">
                <review-preview v-for="(review, i) in reviews" :key="i" :review="review" />
            </ul>
        </section>

        <section class="contact-us-container flex flex-column">
            <h2>Get early access today</h2>
            <p>It only takes a minute to sign up and our free starter tier is extremely generous. If you have any
                questions, our support team would be happy to help you.</p>
            <div>
                <input type="text" placeholder="email@example.com">
                <button class="btn">Get Started For Free</button>
            </div>
        </section>
    </main>
</template>                     

<script>
import featureList from '../cmps/feature-list.vue'
import reviewPreview from '../cmps/review-preview.vue'

export default {
    name: 'homePage',
    data() {
        return {
            reviews: [
                {
                    content: 'Fylo has improved our team productivity by an order of magnitude. Since making the switch our team has become a well-oiled collaboration machine.',
                    byUser: {
                        imgUrl: 'src/assets/img/profile-1.jpg',
                        fullname: 'Satish Patel',
                        profession: 'Founder & CEO, Huddle',
                    }
                },
                {
                    content: 'Fylo has improved our team productivity by an order of magnitude. Since making the switch our team has become a well-oiled collaboration machine.',
                    byUser: {
                        imgUrl: 'src/assets/img/profile-2.jpg',
                        fullname: 'Bruce McKenzie',
                        profession: 'Founder & CEO, Huddle',
                    }
                },
                {
                    content: 'Fylo has improved our team productivity by an order of magnitude. Since making the switch our team has become a well-oiled collaboration machine.',
                    byUser: {
                        imgUrl: 'src/assets/img/profile-3.jpg',
                        fullname: 'Iva Boyd',
                        profession: 'Founder & CEO, Huddle',
                    }
                },
            ]
        }
    },
    components: {
        featureList,
        reviewPreview,
    }
}
</script>