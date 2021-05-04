<template>
<div id="addBlog">
  <h1>Blogify</h1>
  <h2>Add a new Blog Post</h2>
  <form>
    <label >Blog Title</label>
    <input type="text" class="text" v-model="title" required />
    <label >Blog Content</label>
    <textarea v-model="content"></textarea>
    <div id="checkbox">
      <label >Day</label>
      <input type="checkbox" value="Day" v-model="categories" />
      <label >Morning</label>
      <input type="checkbox" value="Morning" v-model="categories" />
      <label >Afternoon</label>
      <input type="checkbox" value="Afternoon" v-model="categories" />
      <label >Evening</label>
      <input type="checkbox" value="Evening" v-model="categories" />
      <label >Night</label>
      <input type="checkbox" value="Night" v-model="categories" />
    </div>
    <label >Author</label>
    <select v-model="author">
      <option v-for="author in authors" :key="author">{{author}}</option>
    </select>
    <div >
    <button class="but-1" @click="post">Add the Blog</button>
    </div>
  </form>
  <div id="preview">
    <h3><strong>Preview Blog</strong></h3>
  <p><strong>Blog title: </strong></p>
  <p>{{title}}</p>
  <p><strong>Blog Content:</strong></p>
  <p>{{content}}</p>
  <p><strong>Time of the day: </strong><ul>
    <li v-for="category in categories" :key="category">{{category}}</li>
  </ul>
   </p>
  <p><strong>Author:</strong> {{author}}</p>
  </div>
</div>
</template>

<script>
export default {
  data(){
    return{
      title: "",
      content : "" , 
      categories: [],
      author: "",
      authors: ["sanket", "george Martin", "William"]
    }
  },
  methods:{
    post: function(){
      return alert("Blog Added");
    }
  }
}
</script>

<style scoped>
h1{
color: coral;
font-weight: bolder;
font-size: 40px;
}

#addBlog{
  box-sizing: border-box;
  margin: 20px auto;
  max-width: 500px;
}

label{
  display: block;
  margin: 20px 0 10px;
}

.text{
  display: block;
  width: 100%;
  padding: 8px;
}

h3{
  margin-top: 10px;
}

textarea{
  display: block;
  width: 100%;
  padding: 8px;
}

#preview{
padding: 10px 20px;
border: 1px solid black;
margin: 30px 0;
}

#checkbox label{
  display: inline-flex;
}

#checkbox input{
  margin-right: 12px;
}

.but-1{
  margin-top: 2%;
}
</style>