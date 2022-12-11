<template>
  <div className="tweet" v-for="tweet in tweetsArray">
    <ProfileImage :image="tweet.user.image" />

    <div className="body">
      <div className="top">
        <User :name="tweet.user.name" :handle="tweet.user.handle" />
        <Timestamp :timestamp="tweet.timestamp" />
      </div>
      <Message :message="tweet.message" />
      <Actions />
    </div>

    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>

<script setup>
import ProfileImage from "../components/ProfileImage.vue";
import User from "../components/User.vue";
import Timestamp from "../components/Timestamp.vue";
import Message from "../components/Message.vue";
import Actions from "../components/Actions.vue";
const props = defineProps(["tweet"]);
const tweetsArray = props.tweet;
</script>

<style scoped>
a {
  color: #42b983;
}
</style>
