<template>
  <div class="flex">
    <div id="Header" class="fixed w-[420px] z-10">
      <div
        class="bg-[#F0F0F0] w-full flex justify-between items-center px-3 py-2"
      >
        <img
          class="rounded-full ml-1 w-10"
          src="https://picsum.photos/100/100"
          alt=""
        />
        <div class="flex items-center justify-center">
          <AccountGroupIcon fillColor="#515151" class="mr-6" />
          <DotsVerticalIcon fillColor="#515151" class="cursor-pointer" />
        </div>
      </div>

      <div id="Search" class="bg-white w-full px-2 border-b shadow-sm">
        <div
          class="px-1 m-2 bg-[#F0F0F0] flex items-center justify-center rounded-md"
        >
          <MagnifyIcon fillColor="#515151" :size="18" class="ml-2" />
          <input
            @click="showFindFriends = !showFindFriends"
            class="ml-5 apperance-none w-full bg-[#F0F0F0] py-1.5 px-2.5 text-gray-700 leading-tight focus:outline-none focus:shadow-outline placeholder:text-sm placeholder:text-gray-500"
            autocomplete="off"
            type="text"
            placeholder="Mulai Chat Baru"
          />
        </div>
      </div>
    </div>

    <ChatsView class="mt-[100px]" />

    <div v-if="open">
      <MessageView />
    </div>

    <div v-else>
      <div
        class="ml-[420px] fixed w-[calc(100vw-420px)] h-[100vh] bg-gray-100 text-center"
      >
        <div class="grid h-screen place-items-center">
          <div>
            <div class="w-full flex items-center justify-center">
              <img width="375" src="https://picsum.photos/400/200" alt="" />
            </div>
            <div class="text-[32px] text-gray-500 font-light mt-10">
              UniTalk
            </div>
            <div class="text-[14px] text-gray-600 mt-2">
              <div>
                Obrolan Tanpa Batas, Menghapus Jarak dan Mewujudkan Kedekatan
              </div>
              <div>
                Membawa Anda Lebih Dekat, Membuat Ruang untuk Momen Bersama yang
                Bermakna.
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import ChatsView from "./ChatsView.vue";
import MessageView from "./MessageView.vue";
import AccountGroupIcon from "vue-material-design-icons/AccountGroup.vue";
import DotsVerticalIcon from "vue-material-design-icons/DotsVertical.vue";
import MagnifyIcon from "vue-material-design-icons/Magnify.vue";
import { ref } from "vue";
let open = ref(true);
</script>

<style lang="scss" scoped>
</style>