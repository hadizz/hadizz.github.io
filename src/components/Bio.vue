<template>
  <div>
    <h2>Bio</h2>
    <p id="bio"></p>
  </div>
</template>

<script>
export default {
  name: 'Bio',
  props: {
    bio: String,
  },
  mounted: function() {
    document.getElementById('bio').innerHTML = this.bio;
    document.getElementById(
      'link'
    ).style = `color: orangered;text-decoration: none;font-weight: bold;`;
  },
};
</script>

<style scoped>
div {
  margin: 1rem 0;
  padding: 0 20px;
}
h2 {
  margin-bottom: 0.3rem;
}
p {
  text-align: justify;
}
</style>
