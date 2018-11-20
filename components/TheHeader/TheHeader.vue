<template>
    <header class="container-fluid">
        <nuxt-link id="logo" to="/">MyBlogs</nuxt-link>       
        <nav>
            <ul class="mynav-links">
                <li><nuxt-link to="/">Home</nuxt-link></li>
                <li><nuxt-link to="/profile">Profile</nuxt-link></li>
                <li><nuxt-link to="/Users">Friends</nuxt-link></li>
                <li><nuxt-link to="/about">About</nuxt-link></li>
            </ul>
        </nav>
    </header>
</template>

<script>
export default {

}
</script>

<style>
header{    
    background-color: #00aba9;
    display: grid;
    grid-template-columns: (2, auto);
    height: 60px;
    box-shadow: 2px 2px 10px grey;
}
#logo{
    font-size: 1.3em;
}
#logo, li a{
    padding: 1em 2em;
    display:block;
    text-transform: uppercase;
    text-decoration: none;
    font-weight: bold;       
    color: #FFFF;
}
nav{
    margin-top: -50px;
    margin-right: 20px;
    justify-self: right;
}
ul{
    text-align: center;
    list-style: none;
}
li{
    display: inline;
}
li a{
    font-size: .8em; 
    display: inline-block;
    background-color: none;
    width: 130px;
    border:none;
    outline: none;
}
li a:hover{
    text-decoration: none;
    color: #FFFF;
    border-bottom: 3px solid #008080;
}
#logo:hover{
    text-decoration: none;
    color:darkblue;
}
li a:hover,
li a:active,
li a.nuxt-link-exact-active{
    border-bottom: 3px solid #008080;
}
</style>
