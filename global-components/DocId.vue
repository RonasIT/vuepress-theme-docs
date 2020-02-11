<template>
  <Badge :text="docId" />
</template> 

<script>
import Badge from "@parent-theme/global-components/Badge.vue";

export default {
  components: {
    Badge
  },
  data: function() {
    return {
      docId: ""
    };
  },
  mounted() {
    const relativePathParts = this.$page.relativePath.split("/");
    const filePath = relativePathParts[relativePathParts.length - 1];
    const filePathParts = filePath.split(".");

    this.docId = filePathParts[0].toUpperCase();
  }
};
</script>