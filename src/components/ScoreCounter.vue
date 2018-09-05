<template>
  <div>
    <h3>{{teamDisplayName}}</h3>
    <p>{{teamDisplayScore}}</p>
    <div>
      <input placeholder="Update Team Name" id="teamInput" type="text" v-model="teamName">
      <button type="Update" name="button" id="updateNameButton" v-on:click="updateName">Update</button>
    </div>
    <div class="">
      <span>Update Score</span>
      <button type="button" name="button" v-on:click="addOne">Add 1</button>
      <button type="button" name="button" v-on:click="subtractOne">Subtract 1</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "ScoreCounter",
  props: {
    team: String
  },
  data: function() {
    return {
      teamName: "",
      teamDisplayName: "Team",
      teamDisplayScore: 0,
    };
  },
  methods: {
    updateName: function() {
      this.teamDisplayName = this.teamName;
    },
    addOne: function() {
      this.teamDisplayScore++;
    },
    subtractOne: function() {
      if (this.teamDisplayScore > 0) {
        this.teamDisplayScore--;
      }
    }
  }
};
</script>

<style lang="css">
</style>
