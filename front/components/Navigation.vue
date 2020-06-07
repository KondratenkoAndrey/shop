<template>
  <div>
    <v-navigation-drawer
      v-model="sidebar"
      disable-resize-watcher
      app
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in menuItems"
          :key="i"
          :to="item.path"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar
      flat
      color="white"
      app
    >
      <span class="d-lg-none">
        <v-app-bar-nav-icon @click.stop="sidebar = !sidebar" />
      </span>
      <v-toolbar-title>
        <router-link to="/" tag="span" style="cursor: pointer">
          {{ title }}
        </router-link>
      </v-toolbar-title>
      <v-spacer />
      <v-toolbar-items class="hidden-sm-and-down">
        <v-tabs>
          <v-tab
            v-for="(item, i) in menuItems"
            :key="i"
            :to="item.path"
            router
          >
            <v-icon left dark>
              {{ item.icon }}
            </v-icon>
            {{ item.title }}
          </v-tab>
        </v-tabs>
      </v-toolbar-items>
      <Cart />
      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>
    </v-app-bar>
  </div>
</template>

<script>
import Cart from '~/components/Cart.vue'

export default {
  components: {
    Cart
  },
  data () {
    return {
      sidebar: false,
      clipped: false,
      drawer: false,
      menuItems: [
        {
          icon: 'mdi-home',
          title: 'Главная',
          path: '/'
        },
        {
          icon: 'mdi-book-open-variant',
          title: 'Каталог',
          path: '/catalog'
        },
        {
          icon: 'mdi-truck',
          title: 'Доставка',
          path: '/delivery'
        },
        {
          icon: 'mdi-information',
          title: 'О компании',
          path: '/about'
        },
        {
          icon: 'mdi-contacts',
          title: 'Контакты',
          path: '/contacts'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Super shop'
    }
  }
}
</script>
