<template>
  <div class="container">
    <div class="edit">

      <ul>
        <li v-for="conversationId of conversationIds" :key="conversationId">
          <span>会话ID: {{ conversationId}} </span>
          <div class="action-buttons">
          <el-button round plain>查询</el-button>
          <el-icon class="delete" @click="deleteConversation(conversationId)"><Delete /></el-icon>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>
<script lang="ts" setup>
import { useConversationStore } from '@/stores/conversationStore';
import {Delete} from "@element-plus/icons-vue";

const conversationStore = useConversationStore();
const conversationIds=conversationStore.conversationIds;

const deleteConversation= (conversationId: string) => {
  conversationStore.deleteConversationFromHistory(conversationId);
};



</script>
<style scoped>
.delete {
  color: gray;
  justify-content:flex-end;
}
.delete:hover {
  color: #c37373;
}

.container {
  position: relative;
  height: 100%;
  width: 100%;
  display: flex;
  flex-direction: column;
}
.edit {
  width: 1000px;
  position: absolute;
  top: 50px;
  left: 55px;
  height: 750px;
  overflow-y: auto;

}
.edit ul {
  list-style-type: none;
  padding: 0;

}

.edit li {
  display: flex; /* 将 <li> 元素设置为 Flex 容器 */
  flex-direction: row;
  justify-content: space-between;

  text-align: left;
  gap: 10px; /* 设置子元素之间的间距为 10px */
  padding:0 25px;/*上下 左右*/

  border-radius: 15px;
  line-height: 60px;
  font-size: 17px;
  cursor: pointer;
  margin-bottom: 15px;
  background-color: #F5F7F9;
}

.edit li:hover {

  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.15);
}
.edit el-button{
  justify-content:flex-end;
}
.action-buttons {
  gap:10px;
  display: flex;
  align-items: center;
}
</style>