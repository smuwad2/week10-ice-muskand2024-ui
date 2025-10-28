<script>
    export default {
        name: 'BlogPost',
        props: {
            subject:String,
            entry: String,
            mood: String,
        },
        computed: {
            imageSrc() {
                return `/assets/${this.mood.toLowerCase()}.png`
            }
        }

    }
</script>


<template>
    <!-- Card layout for a blog post -->
    <div class="card mb-2" style="width: 18rem; margin-bottom: 1rem;">
        <img :src="imageSrc" :alt="mood + ' mood'" class="card-img-top" />
        <div class="card-body">
            <h5 class="card-title">{{ subject }}</h5>
            <p class="card-text">{{ entry }}</p>
        </div>
    </div>
 

</template>

