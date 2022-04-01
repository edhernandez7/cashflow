<template>
  <Layout>
    <template #header>
      <Header></Header>
    </template>
  </Layout>
</template>

<script>
import Layout from '@/components/Layout.vue';
import Header from '@/components/Header.vue';

export default {
  name: "HomeApp",
  components: {
    Layout,
    Header,
  },
};
</script>
