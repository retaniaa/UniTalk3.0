<template>
  <div class="ml-[420px] w-full">
    <div class="w-full">
      <div class="border-l border-green-500 w-full">
        <div
          class="bg-[#F0F0F0] fixed z-10 min-w-[calc(100vw-420px)] flex justify-between items-center px-2 py-2"
        >
          <div class="flex items-center">
            <img
              class="rounded-full mx-1 w-10"
              src="https://picsum.photos/100/100"
              alt=""
            />
            <div class="text-gray-900 ml-1 font-semibold">Frank</div>
          </div>
          <DotsVerticalIcon fillColor="#515151" class="" />
        </div>
      </div>

      <div
        id="MessagesSection"
        class="pt-20 pb-8 z-[-1] h-[calc(100vh-65px)] w-[calc(100vw-420px)] overflow-auto fixed touch-auto"
      >
        <div class="px-20 text-sm">
          <div class="flex w-[calc(100%-50px)]">
            <div class="inline-block bg-gray-200 p-2 rounded-md my-1">
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Veritatis
              incidunt obcaecati tempora laboriosam non consectetur quod id nisi
              iste beatae eligendi, ratione placeat quasi praesentium officiis,
              aliquid in temporibus vel.
            </div>
          </div>

          <div
            class="flex justify-end space-x-1 w-[calc(100%-50px)] float-right"
          >
            <div class="inline-block bg-green-200 p-2 rounded-md my-1">
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Veritatis
              incidunt obcaecati tempora laboriosam non consectetur quod id nisi
              iste beatae eligendi, ratione placeat quasi praesentium officiis,
              aliquid in temporibus vel.
            </div>
          </div>
        </div>
      </div>

      <div class="w-[calc(100vw-420px)] p-2.5 z-10 bg-[#F0F0F0] fixed bottom-0">
        <div class="flex items-center justify-center">
          <EmoticonExcitedOutlineIcon
            :size="27"
            fillColor="#515151"
            class="mx-1.5"
          />
          <PaperclipIcon :size="27" fillColor="#515151" class="mx-1.5 mr-3" />
          <input
            v-model="message"
            class="mr-1 shadow apperance-none rounded-lg w-full py-3 px-4 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
            autocomplete="off"
            type="text"
            placeholder="Message"
          />

          <button
            type=""
            class="ml-3 p-2 w-12 flex items-center justify-center"
          >
            <SendIcon fillcolor="#515151" />
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import DotsVerticalIcon from "vue-material-design-icons/DotsVertical.vue";
import EmoticonExcitedOutlineIcon from "vue-material-design-icons/EmoticonExcitedOutline.vue";
import PaperclipIcon from "vue-material-design-icons/Paperclip.vue";
import SendIcon from "vue-material-design-icons/Send.vue";
</script>

<style lang="scss" scoped>
</style>