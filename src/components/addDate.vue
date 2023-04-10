<template>
  <div>
    <button class="single-date add-date" @click="showModal = true">
      <img src="../assets/icons8-calendar-orange.png" alt="" />
      <div class="selected-date add-selected">Add Date</div>
    </button>
    <div v-if="showModal">
      <input type="text" v-model="newDate" @input="$emit('input' , $event.target.value)"/>
      <button @click="addDate" >Add</button>
      <button @click="showModal = false">Cancel</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showModal: false,
      newDate: "",
    };
  },
  methods: {
    addDate() {
      if (this.newDate) {
        console.log(this.newDate);
        this.$emit("add-new-date" , this.newDate);
        this.$emit("show-modal");
        this.newDate = "";
      }
    },
  },
};
</script>

<style scoped>
.selected-dates {
  width: 98%;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
}
.single-date {
  width: 7rem;
  height: 2rem;
  position: relative;
  background-color: rgb(214, 218, 223);
  border-radius: 0.2rem;
  display: flex;
  align-items: center;
  margin-right: 0.3rem;
  cursor: pointer;
}

.single-date:last-child {
  margin-right: 0;
}
.add-date {
  background-color: white;
  border-color: orangered;
}
.cross-svg {
  position: absolute;
  top: 0;
  left: 90%;
}
.selected-date {
  font-weight: bold;
  padding-left: 0.2rem;
}
</style>
