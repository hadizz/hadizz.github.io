<template>
  <header>
    <img alt="Hadi Zare Avatar" src="../assets/avatar-3.png" />
    <div class="avatar-info">
      <h1 class="name">Hadi Zare</h1>
      <span class="job">Frontend Developer</span>
      <small>Yazd, Iran</small>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header',
};
</script>

<style scoped>
header {
  display: flex;
  flex-direction: row;
  background-color: orangered;
  color: white;
  padding: 20px;
  border-radius: 15px 15px 0 0;
}

.avatar-info {
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin-left: 20px;
}

.name {
  font-size: 28px;
}

.job {
  font-size: 22px;
}

@media screen and (max-width: 590px) {
  /* img {
    width: 50%;
    height: 50%;
  } */
  .name {
    font-size: 23px;
  }
  .job {
    font-size: 18px;
  }
}

@media screen and (max-width: 350px) {
  img {
    width: 35%;
    height: 35%;
  }
  .avatar-info {
    margin-left: 10px;
  }
  .name {
    font-size: 15px;
  }
  .job {
    font-size: 11px;
  }
  small {
    font-size: 11px;
  }
}
</style>
