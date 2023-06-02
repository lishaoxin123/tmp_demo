<template>
  <el-config-provider :locale="currentLocale">
    <!-- <Home /> -->
    <router-view />
    <!-- <ReDialog /> -->
  </el-config-provider>
</template>

<script lang="ts">
// import Home from "./views/home";
import { defineComponent } from "vue";
import { ElConfigProvider } from "element-plus";
import zhCn from "element-plus/lib/locale/lang/zh-cn";
import { ReDialog } from "@/components/ReDialog";
export default defineComponent({
  name: "app",
  components: {
    [ElConfigProvider.name]: ElConfigProvider,
    // Home,
    ReDialog
  },
  computed: {
    currentLocale() {
      return zhCn;
    }
  }
});
</script>
