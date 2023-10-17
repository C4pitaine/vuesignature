<template>
  <div class="form">
    <input type="text" v-model="nameForm" placeholder="NOM">
    <input type="text" v-model="firstnameForm" placeholder="PRENOM">
    <input type="email" v-model="emailForm" placeholder="EMAIL">
    <input type="text" v-model="telForm" placeholder="TELEPHONE">
    <select v-model="citationForm">
        <option v-for="option in citationOptions" :value="option" :key="option.value">{{ option.text }}</option>
    </select>
  </div>
  
  <CarteVisite :name="nameForm" :firstname="firstnameForm" :email="emailForm" :tel="telForm" :citation="citationForm"></CarteVisite>
</template>
  
  <script>
  import CarteVisite from './CarteVisite.vue'

  export default {
    name: 'FormVue',
    props: {
      
    },
    data() {
      return {
        nameForm: "",
        firstnameForm: "",
        emailForm: "",
        telForm: "",
        citationOptions: [
          {value:"1" ,text: "Citation1", author: "author 1"},
          {value:"2" ,text: "Citation2", author: "author 2"},
          {value:"3" ,text: "Citation3", author: "author 3"},
          {value:"4" ,text: "Citation4", author: "author 4"},
          {value:"5" ,text: "Citation5", author: "author 5"}
        ],
        citationForm: "",
      }
    },
    components: {
      CarteVisite
    }
  }
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped>
    .form{
      width:25%;
      height:1000px;
      background-color: grey;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;

        input{
          width:90%;
          height:30px;
          margin: 20px 0;
          font-size: 20px;
        }
        select{
          width:90%;
          height:30px;
          margin: 20px 0;
          font-size: 20px;
        }
    }
  </style>