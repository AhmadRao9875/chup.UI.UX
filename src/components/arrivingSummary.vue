<template>
  <div class="arriving-summary-container">
    <div class="arriving-summary-warapper">
      <div class="arrival-summary-back-button-bar">
        <div class="arrival-back-button">
          <div>
            <button class="arrival-summary-back-button">
              <div class="svg-image">
                <img src="../assets/home.svg" alt="" />
              </div>
              <span class="arrival-back-text">Home Page</span>
            </button>
          </div>
        </div>
        <div class="title-text">
          <h4 class="enter-phone">Arriving Summary</h4>
        </div>
      </div>
      <div class="arrival-summary-content">
        <div class="arrival-details">
          <div class="logo-container">
            <img src="../assets/icons8-disney-logo.svg" alt="" />
          </div>
          <div class="arrival-place-ewt">
            <div class="arrival-place-containr">
              <div class="arrival-place-text">Place in Queue</div>
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
        </div>
        <div class="live-queue">
          <div class="queue-title">
            <h4>The Live Queue Of Pharmacy</h4>
          </div>
          <div class="waiting-card">
            <div class="name-info">
              <span class="number"
                >1.
                <span class="name">John Doe</span>
              </span>
              <span class="time">49 min</span>
            </div>
            <div class="phone-info">
              <h4>030************</h4>
            </div>
          </div>
          <div class="leave-queue">
            <div class="button-card">
              <button class="leave-button">
                <div class="svg-image">
                  <img src="../assets/icons8-cancel.svg" alt="" />
                </div>

                <span class="leave-queue-text">Leave live queue</span>
              </button>
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
  name: "arrivingSummary",
};
</script>

<style>
h1,
h2,
h3,
h4,
h5,
h6,
p {
  margin: 0;
  padding: 0;
}
.arriving-summary-container {
  margin: 0 auto;
}
.arriving-summary-warapper {
  padding: 3rem 10rem;
}

.arrival-summary-back-button-bar {
  display: flex;
  flex-direction: row;
  width: 100%;
  justify-content: space-between;
  align-items: center;
}
.arrival-back-button {
  width: 50%;
  justify-content: center;
  align-items: center;
  display: flex;
  flex-direction: row;
}
.arrival-summary-back-button {
  /* border: none; */
  background: none;
  border-radius: 1rem;
  border-color: green;
  padding: auto;
  display: flex;
  height: 2.5rem;
  flex-direction: row;
  max-width: 20rem;
  width: 10rem;
  justify-content: center;
  align-items: center;
}
.arrival-back-text {
  font-size: 16px;
  font-weight: bold;
  color: #023c0c;
  padding-left: 10px;
}
.title-text {
  text-align: left;
  width: 50%;
}
.arrival-summary-content {
  display: flex;
  width: 100%;
  flex-direction: row;
  padding-top: 2rem;
}
.arrival-details {
  display: flex;
  flex-direction: column;
  width: 50%;
  justify-content: center;
  align-items: center;
}
.arrival-details {
  display: flex;
  flex-direction: column;
  width: 50%;
  border-right: 1px solid black;
  justify-content: center;
  align-items: center;
  gap: 1rem;
}

.arrival-place-ewt {
  padding: 1rem 1rem;
  display: flex;
  justify-content: space-between;
  flex-direction: row;
  width: 15rem;
  height: 2rem;
  background-color: #f1e4db;
  border-radius: 0.5rem;
}
.arrival-place-containr {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.arrival-place-text {
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
  text-align: start;
}
li {
  display: flex;
  justify-content: space-between;
}
.live-queue {
  display: flex;
  flex-direction: column;
  width: 50%;
  height: auto;
  justify-content: center;
  align-items: center;
  gap: 1rem;
}
.queue-title {
  padding-bottom: 1rem;
}
.waiting-card {
  padding: 1rem;
  width: 17rem;
  height: 2rem;
  background-color: #fff;
  border-radius: 0.5rem;
  border: 2px solid rgb(213, 211, 211);
  display: flex;
  flex-direction: column;
}
.name-info {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
.number,
.name,
.time {
  display: inline-block;
  margin-right: 10px;
}

.number {
  font-weight: bold;
}

.phone-info {
  display: inline-block;
}
.button-card {
  padding: 1rem;
  width: 17rem;
  height: 2rem;
  background-color: #fff;
  border-radius: 0.5rem;
  border: 2px solid rgb(213, 211, 211);
  display: flex;
  justify-content: center;
  align-items: center;
}
.leave-button {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 13rem;
  height: 3rem;
  border-radius: 2rem;
  background-color: #fcfdfd;
  color: white;
  font-weight: bold;
  border: 2px solid rgb(248, 3, 44);
}
.leave-queue-text {
  font-size: 13px;
  font-weight: bold;
  color: #fb0505;
  padding-left: 10px;
}
.svg-image img {
  width: 15px;
  height: 15px;
}
</style>
