<template>
  <div class="header">
    <!-- <h2 style="white-space:pre-line">{{message}}</h2> -->
    <div :class="{ red: isRed }">
      {{ message }}
    </div>
    <div class="section">
      <div class="texts">
        <textarea type="text" v-model="message" />
      </div>

      <button v-on:click="clear">Clear</button>
      <button v-on:click="makeCaptial">Cap</button>
      <input :checked="isRed" v-model="isRed" type="checkbox" @click="red" />
    </div>
  

  <div v-bind:style="{color: color_value.color}">
                {{name}} 
        </div>
        <p>Type Something..</p> 
        <form v-on:submit.prevent>
            <input v-on:keypress="submit" type="text" v-model="name" />
        </form>

        
        

        <select v-model="color_value">
            <option v-for="(col, index) in colors" v-bind:key="index" v-bind:value="{color: col}">{{col}}</option>
        </select>
        <ul>
            <li v-for="(item, index) in data" v-bind:key="index">{{item}}</li>
        </ul>

  </div>
</template>

<script>
export default {
  name: "main",
  data() {
    return {
      message: "Hello Vue I am ))))",
      isRed: false,
       colors: ["red", "yellow" , "black", "orange"],
      color_value: {
          color: "black"
      },
      name: "",
      data: []
    
    };
  },
  created: function () {
    console.log("created");
  },
  mounted: function () {
    console.log("mounted");
  },
  methods: {
    clear: function () {
      this.message = "";
    },
    makeCaptial: function () {
      this.message = this.message.toUpperCase();
    },
    red: function () {
      console.log(this.isRed);
    },
    submit: function(e) {
      if (e.keyCode === 13) {
        this.data.push(this.name);
        this.name = "";
      }
    }
  },
};
</script>

<style>
.section {
  display: flex;
  justify-content: center;
  align-items: center;
}
button {
  margin-top: -3px;
  padding-left: 10px;
  padding-top: 12px;
  padding-right: 10px;
  padding-bottom: 6px;
}
.red {
  color: red;
}
input[type="checkbox"] {
  height: 40px;
  width: 40px;
}
</style>