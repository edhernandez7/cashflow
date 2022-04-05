<template>
  <Layout>
    <template #header>
      <Header></Header>
    </template>
    <template #resume>
      <Resume
        :total-label="'Ahorro total'"
        :label="label"
        :total-amount="1000000"
        :amount="amount"
      >
        <template #graphic>
          <Graphic :amounts="amounts" />
        </template>
        <template #action>
          <Action />
        </template>
      </Resume>
    </template>
    <template #movements>
      <Movements :movements="movements" />
    </template>
  </Layout>
</template>

<script>
import Layout from "@/components/Layout.vue";
import Header from "@/components/Header.vue";
import Resume from "@/components/Resume/Index.vue";
import Action from "./Action.vue";
import Movements from "@/components/Movements/Index.vue";
import Graphic from "@/components/Resume/Graphic.vue";

export default {
  name: "HomeApp",
  components: {
    Layout,
    Header,
    Resume,
    Action,
    Movements,
    Graphic,
  },
  data() {
    return {
      label: null,
      amount: null,
      amounts: [100, 200, 500, 200, -400, -600, -300, 0, 300, 500],
      movements: [
        {
          id: 0,
          title: "Movimiento 1",
          description: "Lorem ipsum dolor sit amet",
          amount: 1000,
        },
        {
          id: 1,
          title: "Movimiento 2",
          description: "Lorem ipsum dolor sit amet",
          amount: 1000,
        },
        {
          id: 2,
          title: "Movimiento 3",
          description: "Lorem ipsum dolor sit amet",
          amount: 1000,
        },
        {
          id: 3,
          title: "Movimiento 4",
          description: "Lorem ipsum dolor sit amet",
          amount: -1000,
        },
      ],
    };
  },
};
</script>
