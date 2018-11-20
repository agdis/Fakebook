<template>
  <div>
    <div class="container">
      <div id="post" class="blog-container">
            <div class="friend-info-container">
              <h4>{{title }}</h4>
              <br>
              <p id="postp">{{body }}</p>                
                <br>
            </div>            
        </div>
        <ul>
          <li>
            <nuxt-link id="view" :to="'/'">Back</nuxt-link>
          </li>
        </ul>
    </div>
    <br>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  validate ({ params }) {
    return !isNaN(+params.id)
  },
  async asyncData({params, error}){
    const {data} = await axios.get(`https://jsonplaceholder.typicode.com/posts/${+params.id}`)
    return data
  }
}

</script>

<style scoped>
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
  
</style>
