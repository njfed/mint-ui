<template>
  <div class='mt-colors'>
    <div class="page-title">Colors</div>
    <div class='mt-colors__tips color-warning bg-warning-lv2'>.color-warning.bg-warning-lv2</div>
    <div class='mt-colors__tips color-error bg-error-lv2'>.color-error.bg-error-lv2</div>
    <div class='mt-colors__tips color-primary bg-primary-lv2'>.color-primary.bg-primary-lv2</div>
    <div class='mt-colors__text'>
      <div class='mt-colors__text--content color-content'>正文文字 .color-content</div>
      <div class="mt-colors__text--dim color-dim">可能是日期 .color-dim</div>
      <div class="mt-colors__text--subtitle color-subtitle">
        <span>提示文字 .color-warning</span>
        <span class='color-warning'>重要提示文字</span>
      </div>
      <div class="mt-colors__text--subtitle color-subtitle">
        <span>提示文字 .color-error</span>
        <span class='color-error'>警告提示文字</span>
      </div>
      <div class="mt-colors__text--subtitle color-subtitle">
        <span>提示文字 .color-primary</span>
        <span class='color-primary'>常规提示文字</span>
      </div>
      <div class="mt-colors__text--subtitle color-subtitle">
        <span>提示文字 .color-success</span>
        <span class='color-success'>成功提示文字</span>
      </div>
    </div>
  </div>
</template>

<style scoped>
  .page-title {
    font-size: 30px;
    line-height: 66px;
    text-align: center;
  }

  .mt-colors__tips {
    padding: 5px 0;
    text-align: center;
    margin-bottom: 10px;
  }

  .mt-colors__text {
    padding: 15px;
  }

  .mt-colors__text--content {
    display: inline-block;
    font-size: 16px;
  }

  .mt-colors__text--subtitle {
    font-size: 12px;
    margin-top: 5px;
  }

  .mt-colors__text--dim {
    float: right;
    font-size: 12px;
    margin-top: 5px;
  }
</style>