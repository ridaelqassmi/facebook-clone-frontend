<template>
<div class="container">
    <add-post @submitedPost="submitedPost"/>
    <PostsComponent v-for="Post in Posts" :key="Post.id" :image="Post.image" :nbLikes="Post.nbLikes" :postContent="Post.postContent" :user="Post.user" />
  
</div>
    
</template>
<script>
import axios from 'axios';
import addPost from './addPost.vue';
import PostsComponent from './PostsComponent.vue'
const Url="http://localhost:8080/";
export default {
    components:{
        addPost,
        PostsComponent
    },
    data(){
        return{
            Posts:[],
        }
    },
    methods:{
        submitedPost(content,file){
            console.log(file);
            let obj = {nbLikes:10,postContent:content}
            let formData = new FormData();
            formData.append("file",file);
            formData.append("id",1);

            formData.append("Post",JSON.stringify(obj))
            axios({
                  url:Url+"post/save",
                Headers:{
                    'Content-type':'multipart/form-data'
                },
                data:formData,
                method:"post"
            }).then(res => this.Posts = [res.data,...this.Posts])
        },
        console(){
            console.log(this.Posts[0]);
        }
    },
     mounted(){
        
        this.Posts = axios.get(Url+"post").then(response=> this.Posts =response.data);
        
    }
}
</script>
<style scoped>
.container{
    min-width: 800px;
    margin:20px auto;
    display:flex;
    flex-direction: column;

}
</style>