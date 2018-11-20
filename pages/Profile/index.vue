<template>
    <div class="container">
        <div class="myheader">
            My Profile
        </div>
        <hr>        
        <div class="friendcontainer">
            <div class="img-container">
                <img src="http://carta.fiu.edu/theatre/wp-content/uploads/sites/9/2015/12/avatar.jpg" alt="">
                <h3>Jeffrey Agdol</h3>
                <span>Email: agdoljeffrey@gmail.com</span>
            </div>
            <div class="friend-info-container">
                <ul id="friendsList">
                    <li id="friendsList-li"><b>Nickname:</b> Jeff</li>
                    <li id="friendsList-li"><b>Address:</b> Dumaguete City</li>
                    <li id="friendsList-li"><b>Phone:</b> 09551809406</li>
                    <li id="friendsList-li"><b>Moto: </b> Never give up whatever it takes, stay positive and keep movin.</li>                   
                </ul>
                <br>
            </div>            
        </div>
    </div>
</template>
<style scoped>
.img-container{
    background-color: #fafafa;
}
 img{     
     border:6px solid grey;
     width:60%;
     border-radius: 100%;
     box-shadow: 2px 4px 6px grey;
 }
</style>
