<template>
  <div class="customizedSlots-container">
    <div class="customizedSlots-inner">
      <div class="title-svg">
        <div class="title-box">
          <h1 class="title">Customized Available Slots</h1>
        </div>
        <div class="svg" v-if="showOption" @click="showOptions">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 20 20"
            style="width: 15px; height: 15px"
          >
            <line
              x1="0"
              y1="20"
              x2="20"
              y2="0"
              stroke="#000"
              stroke-width="1.5"
            />
            <line
              x1="0"
              y1="0"
              x2="20"
              y2="20"
              stroke="#000"
              stroke-width="1.5"
            />
          </svg>
        </div>
      </div>
      <hr class="line-break" />
      <div class="alert-text">
        <p class="text">
          Enter the number of slots you would like to be available for each LIVE
          QUEUE, WALK-INs and APPOINTMENTS,
        </p>
      </div>
      <hr />

      <div class="dropdown" @click="showOptions = !showOptions">
        <input
          type="text"
          class="form-control dropdown-toggle"
          v-model="selectedOption"
          placeholder="Select an option"
        />
        <svg
          v-if="showSVG"
          class="dropdown-icon"
          viewBox="0 0 24 24"
          style="width: 15px; height: 15px"
        >
          <path
            fill="currentColor"
            d="M7.41,8.58L12,13.17l4.59-4.59c0.39-0.39,1.02-0.39,1.41,0l0,0c0.39,0.39,0.39,1.02,0,1.41l-5,5C12.01,15.39,11.74,15.5,11.5,15.5s-0.51-0.11-0.71-0.29l-5-5C6.97,9.6,6.97,8.97,7.41,8.58z"
          ></path>
        </svg>
        <div
          class="dropdown-menu"
          :class="{ show: showOptions }"
          aria-labelledby="dropdownMenuButton"
        >
          <a
            v-for="(option, index) in options"
            :key="index"
            class="dropdown-item"
            href="#"
            @click="selectOption(option)"
          >
            <img
              :src="option.profilePic"
              :alt="option.name"
              class="profile-pic"
            />
            <span class="name">{{ option.name }}</span>
          </a>
        </div>
      </div>
      <div class="day-year-dropdown">
        <div class="day-drop">
          <select name="day" id="day" class="days">
            <option value="" selected disabled>Day</option>
            <option value="monday">Monday</option>
            <option value="monda">Tuesday</option>
            <option value="mond">Wednesday</option>
            <option value="mon">Thursday</option>
            <option value="mo">Friday</option>
            <option value="m">Saturday</option>
          </select>
        </div>
        <div class="year-drop"></div>
      </div>
      <hr />
      <div class="morning-slots">
        <div class="morning-title">
          <h2>Morning's Slots</h2>
        </div>
        <div class="live-slots">
          <div class="title">Live Queue Slots</div>
          <div>
            <input
              type="number"
              placeholder="0"
              min="0"
              v-model="liveSlots"
              class="live-input"
            />
          </div>
        </div>
        <div class="walkin-slots live-slots">
          <div class="title">Live Queue Slots</div>
          <div>
            <input
              type="number"
              placeholder="0"
              min="0"
              v-model="liveSlots"
              class="live-input"
            />
          </div>
        </div>
        <div class="appointment-slots live-slots">
          <div class="title">Live Queue Slots</div>
          <div>
            <input
              type="number"
              placeholder="0"
              min="0"
              v-model="liveSlots"
              class="live-input"
            />
          </div>
        </div>
      </div>
      <div class="morning-slots afternoon-slots">
        <div class="morning-title afternoon-title">
          <h2>Afternoon's Slots</h2>
        </div>
        <div class="live-slots">
          <div class="title">Live Queue Slots</div>
          <div>
            <input
              type="number"
              placeholder="0"
              min="0"
              v-model="liveSlots"
              class="live-input"
            />
          </div>
        </div>
        <div class="walkin-slots live-slots">
          <div class="title">Live Queue Slots</div>
          <div>
            <input
              type="number"
              placeholder="0"
              min="0"
              v-model="liveSlots"
              class="live-input"
            />
          </div>
        </div>
        <div class="appointment-slots live-slots">
          <div class="title">Live Queue Slots</div>
          <div>
            <input
              type="number"
              placeholder="0"
              min="0"
              v-model="liveSlots"
              class="live-input"
            />
          </div>
        </div>
      </div>
      <hr class="line-break" />
      <div class="clearall-sve-button">
        <button class="clearall-button" @click="clear">Cear All</button>
        <button class="sve-button" @click="move">Save</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "customizedSlots",
  data() {
    return {
      showOption: true,
      selectedOption: {},
      showOptions: false,
      showSVG: true,
      options: [
        { name: "John Doe", profilePic: "profile_pic_1.jpg" },
        { name: "Jane Smith", profilePic: "profile_pic_2.jpg" },
        { name: "Bob Johnson", profilePic: "profile_pic_3.jpg" },
        // Add more options here as needed
      ],
    };
  },
  mounted() {
    // Set the default option as the first option in the list
    console.log(this.selectOption);
    this.selectedOption = this.options[0].profilePic;
  },
  methods: {
    selectOption(option) {
      this.showSVG = false;
      this.selectedOption = option.name;
      this.showOptions = false;
      this.showSVG = true;
      // Do something with the selected option
    },
  },
};
</script>

<style scoped>
.customizedSlots-container {
  margin: 0 auto;
}
.customizedSlots-inner {
  padding: 1rem 2rem;
}
h1,
h2,
h3,
h4,
h5,
h6,
p,
li,
ul {
  margin: 0;
  padding: 0;
}
hr {
  width: 99%;
}

hr.line-break {
  border: none;
  border-top: 2px dotted blue;
  color: blue;
  /* background-color: blue; */
  height: 2px;
  margin: 0;
}

.title-svg {
  display: flex;
  width: 100%;
  align-items: center;
}
.title-box {
  width: 50%;
  padding-bottom: 1rem;
}

.svg {
  padding-left: 1rem;
  width: 50%;
  justify-content: end;
  display: flex;
}

.alert-text {
  padding: 1rem 1rem;
}

.text {
  color: gray;
}
.dropdown {
  position: relative;
  margin-top: 1rem;
}
.dropdown-item {
  display: flex;
  align-items: center;
}

.dropdown-icon {
  position: absolute;
  right: 10%;
  top: 50%;
  transform: translateY(-50%);
  fill: #333;
  pointer-events: none;
}

.profile-pic {
  width: 30px;
  height: 30px;
  border-radius: 50%;
  margin-right: 10px;
}

.name {
  font-weight: bold;
}
.dropdown-menu {
  display: none;
}
.show {
  display: block;
}
input {
  width: 90%;
  height: 2rem;
  border: 2px solid gray;
  border-radius: 0.5rem;
}

select option:disabled {
  color: gray;
}

.day-drop {
  padding-top: 1rem;
}
.days {
  width: 7rem;
  height: 2rem;
  border-radius: 0.2rem;
}
.morning-slots {
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
}
.afternoon-slots {
  padding-bottom: 1rem;
}
.live-slots {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  background-color: rgb(217, 213, 213);
  border: transparent;
  border-radius: 0.5rem;
  height: 3rem;
}
.title {
  padding-left: 0.5rem;
}
.morning-title {
  padding-top: 1rem;
}
.live-input {
  background: transparent;
  height: 2rem;
  max-width: 10rem;
  text-align: center;
  border-color: orangered;
}

.live-input::placeholder {
  color: orangered;
}
.clearall-sve-button {
  padding-top: 1rem;
  display: flex;
  justify-content: flex-end;
}
.clearall-button,
.sve-button {
  width: 8rem;
  height: 2rem;
  border-radius: 1rem;
  text-align: center;
}
.sve-button {
  background-color: rgb(229, 230, 229);
  color: rgb(136, 135, 135);
  font-weight: bold;
  border: none;
}
.clearall-button {
  background-color: white;
  border-color: rgb(199, 196, 196);
  border-radius: 1rem;
}

/* media Query */
@media only screen and (max-width: 600px) {
  .customizedSlots-inner {
    padding: 0;
  }
}
</style>
