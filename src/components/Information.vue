<template>
  <div class="f-row">
    <img :alt="alt" :src="src" />
    <div v-if="alt == 'phone'">
      <span>{{ text }}</span>
    </div>
    <div v-else>
      <a v-if="alt === 'email'" :href="'mailto:' + href" target="_blank">{{
        text
      }}</a>
      <a v-else :href="href" target="_blank">{{ text }}</a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Information',
  props: {
    alt: String,
    src: String,
    text: String,
    href: String,
  },
};
</script>

<style scoped>
.f-row {
  display: flex;
  flex-direction: row;
  align-items: center;
  /* justify-content: center; */
  margin-bottom: 5px;
}
img {
  width: 30px;
  height: 30px;
  margin-right: 8px;
}
a {
  color: white;
  text-decoration: none;
}
</style>
