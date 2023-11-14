<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ChatGPT in 1 file</title>
  <script src="/files/tailwind.js"></script>
  <script src="/files/vue.global.js"></script>
  <script src="/files/axios.min.js"></script>
</head>

<body>
  <main id="app" class="min-h-screen bg-gray-100 p-8">
    <div class="max-w-2xl mx-auto">
      <div class="mb-4">
        <h1 class="text-4xl font-bold text-center">ChatGPT Demo in 1 file</h1>
      </div>
      <div class="bg-white shadow rounded-lg p-6">
        <div class="flow-root">
          <div class="mt-6">
            <!-- Chat Input -->
            <form @submit.prevent="sendMessage">
              <div class="flex space-x-3">
                <input type="text" v-model="userInput" placeholder="Type your message here..."
                  class="flex-1 rounded-md shadow-sm p-2">
                <button type="submit" class="px-4 py-2
                      bg-blue-500 text-white rounded-md
                      hover:bg-blue-600">
                  <svg v-if="isLoading" aria-hidden="true"
                    class="w-4 relative -top-0.5 mr-1 inline-block text-gray-200 animate-spin fill-blue-600"
                    viewBox="0 0 100 101" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path
                      d="M100 50.5908C100 78.2051 77.6142 100.591 50 100.591C22.3858 100.591 0 78.2051 0 50.5908C0 22.9766 22.3858 0.59082 50 0.59082C77.6142 0.59082 100 22.9766 100 50.5908ZM9.08144 50.5908C9.08144 73.1895 27.4013 91.5094 50 91.5094C72.5987 91.5094 90.9186 73.1895 90.9186 50.5908C90.9186 27.9921 72.5987 9.67226 50 9.67226C27.4013 9.67226 9.08144 27.9921 9.08144 50.5908Z"
                      fill="currentColor" />
                    <path
                      d="M93.9676 39.0409C96.393 38.4038 97.8624 35.9116 97.0079 33.5539C95.2932 28.8227 92.871 24.3692 89.8167 20.348C85.8452 15.1192 80.8826 10.7238 75.2124 7.41289C69.5422 4.10194 63.2754 1.94025 56.7698 1.05124C51.7666 0.367541 46.6976 0.446843 41.7345 1.27873C39.2613 1.69328 37.813 4.19778 38.4501 6.62326C39.0873 9.04874 41.5694 10.4717 44.0505 10.1071C47.8511 9.54855 51.7191 9.52689 55.5402 10.0491C60.8642 10.7766 65.9928 12.5457 70.6331 15.2552C75.2735 17.9648 79.3347 21.5619 82.5849 25.841C84.9175 28.9121 86.7997 32.2913 88.1811 35.8758C89.083 38.2158 91.5421 39.6781 93.9676 39.0409Z"
                      fill="currentFill" />
                  </svg>
                  Send
                </button>
              </div>
            </form>
          </div>

          <!-- Chat Messages -->
          <ul class="divide-y divide-gray-200">
            <li class="py-3 sm:py-4" v-for="message in messages">
              <div class="flex items-center space-x-4" v-if="message.role !== 'system'"
                v-bind:class="messageClasses(message.role)">
                <div class="flex-shrink-0">
                  <img v-if="message.role === 'assistant'" class="w-8 h-8 rounded-full"
                    src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTagONv1r-0HPnlnWClF12amS_KdrPX83zlhcXHyek&s"
                    alt="ChatGPT Icon" />
                </div>
                <div class="flex-1 min-w-0">
                  <p class="text-sm text-gray-800 break-normal whitespace-pre-line"
                    v-bind:class="messageClasses(message.role)">
                    <span v-if="message.role === 'user'" class="font-bold">Code Dạo: </span>
                    {{ message.content }}
                  </p>
                </div>
              </div>
            </li>
          </ul>

        </div>
      </div>
    </div>
  </main>
</body>
<script>
  const {
    createApp,
    ref
  } = Vue;

  // Real GPT
  // const OPEN_AI_ENDPOINT = 'https://api.openai.com/v1'

  // Security, do not deploy this in production
  const chatGPTKey = 'sk-*****'; // Create an API key from here

  // Local GPT
  // const OPEN_AI_ENDPOINT = 'http://localhost:8000/v1'

  createApp({
    setup() {
      const userInput = ref('');
      const messages = ref([{
        role: 'system',
        content: "You're a helpful chat bot. Answer short and concise in 150 tokens only."
      }]);
      const isLoading = ref(false);




      const messageClasses = (role) => ({
        'text-right justify-end': role === 'user',
        'text-left justify-start': role === 'assistant',
      });

      async function sendMessage() {
        if (!userInput.value.trim()) return;

        // Append user message
        messages.value.push({
          role: 'user',
          content: userInput.value
        });

        try {
          isLoading.value = true
          userInput.value = '';

          // Send API request to OpenAI endpoint
          const response = await axios.post(
            `${OPEN_AI_ENDPOINT}/chat/completions`, {
              // model: 'gpt-3.5-turbo',
              model: 'gpt-4-1106-preview',
              messages: messages.value,
              temperature: 0.9,
              max_tokens: 150,
            }, {
              headers: {
                'Content-Type': 'application/json',
                'Authorization': `Bearer ${chatGPTKey}`,
              },
            }
          );

          // Append ChatGPT response
          messages.value.push({
            role: 'assistant',
            content: response.data.choices[0].message.content
          });
        } catch (error) {
          console.error('There was an error with the API request', error);
        } finally {
          isLoading.value = false;
        }
      }

      return {
        userInput,
        messages,
        messageClasses,
        sendMessage,
        isLoading,
      };
    },
  }).mount('#app');
</script>

</html>