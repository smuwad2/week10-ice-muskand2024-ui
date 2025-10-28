<script>
    export default {
        // Add code if/as necessary
        // Hint: Add properties subject, entry and mood
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
    <!-- TODO: add your template code here Use boostrap card --> 
    <div class="card" style="width: 18rem;">
    <img :src="imageSrc" :alt="mood + ' mood'" class="card-img-top" />
    <div class="card-body">
        <h5 class="card-title">{{ subject }}</h5>
        <p class="card-text">{{ entry }}</p>
        <slot></slot>
    </div>
    </div>

</template>

