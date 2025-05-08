<script setup>
import {
  Disclosure,
  DisclosureButton,
  DisclosurePanel,
  Menu,
  MenuButton,
  MenuItem,
} from "@headlessui/vue";
import { Bars3Icon, BellIcon, XMarkIcon } from "@heroicons/vue/24/outline";

const user = {
  name: "Jami",
  email: "jamixcs@gmail.com",
  imageUrl: jami,
};
const navigation = [
  // { name: "Dashboard", href: "#", current: true },
  // { name: "接案", href: "#", current: false },
  // { name: "切版", href: "#", current: false },
];

import { ref, reactive } from "vue";
import { computed } from "vue";

import Header from "./header.vue";
import List from "./list.vue";
import aithon from "../img/aithon.png";
import chaobang from "../img/chaobang.jpeg";
import atec from "../img/atec.png";

import t1 from "../img/t1.png";
import t2 from "../img/t2.jpg";
import t3 from "../img/t3.jpg";
import t4 from "../img/t4.jpg";
import t6 from "../img/t6.jpg";
import jami from "../img/jami.jpg";

const portfolioCategories = reactive([
  {
    title: "接案作品",
    projects: [
      {
        name: "職缺平台系統",
        team: "團隊：前端 2 人",
        content: `擔任專案窗口，統籌需求釐清與目標對齊，協調資源配置，確保專案範疇、時程與品質如期落實。
建立專案管理流程與協作機制，定期同步進度與問題
切分任務並分配至前端團隊，根據進度與優先級調整任務安排，持續追蹤並解決卡點
應對需求變動，評估修改範圍與影響，快速與業主與團隊對齊共識並重新安排時程
參與前端開發，根據流程圖設計並實作 RWD 畫面與互動元件，串接 Firebase 資料庫與帳號系統。
規劃並實作前端邏輯與流程，包括：
• Vue 3 專案架構初始化
• Pinia store 設計與管理
• 登入與帳號權限管理（Firebase Authentication）
• 資料存取（Cloud Firestore、Cloud Storage）
• CRUD 操作：求職者履歷與評論的建立、編輯、刪除
• 企業／求職者之帳號會員資料管理
• 響應式設計（RWD），支援 Desktop、Mobile 裝置瀏覽
• Husky 設定，建立統一的程式碼提交規範`,
        href: "",
        target: "",
        src: atec,
        alt: "atec",
        time: "2025/2~至今",
        tag: [
          "Vue 3",
          "Pinia",
          "Quasar",
          "RWD",
          "Firebase Authentication",
          "Cloud Firestore",
          "Cloud Storage",
          "Husky",
          "專案窗口",
          "協作開發",
          "API 串接",
        ],
      },
      {
        name: "兆邦醫材網站製作",
        team: "團隊：前端 2 人、UI/UX 設計 1 人、PM 1 人",
        content: `使用 Vue 2 + Nuxt.js 架構開發網站，配合 Vuex 管理狀態，並整合 Sass 進行樣式設計，與設計師、後端工程師密切協作，根據設計稿精準實作畫面並滿足業主需求。
規劃並實作前端頁面與邏輯，包括：
• 首頁、公司介紹、個案實例、聯絡我們等主要頁面開發
• RWD 響應式設計，支援多裝置瀏覽
• 串接後端 API，實現動態內容與資料互動`,
        href: "https://chao-bang.com/",
        target: "blank",
        src: chaobang,
        alt: "chaobang",
        time: "2024/12~2024/2",
        tag: [
          "Vue 2",
          "Nuxt.js",
          "Vuex",
          "RWD",
          "協作開發",
          "前後端分離",
          "API 串接",
        ],
      },
      {
        name: "2024 數位城市治理黑客松 - 官網",
        team: "團隊：前端 2 人",
        content: `負責設計與開發「台南市政府 × 好想工作室 AI 松」活動官網，使用 Hexo 框架建置靜態網站。
根據時程與需求，整合內容並彈性調整版面，確保報名資訊、活動進度與講者內容即時更新、同步無誤。
優化資訊結構與頁面引導，提升使用者在瀏覽活動內容、進行報名時的操作體驗。`,
        href: "https://aithon2024.goodideas-studio.com/",
        target: "blank",
        src: aithon,
        alt: "aithon",
        time: "2024/8~2024/12",
        tag: ["Hexo", "HTML", "CSS ", "Sass", "JavaScript", "RWD", "協作開發"],
      },
    ],
  },
  {
    title: "切版作品",
    projects: [
      {
        name: "原生切版",
        content:
          "掌握 Box Model、Line-box、Normal Flow 及 Inline / Block 元素的運用，實踐語意化標記，製作簡單動畫效果，並理解程式碼在瀏覽器中的運作方式。",
        href: "https://jamixcs.github.io/t1/",
        target: "blank",
        src: t1,
        alt: "t1",
        time: "2024/2",
        tag: ["HTML", "CSS"],
      },
      {
        name: "原生切版",
        content:
          "進一步熟悉原生寫法，養成良好命名習慣，使用 GitMind 建立 HTML 結構樹狀圖，並啟動切版流程。",
        href: "https://jamixcs.github.io/t2/",
        target: "blank",
        src: t2,
        alt: "t2",
        time: "2024/3",
        tag: ["HTML", "CSS"],
      },
      {
        name: "UI 框架切版",
        content:
          "使用 Bootstrap 練習 Row / Col 格線系統，熟悉 Flex 和 Grid 語法，高效建構 RWD 版面，並運用 Dropdown、Modal 等 UI 元件提升互動體驗。",
        href: "https://jamixcs.github.io/t3/",
        target: "blank",
        src: t3,
        alt: "t3",
        time: "2024/3",
        tag: ["HTML", "CSS", "Bootstrap", "RWD"],
      },
      {
        name: "UI 框架切版",
        content:
          "深入理解容器與內容的區別，實踐排版與內容分離的設計理念。釐清設計稿中的變動與固定距離，優化 RWD 版面設計。",
        href: "https://jamixcs.github.io/t4/",
        target: "blank",
        src: t4,
        alt: "t4",
        time: "2024/4",
        tag: ["HTML", "CSS", "Bootstrap", "RWD"],
      },
      {
        name: "UI 框架切版 + 預處理器",
        content:
          "掌握 Sass 中 mixin 與 extend 的應用，實現元件複用。練習巢狀寫法與檔案拆分，提升程式碼的結構與可維護性。",
        href: "https://jamixcs.github.io/t6/",
        target: "blank",
        src: t6,
        alt: "t6",
        time: "2024/5",
        tag: ["HTML", "CSS", "Bootstrap", "Sass", "RWD"],
      },
    ],
  },
]);
</script>
<template>
  <div class="min-h-full">
    <Disclosure as="nav" class="bg-slate-600" v-slot="{ open }">
      <div class="mx-auto px-4">
        <div class="flex h-16 items-center justify-between">
          <div class="flex items-center">
            <div class="shrink-0">
              <p class="text-white">Jami's Portfolio</p>
            </div>
            <div class="hidden md:block">
              <div class="ml-10 flex items-baseline space-x-4">
                <a
                  v-for="item in navigation"
                  :key="item.name"
                  :href="item.href"
                  :class="[
                    item.current
                      ? 'bg-gray-900 text-white'
                      : 'text-gray-300 hover:bg-gray-700 hover:text-white',
                    'rounded-md px-3 py-2 text-sm font-medium',
                  ]"
                  :aria-current="item.current ? 'page' : undefined"
                  @click="selectCategory(item.name)"
                  >{{ item.name }}</a
                >
              </div>
            </div>
          </div>
          <div class="md:block">
            <div class="ml-4 flex items-center md:ml-6">
              <!-- Profile dropdown -->
              <Menu as="div" class="relative ml-3">
                <div>
                  <MenuButton
                    class="relative flex max-w-xs items-center rounded-full bg-gray-800 text-sm focus:ring-2 focus:ring-white focus:ring-offset-2 focus:ring-offset-gray-800 focus:outline-hidden"
                  >
                    <span class="absolute -inset-1.5" />
                    <!-- <span class="sr-only">Open user menu</span> -->
                    <img
                      class="size-8 rounded-full"
                      :src="user.imageUrl"
                      alt=""
                    />
                  </MenuButton>
                </div>
              </Menu>
            </div>
          </div>
        </div>
      </div>

      <DisclosurePanel class="md:hidden">
        <div class="space-y-1 px-2 pt-2 pb-3 sm:px-3">
          <DisclosureButton
            v-for="item in navigation"
            :key="item.name"
            as="a"
            :href="item.href"
            :class="[
              item.current
                ? 'bg-gray-900 text-white'
                : 'text-gray-300 hover:bg-gray-700 hover:text-white',
              'block rounded-md px-3 py-2 text-base font-medium',
            ]"
            :aria-current="item.current ? 'page' : undefined"
            >{{ item.name }}</DisclosureButton
          >
        </div>
        <div class="border-t border-gray-700 pt-4 pb-3">
          <div class="flex items-center px-5">
            <div class="shrink-0">
              <img class="size-10 rounded-full" :src="user.imageUrl" alt="" />
            </div>
            <div class="ml-3">
              <div class="text-base/5 font-medium text-white">
                {{ user.name }}
              </div>
              <div class="text-sm font-medium text-gray-400">
                {{ user.email }}
              </div>
            </div>
          </div>
          <div class="mt-3 space-y-1 px-2">
            <DisclosureButton
              v-for="item in userNavigation"
              :key="item.name"
              as="a"
              :href="item.href"
              class="block rounded-md px-3 py-2 text-base font-medium text-gray-400 hover:bg-gray-700 hover:text-white"
              >{{ item.name }}</DisclosureButton
            >
          </div>
        </div>
      </DisclosurePanel>
    </Disclosure>
    <main
      class="flex flex-row flex-wrap items-center justify-center gap-4 p-[30px] text-2xl"
    >
      <div v-for="(portfolio, index) in portfolioCategories" :key="index">
        <Header :portfolioTitle="portfolio.title" class="font-bold" />
        <List :portfolioProjects="portfolio.projects" />
      </div>
    </main>
  </div>
</template>
