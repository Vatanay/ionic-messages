<template>
  <div class="messages">
    <div v-for="(message, index) in messages" :key="index" :class="{'from-me': message.sender === 'me', 'from-them': message.sender === 'them'}">
      <img :src="message.avatar" class="avatar">
      {{message.text}}
    </div>
  </div>
</template>
<script>
export default {
  name: 'IonMessages',
  props: {
    messages: {
      type: Object,
      default: () => ({}),
    }
  }
}
</script>

<style scoped>
.messages {
  font-family: Helvetica Neue,Arial;
  display: flex;
  flex-direction: column;
  width: 100%;
}

.messages .avatar{
  width: 28px;
  height: 28px;
  border-radius: 100%;
  position:absolute;
  top:0;
}

.messages > div {
  display: flex;
  word-wrap: break-word;
  line-height: 24px;
  position: relative;
  padding: 7.5px 15px;
  border-radius: 7.5px;
  margin-bottom: 10px;
}
.messages div.from-them{
  border-top-left-radius: 0;
  align-self: flex-start;
  background: #E5E5EA;
  color: black;
  float: left;
  margin-left: 35px;
}

.messages div.from-them .avatar{
  left:-35px;
}

.messages div.from-me{
  border-top-right-radius: 0;
  align-self: flex-end;
  color: white;
  background: #0B93F6;
  float: right;
  margin-right: 35px;
}
.messages div.from-me .avatar{
  right:-35px;
}

.messages div:before{
  position: absolute;
  top: 0;
  z-index: 100;
  content: '';
  border-style: solid;
}
.messages  div.from-me:before{
  right: -7px;
  border-width: 8px 8px 0 0;
  border-top-right-radius: 2px;
  border-color: #0B93F6 transparent transparent transparent;
}
.messages div.from-them:before{
  left: -7px;
  border-width: 0 8px 8px 0;
  border-top-left-radius: 2px;
  border-color: transparent #E5E5EA transparent transparent;
}
</style>