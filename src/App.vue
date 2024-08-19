<template>
  <el-config-provider namespace="ep" :size>
    <el-pagination
      :page-sizes="[10, 20, 30, 40, 50]"
      :total="50"
      :background="true"
      :layout="'total, prev, pager, next, sizes, jumper'"
    />
    <el-button>测试按钮</el-button>
  </el-config-provider>
</template>

<script setup>
import { ref } from "vue";
const size = ref("small");
window.addEventListener("resize", (e) => {
  const width = window.innerWidth;
  size.value = width < 1920 ? "small" : width < 2560 ? "default" : "large";
});
</script>
