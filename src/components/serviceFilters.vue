<template>
  <div class="filter-container">
    <div class="filter-container-inner">
      <div class="title-svg">
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
        <div>
          <h1 class="title">Filters</h1>
        </div>
      </div>
      <hr />

      <div class="positions">
        <div class="sub-head">
          <h2>Customers</h2>
        </div>
        <div class="customer-options">
          <label>
            <input type="radio" value="1" />
            Option 1
          </label>
          <label>
            <input type="radio" value="1" />
            Option 1
          </label>
        </div>
      </div>
      <hr />
      <div class="service">
        <div class="sub-head">
          <h2>Status</h2>
        </div>
        <div class="customer-options">
          <label>
            <input type="radio" value="1" />
            Option 1
          </label>
          <label>
            <input type="radio" value="1" />
            Option 1
          </label>
          <label>
            <input type="radio" value="1" />
            Option 1
          </label>
        </div>
      </div>
      <hr />
      <div class="service">
        <div class="sub-head">
          <h2>Service</h2>
        </div>
        <div class="service-options">
          <label>
            <input type="checkbox" value="1" />
            Option 1
          </label>
          <label>
            <input type="checkbox" value="1" />
            Option 1
          </label>
          <label>
            <input type="checkbox" value="1" />
            Option 1
          </label>
          <label>
            <input type="checkbox" value="1" />
            Option 1
          </label>
          <label>
            <input type="checkbox" value="1" />
            Option 1
          </label>
          <label>
            <input type="checkbox" value="1" />
            Option 1
          </label>
          <label>
            <input type="checkbox" value="1" />
            Option 1
          </label>
          <label>
            <input type="checkbox" value="1" />
            Option 1
          </label>
          <label>
            <input type="checkbox" value="1" />
            Option 1
          </label>
        </div>
        <button class="showmore">show More</button>
      </div>
      <hr />
      <div class="service">
        <div class="sub-head">
          <h2>Staff</h2>
        </div>
        <div class="service-options">
          <label>
            <input type="checkbox" value="1" />
            Option 1
          </label>
          <label>
            <input type="checkbox" value="1" />
            Option 1
          </label>
          <label>
            <input type="checkbox" value="1" />
            Option 1
          </label>
          <label>
            <input type="checkbox" value="1" />
            Option 1
          </label>
          <label>
            <input type="checkbox" value="1" />
            Option 1
          </label>
          <label>
            <input type="checkbox" value="1" />
            Option 1
          </label>
          <label>
            <input type="checkbox" value="1" />
            Option 1
          </label>
          <label>
            <input type="checkbox" value="1" />
            Option 1
          </label>
          <label>
            <input type="checkbox" value="1" />
            Option 1
          </label>
        </div>
        <button class="showmore">show More</button>
      </div>
      <hr />
      <div class="positions">
        <div class="sub-head">
          <h2>Waited Time</h2>
        </div>
        <div class="customer-options waited-time">
          <label>
            <input type="radio" value="1" />
            Option 1
          </label>
          <label>
            <input type="radio" value="1" />
            Option 1
          </label>
        </div>
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
export default {
  name: "serviceFilters",
  data() {
    return {
      selectedOption: "",
      quantity: 1,
      showOption: true,
    };
  },
  methods: {
    decreaseQuantity() {
      if (this.quantity >= 2) {
        this.quantity--;
      }
    },
    increaseQuantity() {
      if (this.quantity >= 1) {
        this.quantity++;
      }
    },
    showOptions() {
      this.showOption = !this.showOption;
    },
  },
};
</script>

<style scoped>
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
.position-container {
  margin: 0 auto;
}
.position-container-inner {
  padding: 1rem 2rem;
}
.title-svg {
  display: flex;
  width: 100%;
  align-items: center;
}
.title {
}

.svg {
  padding-left: 1rem;
  width: 30%;
}
label {
  display: block;
  padding-bottom: 0.7rem;
  padding-left: 0.5rem;
}
.sub-head {
  padding-bottom: 1rem;
}
.positions {
  display: flex;
  flex-direction: column;
}

.waited-time {
  padding-bottom: 1rem;
}

.customer-options {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
}

.service-options {
  display: flex;
  flex-direction: column;
  flex-wrap: wrap;
  height: 9rem;
}
.showmore {
  border: none;
  font-weight: bold;
  background: transparent;
  text-decoration: underline;
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
</style>
