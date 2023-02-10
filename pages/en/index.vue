<template>
  <div>
    <ContentList
      v-slot="{ list }"
      :query="{
        limit: 10,
        only: ['title', 'subtitle', 'author', 'updatedAt', 'head', '_path'],
      }"
    >
      <div v-for="article in list" :key="article._path">
        {{ article.title }}
      </div>
    </ContentList>
  </div>
</template>
