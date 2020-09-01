<template>
  <div id="root">
    <section id="hero">
        <div class="container">
          <h1 class="title">
            Jared Stanley
          </h1>
          <h2 class="subtitle">
            Creative Technologist | UX/Design Manager
          </h2>
      </div>
    </section>

    <section id="section">
      <div class="container">
        <div class="columns">

            <div v-for="post in posts" :key="post.slug">
              <nuxt-link :to="post.slug">
                  
              <div class="post">  
                <h3 class="s">
                  <!-- <nuxt-link :to="'/blog/' + post.slug"> -->
                  <!-- <nuxt-link :to="/blog/${post.slug}"> -->
                    {{ post.title }}
                </h3>
                <div class="date">
                  {{ post.month }}/{{ post.day }}/{{ post.year }}
                </div>
                <div class="description">
                  {{ post.description }}
                </div>
              </div>
              </nuxt-link>
              
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
  *{
    padding: 0;
    margin: 0;
  }
  #root{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  #hero, #section{
    
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    max-width: 1440px;
  }
  
  .container{
    /* display: flex; */
    max-width: 80%;
  }
  h1{
    width: 100%;
    background: #f5d467;
  }
  h3 a {
    color: #053575;
  }
  div a:hover {
    color: #066534;
  }
  div a {
     text-decoration: none;
  }
  .post{
   
    background:ivory;
    margin: 10px;
    padding: 10px;
  }
  .date{
    display: inline;
    font-size: 0.75em;
    background-color:greenyellow;
    border-radius: 4px;
    padding: 2px;
    
  }
  .description{
    font-size: 0.85em;
  }
</style>