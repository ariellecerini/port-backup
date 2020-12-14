<template>
<div class="col-lg-6">
    <div class="card card-list--hover shadow border-0">
        <div class="card-body py-5">
            <img
                :src="`/${post.attributes.image}`"
                class="img-fluid shadow mb-5"
            />
            <a 
            :href="`${post.attributes.url}`"
            >
                <h6 :class="`text-${ct} display-4 text-uppercase`">
                    {{ post.attributes.title }}
                </h6>
            </a>
            <p class="description mt-3">
                {{ post.attributes.description }}
            </p>
            <div>
                <span v-for="tag in tags" v-if="tags.length > 0"
                    :class="`badge badge-pill badge-${ct}`">
                    {{ tag }}
                </span>
            </div>
            <a 
            :class="`btn`" 
            :href="`${post.attributes.url}`" 
            style="`margin-left: 40px; margin-top: 10px;`">
            View Website
            </a>

        </div>
    </div>
</div>
</template>

<script>
export default {
    layout: 'arielle-cerini',
    name: 'post-card-web',
    props: {
        post: Object,
        prefix: String,
        ct: String
    },
    computed: {
        tags () {
           return this.post.attributes.tags ? this.post.attributes.tags.split(',') : []
        }
    }
}
</script>