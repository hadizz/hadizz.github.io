<template>
  <header>
    <div class="left">
      <img alt="Hadi Zare Avatar" src="../assets/avatar-3.png" />
      <div class="avatar-info">
        <h1 class="name">Hadi Zare</h1>
        <span class="job">Frontend Developer</span>
        <small>Yazd, Iran</small>
      </div>
    </div>
    <div class="right">
      <div class="mr">
        <Information
          alt="linkedin"
          :src="images.linkedin"
          text="/in/hadizare"
          href="https://linkedin.com/in/hadizare"
        />

        <Information
          alt="web"
          :src="images.web"
          text="hadiz.ir"
          href="https://hadiz.ir"
        />
      </div>
      <div>
        <Information alt="phone" :src="images.phone" text="09025413379" />

        <Information
          alt="email"
          :src="images.email"
          text="hadizareoriginal@gmail.com"
          href="hadizareoriginal@gmail.com"
        />
      </div>
    </div>
  </header>
</template>

<script>
import Information from './Information';
import phoneImage from '../assets/phone.png';
import emailImage from '../assets/message.png';
import linkedinImage from '../assets/linkedin.svg';
import webImage from '../assets/web.png';

export default {
  name: 'Header',
  components: {
    Information,
  },
  data() {
    return {
      images: {
        phone: phoneImage,
        email: emailImage,
        linkedin: linkedinImage,
        web: webImage,
      },
    };
  },
};
</script>

<style scoped>
header {
  display: flex;
  flex-direction: row;
  justify-content: space-between;

  background-color: orangered;
  color: white;
  padding: 20px;
  border-radius: 15px 15px 0 0;
}
.left {
  display: flex;
  flex-direction: row;
}

.left img {
  width: 111px;
  height: 96px;
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

.right {
  display: flex;
  flex-direction: row;
  align-items: center;
}
.mr {
  margin-right: 20px;
}

.right img {
  width: 30px;
  height: 30px;
}

@media screen and (max-width: 1300px) {
  .mr {
    margin-right: 0;
  }

  header {
    flex-direction: column;
  }

  .right {
    flex-direction: column;
    align-items: unset;
    margin-top: 1rem;
  }
}

@media screen and (max-width: 590px) {
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
