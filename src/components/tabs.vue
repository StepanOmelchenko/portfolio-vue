<template lang="pug">
  .tabs
    ul.tabs__list
      li.tabs__item(v-for="tab in tabs")
        router-link(
          :to="tab.href"
        ).tabs__link {{tab.name}}
</template>
<script>
export default {
  data() {
    return {
      tabs: [
        {name: 'Skills', href: "/"},
        {name: 'Works', href: "/pages/about"},
        {name: 'articles', href: "/pages/30"},
        {name: 'Users', href: "/pages/40"}
      ]
    }
  }
}
</script>
<style src="styles/tabs.scss" lang="scss" scoped></style>