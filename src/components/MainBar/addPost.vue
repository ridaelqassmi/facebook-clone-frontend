<template>
    <div class="container">
        <div class="row">
            <img src="../../assets/man.png" alt="">
            <input type="text" placeholder="What's on your mind!" v-model="content" @keyup.enter="submitForm">
        </div>
        
        <div class="row2">
            <div class="column">
                <img src="../../assets/live-stream.png" alt="">
                <p>Live video</p>
            </div>
            <div class="column">
                <img src="../../assets/video-player.png" alt="">
                <label for="upload">Image/videos<input ref='image' type="file" style="display:none"  id='upload'></label>
                
            </div>
            <div class="column">
                <img src="../../assets/smile.png" alt="">
                <p>Feeling</p>
            </div>
        </div>
    </div>

</template>

<script>

export default {
    data(){
        return {
            content:'',

        }
    },
    emits:['submitedPost'],
    methods:{
        submitForm(){
            this.$emit("submitedPost",this.content,this.$refs.image.files[0]);
        }
    }
   

}
</script>
<style scoped>
.container{
    background:white;
    padding:10px 20px;
    border-radius: 19px;
    
}
.row{
    display:flex;
    align-items:center;
    border-bottom: solid rgb(134, 133, 133,0.25) 2px;
    
}
.row2{
    display: flex;
    align-items: center;
   
    justify-content: space-evenly;
    
}
.row> input{
    flex:1;
    padding:15px 30px;
    border-radius:28px;
    background :#f0f2f5;
    outline:none;
    border:none;
    margin:20px;
    font-size: 20px;
    color:#1c1e21;
}
.row img,.row2 img{
    width:40px;
    padding:5px 10px
}
.column{
    flex:1;
    display:flex;
    align-items: center;
    justify-content: center;
    margin:10px 0;
    
}
.column:hover{
    background:hsl(215, 64%, 91%);
    border-radius: 20px;
}
.column p,.column label{
     font-size:20px;
    font-weight: bold;
    color:#050505
}
</style>