<!-- This code was generated by Builder.io -->
<template>
  <div class="main-container">
    <header class="resource-header">
      <h1 class="resource-title">Resource</h1>
    </header>
    <div class="resource-description">
      <p>Discover more projects</p>
    </div>
    <div class="resource-content">
      <p>
        <span class="transparent-background">Use your designs or a sample design from the Figma Community to try
          out the plugin</span>
      </p>
    </div>
    <div class="custom-html-container">
      <div class="custom-html">
        <p class="word-color">Hello there, I am custom HTML code!</p>
        <div class="word-color">QQQQQ</div>
      </div>
    </div>
    <slot />
    <div class="input-container">
      <label for="text-input" class="input-label">Enter some text...</label>
      <input type="text" id="text-input" class="text-input" />
    </div>
    <div class="custom-html-container">
      <div class="custom-html">
        <p class="word-color">Hello there, I am custom HTML code!</p>
        <div class="word-color">QQQQQ</div>
      </div>
    </div>
    <img loading="lazy" srcSet="..." alt="pic" class="image" />
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
};
</script>

<style scoped>
.main-container {
  display: flex;
  padding: 20px;
  flex-direction: column;
  background-color: rgba(56, 0, 66, 1);
  margin-bottom: 4px;
}

.resource-header {
  color: #caf829;
  font-family: Poppins, sans-serif;
  font-size: 50px;
  font-weight: 500;
  line-height: 170.36%;
  letter-spacing: -1px;
  align-self: start;
  width: 1177px;
  max-width: 100%;
}

@media (max-width: 991px) {
  .resource-header {
    font-size: 40px;
  }
}

.resource-description {
  color: #fff;
  font-family: Poppins, sans-serif;
  font-size: 72px;
  font-weight: 400;
  line-height: 118.31%;
  letter-spacing: -2.88px;
  align-self: stretch;
  margin-top: 50px;
}

@media (max-width: 991px) {
  .resource-description {
    max-width: 100%;
    font-size: 40px;
  }
}

.resource-content {
  align-self: start;
  color: #fff;
  font-feature-settings: "clig" off, "liga" off;
  font-family: Inter, sans-serif;
  font-size: 40px;
  font-weight: 400;
  line-height: 140%;
  margin-top: 20px;
  width: 100%;
}

@media (max-width: 991px) {
  .resource-content {
    max-width: 100%;
  }
}

.custom-html-container {
  display: flex;
  flex-direction: column;
  position: relative;
  margin-top: 20px;
}

.slot {
  display: flex;
  flex-direction: column;
  position: relative;
  margin-top: 20px;
}

.input-container {
  position: relative;
  margin-top: 20px;
  height: auto;
}

.input-label {
  color: #fff;
}

.text-input {
  padding: 10px;
}

.custom-html-container {
  display: flex;
  flex-direction: column;
  position: relative;
  margin-top: 20px;
  height: auto;
  padding-bottom: 30px;
}

.image {
  aspect-ratio: 3.23;
  object-fit: contain;
  object-position: center;
  width: 100%;
  margin-top: 20px;
  min-height: 400px;
  min-width: 20px;
  overflow: hidden;
  cursor: pointer;
  pointer-events: auto;
  margin-right: auto;
  max-width: 1071px;
  margin-left: auto;
}
</style>
