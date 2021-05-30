<template>
  <v-app :style="{background: $vuetify.theme.themes.dark.background}">
    <v-container fluid>
      <v-row>
        <v-col cols="12" sm="3" class="border">
          
            <v-app-bar flat color="rgba(0,0,0,0)">
               <v-btn
                tile
                color="white" x-large block>
                <v-icon left color="red">
                fas fa-plus
                </v-icon>
                <v-divider
                  class="mx-3"
                  vertical
                ></v-divider>
                New Conversation
              </v-btn>
            </v-app-bar>
           
              <v-app-bar flat color="rgba(0,0,0,0)">
                <v-toolbar-title class="title">
              Chat 
            </v-toolbar-title>

            <v-spacer></v-spacer>
            <v-btn
              icon
            >
              <v-icon>fas fa-ellipsis-h</v-icon>
            </v-btn>
              </v-app-bar>
             <v-app-bar flat color="rgba(0,0,0,0)">

       <v-text-field
            filled
            label="Search Here"
            append-icon="mdi-magnify"
            color="grey"
          ></v-text-field>
             </v-app-bar>
            
 <v-list two-line color="rgba(0,0,0,0)">
      <v-list-item-group
        v-model="selected"
        active-class="blue lighten-4"
        multiple
      >
        <template v-for="(item, index) in items">
          <v-list-item :key="item.title">
            <v-badge
        bordered
        bottom
        color="green"
        dot
        offset-x="22"
        offset-y="26"
      >
            <v-list-item-avatar>
            <v-img :src="item.avatar"></v-img>
          </v-list-item-avatar>
            </v-badge>
            <template >
              <v-list-item-content>
                <v-list-item-title v-text="item.title"></v-list-item-title>

                <v-list-item-subtitle v-text="item.subtitle"></v-list-item-subtitle>
              </v-list-item-content>
            </template>
          </v-list-item>

          <v-divider
            v-if="index < items.length - 1"
            :key="index"
          ></v-divider>
        </template>
      </v-list-item-group>
    </v-list>
           
        </v-col>
        <v-col cols="12" sm="6" class="border">
          <v-app-bar color="rgba(0,0,0,0)" flat>
            <v-badge
                bordered
                bottom
                color="green"
                dot
                offset-x="11"
                offset-y="13"
              >
                <v-avatar class="mt-n7" size="40" elevation="10">
                  <img src="psgg.jpg" />
                </v-avatar>
             </v-badge>
             <v-toolbar-title class="title pl-0 ml-2 mt-n4">
               GENERAL CHAT: FOOTBALL CLUB "PSG"
            </v-toolbar-title>
            <v-spacer></v-spacer>
            <v-toolbar-title class="title pl-0 mr-2 mt-n4">
               Members:
            </v-toolbar-title>
            <v-btn
              color="black"
              icon
              class="mt-n5 mr-n2"
              outlined
              max-height="35"
              max-width="35"
            >
              <v-icon small>fas fa-plus</v-icon>
            </v-btn>
            <v-avatar class="mt-n5 mr-2" size="30" elevation="10">
                  <img src="navas.png" />
            </v-avatar>
            <v-divider vertical inset class="mt-n1"></v-divider>
            <v-btn
              color="black"
              icon
              class="mt-n5"
            >
              <v-icon>mdi-cog</v-icon>
            </v-btn>
          </v-app-bar>
           <v-app-bar color="rgba(0,0,0,0)" flat class="mb-16">
          
            <v-spacer></v-spacer>
            <v-card class="mt-10 mr-2" max-width="350px" color="teal darken-2" dark>
    <v-list-item three-line>
      <v-list-item-content>
        <div class=" mb-4">
          Heyyy, my winners! How are you feeling today? 
        </div>
        <v-list-item-subtitle>16 mins ago</v-list-item-subtitle>  
      </v-list-item-content>
    </v-list-item>
  </v-card >
            <v-badge
                bordered
                bottom
                color="green"
                dot
                offset-x="10"
                offset-y="10"
              >
            <v-avatar class="mt-n5 " size="30" elevation="10">
                  <img src="coach.jpg" />
            </v-avatar>
            </v-badge>
          </v-app-bar>
           <v-app-bar color="rgba(0,0,0,0)" flat class="mb-16">
          <v-badge
                bordered
                bottom
                color="green"
                dot
                offset-x="16"
                offset-y="9"
              >
            <v-avatar class="mt-n5 mr-2" size="30" elevation="10">
                  <img src="neymar.png" />
            </v-avatar>
            </v-badge>
            <v-card class="mt-10 " max-width="350px">
    <v-list-item three-line>
      <v-list-item-content>
        <div class=" mb-4">
          Hey! Me and Icardi have found motivational photos for you!
        </div>
        <v-list-item-subtitle>12 mins ago</v-list-item-subtitle>  
      </v-list-item-content>
    </v-list-item>
  </v-card >
          </v-app-bar>
          <v-app-bar color="rgba(0,0,0,0)" flat class="mb-16">
            <v-badge
                bordered
                bottom
                color="green"
                dot
                offset-x="10"
                offset-y="10"
              >
            <v-avatar class="mt-n5 " size="30" elevation="10">
                  <img src="icardi.png" />
            </v-avatar>
            </v-badge>
            <v-card class="mt-10 ml-2" max-width="350px">
    <v-list-item three-line>
      <v-list-item-content>
        <div class=" mb-4">
          Icardi shared 3 photos :<br><br>
           <v-avatar
                size="60"
                tile
                class="mr-2"
              >
                <v-img src="1.jpg"></v-img>
              </v-avatar>
              <v-avatar
                size="60"
                tile
                class="mr-2"
              >
                <v-img src="2.jpg"></v-img>
              </v-avatar>
              <v-avatar
                size="60"
                tile
              >
                <v-img src="3.jpg"></v-img>
              </v-avatar>
        </div>
       
        <v-list-item-subtitle>10 mins ago</v-list-item-subtitle>  
      </v-list-item-content>
    </v-list-item>
  </v-card >
  
              <v-btn
              color="black"
              icon
              class="mb-n10"
            >
              <v-icon color="red">fas fa-thumbs-up</v-icon>
            </v-btn>
           
          </v-app-bar>
           <v-app-bar color="rgba(0,0,0,0)" flat class="mb-8">
          
            <v-spacer></v-spacer>
            <v-card class="mt-10 mr-2" max-width="350px" color="teal darken-2" dark>
    <v-list-item three-line>
      <v-list-item-content>
        <div class=" mb-4">
          Yes, that would be awesome!
          See You, Guys, on our Stadium!
        </div>
        <v-list-item-subtitle>5 mins ago</v-list-item-subtitle>  
      </v-list-item-content>
    </v-list-item>
  </v-card >
            <v-badge
                bordered
                bottom
                color="green"
                dot
                offset-x="10"
                offset-y="10"
              >
            <v-avatar class="mt-n5 " size="30" elevation="10">
                  <img src="coach.jpg" />
            </v-avatar>
            </v-badge>
          </v-app-bar>
          <v-app-bar color="rgba(0,0,0,0)" flat class="mb-16">
          
            <v-spacer></v-spacer>
            <v-card class="mt-10 mr-2" max-width="350px" color="teal darken-2" dark>
    <v-list-item three-line>
      <v-list-item-content>
        <div class=" mb-4">
          Good Luck, Guys, after 5 hours we will play against Bayer!
        </div>
        <v-list-item-subtitle>3 mins ago</v-list-item-subtitle>  
      </v-list-item-content>
    </v-list-item>
  </v-card >
            <v-badge  
                bordered
                bottom
                color="green"
                dot
                offset-x="10"
                offset-y="10"
              >
            <v-avatar class="mt-n5 " size="30" elevation="10">
                  <img src="coach.jpg" />
            </v-avatar>
            </v-badge>
          </v-app-bar>
         <v-app-bar color="rgba(0,0,0,0)" flat>
            <v-text-field
            
            v-model="message"
            append-icon="mdi-emoticon"
            :append-outer-icon="message ? 'mdi-send' : 'mdi-microphone'"
            filled
            clear-icon="mdi-close-circle"
            clearable
            label="Message"
            type="text"
            @click:append-outer="sendMessage"
            @click:clear="clearMessage"
          ></v-text-field>
         </v-app-bar>
        </v-col>
        <v-col cols="12" sm="3">
          <v-card class="text-center mt-8 mb-3" shaped >
             <v-badge
                bordered
                bottom
                color="green"
                dot
                offset-x="11"
                offset-y="13"
              >
                <v-avatar class="mt-n7" size="60" elevation="10">
                  <img src="coach.jpg" />
                </v-avatar>
             </v-badge>
                <v-card-title class="layout justify-center">Pochettino Coach</v-card-title>
                <v-card-subtitle class="layout justify-center">Coach Of PSG football club</v-card-subtitle>
                <v-list>
                </v-list>
              </v-card>
              <v-expansion-panels v-model="panel" multiple>
    <v-expansion-panel>
      <v-expansion-panel-header>
        <h3>Information</h3>   
      </v-expansion-panel-header>
      <v-expansion-panel-content>
        
      </v-expansion-panel-content>
    </v-expansion-panel>
    <v-expansion-panel>
      <v-expansion-panel-header>
        <h3>Images(99+)</h3>   
      </v-expansion-panel-header>
      <v-expansion-panel-content>
        
      </v-expansion-panel-content>
    </v-expansion-panel>
 <v-expansion-panel >
      <v-expansion-panel-header>
        <h3>Files(3) </h3>  
      </v-expansion-panel-header>
      <v-expansion-panel-content>
        <v-list shaped>
      <v-list-item-group
        
      >
        <v-list-item
          v-for="(item, i) in files"
          :key="i"
        >
          <v-list-item-icon>
            <v-icon v-text="item.icon" color="red"></v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title v-text="item.text"></v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list-item-group>
    </v-list>
      </v-expansion-panel-content>
    </v-expansion-panel>
    <v-expansion-panel>
      <v-expansion-panel-header>
        <h3>Pinned items</h3>   
      </v-expansion-panel-header>
      <v-expansion-panel-content>
        
      </v-expansion-panel-content>
    </v-expansion-panel>

    
  </v-expansion-panels>
  
        </v-col>
      </v-row>
    </v-container>
  </v-app>
</template>
<script>
export default {
  data: () => ({
     selected: [2],
      items: [
        {
           avatar: 'neymar.png',
          subtitle: `Let's go to our training area together at 10:10AM !`,
          title: 'Neymar Winger',
        },
        {
           avatar: 'mbappe.jpg',
          subtitle: `My Training Plans for Today`,
          title: 'My Private Chat',
        },
        {
           avatar: 'navas.png',
          subtitle: 'Did you see our coach today?',
          title: 'Navas GoalKeeper',
        },
        {
           avatar: 'draxler.png',
          subtitle: 'PSG wants to make agreement with me',
          title: 'Draxler MidFielder',
        },
        {
           avatar: 'kimpembe.png',
          subtitle: 'Don`t be late, bro! Today is suitable day to train!',
          title: 'Kimpembe Captain Defender',
        },
        {
           avatar: 'coach.jpg',
          subtitle: `Yesterday you showed your best! Congrats!`,
          title: 'Pochettino Coach',
        },
        {
           avatar: 'icardi.png',
          subtitle: `Wish I could come, but I'm out of town this weekend.`,
          title: 'Icardi Forward',
        },
        {
           avatar: 'simonsxavi.jpg',
          subtitle: 'Brother, could you teach me how to shoot?',
          title: 'Xavi Simons Young Talent',
        },
      ],
      files: [
        { text: 'Landing_page.zip', icon: ' mdi-cloud-upload' },
        { text: 'Requirements.pdf', icon: ' mdi-cloud-upload' },
        { text: 'Uwagi.docx', icon: ' mdi-cloud-upload' },
      ],
     panel: [2],
    
      password: 'Password',
      show: false,
      message: 'Type a message here',
      marker: true,
      iconIndex: 0,

      
  }),
  computed: {
    theme() {
      return this.$vuetify.theme.dark ? "dark" : "light";
    },
    
  },
  methods: {
      sendMessage () {
        this.resetIcon()
        this.clearMessage()
      },
      clearMessage () {
        this.message = ''
      },
      resetIcon () {
        this.iconIndex = 0
      },
    },
  
};
</script>
<style scoped>
.border {
  border-right: 1px solid grey;
}
</style>
