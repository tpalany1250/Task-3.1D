<template>
    <!-- Chatbox button -->
    <button class="chatbox-button" @click="toggleChatbox">Chat</button>

    <!-- Chatbox -->
    <div v-if="showChatbox" class="chatbox">
      <!-- Chatbox content -->
      <div v-for="message in messages" :key="message.content">
        <strong v-if="message.sender === 'user'">You: </strong>
        <strong v-if="message.sender === 'ai'">AI: </strong>
        {{ message.content }}
      </div>

      <!-- Input and send button -->
      <div class="chatbox-input">
        <input v-model="userMessage" type="text" placeholder="Type your message...." @keyup.enter="sendMessage" />
        <button @click="sendMessage">Send</button>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        messages: [],
        userMessage: '',
        showChatbox: false, // Initially hidden
      };
    },
    methods: {
    toggleChatbox() {
      this.showChatbox = !this.showChatbox;
    },
    sendMessage() {
      if (!this.userMessage) return;
      this.messages.push({ sender: 'user', content: this.userMessage });
      this.messages.push({ sender: 'ai', content: this.getAIResponse(this.userMessage) });
      this.userMessage = '';
    },
    getAIResponse(question) {
      const predefinedAnswers = {
      'hello': 'Hi, how can I assist you today?',
      'tell me about your car models': 'We offer a wide range of car models, including sedans, SUVs, sports cars, and electric vehicles. Each model comes with various features and options to choose from. Is there a specific model you would like to know more about?',
      'what are the available colors?': 'Our cars are available in a variety of colors, including classic black, elegant white, sporty red, and more. You can also inquire about custom color options for certain models.',
      'what is the price range?': 'The price range for our car models varies depending on the model, trim level, and optional features. Please browse through our car catalog or contact our sales team to gather more detailed pricing information.',
      'do you offer financing options?': 'Yes, we offer financing options to make it easier for you to own your dream car. Our financing plans come with competitive interest rates and flexible terms. Would you like to learn more about our financing options?',
      'how can I schedule a test drive?': 'You can scheduling a test drive by contacting our dealership, and our friendly staff will assist you in scheduling a test drive.',
      'what is your warranty coverage?': 'Our cars come with a comprehensive warranty package that covers various components of the vehicle. The warranty duration and coverage details may vary by model. To get specific warranty information, please provide the model you are interested in.',
      'where is your dealership located?': 'We are located in the heart of Melbourne. You can find detailed directions on our websites contact page. Feel free to visit us anytime during our business hours.',
      'how can I contact your customer support?': 'You can reach our customer support team by phone at (04) 1234 5678. We are here to assist you with any inquiries or assistance you may need.',
    };

      for (let key in predefinedAnswers) {
        if (question.toLowerCase().includes(key)) {
          return predefinedAnswers[key];
        }
      }
      return 'I\'m sorry, I don\'t understand.';
    },
  },
};
  </script>


<style scoped>
.chatbox-button {
  position: fixed;
  bottom: 20px;
  right: 20px;
  z-index: 999; /* Adjust this value as needed */
  background-color: rgb(101, 228, 185);
  color: #fff;
  border: none;
  border-radius: 5px;
  padding: 10px 20px;
  cursor: pointer;
}

.chatbox {
  position: fixed;
  bottom: 20px;
  right: 20px;
  z-index: 999; /* Adjust this value to appear above other elements */
  background-color: #3b3737;
  border: 1px solid #ccc;
  border-radius: 5px;
  width: 300px;
  max-height: 400px;
  overflow-y: auto;
  padding: 10px;
  box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.2);
  color: rgb(0, 255, 170);
}


.chatbox-input {
  display: flex;
  margin-top: 10px;
}

/* text box writing */
.chatbox-input input {
  flex: 1;
  padding: 5px;
  border: 1px solid #ccc;
  border-radius: 3px;
  margin-right: 5px;
}

.chatbox-input button {
  background-color: rgb(101, 228, 185);
  color: #ffffff;
  border: none;
  border-radius: 3px;
  padding: 5px 10px;
  cursor: pointer;
}
</style>