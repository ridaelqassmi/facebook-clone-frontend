<template>
    <div class="container">
        <div class="row">
            <img :src="'data:image/png;base64,'+user.profilePic" alt="">
            <p>{{user.firstName}} {{user.lastName}}</p>

        </div>
        <div class="content">
            <p>{{postContent}} </p>
        </div>
        <div class="images">
           <!-- <img src="../../assets/morocco.png" alt="">-->
           <img  :src="'data:image/png;base64,'+image" alt="">
        </div>
        <div class="detaill">
            <p>{{nbLikes}} likes</p>
        </div>
        <div class="options">
            <div class="column">
                <img src="../../assets/thumb-up.png" alt="">
                <p>like</p>

            </div>
            <div class="column">
                <img src="../../assets/icons8-commentaires-96.png" alt="">
                <p>commentaire</p>
            </div>
            <div class="column">
<img src="../../assets/icons8-commentaires-96.png" alt="">
                <p>commentaire</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props:["image","nbLikes","postContent","user"],
}
</script>
<style scoped>
.container{
 background:white;
    
    border-radius: 19px;
    width: 100%;
   box-shadow:  5px 5px 0px -1px rgba(157,157,157,0.32)

}
.row{
    display: flex;
    align-items: center;
    padding: 10px 15px ;
    gap:10px;
   
}
.content{
    padding:20px;

}
.content>p{
    font-size: 18px;
}
.row >img{
    margin: 10px 0px;
    width:50px;
   
    
}
.row p{
     font-size:20px;
    font-weight: bold;
    color:#050505
}
.images{
    width:100%;

}
.images>img{
    width:100%;
}
.options{
    display: flex;
    justify-content: space-evenly;
    border-top:solid black 1px;
    padding: 10px ;
    
}
.options .column{
    flex:1;
    display: flex;
    justify-content: center;
    align-items: center;
}
.options .column img{
    width:40px;
}
</style>