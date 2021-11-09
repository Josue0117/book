<template>
  <div class="content">
    <nav class="navbar navbar-expand-lg">
      <div class="title">
        <p class="navbar-title">{{ navBarTitle }}</p>
        <p class="navbar-subtitle">{{ navBarSubtitle }}</p>
      </div>
      <button class="navbar-toggler" @click="showMenu">
        <span class="navbar-toggler-icon"></span>
      </button>

      <div
        class="navbar-collapse collapse"
        id="navbarSupportedContent"
      >
        <ul class="navbar-nav mr-auto">
          <li class="nav-item">
            <NuxtLink class="nav-link" to="/">
              <div class="container-link-to-index">
                <div class="link-to-index left"></div>
                <div class="link-to-index center"></div>
                <div class="link-to-index rigth"></div>
              </div>
            </NuxtLink>
          </li>
          <li class="nav-item">
            <NuxtLink class="nav-link" to="#">Skills</NuxtLink>
          </li>
          <li class="nav-item">
            <NuxtLink class="nav-link" to="#">Acerca de mi</NuxtLink>
          </li>
          <li class="nav-item">
            <NuxtLink class="nav-link" to="#">Proyecto</NuxtLink>
          </li>
        </ul>
      </div>
    </nav>
  </div>
</template>

<script>
import { CARD_1_TITLE, CARD_1_SUBTITLE } from '@/constants-static-texts.js'
export default {
  data: () => {
    return {
      navBarTitle: CARD_1_TITLE,
      navBarSubtitle: CARD_1_SUBTITLE,
    }
  },
  methods: {
    showMenu() {
      const menu = document.getElementById('navbarSupportedContent')
      if (menu.classList.contains('show')) {
        menu.classList.remove('show')
      } else {
        menu.classList.add('show')
      }
    },
  },
}
</script>

<style scoped>
.content {
  background-color: #c4c4c4;
}

.navbar {
  padding: 0;
}

.title {
  margin-left: 8%;
  text-align: center;
}

p.navbar-title {
  color: white;
  text-align: center;
  margin-bottom: 0;
}

p.navbar-subtitle {
  color: #01A4FF;
}

.nav-link {
  color: #6B6666;
}

.nav-link:hover {
  color:white;
}

.link-to-index {
  border: solid 2px;
  display: none;
}

.left {
  border-right: #6B6666;
  border-radius: 5px 0px 0px 5px;
  width: 10px;
  height: 20px;
  margin-left: -13px;
  margin-bottom: -25px;
}

.center {
  border-radius: 5px;
  width: 25px;
  height: 30px;
}

.rigth {
  border-left: #6B6666;
  border-radius: 0px 5px 5px 0px;
  width: 10px;
  height: 20px;
  margin-left: 28px;
  margin-top: -25px;
}


@media (min-width: 954px) {
  p.navbar-title {
    font-size: 25px;
    margin-top: 10px;
    width: 100%;
  }

  p.navbar-subtitle {
    margin-top: -8px;
  }

  #navbarSupportedContent {
    position: absolute;
    right: 8%;
  }

  .container-link-to-index {
    margin-top: 5px;
  }

  .nav-link {
    margin-left: 20px;
    font-size: 18px;
  }

  .link-to-index {
    display: block;
  }
}

</style>
