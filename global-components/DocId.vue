<template>
  <Badge :text="docId" />
</template> 

<script>
import Badge from "@parent-theme/global-components/Badge.vue";

export default {
  components: {
    Badge
  },
  props: {
    relativePath: String
  },
  data: function() {
    return {
      docId: ""
    };
  },
  mounted() {
    const relativePath = this.relativePath
      ? this.relativePath
      : this.$page.relativePath;

    const relativePathParts = relativePath.split("/");
    const filePath = relativePathParts[relativePathParts.length - 1];
    const filePathParts = filePath.split(".");

    this.docId = filePathParts[0].toUpperCase();
  }
};
</script>