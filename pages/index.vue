<template>
  <div>
    <section class="hero is-primary has-text-centered">
      <div class="hero-body">
        <div class="container">
          <h1 class="title">
            Tech Blog
          </h1>
          <h2 class="subtitle">
            An awesome blog
          </h2>
        </div>
      </div>
    </section>

    <section class="section">
      <div class="container">
        <div class="columns">
          <div class="column is-three-fifths is-offset-one-fifth">
            <div v-for="post in posts" :key="post.slug" class="mb-5">
              <div>
                <br/>
                </div>  
              <h3 class="title is-4">
                <nuxt-link :to="post.slug">
                <!-- <nuxt-link :to="'/blog/' + post.slug"> -->
                <!-- <nuxt-link :to="/blog/${post.slug}"> -->
                  {{ post.title }}
                </nuxt-link>
              </h3>
              <div>
                {{ post.description }}
              </div>
            </div>
            
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  async asyncData ({ $content }) {
    const posts = await $content('posts').sortBy('createdAt', 'desc').fetch()
    return { posts }
  }
}
</script>

<style>
  section > .section{
    display:flex;
  }
  section > .container{
    display: flex;
  }
  h1{
    background: #fe5000;
  }
  h3 a {
    color: #053575;
  }
  h3 a:hover {
    color: #faf000;
  }
</style>