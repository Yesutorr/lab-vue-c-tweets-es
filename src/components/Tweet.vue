<script setup>
import ProfileImage from "./ProfileImage.vue";
import Timestamp from "./Timestamp.vue";
import User from "./User.vue";
import Message from "./Message.vue";
import Actions from "./Actions.vue";

const props = defineProps({
  tweet: Object,
});
</script>

<template>
  <div class="tweet">
    <ProfileImage :image="props.tweet.user.image" />
    <div class="body">
      <div class="top">
        <User :userData="props.tweet.user" />
        <Timestamp :time="props.tweet.timestamp" />
      </div>

    <Message :message="props.tweet.message" />


      <Actions />

    </div>

    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>

<style scoped>
a {
  color: #42b983;
}
</style>
