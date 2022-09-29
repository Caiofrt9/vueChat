<template>
  <v-app :style="{background: $vuetify.theme.themes.dark.background}">
    <v-container fluid>
      <v-row>
        <v-col cols="12" sm="4" class="border">
            
          <v-app-bar flat shaped  color="blue">
            <v-toolbar-title class="title " >
              My Chats 
            </v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn
              icon
            >
              <v-icon >fas fa-plus</v-icon>
            </v-btn>
              </v-app-bar>
             <v-app-bar flat color="rgba(0,0,0,0)">

                

       <v-text-field
            label="Pesquisar"
            append-icon="mdi-magnify"
            color="blue lighten-3"
            class="mt-10"
          ></v-text-field>
             </v-app-bar>
            
 <v-list two-line color="rgba(0,0,0,0)">
      <v-list-item-group
        v-model="selected"
        active-class="grey"
        multiple
      >
        <template v-for="(item, index) in items">
          <v-list-item :key="item.title">
            <v-badge
        bordered
        bottom
        color="blue"
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

        <!-- Segunda coluna -->

        <v-col cols="12" sm="8" class="border">
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
                  <img src="https://cdn.vuetifyjs.com/images/lists/1.jpg" />
                </v-avatar>
             </v-badge>
             <v-toolbar-title class="title pl-0 ml-2 mt-n4 " >
               User
            </v-toolbar-title>
            
          </v-app-bar>
           <v-app-bar color="rgba(0,0,0,0)" flat class="mb-16">
          
            <v-spacer></v-spacer>
            <v-card class="mt-10 mr-2" max-width="350px" color="blue" dark>
    <v-list-item three-line>
      <v-list-item-content>
        <div class=" mb-4">
          Lorem Ipsum is simply dummy text of the printing and typesetting industry. 
        </div>
        <v-list-item-subtitle>16 mins ago </v-list-item-subtitle>  
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
                  <img src="https://cdn.vuetifyjs.com/images/lists/1.jpg" />
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
                  <img src="https://cdn.vuetifyjs.com/images/lists/1.jpg" />
            </v-avatar>
            </v-badge>
            <v-card class="mt-10 " max-width="350px">
    <v-list-item three-line>
      <v-list-item-content>
        <div class="mb-4">
          Lorem Ipsum is simply dummy text of the printing and typesetting industry.
        </div>
        <v-list-item-subtitle>12 mins ago</v-list-item-subtitle>  
      </v-list-item-content>
    </v-list-item>
  </v-card >
            <v-btn
              color="black"
              icon
              class="mb-n10"
            >
              <v-icon>fas fa-ellipsis-h</v-icon>
            </v-btn>
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
                  <img src="https://cdn.vuetifyjs.com/images/lists/1.jpg" />
            </v-avatar>
            </v-badge>
            <v-card class="mt-10 ml-2" max-width="350px">
    <v-list-item three-line>
      <v-list-item-content>
        <div >
          Lorem Ipsum is simply dummy text of the printing and typesetting industry.<br><br>

        </div>
       
        <v-list-item-subtitle>12 mins ago</v-list-item-subtitle>  
      </v-list-item-content>
    </v-list-item>
  </v-card >
           
          </v-app-bar>
           <v-app-bar color="rgba(0,0,0,0)" flat class="mb-8">
          
            <v-spacer></v-spacer>
            <v-card class="mt-10 mr-2" max-width="350px" color="blue" dark>
    <v-list-item three-line>
      <v-list-item-content>
        <div class=" mb-4">
          Lorem Ipsum is simply dummy text of the printing and typesetting industry.
        </div>
        <v-list-item-subtitle>2 mins ago </v-list-item-subtitle>  
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
                  <img src="https://cdn.vuetifyjs.com/images/lists/1.jpg" />
            </v-avatar>
            </v-badge>
          </v-app-bar>
          <v-app-bar color="rgba(0,0,0,0)" flat class="mb-16">
          
            <v-spacer></v-spacer>
            <v-card class="mt-10 mr-2" max-width="350px" color="blue" dark>
    <v-list-item three-line>
      <v-list-item-content>
        <div class=" mb-4">
          Lorem Ipsum is simply dummy text of the
        </div>
        <v-list-item-subtitle>3 mins ago </v-list-item-subtitle>  
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
                  <img src="https://cdn.vuetifyjs.com/images/lists/1.jpg" />
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
           avatar: 'https://cdn.vuetifyjs.com/images/lists/1.jpg',
          subtitle: `Lorem Ipsum is simply dummy text of the printing and typesetting industry.`,
          title: 'User',
        },
        {
           avatar: 'https://cdn.vuetifyjs.com/images/lists/1.jpg',
          subtitle: `Lorem Ipsum is simply dummy text of the printing and typesetting industry.`,
          title: 'eu, User, User2',
        },
        {
           avatar: 'https://cdn.vuetifyjs.com/images/lists/1.jpg',
          subtitle: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry.',
          title: 'User',
        },
        {
           avatar: 'https://cdn.vuetifyjs.com/images/lists/1.jpg',
          subtitle: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry.',
          title: 'User',
        },
        {
           avatar: 'https://cdn.vuetifyjs.com/images/lists/1.jpg',
          subtitle: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry.',
          title: 'User',
        },
        {
           avatar: 'https://cdn.vuetifyjs.com/images/lists/1.jpg',
          subtitle: `Lorem Ipsum is simply dummy text of the printing and typesetting industry.`,
          title: 'User',
        },
        {
           avatar: 'https://cdn.vuetifyjs.com/images/lists/1.jpg',
          subtitle: `Lorem Ipsum is simply dummy text of the printing and typesetting industry.`,
          title: 'User',
        },
        {
           avatar: 'https://cdn.vuetifyjs.com/images/lists/1.jpg',
          subtitle: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry.',
          title: 'User',
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