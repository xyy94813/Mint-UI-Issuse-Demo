<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <button @click.prevent.stop="handleShowMsgBoxClick">show message box</button>
  </div>
</template>

<script>
import MessageBox from "mint-ui/lib/message-box/index";
import "mint-ui/lib/message-box/style.css";

export default {
  name: "HelloWorld",
  data() {
    return {
      msg: "For Mint-UI Issuse"
    };
  },
  methods: {
    handleShowMsgBoxClick(e) {
      const p = MessageBox.confirm("Are you sure?");
      p.then(
        action => {
          alert("confirm");
        },
        action => {
          alert("cancel");
        }
      );
      console.log(p);
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}
</style>
