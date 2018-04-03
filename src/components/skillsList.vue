<template lang="pug">
  .skills__box
    .skills__title {{skillType}}
    ul.skills__list
      skills-item(
        v-for="skill in skills"
        v-if="convertSkillStringToNum(skillType) === skill.type"
        :key="skill.id"
        :skill="skill"
      )
    skill__input(
      :type="convertSkillStringToNum(skillType)"
    )
</template>
<script>
import skillsItem from "./skillsItem";
import skillInput from "./skillInput";

export default {
  components: { skillsItem, skillInput },
  props: {
    skillType: String,
    skills: Array
  },
  methods: {
    convertSkillStringToNum(skillGroupName) {
      switch (skillGroupName) {
        case "frontend":
          return 1;
        case "workflow":
          return 2;
        case "backend":
          return 3;
      }
    }
  }
};
</script>

<style lang="scss" scoped>

.skills__title {
    font-size: 16px;
    font-weight: 500;
    color: #566358;
    margin-bottom: 20px;
}

.skills__box {
    margin-top: 30px;
    width: 100px;

    &:first-child{
      margin-top: 0;
    }
}

</style>