<template>
  <h1 class="text-2xl">
    TypeScript一路向北
  </h1>
  <article>
    <p>{{ $route.params.slug }}</p>
    <ContentDoc class="prose lg:prose-xl prose-slate" path="/articles/" />
    <ContentDoc class="prose lg:prose-xl prose-slate" path="/wind/" />
  </article>
</template>
<!-- <template> -->
<!--  <main> -->
<!--    <ContentList v-slot="{ list }" path="/articles"> -->
<!--      <div v-for="article in list" :key="article._path"> -->
<!--        <h2>{{ article.title }}</h2> -->
<!--        <p>{{ article.description }}</p> -->
<!--      </div> -->
<!--    </ContentList> -->
<!--  </main> -->
<!-- </template> -->
