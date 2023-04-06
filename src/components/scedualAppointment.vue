<template>
  <div class="appointment-container">
    <div class="appointment-wrapper">
      <div class="back-button-bar">
        <button class="back-button">
          <div class="svg-image">
            <svg width="6" height="10">
              <polygon points="6,0 0,5 6,10" />
            </svg>
          </div>

          <span class="back-text">Back</span>
        </button>
        <button class="back-button detail-button">Enter Details</button>
      </div>
      <div class="appointment-content">
        <div class="dr-details">
          <div class="logo-container">
            <img src="../assets/icons8-disney-logo.svg" alt="" />
          </div>
          <div class="date-time">
            <div class="data-time-container">
              <div class="date-container">
                <div class="date-text">Date</div>
                <div class="time">wed, Feb 08 2023</div>
              </div>
              <div class="time-container">
                <div class="time-text">Time</div>
                <div class="time">9:30</div>
              </div>
            </div>
          </div>
          <div class="service-staff">
            <div class="service-staff-container">
              <div class="service-container">
                <div class="service-text">Service</div>
                <div class="service">Pharmacy</div>
              </div>
              <div class="staff-container">
                <div class="staff-text">Staff</div>
                <div class="staff">Dr. Jamauddin Idris</div>
              </div>
            </div>
          </div>
        </div>
        <div class="appointment-details">
          <form class="appointment-form">
            <div class="form-group">
              <label for="name">Name *</label>
              <input
                type="text"
                id="name"
                placeholder="Kadigah Rusian"
                name="name"
                required
              />
            </div>

            <div class="phone-number">
              <label for="phone">Whatsapp Number *</label>
              <div class="phone-number-containers">
                <select class="my-selects">
                  <option value="option1">Us</option>
                  <option value="option2">UK</option>
                  <option value="option3">GreenWay</option>
                </select>
                <input
                  type="tel"
                  placeholder="enter your phone"
                  class="phone-fields"
                />
              </div>
            </div>

            <div class="form-group">
              <label for="email">Email *</label>
              <input
                type="email"
                id="email"
                placeholder="Ex: Jamaluddin@gmail.com"
                name="email"
                required
              />
            </div>
            <div class="submit-button">
              <button class="sub-button" type="submit">
                Schedual Appointment
              </button>
            </div>
            <div class="aggrement">
              <p class="terms">
                By clicking 'Confirm' you agree the Chup's Privacy and Policy
                and Terms of Use
              </p>
            </div>
          </form>
        </div>
      </div>
      <div class="powerd-by">
        <div>Powerd by</div>
        <span> <img src="../assets/icons8-disney-logo.svg" alt="" /></span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "appointmentContainer",
};
</script>

<style>
.appointment-container {
  margin: 0 auto;
}
.appointment-wrapper {
  padding: 3rem 10rem;
}
.back-button-bar {
  display: flex;
  flex-direction: row;
  flex: 1;
  justify-content: space-between;
}
.back-button {
  border: none;
  background: none;
  padding: 0;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}
.detail-button {
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
.appointment-content {
  display: flex;
  flex-direction: row;
  width: 100%;
}
.dr-details {
  display: flex;
  flex-direction: column;
  width: 50%;
  gap: 1rem;
  justify-content: center;
  align-items: center;
}
.logo-container {
  display: flex;
  justify-content: center;
}
.date-time {
  width: 15rem;
  height: 5rem;
  background-color: #f1e4db;
  border-radius: 0.5rem;
}
.data-time-container {
  padding: 1rem 1rem;
  display: flex;
  justify-content: center;
  flex-direction: column;
}
.date-container {
  display: flex;
  justify-content: space-between;
}
.date-text {
  /* padding-right: 2rem; */
}
.date {
  font-weight: bold;
}
.time-container {
  display: flex;
  justify-content: space-between;
}
.time-text {
  /* padding-right: 2rem; */
}
.time {
  font-weight: bold;
  display: flex;
}

.service-staff {
  /* padding-top: 1rem; */
  width: 15rem;
  height: 5rem;
  background-color: #f1e4db;
  border-radius: 0.5rem;
}
.service-staff-container {
  padding: 1rem 1rem;
  display: flex;
  justify-content: center;
  flex-direction: column;
}
.service-container {
  display: flex;
  justify-content: space-between;
}
.service-text {
  /* padding-right: 2rem; */
}
.service {
  font-weight: bold;
  display: flex;
}

.staff-container {
  display: flex;
  justify-content: space-between;
}
.staff--text {
  /* padding-right: 2rem; */
}
.staff {
  font-weight: bold;
}

.appointment-details {
  display: flex;
  flex-direction: column;
  width: 50%;
  border-left: 1px solid black;
}
.appointment-form {
  display: flex;
  /* padding-left: 2rem; */
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.form-group {
  display: flex;
  flex-direction: column;
  margin-bottom: 1rem;
  justify-content: center;
}

label {
  margin-bottom: 0.5rem;
}
/* input {
  width: 15rem;
  height: 1.5rem;
  border-radius: 5px;
  border-color: #ccc;
} */
.Wpnumber {
  border-left: none;
  width: 10rem;
}
.whatsapp-input-group {
  display: flex;
  align-items: center;
}
.phone-number{
    padding-bottom: 1rem;
}
.phone-number-containers {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}
.my-selects {
  border-right: none;
  width: auto;
  max-width: 4rem;
  /* border-radius: 0.5rem; */
  border-top-right-radius: 0;
  border-bottom-right-radius: 0;
}
.phone-fields {
  border-left: none;
  max-width: 10rem;
  /* border-radius: 0.5rem; */
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
.submit-button {
  display: flex;
  justify-content: center;
}
.sub-button {
  width: 12rem;
  height: 2.5rem;
  border-radius: 2rem;
  background-color: #125834;
  color: white;
  font-weight: bold;
}
.aggrement {
  width: 70%;
  text-align: center;
  color: #373535;
}
.powerd-by {
  display: flex;
  flex-direction: row;
  justify-content: center;
  width: 100%;
  align-items: center;
}
</style>
