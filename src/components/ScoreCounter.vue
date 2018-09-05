<template>
  <div>
    <h3>Team</h3>
    <p>0</p>
    <div>
      <input placeholder="Update Team Name" type="text" name="" value="">
      <button type="Update" name="button" v-on:click="updateName">Update</button>
    </div>
    <div class="">
      <span>Update Score</span>
      <button type="button" name="button" v-on:click="">Add 1</button>
      <button type="button" name="button" v-on:click="">Subtract 1</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ScoreCounter',
  props: {
    team: String
  },

}
</script>

<style lang="css">
</style>
