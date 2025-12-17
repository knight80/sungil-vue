<template>
  <div>
    <a-button type="primary" @click="showModal">모달 열기</a-button>
    <a-modal v-model:open="visible" title="안녕하세요!" @ok="handleOk">
      <p>Vue 3와 antd로 만든 모달입니다.</p>
    </a-modal>
  </div>
</template>
<script setup lang="ts">
import {ref} from 'vue'

const visible = ref(false)

const showModal =()=>{
    console.log('showModal')
    visible.value = true
}

const handleOk = () =>{
    console.log('handleOk')
    visible.value = false
}

</script>