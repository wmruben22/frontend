<template>
    <div>
    <h4 class="text-h4">Messages</h4>
  
    <v-list>
        <v-list-item-group color="primary">
      <v-list-item
        v-for="message in messages"
        :key="message.id"
      >

        <v-list-item-content>
          <v-list-item-title v-text="message"></v-list-item-title>
        </v-list-item-content>

        
      </v-list-item>
    </v-list-item-group>
    </v-list>
 
    </div>
</template>
<script>
import axios from 'axios';
export default {
    data() {
        return {
            messages: ["hello", "hi", "it's working"]

        };
    },
    async created() {
        this.messages = (await axios.get('http://localhost:3000/messages')).data;
    }
};

</script>
