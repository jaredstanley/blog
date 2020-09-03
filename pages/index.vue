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
                <h3>
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
@import url(http://fonts.googleapis.com/css?family=Open+Sans+Condensed:300,300italic,700);

@import url(http://fonts.googleapis.com/css?family=Arimo:700,700italic);


html {
  font-size: 18px;
  max-width: 100%;
}

body {
  color: #444;
  font-family: 'Arimo', sans-serif;
  font-weight: 300;
  margin: 0 auto;
  max-width: 48rem;
  line-height: 1.45;
  padding: .25rem;
}

a,
a:visited {
  color: #3498db;
}

a:hover,
a:focus,
a:active {
  color: #2980b9;
}

h2{
 font-size: 1.25em;
}

h4,
h5,
h6 {
  font-family: 'Open Sans', Helvetica, sans-serif;
}

h1,
h2,
h3 {
  border-bottom: 2px solid #fafafa;
  text-align: left;
}

blockquote {
  border-left: 8px solid lightgray;
  padding: 1rem;
}

pre,
code {
  background-color: lightgray;
}
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
    /* max-width: 80%; */
  }
  h1{
    width: 100%;
    background: azure;
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
   
    background-color:azure; 
    margin: 20px 0px;
    padding: 10px;
  }
  .date{
    display: inline;
    font-size: 0.65em;
    background-color:lightblue;
    border-radius: 4px;
    padding: 4px;
    
  }
  .description, p{
    font-size: 0.85em;
    font-family: 'Open Sans', Helvetica, sans-serif;
  }

  ol, ul{
    font-size: 0.75em;
    font-weight: 100;
    list-style-type: circle;
  }

  
</style>
