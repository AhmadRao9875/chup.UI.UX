<template>
  <div class="single-time">
    <div class="time-svg">
      <img src="../assets/icons8-clock.svg" alt="" />
    </div>
    <div class="start-end-date">
      <div class="start">
        <select name="time" id="time" v-model="startTime">
          <option
            :value="time"
            v-for="time in times"
            :key="time.index"
          ></option>
        </select>
      </div>

      <svg
        xmlns="http://www.w3.org/2000/svg"
        width="20"
        height="20"
        viewBox="0 0 20 20"
        class="time-between-sign"
      >
        <rect x="2" y="8" width="10" height="1.5" fill="black" />
      </svg>
      <div class="end">
        <select name="end-time" id="end-time" v-model="endTime">
          <option
            :value="time"
            v-for="time in times"
            :key="time.index"
          ></option>
        </select>
      </div>
    </div>
    <div class="remove-svg">
      <img src="../assets/icons8-minus-sign-24.png" alt="" />
    </div>
  </div>
  <button class="single-date add-date" @click="showModal = true">
    <img src="../assets/icons8-calendar-orange.png" alt="" />
    <div class="selected-date add-selected">Add Time</div>
  </button>
</template>
<script>
export default {
  name: "addTime",
  props: {
    times: {
      type: Array,
      required: true,
    },
  },
  data() {
    return {
      showModal: false,
      startTime: "",
      endTime: "",
    };
  },
  methods: {
    addTime() {
      this.$emit("add-new-time", {
        startTime: this.startTime,
        endTime: this.endTime,
      });
      this.startTime = "";
      this.endTime = "";
    },
  },
};
</script>

<style scoped>
.selected-times {
  width: 98%;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  background-color: rgb(214, 218, 223);
}
.single-time {
  width: 100%;
  height: 2rem;

  border-radius: 0.2rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-right: 0.3rem;
  cursor: pointer;
}
select {
  border: none;
  background: transparent;
  font-weight: bold;
  -webkit-appearance: none;
  -moz-appearance: none;
  appearance: none;
  background-image: none;
}
.time-svg {
  width: 10%;
  display: flex;
  align-items: center;
}
.remove-svg {
  width: 70%;
  display: flex;
  justify-content: flex-end;
}
.time-between-sign {
  position: absolute;
}

.start-end-date {
  display: flex;
  width: 20%;
  position: relative;
  align-items: center;
  justify-content: space-around;
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
</style>
