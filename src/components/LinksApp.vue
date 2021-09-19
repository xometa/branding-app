<template>
  <div class="body">
    <div class="container">
      <main class="main">
        <Header />
        <div class="links" v-for="(link, index) in links" :key="index">
          <Link
            :text="link.text"
            :icon="link.icon"
            :url="link.url"
            :styles="link.styles"
          />
        </div>
        <Footer />
      </main>
    </div>
  </div>
</template>

<script>
import Header from "./Header.vue";
import Link from "./Link.vue";
import Footer from "./Footer.vue";

export default {
  name: "LinksApp",
  components: {
    Header,
    Link,
    Footer,
  },
  data() {
    return {
      links: [
        {
          text: "GitHub",
          icon: "fab fa-github",
          url: "https://github.com/xometa/",
          styles: {
            color: "#FFF",
            background: "#24292F",
          },
        },
        {
          text: "Linkedin",
          icon: "fab fa-linkedin",
          url: "https://linkedin.com/in/gerardo-zometa-díaz-",
          styles: {
            color: "#FFF",
            background: "#0A63BC",
          },
        },
        {
          text: "Instagram",
          icon: "fab fa-instagram",
          url: "https://instagram.com/zometadiaz",
          styles: {
            color: "#FFF",
            background: "#F04A48",
          },
        },
        
        {
          text: "Twitter",
          icon: "fab fa-twitter",
          url: "https://twitter.com/zometadiaz/",
          styles: {
            color: "#FFF",
            background: "#00acee",
          },
        },
      ],
    };
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  font-family: "Roboto", sans-serif;
}

*,
*::before,
*::after {
  box-sizing: border-box;
}

body {
  background-image: url("../assets/Background.jpg");
  background-position: center;
  background-size: cover;
}

.container {
  padding: 32px;
  background: linear-gradient(
    to bottom,
    rgba(0, 0, 0, 0.8),
    rgba(0, 0, 0, 0.8)
  );
  min-height: 102vh;
}

.main {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 50%;
}

@media only screen and (max-width: 600px) {
  .main {
    width: 80%;
  }
}

.links {
  width: 100%;
}
</style>
