<template>
  <v-app>
    <v-app-bar app clipped-leftS flat dark dense>
      <v-toolbar-title>
        <span>haskap controle panel</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
    </v-app-bar>

    <v-navigation-drawer app flat dark mini-variant permanent expand-on-hover>
      <v-list>
        <v-list-item
          v-for="item in navbarlist"
          :key="item.route"
          :to="item.route"
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>
          <v-list-item-content>{{ item.text }}</v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "haskap-panel",
  components: {},
  data: () => ({
    navbarlist: [
      {
        to: "Homr",
        icon: "mdi-home",
        text: "Home",
      },
    ],
  }),
};
</script>