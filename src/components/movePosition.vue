<template>
  <div class="position-conatainer">
    <div class="position-conatainer-inner">
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
          <h1 class="title">Move Position</h1>
        </div>
      </div>
      <hr />
    </div>
    <div class="positions">
      <div class="sub-head">
        <h2>Move Position</h2>
      </div>
      <div class="radios">
        <div>
          <label>
            <input
              type="radio"
              name="option"
              value="1"
              v-model="selectedOption"
            />
            Option 1
          </label>
          <label>
            <input
              type="radio"
              name="option"
              value="2"
              v-model="selectedOption"
            />
            Option 2
          </label>
          <label>
            <input type="radio" name="quantity" value="1" />
            <button
              class="quantity-button"
              type="button"
              @click="decreaseQuantity"
            >
              -
            </button>
            <input
              type="number"
              name="quantity"
              v-model="quantity"
              min="1"
              max="100"
            />
            <button
              class="quantity-button"
              type="button"
              @click="increaseQuantity"
            >
              +
            </button>
          </label>
        </div>
      </div>
    </div>
    <hr />
    <div class="service">
      <div class="sub-head">
        <h2>Service</h2>
      </div>
      <div class="service-options">
        <label>
          <input
            type="radio"
            name="option"
            value="1"
            v-model="selectedOption"
          />
          Option 1
        </label>
        <label>
          <input
            type="radio"
            name="option"
            value="1"
            v-model="selectedOption"
          />
          Option 1
        </label>
        <label>
          <input
            type="radio"
            name="option"
            value="1"
            v-model="selectedOption"
          />
          Option 1
        </label>
        <label>
          <input
            type="radio"
            name="option"
            value="1"
            v-model="selectedOption"
          />
          Option 1
        </label>
        <label>
          <input
            type="radio"
            name="option"
            value="1"
            v-model="selectedOption"
          />
          Option 1
        </label>
        <label>
          <input
            type="radio"
            name="option"
            value="1"
            v-model="selectedOption"
          />
          Option 1
        </label>
        <label>
          <input
            type="radio"
            name="option"
            value="1"
            v-model="selectedOption"
          />
          Option 1
        </label>
        <label>
          <input
            type="radio"
            name="option"
            value="1"
            v-model="selectedOption"
          />
          Option 1
        </label>
        <label>
          <input
            type="radio"
            name="option"
            value="1"
            v-model="selectedOption"
          />
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
          <input
            type="radio"
            name="option"
            value="1"
            v-model="selectedOption"
          />
          Option 1
        </label>
        <label>
          <input
            type="radio"
            name="option"
            value="1"
            v-model="selectedOption"
          />
          Option 1
        </label>
        <label>
          <input
            type="radio"
            name="option"
            value="1"
            v-model="selectedOption"
          />
          Option 1
        </label>
        <label>
          <input
            type="radio"
            name="option"
            value="1"
            v-model="selectedOption"
          />
          Option 1
        </label>
        <label>
          <input
            type="radio"
            name="option"
            value="1"
            v-model="selectedOption"
          />
          Option 1
        </label>
        <label>
          <input
            type="radio"
            name="option"
            value="1"
            v-model="selectedOption"
          />
          Option 1
        </label>
        <label>
          <input
            type="radio"
            name="option"
            value="1"
            v-model="selectedOption"
          />
          Option 1
        </label>
        <label>
          <input
            type="radio"
            name="option"
            value="1"
            v-model="selectedOption"
          />
          Option 1
        </label>
        <label>
          <input
            type="radio"
            name="option"
            value="1"
            v-model="selectedOption"
          />
          Option 1
        </label>
      </div>
      <button class="showmore">show More</button>
    </div>
    <hr />
    <div class="move-clear-buttons">
      <button class="move-button" @click="move">Move</button>
      <button class="clear-button" @click="clear">Cear All</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "movePosition",
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
    showOptions(){
        this.showOption = !this.showOption;
    }
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

input[type="number"] {
  width: 20px;
  height: 20px;
  border-radius: 5px;
  border: none;
  font-weight: bold;
  text-align: center;
  appearance: textfield;
  background-color: rgb(180, 177, 177);
}
input[type="number"]::-webkit-outer-spin-button,
input[type="number"]::-webkit-inner-spin-button {
  -webkit-appearance: none;
  margin: 0;
}

.quantity-button {
  width: 20px;
  height: 20px;
  font-weight: bold;
  text-align: center;
  color: rgb(189, 186, 186);
  background-color: white;
  border-color: rgb(189, 186, 186);
  border-radius: 5px;
  margin: 0.2rem;
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

.move-clear-buttons {
  display: flex;
}
.clear-button,
.move-button {
  width: 8rem;
  height: 2rem;
  border-radius: 1rem;
  text-align: center;
}
.move-button {
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
