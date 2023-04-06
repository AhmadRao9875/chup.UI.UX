<template>
  <div class="mark-arrival-container">
    <div class="mark-arrival-wrapper">
      <div class="mark-arrival-back-button-bar">
        <div class="back-button">
          <button class="mark-arrival-back-button">
            <div class="svg-image">
              <img src="../assets/home.svg" alt="" />
            </div>

            <span class="back-text">Home Page</span>
          </button>
        </div>
        <div class="title-text">
          <h4 class="enter-phone">Enter Phone</h4>
        </div>
      </div>
      <div class="phone-details">
        <svg width="50" height="50">
          <circle cx="25" cy="25" r="20" fill="#f16527" />
          <path
            d="M15 25 L22 32 L35 18"
            stroke="#FFFFFF"
            stroke-width="4"
            fill="none"
          />
        </svg>
        <div class="phone-title">
          <h4>Please , enter your phone number to mark your ARRIVAL</h4>
        </div>
        <div class="phone-number">
          <div class="phone-number-container">
            <select class="my-select">
              <option value="option1">Us</option>
              <option value="option2">UK</option>
              <option value="option3">GreenWay</option>
            </select>
            <input
              type="tel"
              placeholder="enter your phone"
              class="phone-field"
            />
          </div>
        </div>
        <div class="confirm-button">
          <button class="confirmation">Confirm</button>
        </div>
        <div class="powerd-by">
          <div>Powerd by</div>
          <span> <img src="../assets/icons8-disney-logo.svg" alt="" /></span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "markArrival",
};
</script>

<style>
.mark-arrival-container {
  margin: 0 auto;
}
.mark-arrival-wrapper {
  padding: 3rem 10rem;
}
.mark-arrival-back-button-bar {
  display: flex;
  flex-direction: row;
  width: 100%;
  justify-content: space-between;
  align-items: center;
}
.back-button {
  width: 50%;
}
.mark-arrival-back-button {
  border: none;
  background: none;
  padding: 0;
  display: flex;
  flex-direction: row;
  width: 50%;
  justify-content: center;
  align-items: center;
}
.title-text {
  text-align: left;
  width: 50%;
}
.enter-phone {
  font-size: 16px;
  font-weight: bold;
  color: #000;
  padding-left: 10px;
}

.back-text {
  font-size: 16px;
  font-weight: bold;
  color: #000;
  padding-left: 10px;
}
.phone-details {
  padding-top: 2rem;
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding-left: 5rem;
}
.phone-title {
  width: 25%;
  text-align: center;
}
.phone-number {
}
.phone-number-container {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  padding-top: 2rem;
}
.my-select {
  border-right: none;
  width: auto;
  max-width: 4rem;
  border-radius: 0.5rem;
  border-top-right-radius: 0;
  border-bottom-right-radius: 0;
}
.phone-field {
  border-left: none;
  max-width: 10rem;
  border-radius: 0.5rem;
  border-top-left-radius: 0;
  border-bottom-left-radius: 0;
}
input,
select {
  box-sizing: border-box;
  height: 2rem;
  padding: 0rem 0.5rem;
  font-size: 16px;
  border: 1px solid #ccc;
  border-radius: 4px;
}
.confirm-button {
  padding-top: 1rem;
}
.confirmation {
  width: 15rem;
  height: 2.5rem;
  border-radius: 2rem;
  background-color: #125834;
  color: white;
  font-weight: bold;
}
</style>
