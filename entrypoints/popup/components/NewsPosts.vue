<template>
  <ul class="list" v-if="this.list.length > 0">
    <li v-for="item in list" :key="item.id">
      <a :href="'https://linux.do/t/topic/' + item.id" target="_blank" :title="item.title">
        {{ item.title }}
        <em>{{ item.highest_post_number }}</em>
      </a>
    </li>
  </ul>
  <div class="nodata" v-else>暂无最新话题</div>
</template>

<script>
export default {
  props: ['list'],
};
</script>
