<template>
  <div class="app">
    <div class="container">
      <nav class="navbar">
        <div>
          <img class="col-3" src="@/assets/logo.png">
        </div>
      </nav>
      <div>
        <div class="row logo">
          <div class="col-3 offset-4">
            <img class="w-100" src="@/assets/contacts.png">
          </div>
        </div>
        <div class="row enter">
          <div class="col-5 d-flex flex-column">
            <label for='name'>Имя *</label>
            <input type="text" name="name"  id='name' class="form-control" v-model="postData.name">
            <label for='email'>E-mail *</label>
            <input type="email" name="email" id='email' class="form-control" v-model="postData.email">
          </div>
          <div class="col-6 offset-1 d-flex flex-column">
            <label for='comment'>Коментарий *</label>
            <input type="comment" name="comment" id='comment' class="form-control" v-model="postData.comment">
          </div>
        </div>
        <div class="row button">
          <button type="button" class="btn btn-danger offset-9 col-3" @clicl="post(postData)">Записать</button>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import axios from 'axios';
export default {
  data() {
    return {
      postData: {
        name: "",
        email: "",
        comment: "",
      }
    }
  },
  methods: {
    post(data) {
      const path = 'app.php';
      axios.post(path, data)
        .then(() => {
          console.log(this.postData);
        })
    }
  }
};
</script>

<style>
.app {
  background-color: #2d3136;
}
label {
  color: white
}
#comment, #email, #name {
  background-color: #2f3338;
  color: white;
  border-color: #4c4f53
}
.logo {
  margin-top: 50px;
}

.button {
  margin-top: 20px;
  padding-bottom: 20px;
}
</style>