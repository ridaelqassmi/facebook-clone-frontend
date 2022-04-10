<template>
    <div class="container">
        <div class="row">
            <img src="../../assets/man.png" alt="">
            <p>Rida elqassmi</p>
        </div>
        <div class="row">
            <img src="../../assets/man.png" alt="">
            <p>Friend</p>
        </div>
        <div class="row">
            <img src="../../assets/users-group.png" alt="">
            <p>Rida Groupe</p>
        </div>
        <div class="row">
            <img src="../../assets/store.png" alt="">
            <p>Market Place</p>
        </div>
        <div class="row">
            <img src="../../assets/games.png" alt="">
            <p>Gaming</p>
        </div>
        <div class="row">
            <img src="../../assets/man.png" alt="">
            <p>Rida elqassmi</p>
        </div>

    </div>
</template>
<style scoped>
.container{
  
    max-width: 300px;
    border-radius: 0px 18px;
    padding:10px 20px;
}
.row{
    display: flex;
    gap:10px;
    padding:10px 20px;
    align-items: center;
}
.row:hover{
    background:hsl(215, 64%, 91%);
    border-radius: 20px;
}
.row img{
    width:40px
}
.row p{
    font-size:20px;
    font-weight: bold;
    color:#050505
}

</style>