<template>
  <section id="footer-links">
    <div class="row">
      <img
        class="logo"
        src="../assets/images/logotype-2-139x23.png"
        alt="logo"
      />
      <ul class="row">
        <li v-for="(link, index) in links" :key="link.title + index">
          <a :href="link.link">{{ link.title }}</a>
        </li>
      </ul>
      <ul class="row">
        <li v-for="icon in icons" :key="icon.title">
          <a href="#"><i class="fab" :class="icon.class"></i></a>
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
  name: "FooterLink",
  props: ["links"],
  data() {
    return {
      icons: [
        {
          name: "instagram",
          class: "fa-instagram",
        },
        {
          name: "instagram",
          class: "fa-linkedin-in",
        },
        {
          name: "instagram",
          class: "fa-facebook-f",
        },
        {
          name: "instagram",
          class: "fa-twitter",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
#footer-links {
  height: 60%;
  margin: 30px 0;

  .row {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .logo {
    width: 7%;
    cursor: pointer;
  }
}
</style>