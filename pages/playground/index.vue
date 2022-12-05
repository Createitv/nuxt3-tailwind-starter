<script setup type='ts'>
const editor = ref(null)
onMounted(() => {
  console.log(editor.value)
  editor.value.contentWindow.postMessage({
    eventType: 'populateCode',
    language: 'typescript',
    files: [
      {
        name: 'main.ts',
        content: 'console.log("example")\n',
      },
    ],
  }, '*')
})
</script>

<template>
  <div>
    <h1>Playground</h1>
    <iframe
      ref="editor"
      height="250px"
      src="https://onecompiler.com/embed/typescript?codeChangeEvent=true&availableLanguages=true&hideLanguageSelection=true&hideNew=true&hideStdin=true&listenToEvents=true&hideTitle=true"
      width="100%"
    />
  </div>
</template>

<style scoped>
#frame {
  font-size: 150%;
}
</style>
