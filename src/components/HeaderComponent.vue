<template>
   <div class="nav">
       <div class="nav-left">
           <div class="brand">
               <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/b/b8/2021_Facebook_icon.svg/1200px-2021_Facebook_icon.svg.png" alt=""  >
                <input type="search" >
           </div>
       </div>
       <div class="nav-middle">
           <a href="">
               <img src='../assets/home.png'>
           </a>
           <a href="">
               <img src='../assets/video.png'>
           </a>
           <a href="">
               <img src='../assets/users-group.png'>
           </a>
           <a href="">
               <img src='../assets/store.png'>
           </a>
           <a href="">
               <img src='../assets/games.png'>
           </a>
       </div>
       <div class="nav-right">
           
       </div>
   </div>
</template>


<style scoped>
.nav{
    display:grid;
    grid-template-columns: 2fr 3fr 2fr;
  
   padding:5px 50px 5px 50px;
    background: #ffffff;
    border-bottom: solid rgb(134, 133, 133,0.25) 2px ;
}
.nav-middle,.nav-left,.nav-right{
    display: flex;
    align-items: center;
   

}
.brand{
     display: flex;
    align-items: center;
}
.brand img{
    width:50px;
    height: 50px;
    border-radius: 50%;

}
.brand input{
    width:300px;

    padding:15px 30px;
    border-radius:28px;
    background :#f0f2f5;
    outline:none;
    border:none;
    margin:20px;
    font-size: 20px;
    color:#1c1e21;

}
.nav-middle{
display: flex;
justify-content: space-between;
}
.nav-middle> a> img{
    width: 40px;
}
.nav-middle> a{
    padding: 10px 50px;
    border-radius: 10px;
}
.nav-middle> a:hover{
    background:hsl(215, 64%, 91%);
    border-bottom: solid blue 5px;

}
</style>