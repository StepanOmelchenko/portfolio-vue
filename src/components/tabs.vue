<template lang="pug">
  .tabs
    ul.tabs__list
      li.tabs__item(v-for="tab in tabs")
        router-link.tabs__link(:to="tab.href" :class="{'tabs__item--active' : tab.active}" v-on:click="setActive(tab)") {{tab.name}}
</template>

<script>
export default {
    data() {
        return {
            tabs: [
                {name: 'About', href: "/", active: true},
                {name: 'Works', href: "/works", active: false},
                {name: 'Articles', href: "/blog", active: false}
            ],
            tabsList: document.querySelectorAll('tabs__item')
        }
    },
    methods: {
        setActive(tab) {
            console.log(tab);
            this.tabsList.forEach((item) => {
                item.active = false;
            });
            tab.active = true;
        }
    }
}
</script>

<style src="styles/tabs.scss" lang="scss" scoped>

</style>