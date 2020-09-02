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
 @media print {
  *,
  *:before,
  *:after {
    background: transparent !important;
    color: #000 !important;
    box-shadow: none !important;
    text-shadow: none !important;
  }

  a,
  a:visited {
    text-decoration: underline;
  }

  a[href]:after {
    content: " (" attr(href) ")";
  }

  abbr[title]:after {
    content: " (" attr(title) ")";
  }

  a[href^="#"]:after,
  a[href^="javascript:"]:after {
    content: "";
  }

  pre,
  blockquote {
    border: 1px solid #999;
    page-break-inside: avoid;
  }

  thead {
    display: table-header-group;
  }

  tr,
  img {
    page-break-inside: avoid;
  }

  img {
    max-width: 100% !important;
  }

  p,
  h2,
  h3 {
    orphans: 3;
    widows: 3;
  }

  h2,
  h3 {
    page-break-after: avoid;
  }
}

pre,
code {
  font-family: Menlo, Monaco, "Courier New", monospace;
}

pre {
  padding: .5rem;
  line-height: 1.25;
  overflow-x: scroll;
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

.modest-no-decoration {
  text-decoration: none;
}

html {
  font-size: 12px;
}

@media screen and (min-width: 32rem) and (max-width: 48rem) {
  html {
    font-size: 15px;
  }
}

@media screen and (min-width: 48rem) {
  html {
    font-size: 16px;
  }
}

body {
  line-height: 1.85;
}

p,
.modest-p {
  font-size: 1rem;
  margin-bottom: 1.3rem;
}

h1,
.modest-h1,
h2,
.modest-h2,
h3,
.modest-h3,
h4,
.modest-h4 {
  margin: 1.414rem 0 .5rem;
  font-weight: inherit;
  line-height: 1.42;
}

h1,
.modest-h1 {
  margin-top: 0;
  font-size: 3rem;
}

h2,
.modest-h2 {
  font-size: 2rem;
}

h3,
.modest-h3 {
  font-size: 1.5rem;
}

h4,
.modest-h4 {
  font-size: 1.25rem;
}

h5,
.modest-h5 {
  font-size: 1rem;
}

h6,
.modest-h6 {
  font-size: .88rem;
}

small,
.modest-small {
  font-size: .707em;
}

/* https://github.com/mrmrs/fluidity */

img,
canvas,
iframe,
video,
svg,
select,
textarea {
  max-width: 100%;
}

@import url(http://fonts.googleapis.com/css?family=Open+Sans+Condensed:300,300italic,700);

@import url(http://fonts.googleapis.com/css?family=Arimo:700,700italic);

html {
  font-size: 18px;
  max-width: 100%;
}

body {
  color: #444;
  font-family: 'Open Sans Condensed', sans-serif;
  font-weight: 300;
  margin: 0 auto;
  max-width: 48rem;
  line-height: 1.45;
  padding: .25rem;
}

h1,
h2,
h3,
h4,
h5,
h6 {
  font-family: Arimo, Helvetica, sans-serif;
}

h1,
h2,
h3 {
  border-bottom: 2px solid #fafafa;
  text-align: left;
}

blockquote {
  border-left: 8px solid #fafafa;
  padding: 1rem;
}

pre,
code {
  background-color: #fafafa;
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
    max-width: 80%;
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
  .description{
    font-size: 0.85em;
  }
</style>
