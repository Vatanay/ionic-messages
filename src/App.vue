<template>
  <IonMessages :messages="messages"/>
</template>

<script>
import IonMessages from "@/components/IonMessages.vue";

export default {
  name: 'App',
  components: {
    IonMessages
  },
  data() {
    return {
      messages: [{
        text: "Hello there!",
        sender: "me",
        avatar: "http://via.placeholder.com/360x360"
      },{
        text: "Hi.",
        sender: "them",
        avatar: "http://via.placeholder.com/360x360"
      }]
    };
  },
}
</script>

