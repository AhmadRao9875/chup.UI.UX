<template>
  <div class="confirmation-container">
    <div class="confirmation-wrapper">
      <div class="back-button-bar">
        <button class="back-button">
          <div class="svg-image">
            <img src="../assets/home.svg" alt="" />
          </div>

          <span class="back-text">Back</span>
        </button>
      </div>
      <div class="confirmation-content">
        <div class="confirmation-message">
          <div class="confirmation-tick">
            <svg width="50" height="50">
              <circle cx="25" cy="25" r="20" fill="#4CAF50" />
              <path
                d="M15 25 L22 32 L35 18"
                stroke="#FFFFFF"
                stroke-width="4"
                fill="none"
              />
            </svg>
          </div>
          <div class="message">
            <h2>
              You Successfully Sheduled an Appointment at the Green Clinic
            </h2>
          </div>
        </div>
        <div class="confirmation-details">
          <div class="place-ewt">
            <div class="place-containr">
              <div class="place-text">Place in Queue</div>
              <div class="place">4th</div>
            </div>
            <div class="ewt-container">
              <div class="ewt-text">EWT</div>
              <div class="ewt">5 min - 16 min</div>
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
          <div class="whatsapp-service">
            <div class="tumbnail-message">
              <div><img src="../assets/icons8-whatsapp.svg" alt="" /></div>
              <div class="short-text">
                <h6 class="short-headin">Sit Tight!</h6>
              </div>
            </div>
            <div class="message-box">
              <p>We will Whatsapp you the Time to come to clinic</p>
            </div>
            <div class="done-button">
              <button class="don-button" type="submit">Done</button>
            </div>
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
  name: "confirmedAppointment",
};
</script>

<style>
h1,
h2,
h3,
h4,
h5,
h6, p {
  margin: 0;
  padding: 0;
}
.confirmation-container {
  margin: 0 auto;
}
.confirmation-wrapper {
  padding: 3rem 10rem;
}
.back-button-bar {
  display: flex;
  flex-direction: row;
  flex: 1;
  justify-content: space-between;
}
.back-button {
  border: 1px solid lightgray;
  border-radius: 20px;
  background: none;
  width: 10rem;
  height: 2.5rem;
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
.confirmation-content {
  display: flex;
  flex-direction: row;
  width: 100%;
}
.confirmation-message {
  display: flex;
  flex-direction: column;
  width: 50%;
  justify-content: center;
  align-items: center;
}
.message {
  width: 80%;
  display: flex;
  text-align: center;
  align-items: center;
  justify-content: center;
  font-weight: bold;
}
.confirmation-details {
  display: flex;
  flex-direction: column;
  width: 50%;
  border-left: 1px solid black;
  justify-content: center;
  align-items: center;
  gap: 1rem;
}

.place-ewt {
  padding: 1rem 1rem;
  display: flex;
  justify-content: space-between;
  flex-direction: row;
  width: 15rem;
  height: 2rem;
  background-color: #f1e4db;
  border-radius: 0.5rem;
}
.place-containr {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.place-text {
  color: grey;
}
.place {
  font-weight: bold;
  display: flex;
}

.ewt-container {
  display: flex;
  border-left: 1px grey;
  flex-direction: column;
}
.ewt-text {
  color: grey;
  text-align: center;
}
.ewt {
  font-weight: bold;
  display: flex;
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
  width: 17rem;
  height: auto;
  background-color: #fff;
  border-radius: 0.5rem;
  border: 2px solid rgb(213, 211, 211);
}
.whatsapp-service {
  border-radius: 0.5rem;
  border: 2px solid rgb(213, 211, 211);
  display: flex;
  align-items: start;
  flex-direction: column;
  width: 15rem;
  padding: 1rem 1rem;
}
.tumbnail-message {
  align-items: center;
  display: flex;
  justify-content: start;
  gap: .7rem;
}
.message-box {
  font-size: 0.7rem;
  font-weight: bold;
}
.done-button {
  display: flex;
  justify-content: center;
}
.don-button {
  width: 15rem;
  height: 2.5rem;
  border-radius: 2rem;
  background-color: #125834;
  color: white;
  font-weight: bold;
}
</style>
