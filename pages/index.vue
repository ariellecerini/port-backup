<template>


    <div class="profile-page">
        <section class="section-profile-cover my-0"></section>
        <section class="section section-skew">
            <div class="container">
                <card shadow class="card-profile mt--300" no-body>
                    <div class="px-4">

                            
                                <div class="font-weight-800">
                                <p>Critical Designer + Visual Coder + Dinosaur + Educator + Maker + Creator + Inventor + Artist + Design Rebel + Dinosaur + Web Designer + Academic + Researcher + Professional Student + Entrepreneur + Individual + Dreamer + Idealist</p>
                                </div>

                                <div id="title_info">
                                    <h1 id="subtitle"> PhD. Student @ RPI</h1>
                                </div>
                                    <br>
                            
                    </div>
                </card>



                
            </div>
        </section>
       
       
      
    </div>
</template>
<script>
import Exhibit from '~/components/Exhibit.vue'

export default {
  layout: 'arielle-cerini',
  components: {
    Exhibit
  },
  props: ['slug'],
  async asyncData() {
    const resolve = require.context('~/posts/', true, /\.md$/)
    const imports = resolve
      .keys()
      .map((key) => {
        const [, slug] = key.match(/\/(.+)\.md$/)
        return Object.assign(resolve(key), { slug })
      })
    return {
      posts: imports
    }
  }
}
</script>
<style>
img {
    max-width: 100%;
}
.card-body {
    max-width: 100%;
}
.text-link {
    color: black;
    text-decoration: underline;
}
.text-link:hover {
    color: black;
}
.company-name {
    font-weight: 800;
}
</style>
