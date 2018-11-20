<template>
    <div class="container">
        <div class="myheader">
            My Friends List
        </div>
        <hr>
        <div class="friendcontainer" v-for="user in users">
            <div class="img-container">
                <img src="http://carta.fiu.edu/theatre/wp-content/uploads/sites/9/2015/12/avatar.jpg" alt="">
                <hr id="userline">
                <h3>{{ user.name }}</h3>
                <span>Email: {{ user.email }}</span>
            </div>
            <div class="friend-info-container">
                <ul id="friendsList">
                    <li id="friendsList-li"><b>Phone:</b> {{ user.phone }}</li>
                    <li id="friendsList-li"><b>Website:</b> {{ user.website }}</li>
                    <li id="friendsList-li"><b>Company:</b> {{ user.company.name }}<br><b>CatchPhrase:</b> {{ user.company.catchPhrase }}<br><b>Bs:</b> {{ user.company.bs }}<br></li>                   
                </ul>
                <br>
                <nuxt-link id="viewprofile" :to="'/profile/' + user.id">...</nuxt-link>
            </div>            
        </div>
    </div>
</template>

<script>
import axios from 'axios'

export default {
  title: '',
  async asyncData () {
    const {data} = await axios.get('https://jsonplaceholder.typicode.com/users')
    return {users:data}
  }
}
</script>


<style scoped>
 img{     
     border:6px solid grey;
     width:60%;
     border-radius: 100%;
     box-shadow: 2px 4px 6px grey;
 }
 #userline{
     margin-top: 10px;
     margin-bottom: 10px;
     color: white;
 }
</style>
