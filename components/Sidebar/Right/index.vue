<template>
  <div class="flex flex-col">
    <!-- Preview card: What's happening -->
    <SidebarRightPreviewCard title="What's happening?">
      <SidebarRightPreviewCardItem
        v-for="whatsHappening in whatsHappeningItems"
      >
        <h2 class="font-bold text-gray-800 dark:text-white">
          {{ whatsHappening.title }}
        </h2>
        <p class="text-gray-400 text-xs">{{ whatsHappening.count }}</p>
      </SidebarRightPreviewCardItem>
    </SidebarRightPreviewCard>

    <!-- Preview card: Who to follow -->
    <SidebarRightPreviewCard title="Who to follow">
      <SidebarRightPreviewCardItem v-for="whoToFollow in whoToFollowItems">
        <div class="flex flex-row justify-between items-center p-2">
          <div class="flex flex-row">
            <img
              class="size-10 rounded-full"
              :src="whoToFollow.image"
              :alt="whoToFollow.name"
            />

            <div class="flex flex-col ml-2">
              <h2 class="text-sm font-bold text-gray-900 dark:text-white">
                {{ whoToFollow.name }}
              </h2>
              <p class="text-gray-400 text-xs">{{ whoToFollow.handle }}</p>
            </div>
          </div>

          <div class="flex h-full">
            <button
              class="px-4 py-2 font-bold text-xs text-white dark:text-black bg-black dark:bg-white rounded-full"
            >
              Follow
            </button>
          </div>
        </div>
      </SidebarRightPreviewCardItem>
    </SidebarRightPreviewCard>
  </div>
</template>

<script setup>
const whatsHappeningItems = ref([
  { title: "SpaceX", count: "18.8k Tweets" },
  { title: "#CodingIsFun", count: "5.7k Tweets" },
  { title: "#artforall", count: "1.2k Tweets" },
]);

const whoToFollowItems = ref([
  {
    name: "Joe biden",
    handle: "@joBiden",
    image: "https://picsum.photos/200/200",
  },
  {
    name: "Joe biden",
    handle: "@joBiden",
    image: "https://picsum.photos/200/200",
  },
  {
    name: "Joe biden",
    handle: "@joBiden",
    image: "https://picsum.photos/200/200",
  },
]);
</script>
