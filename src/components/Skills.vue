<template>
  <div class="hello">
    <div :class="alertObject">
      <h1>{{ message }}</h1>
      <button @click.prevent="changeName" :disabled="btnState">Some text</button>
      <ul>
        <li v-for="(skill, index) in skills" :key="index">{{ skill.name }} is at index {{ index }}</li>
      </ul>
      <p v-if="skills.length >= 1">You have more than one skill</p>
      <p v-else>You need to amass more skills</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Skills',
  data () {
    return {
      skills: [
        { name: "Javeling" },
        { name: "Plumbing" },
      ],
      message: "Some text goes in here",
      alertObject: {
        alert: true
      }

    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style src="./styles/skills.css" scoped>

</style>
