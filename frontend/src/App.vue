<template>
    <v-app id="inspire">
        <v-navigation-drawer v-model="drawer" app temporary>
            <v-list>
                <v-list-item v-for="[icon, text,link] in links" :key="icon" :to="link" link>
                    <v-list-item-icon>
                        <v-icon>{{ icon }}</v-icon>
                    </v-list-item-icon>

                    <v-list-item-content>
                        <v-list-item-title>{{ text }}</v-list-item-title>
                    </v-list-item-content>
                </v-list-item>
            </v-list>
        </v-navigation-drawer>

        <v-app-bar app>
            <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>

            <v-toolbar-title>vueCom</v-toolbar-title>
        </v-app-bar>

        <v-main>
            <router-view />
        </v-main>
    </v-app>
</template>

<script>
export default {
    data: () => ({
        drawer: null,
        links: [
            ["mdi-home", "Home" , "/"],
            ["mdi-account-cowboy-hat", "About", "/about"]          
        ]
    })
};
</script>
