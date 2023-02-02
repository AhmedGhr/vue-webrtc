<template>
  <div class="mt-3">
    <div class="text-center" v-if="user">
      Welcome back <span class="font-weight-bold text-info">{{ user.displayName }}</span
      >, <a href="#" role="button" class="text-danger" @click="$emit('logout')">logout</a>
    </div>
    <div class="container text-center">
      <div class="row justify-content-center">
        <div class="col-10 col-md-10 col-lg-8 col-xl-7">
          <h4 class="display-4 mb-2" style="color : #23a49b">EnovaMeet</h4>
            <p>
                In this app , I have used vue-webrtc component , and Firebase to make a realtime video-chat app
            </p> 
          <router-link class="btn mr-2" to="/login" style="background-color :#23a49b" v-if="!user"
            >Log In</router-link 
          >
          &nbsp;&nbsp;
          <router-link class="btn  mr-2" to="/register" style="background-color :#23a49b" v-if="!user"
            >Register</router-link
          >
          <router-link class="btn  mr-2" to="/rooms" v-if="user" style="background-color :#23a49b">Rooms</router-link>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "Home",
  props : ['user']
  
}
</script>


