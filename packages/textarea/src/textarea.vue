<template>
  <div class='mint-textarea'>
    <textarea class='mint-textarea__content' v-model='content' :placeholder='placeholder' :rows='rows'></textarea>
    <div class="mint-textarea__cnt" v-if='hasLimit'>{{inputCount}}/{{limit}}</div>
  </div>
</template>

<script>
/**
 * mt-textarea
 * @module components/textarea
 * @desc 自定义多行文本输入框
 * @param {Number} [limit] - 限制输入的字符数
 * @param {Number} [rows] - 显示高度支持的行数
 * @param {String} [placeholder] - 提示文字
 *
 * @example
 * <mt-textarea :limit='50'>
 * </mt-textarea>
 */

function cutStr(str, limit) {
  if (!str) {
    return '';
  }

  if (limit && (str.length > limit)) {
    str = str.substring(0, limit);
  }

  return str;
}

export default {
  name: 'mt-textarea',
  data: function() {
    return {
      content: ''
    };
  },
  props: {
    value: String,
    rows: {
      type: Number,
      default: 4
    },
    placeholder: String,
    limit: {
      type: Number
    }
  },
  computed: {
    hasLimit: function() {
      return this.limit > 0;
    },
    inputCount: function() {
      return this.value && this.value.length || 0;
    }
  },
  watch: {
    content: function(newVal) {
      newVal = cutStr(newVal, this.limit);
      this.content = newVal;
      this.$emit('input', newVal);
    },
    value: function(newVal) {
      this.content = cutStr(newVal, this.limit);
    }
  }
};
</script>

<style lang="css">
  @import "../../../src/style/var.css";

  @component-namespace mint {
    @component textarea {
      padding: 2px 0;

      .mint-textarea__content {
        -webkit-appearance: none;
        -moz-appearance: none;
        appearance: none;
        border-radius: 0;
        border: 0;
        -webkit-box-flex: 1;
        -ms-flex: 1;
        flex: 1;
        outline: 0;
        line-height: 1.6;
        font-size: inherit;
        width: 100%;
      }

      .mint-textarea__cnt {
        text-align: right;
        color: $disabled-color;
        font-size: 12px;
      }
    }
  }
</style>
