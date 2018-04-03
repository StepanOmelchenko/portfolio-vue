<template lang="pug">
  li.skill__wrap
      .skill__name {{skill.name}}
      .skill__value 
        input(type="text" :value="skill.percents").input__value
        span &#37; 
      .skill__btn
        button(type="button" @click="removeExistedSkill(skill.id)").btn Удалить
</template>

<script>
import { mapMutations } from "vuex";
export default {
  props: {
    skill: Object
  },
  methods: {
    ...mapMutations(['removeSkill']),
    removeExistedSkill(skillId) {
      this.removeSkill(skillId);
    }
  }
};
</script>

<style lang="scss" scoped>

</style>