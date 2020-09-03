<template>
  <section class="section">
    <div class="container">
      <div class="columns">
        <div>
          <h1 class="title">
            {{ post.title }}
          </h1>
          <div class="date">
            {{ post.month }}/{{ post.day }}/{{ post.year }}
          </div>
          
          <nuxt-content :document="post" />
    
          <div class="">
            <nuxt-link   to="/">
              View All Posts
            </nuxt-link>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  async asyncData ({ $content, params }) {
    const post = await $content('posts', params.slug).fetch()
    
    return { post }
  }
  
 
}
</script>

<style>
  .nuxt-content h2 {
    font-size: 1.25rem;
    font-weight: 600;
    line-height: 1.125;
    margin-top: 1.5rem;
    margin-bottom: 1.5rem;
  }
  .nuxt-content h2 > a::before {
    content: "#";
  }
  .nuxt-content h2 a .icon {
    height: 0.5rem;
    width: 0.5rem;
  }
</style>