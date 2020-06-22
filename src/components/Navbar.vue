<template>
  <nav>
    <div class="menu-item"><a href="#">Меню 1</a></div>
    <Dropdown title="Меню 2" :items="menu2" />
    <Dropdown title="Меню 3" :items="menu3" />
    <Dropdown title="Меню 4" :items="menu4" />
    <div class="menu-item"><a href="#">Меню 5</a></div>
  </nav>
</template>

<script>
import Dropdown from './Dropdown';

export default {
  name: 'navbar',
  components: {
    Dropdown
  },
  data () {
    return {
      menu2: [
        {
          title: 'Подменю 2 - 1',
          link: '#'
        },
        {
          title: 'Подменю 2 - 2',
          link:'#'
        },
        {
          title: 'Подменю 2 - 3',
          link: '#'
        }
      ],
      menu3: [
        {
          title: 'Подменю 3 - 1',
          link: '#'
        },
        {
          title: 'Подменю 3 - 2',
          link:'#'
        },
        {
          title: 'Подменю 3- 3',
          link: '#'
        }
      ],
      menu4: [
        {
          title: 'Подменю 4 - 1',
          link: '#'
        },
        {
          title: 'Подменю 4 - 2',
          link:'#'
        },
        {
          title: 'Подменю 4 - 3',
          link: '#'
        }
      ]

    }
  }
}
</script>

<style>
nav {
  display: flex;
  align-items: center;
  justify-content: center;
  min-width: 1024px;
  max-width: 1280px;
}

nav .menu-item {
  flex:1 1 auto;
  justify-content: center;
  color: #FFF;
  padding: 20px 20px;
  position: relative;
  text-align: center;
  border-bottom: 3px solid transparent;
  display: flex;
  transition: 0.4s;
}

nav .menu-item.active,
nav .menu-item:hover {
  background-color: #444;
  border-bottom-color: #FF5858;
}

nav .menu-item a {
  color: inherit;
  text-decoration: none;
}
</style>