<template>
  <div class="appointment-container">
    <div class="appointment-wrapper">
      <div class="back-button-bar">
        <button class="back-button">
          <div class="svg-image">
            <img src="../assets/home.svg" alt="" />
          </div>

          <span class="back-text">Home Page</span>
        </button>
        <h4 class="summary-text">Appointment Summary</h4>
      </div>
      <div class="summary-content">
        <div class="summary-details">
          <div class="logo-container">
            <img src="../assets/icons8-disney-logo.svg" alt="" />
          </div>
          <div class="summary-date-time">
            <div class="summary-data-time-container">
              <div class="summary-date-container">
                <div class="summary-date-text">Date</div>
                <div class="time">wed, Feb 08 2023</div>
              </div>
              <div class="summary-time-container">
                <div class="summary-time-text">Time</div>
                <div class="time">9:30</div>
              </div>
            </div>
          </div>
          <div class="patatient-details">
            <ul>
              <li>Name: <span class="name">John Smith</span></li>
              <li>Service: <span class="name">Pharmacy</span></li>
              <li>Staff: <span class="name">Dr Jamaluddin Idris</span></li>
              <li>Status: <span class="name">Booked</span></li>
            </ul>
          </div>
        </div>
        <div class="reschedule-cancel-buttons">
          <div class="buttons">
            <button class="reschedual-button">
              <div class="svg-image">
                <img src="../assets/icons8-calendar-24.png" alt="" />
              </div>

              <span class="back-text">Reschedule</span>
            </button>
            <button class="cancel-button">
              <div class="svg-image">
                <img src="../assets/icons8-cancel.svg" alt="" />
              </div>

              <span class="back-text">Cancel Appointment</span>
            </button>
          </div>
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
  name: "appointmentSummary",
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
.summary-text {
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
.summary-content {
  display: flex;
  flex-direction: row;
  width: 100%;
}
.summary-details {
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
.summary-date-time {
  width: 19rem;
  height: 5rem;
  background-color: #f1e4db;
  border-radius: 0.5rem;
}
.summary-data-time-container {
  padding: 1rem 1rem;
  display: flex;
  justify-content: center;
  flex-direction: column;
}
.summary-date-container {
  display: flex;
  justify-content: space-between;
}
.summary-date-text {
  /* padding-right: 2rem; */
}
.date {
  font-weight: bold;
}
.summary-time-container {
  display: flex;
  justify-content: space-between;
}
.summary-time-text {
  /* padding-right: 2rem; */
}
.time {
  font-weight: bold;
  display: flex;
}

.reschedule-cancel-buttons {
  display: flex;
  flex-direction: column;
  width: 50%;
  border-left: 1px solid black;
  justify-content: center;
  align-items: center;
}
.buttons {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  border: 2px solid lightgray;
  padding: 1rem 1rem;
  border-radius: 0.5rem;
}
.reschedual-button {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  width: 17rem;
  height: 3rem;
  border-radius: 2rem;
  background-color: #fdfcfd;
  color: white;
  font-weight: bold;
  border: 2px solid rgb(113, 3, 248);
}
.cancel-button {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  width: 17rem;
  height: 3rem;
  border-radius: 2rem;
  background-color: #fcfdfd;
  color: white;
  font-weight: bold;
  border: 2px solid rgb(248, 3, 44);
}
.appointment-form {
  display: flex;
  /* padding-left: 2rem; */
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
li,
ul {
  list-style: none;
  padding: 0;
}
.name {
  font-weight: bold;
}
li {
  display: flex;
  justify-content: space-between;
}
.patatient-details {
  width: 15rem;
  height: auto;
  padding: 1rem 2rem;
  background-color: #fff;
  border-radius: 0.5rem;
  border: 2px solid rgb(213, 211, 211);
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

.powerd-by {
  display: flex;
  flex-direction: row;
  justify-content: center;
  width: 100%;
  align-items: center;
}
</style>
