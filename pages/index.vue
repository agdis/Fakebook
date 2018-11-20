<template>
  <div>
    <div class="container">
      <div class="blogpost-field">
        <div class="blog-post-container">
          <textarea name="postblog" id="postblog" placeholder="create your blog post here.."></textarea>
          <input id="createpost-btn" type="button" name="submit" value="Share now">
        </div>
      </div>
    </div>
    <div class="container" v-for="post in posts">
      <div id="post" class="blog-container">
            <div class="friend-info-container">
              <h4>{{ post.title }}</h4>
              <br>
              <p id="postp">{{ post.body }}</p>                
                <br>
            </div>            
        </div>
        <ul>
          <li>
            <nuxt-link id="view" :to="'/posts/' + post.id">readmore</nuxt-link>
          </li>
        </ul>
    </div>
    <br>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  title: '',
  async asyncData () {
    const {data} = await axios.get('https://jsonplaceholder.typicode.com/posts')
    return {posts:data}
  }
}
</script>

<style scoped>
.blogpost-field{
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}
  .blog-post-container{    
    grid-column:2;
    grid-row: 4;
    width: 100%;
    color: black;
  }
  #postblog{
    width: 500px;
    height: 150px;
    padding: 20px;
    resize: none;
    border: 2px solid #00aba9;
    box-shadow: 1px 1px 2px grey;
    border-radius: 10px;
    font-size: 14pt;    
  }
  #createpost-btn{
    width: 120px;
    float: right;
    margin-top: 10px;
    color:white;
    background-color: #00aba9;
    border: none;
    outline: none;
    font-weight: 500;
    font-size: 12pt;
    padding: 10px;
    border-radius: 10px;
    box-shadow: 1px 1px 2px grey;
  }
  #createpost-btn:hover{
    font-size: 14pt;
    margin-bottom: -3px;
  }
  .blogs-container{
    grid-column: 4;
    grid-row: 4;
  }
  .blog-container{
    position: relative;
    width: 80%;
    margin-left: 10%;
    margin-top: 20px;
    padding: 5px;
    font-size: 14pt;  
  }
  #view{
    color: blue;
    font-weight: 500;
  }
  #view:hover{
    margin-bottom: -3px;
  }
  #post{
    text-align: center;
  }
  #postp{
    display:block;
    text-overflow: ellipsis;
    width: 100%;
    overflow: hidden;
    white-space: nowrap;
  }
</style>
