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
            <button class="onof-buttons off-toggle-button toggle-btn">
              <label class="toggle">
                <input type="checkbox" />
                <span class="slider round"></span> </label
              >Off (Close All the Day)
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
          <div
            v-for="(date, index) in dates"
            :key="date.index"
            :date="date"
            class="single-date"
            @click="removeDate(date, index)"
          >
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
            <div class="selected-date">{{ date.day1 }}</div>
          </div>
          <addDate @add-new-date="addNewDate" @show-modal="showModal = false" />
        </div>
      </div>
      <hr />
      <div class="date time">
        <div class="date-title time-title"><h4>Times</h4></div>
        <div class="selected-times">
          <div class="single-time">
            <div class="time-svg">
              <img src="../assets/icons8-clock.svg" alt="" />
            </div>
            <div class="start-end-date">
              <div class="start">
                <select name="time" id="time">
                  <option value="">1:00am</option>
                  <option value="">2:00am</option>
                  <option value="">3:00am</option>
                  <option value="">4:00am</option>
                  <option value="">5:00am</option>
                  <option value="">6:00am</option>
                  <option value="">7:00am</option>
                  <option value="">8:00am</option>
                  <option value="">9:00am</option>
                  <option value="">10:00am</option>
                  <option value="">11:00am</option>
                  <option value="">12</option>
                  <option value="">1:00pm</option>
                  <option value="">2:00pm</option>
                  <option value="">3:00pm</option>
                  <option value="">4:00pm</option>
                  <option value="">5:00pm</option>
                  <option value="">6:00pm</option>
                  <option value="">7:00pm</option>
                  <option value="">8:00pm</option>
                  <option value="">9:00pm</option>
                  <option value="">10:00pm</option>
                  <option value="">11:00pm</option>
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
                <select name="end-time" id="end-time">
                  <option value="">1:00am</option>
                  <option value="">2:00am</option>
                  <option value="">3:00am</option>
                  <option value="">4:00am</option>
                  <option value="">5:00am</option>
                  <option value="">6:00am</option>
                  <option value="">7:00am</option>
                  <option value="">8:00am</option>
                  <option value="">9:00am</option>
                  <option value="">10:00am</option>
                  <option value="">11:00am</option>
                  <option value="">12</option>
                  <option value="">1:00pm</option>
                  <option value="">2:00pm</option>
                  <option value="">3:00pm</option>
                  <option value="">4:00pm</option>
                  <option value="">5:00pm</option>
                  <option value="">6:00pm</option>
                  <option value="">7:00pm</option>
                  <option value="">8:00pm</option>
                  <option value="">9:00pm</option>
                  <option value="">10:00pm</option>
                  <option value="">11:00pm</option>
                </select>
              </div>
            </div>

            <div class="remove-svg">
              <img src="../assets/icons8-minus-sign-24.png" alt="" />
            </div>
          </div>
          <hr />
          <button class="single-date add-date" @click="showModal = true">
            <img src="../assets/icons8-calendar-orange.png" alt="" />
            <div class="selected-date add-selected">Add Date</div>
          </button>
        </div>
      </div>
      <hr />
      <div class="add-description">
        <label for="input">Add Des (Optional)</label>
        <textarea name="myTextArea" rows="4" cols="40"></textarea>
      </div>
      <hr />
      <div class="save-clear-buttons">
        <button class="save-button" @click="move">Save</button>
        <button class="clear-button" @click="clear">Cear All</button>
      </div>
    </div>
  </div>
</template>

<script>
import addDate from "../components/addDate.vue";
export default {
  components: {
    addDate,
  },
  name: "specificDay",
  data() {
    return {
      showOption: true,
      selectedOption: {},
      showOptions: false,
      showSVG: true,
      isOn: false,
      selectedDate: "",
      showModal: false,
      options: [
        { name: "John Doe", profilePic: "profile_pic_1.jpg" },
        { name: "Jane Smith", profilePic: "profile_pic_2.jpg" },
        { name: "Bob Johnson", profilePic: "profile_pic_3.jpg" },
        // Add more options here as needed
      ],
      dates: [
        { day1: "12 feb, 2023" },
        { day1: "13 feb, 2023" },
        { day1: "14 feb, 2023" },
        { day1: "15 feb, 2023" },
        { day1: "16 feb, 2023" },
        { day1: "17 feb, 2023" },
        { day1: "18 feb, 2023" },
        { day1: "19 feb, 2023" },
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
    removeDate(dateToRemove) {
      console.log("method is called");
      const index = this.dates.indexOf(dateToRemove);
      console.log("this is index", index);

      if (index >= 0) {
        this.dates.splice(index, 1);
      }
    },
    addNewDate(selectedDate) {
      this.showModal = false;
      if (selectedDate) {
        const newDateObj = { day1: selectedDate };
        console.log(newDateObj);
        this.dates.push(newDateObj);
        this.selectedDate = "";
      }
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
.off-toggle-button {
  width: 12rem;
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
.add-selected {
  color: orangered;
}
.selected-times {
  background-color: rgb(214, 218, 223);
  width: 98%;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
}
.single-time {
  width: 100%;
  height: 2rem;
  background-color: rgb(214, 218, 223);
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
.add-description {
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
  margin-top: 1rem;
}

.save-clear-buttons {
  display: flex;
}
.clear-button,
.save-button {
  width: 8rem;
  height: 2rem;
  border-radius: 1rem;
  text-align: center;
}
.save-button {
  background-color: rgb(1, 60, 1);
  color: white;
  font-weight: bold;
}
.clear-button {
  background-color: white;
  border-color: rgb(199, 196, 196);
  border-radius: 1rem;
}

/* Media Query  */

@media only screen and (max-width: 600px) {
  .specificDay-inner {
    padding: 0;
  }
  .title-svg {
    flex-direction: column-reverse;
  }
  .svg {
    width: 100%;
  }
  .title-box {
    width: 100%;
  }
  .check-values {
    max-width: 100%;
  }
  .for-label {
    margin: 0;
    padding: 0;
  }
  .date {
    width: 100%;
  }
  .date-radio-values {
    max-width: 100%;
  }
  .selected-dates {
    width: 100%;
    margin: 0;
  }
  .single-date {
    margin: 0;
  }
  .start-end-date {
    width: 33%;
  }
  .remove-svg {
    width: 33%;
  }
  .time-svg {
    width: 33%;
  }
}
</style>
