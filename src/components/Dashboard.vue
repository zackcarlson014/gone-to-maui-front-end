<template>
  <v-app id="inspire">

    <v-app-bar app>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title>Gone to Maui</v-toolbar-title>
    </v-app-bar>

    <v-navigation-drawer
      v-model="drawer"
      fixed
      temporary
    >
      <!--  -->
    </v-navigation-drawer>

    <v-main class="grey lighten-2">
      <v-container>
        <v-row>
          <template v-for="n in categories">
            <v-col
              :key="n"
              class="mt-2"
              cols="12"
            >
              <strong>{{ n }}</strong>
            </v-col>

            <v-col
              v-for="j in 6"
              :key="`${n}${j}`"
              cols="6"
              md="2"
            >
              <v-sheet height="150"></v-sheet>
            </v-col>
          </template>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
    export default {
        name: 'Dashboard',
        data: () => ({ 
            drawer: null,
            categories: [
                'Legs',
                'Back',
                'Shoulders',
                'Core',
                'Chest',
                'Arms',
            ],
        }),
    }
</script>