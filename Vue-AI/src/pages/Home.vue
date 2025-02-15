<template>
  <div class="main-container">
    <div class="ai-function-container">
      <!-- AI 写作盒子 -->
      <div class="ai-left top">
        <h2>AI 写作</h2>
        <p>在这里可以使用 AI 进行写作相关的操作。无论是创意文章、商业文案还是学术论文，AI 都能为你提供灵感和辅助。</p>
        <div class="ai-button">
        <el-button type="primary" plain >开始写作</el-button>
        </div>
      </div>
      <!-- AI 翻译盒子 -->
      <div class="ai top">
        <h2>AI 翻译</h2>
        <p>使用 AI 进行文本翻译的功能将会在这里实现。支持多种语言互译，快速准确，满足你的各种翻译需求。</p>
        <div class="ai-button">
        <el-button type="primary" plain>开始翻译</el-button>
        </div>
      </div>
      <!-- AI 博客盒子 -->
      <div class="ai-right top">
        <h2>AI 博客</h2>
        <p>AI 辅助博客创作等功能将在这个区域呈现。从选题到内容生成，再到排版优化，AI 全方位助力你的博客创作之旅。</p>
        <div class="ai-button">
        <el-button type="primary" plain>创建博客</el-button>
        </div>
      </div>
      <!-- AI 图像生成盒子 -->
      <div class="ai-left">
        <h2>AI 图像生成</h2>
        <p>通过输入文字描述，AI 可以为你生成逼真的图像。无论是风景、人物还是抽象艺术，都能轻松实现。</p>
        <div class="ai-button">
        <el-button type="primary" plain>生成图像</el-button>
        </div>
      </div>
      <!-- AI 代码辅助盒子 -->
      <div class="ai">
        <h2>AI 代码辅助</h2>
        <p>在编程过程中遇到困难？AI 代码辅助功能可以帮助你快速找到解决方案，提高编程效率。</p>
       <div class="ai-button">
        <el-button type="primary" plain>获取代码建议</el-button>
       </div>
      </div>
      <!-- AI 语音交互盒子 -->
      <div class="ai-right">
        <h2>AI 语音交互</h2>
        <p>与 AI 进行语音交互，通过语音指令完成各种任务，让操作更加便捷。</p>
        <div class="ai-button">
        <el-button type="primary" plain>开始语音交互</el-button>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
// 这里可以添加一些逻辑，比如组件挂载时的初始化等，目前只是简单布局，暂不需要额外逻辑
</script>

<style scoped>
.main-container {
  width: 1110px;
  height: 800px;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #f0f0f0;
  padding: 20px;
  box-sizing: border-box;
}

.ai-function-container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: repeat(2, 1fr);
  gap: 20px;
  width: 100%;
  height: 100%;
}
.ai-left,
.ai-right,
.ai{
  margin:0;
  display: flex;
  flex-direction:column;
  justify-content: center;
  align-items: center;



  height: 300px;
  width:300px;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  background-color: white;
  transition: all 0.3s ease;


}
.ai{
  margin-left: 20px;
}
.ai-left {
  margin-left: 30px;
}
.ai-right {
  margin-right: 30px;
}
.ai-right:hover,
.ai-left:hover,
.ai:hover {
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  transform: translateY(-5px);
}
.top{
  margin-top: 50px;
}

h2 {
  margin-top: 0;
  color: #333;
}

p {
  color: #666;
}

.ai-button {
margin-top: 30px;
}

</style>