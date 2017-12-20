<template>
  <div class="page-textarea">
    <div class="page-title">Textarea</div>
    <mt-cell title="标题文字">
      <mt-textarea v-model='content' :limit='50' placeholder='自定义文本域'></mt-textarea>
    </mt-cell>
  </div>
</template>

<script type="text/javascript">
  export default {
    data: function() {
      return {
        content: ''
      };
    }
  };
</script>
