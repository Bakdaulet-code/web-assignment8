<template>
    <nav>
        <v-navigation-drawer v-model="drawer" dark app mini-variant mini-variant-width="100" class="white">
            <v-list>
                <v-list-item class="mb-16">
                    <v-list-item-content>
                        <v-icon class="mb-2" large color="red">fas fa-dragon</v-icon>
                    </v-list-item-content>
                </v-list-item>
            </v-list>
            <v-list flat>
                <v-list-item router to="/">
                <v-list-item-content>
                    <v-icon class="mb-2" color="black">fas fa-folder</v-icon>
                </v-list-item-content>
                </v-list-item>
                <v-list-item router to="/">
                <v-list-item-content>
                    <v-icon class="mb-2" color="black">fas fa-calendar-check</v-icon>
                </v-list-item-content>
                </v-list-item>
                 <v-list-item router to="/">
                <v-list-item-content>
                    <v-icon class="mb-2" color="red">fas fa-envelope</v-icon>
                </v-list-item-content>
                </v-list-item>
                <v-list-item router to="/">
                <v-badge color="blue" dot overlap>
                        <v-list-item-content>
                            <v-icon class="mb-2" color="black">fas fa-bell</v-icon>
                        </v-list-item-content>
                    </v-badge>
                    </v-list-item>
                <v-list-item router to="/">
                        <v-list-item-content>
                            <v-icon class="mb-2" color="black">fas fa-share-alt</v-icon>
                        </v-list-item-content>
                    </v-list-item>
                    <v-list-item router to="/">
                        <v-list-item-content>
                            <v-icon class="mb-2" color="black">fas fa-image</v-icon>
                        </v-list-item-content>
                    </v-list-item>
            </v-list>
            <v-list style="position: absolute; bottom:0" class="ml-5" flat>
                 <v-list-item router to="/">
                <v-list-item-content>
                    <v-icon color="black">fas fa-users</v-icon>
                    </v-list-item-content>
                </v-list-item>
                 <v-list-item router to="/">
                <v-list-item-content>
                    <v-icon color="black">fas fa-cog</v-icon>
                    </v-list-item-content>
                </v-list-item>
                <v-list-item router to="/">
                <v-list-item-avatar class="mb-5">
                <v-badge
                    bordered
                    bottom
                    color="green"
                    dot
                    offset-x="10"
                    offset-y="10"
                    >
        <v-avatar size="40">
          <v-img src="mbappe.jpg"></v-img>
        </v-avatar>
      </v-badge>
              </v-list-item-avatar>
                </v-list-item>
            </v-list>
        </v-navigation-drawer>
    </nav>
</template>
<script>
export default {
    data: () =>({
        drawer: true
    })
}
</script>