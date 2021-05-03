<template>
<div id="addBlog">
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
      <option :V-for="author in authors">{{author}}</option>
    </select>
  </form>
  <div id="preview">
    <h3>Preview Blog</h3>
  <p>Blog title: </p>
  <p>{{title}}</p>
  <p>Blog Content:</p>
  <p>{{content}}</p>
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
      author: " "
    },
    authors= ["Sanket", " Nikesh"]
  }
}
</script>

<style scoped>
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

</style>