<template>
  <main class="p-5 my-0 mx-auto bg-white">
    <input id="tab1" type="radio" name="tabs" checked>
    <label for="tab1">{{ data[0].title }}</label>
    <section id="content1" v-html="data[0].content"></section>

    <input id="tab2" type="radio" name="tabs">
    <label for="tab2">{{ data[1].title }}</label>
    <section id="content2" v-html="data[1].content"></section>

    <input id="tab3" type="radio" name="tabs">
    <label for="tab3">{{ data[2].title }}</label>
    <section id="content3" v-html="data[2].content"></section>

    <input id="tab4" type="radio" name="tabs">
    <label for="tab4">{{ data[3].title }}</label>
    <section id="content4" v-html="data[3].content"></section>
  </main>
</template>

<script>
import DataJson from '../../../data.json'

export default {
  data() {
    return {
      data: DataJson
    }
  }
}
</script>

<style scoped>
::v-deep #content3 ul li {
    list-style-position: inside;
}

.tabArea {
  border-bottom: 1px solid #ccc;
}
section {
  display: none;
  padding: 20px;
  position: absolute;
  width: 100%;
  right: 0
}
input {
  display: none;
}
label {
  display: inline-block;
  margin: 0 0 -1px;
  padding: 15px 25px;
  font-weight: 600;
  text-align: center;
  color: #bbb;
  border: 1px solid transparent;
}
label:hover {
  color: #888;
  cursor: pointer;
}
input:checked + label {
  color: #555;
  border: 1px solid #ddd;
  border-top: 2px solid black;
  border-bottom: 1px solid #fff;
}
#tab1:checked ~ #content1,
#tab2:checked ~ #content2,
#tab3:checked ~ #content3,
#tab4:checked ~ #content4 {
  display: block;
}
@media screen and (max-width: 650px) {
  label {
    text-align: left;
    display: block;
  }
  label:before {
    margin: 0;
    font-size: 18px;
  }
  section {
    position: relative;
  }
  .tabArea {
    border: none;
  }
}
@media screen and (max-width: 400px) {
  label {
    padding: 15px;
  }
}
</style>