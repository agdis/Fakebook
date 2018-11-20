<template>
    <div class="container">
        <div class="myheader">
            My Friend's Profile
        </div>
        <hr>        
        <div class="friendcontainer">
            <div class="img-container">
                <img src="http://carta.fiu.edu/theatre/wp-content/uploads/sites/9/2015/12/avatar.jpg" alt="">
                <hr id="userline">
                <h3>{{name }}</h3>
                <span>Email: {{email}}</span>
            </div>
            <div class="friend-info-container">
                <ul id="friendsList">
                    <li id="friendsList-li"><b>Username:</b> {{username}}</li>
                    <li id="friendsList-li"><b>Address:</b> <br><b>Street:</b> {{address.street}}<br> <b>Suite:</b> {{address.suite}}<br><b>City:</b> {{address.city}}<br><b>Zipcode:</b> {{address.zipcode}}</li>
                    <li id="friendsList-li"><b>Phone:</b> {{phone}}</li>
                    <li id="friendsList-li"><b>Website:</b> {{website }}</li>
                    <li id="friendsList-li"><b>Company:</b> {{company.name }}<br><b>CatchPhrase:</b> {{company.catchPhrase}}<br><b>Bs:</b> {{company.bs}}<br></li>                   
                </ul>
                <br>
                <nuxt-link to="/users" id="profile">Back</nuxt-link>
            </div>            
        </div>
    </div>
</template>


<script>
import axios from 'axios'

export default {
  validate ({ params }) {
    return !isNaN(+params.id)
  },
  async asyncData({params, error}){
    const {data} = await axios.get(`https://jsonplaceholder.typicode.com/users/${+params.id}`)
    return data
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
</style>
