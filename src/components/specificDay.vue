<template>
  <div class="specificDay-container">
    <div class="specificDay-inner">
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
          Choose the hour and dates you would like the staff to be ON in, You
          can chnage a period of dates or seprated dates.
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
      <hr />
      <div class="onOff">
        <h3>On or Off</h3>
        <div class="onOff-buttons">
          <div class="onButton">
            <button class="onof-buttons toggle-btn">
              <label class="toggle">
                <input type="checkbox" />
                <span class="slider round"></span>
              </label>
              On
            </button>
          </div>
          <div class="offButton">
            <button class="onof-buttons toggle-btn">
              <label class="toggle">
                <input type="checkbox" />
                <span class="slider round"></span> </label
              >Off
            </button>
          </div>
        </div>
      </div>
      <hr />
      <div class="for">
        <div class="for-title">
          <h4>For</h4>
        </div>
        <div class="check-values">
          <label class="for-label">
            <input type="checkbox" />
            All
          </label>
          <label class="for-label">
            <input type="checkbox" />
            Walk In
          </label>
          <label class="for-label">
            <input type="checkbox" />
            Live Queue
          </label>
          <label class="for-label">
            <input type="checkbox" />
            Appointment
          </label>
        </div>
      </div>
      <hr />
      <div class="date">
        <div class="date-title"><h4>Date</h4></div>
        <div class="date-radio-values">
          <label class="for-label">
            <input type="radio" name="data-option" />
            Add End Date
          </label>
          <label class="for-label">
            <input type="radio" name="data-option" />
            Add Separated Date
          </label>
        </div>
        <div class="selected-dates">
          <div class="single-date">
            <svg
              class="cross-svg"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 24 24"
              style="width: 10px; height: 10px; border-radius: 50%"
            >
              <rect width="100%" height="100%" fill="rgb(100, 200,10)" />
              <line
                x1="5"
                y1="12"
                x2="19"
                y2="12"
                stroke="#fff"
                stroke-width="3"
              />
            </svg>
            <div class="selected-date">12 Feb, 2023</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "specificDay",
  data() {
    return {
      showOption: true,
      selectedOption: {},
      showOptions: false,
      showSVG: true,
      isOn: false,
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
    toggleSlider() {
      this.isOn = !this.isOn;
    },
  },
};
</script>

<style scoped>
.specificDay-container {
  margin: 0 auto;
}
.specificDay-inner {
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
  align-items: center;
  /* flex-wrap: wrap; */
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
  margin-bottom: 1rem;
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
.form-control {
  width: 90%;
  height: 2rem;
  border: 2px solid gray;
  border-radius: 0.5rem;
}
.onOff {
  display: flex;
  flex-direction: column;
}
.onOff-buttons {
  display: flex;
  flex-direction: row;
  position: relative;
  flex-wrap: wrap;
  max-width: 50%;
  gap: 1rem;
}
.onof-buttons {
  position: relative;
  width: 9rem;
  height: 2rem;
  border-radius: 0.2rem;
}

/* buttons */

/* toggler */
.toggle-btn {
  display: inline-block;
  color: black;
  border: none;
  text-align: start;
}

.toggle {
  position: absolute;
  top: 50%;
  right: 10px;
  transform: translateY(-50%);
  display: inline-block;
  width: 2rem;
  height: 1rem;
}

.toggle input {
  display: none;
}

.slider {
  position: absolute;
  cursor: pointer;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: #c9ccc9;
  -webkit-transition: 0.4s;
  transition: 0.4s;
}

.slider:before {
  position: absolute;
  content: "";
  height: 10px;
  width: 10px;
  left: 4px;
  bottom: 4px;
  background-color: white;
  -webkit-transition: 0.4s;
  transition: 0.4s;
}

input:checked + .slider {
  background-color: #022e03;
}

input:checked + .slider:before {
  -webkit-transform: translateX(19px);
  -ms-transform: translateX(19px);
  transform: translateX(19px);
}

.slider.round {
  border-radius: 34px;
}

.slider.round:before {
  border-radius: 50%;
}
.check-values {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  max-width: 50%;
  flex-wrap: wrap;
}

.for-label {
  display: flex;
  align-items: center;
  padding-right: 5rem;
}
.for-label:last-child {
  padding-right: 0;
}
.date-radio-values {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  max-width: 50%;
  flex-wrap: wrap;
}
.date-radio-values .for-label {
  padding: 0;
}
.selected-dates {
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
}
.cross-svg {
  position: absolute;
  top: 0;
  left: 90%;
}
.selected-date{
    font-weight: bold;
    padding-left: .2rem ;
}
</style>
