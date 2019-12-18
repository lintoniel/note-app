<template>
  <div class="textarea">
    <div class="textarea__input">
      <input placeholder="Введите заголовок"
        v-model="note.header"
      />
    </div>
    <div class="textarea__main">
      <textarea placeholder="Введите заметку"
        v-model="note.message"
    ></textarea>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      note: {
        header: '',
        message: '',
      }
    }
  },
  methods: {
    setTextAreaActive(value) {
      this.isTextAreaActive = value;
    },
    setInputVisibility(value) {
      this.isInputActive = value;
    }
    
  }
}
</script>

<style lang="scss" scoped>
.textarea {
  position: relative;
  font-family: sans-serif;
  margin-top: 30px;
    &__input {
      text-align: center;
      & input {
        width: 600px;
        height: 40px;
        padding: 10px;
        box-shadow: 0 1px 2px 0 rgba(60,64,67,0.302), 0 2px 6px 2px rgba(60,64,67,0.149);
        border-radius: 4px;
        font-size: 16px;
      }
        &::-moz-placeholder {
          font-family: sans-serif;
          color: #80888f;
        }

        &::-webkit-input-placeholder {
          font-family: sans-serif;
          color: #80888f;
        }
    }
    &__main {
      text-align: center;
       & textarea {
        width: 600px;
        height: 200px;
        resize: none;
        padding: 10px;
        box-shadow: 0 1px 2px 0 rgba(60,64,67,0.302), 0 2px 6px 2px rgba(60,64,67,0.149);
        border-radius: 4px;
        margin-top: 8px;
          &::-moz-placeholder {
            font-family: sans-serif;
            color: #80888f;
          }

          &::-webkit-input-placeholder {
            font-family: sans-serif;
            color: #80888f;
          }
      }
  }
}
</style>
