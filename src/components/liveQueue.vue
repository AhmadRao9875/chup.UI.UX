<template>
  <div class="live-queue-container">
    <div class="live-queue-wrapper">
      <div class="queue-content">
        <div class="welcome-box">
          <div class="logo-container">
            <img src="../assets/icons8-disney-logo.svg" alt="" />
          </div>
          <div class="caption">
            <h1>Welcome To The Green Clinic</h1>
          </div>
          <div class="adress-box">
            <span><img src="../assets/icons8-location-24.png" alt="" /></span>
            <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit.</p>
          </div>
        </div>
        <div class="queue-data">
          <div class="waiting-details">
            <div class="dr-name">
              <h3>Dr Jamaluddin Idris</h3>
            </div>
            <hr />
            <div class="ewt-details">
              <div class="queue-ewt-text">Estimated Waiting Time (EWT)</div>
              <div class="ewt-time">0 min - 12 min</div>
            </div>
            <div class="total-people">
              <div class="people-logo">
                <img src="../assets/icons8-user-account-24.png" alt="" />
              </div>
              <div class="people-text">
                <p>3 People are Waiting</p>
              </div>
            </div>
          </div>
          <div class="join-mark-buttons">
            <div class="buttonss">
              <button class="join-live-button">
                <span class="queue-text">Join Live Queue</span>
              </button>
              <button class="mark-arrival-button">
                <span class="arrival-text">Mark Arrival</span>
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
hr {
  width: 12rem;
  height: 2px;
  color: gray;
}
.live-queue-container {
  margin: 0 auto;
}
.live-queue-wrapper {
  padding: 3rem 10rem;
}
.queue-content {
  display: flex;
  flex-direction: row;
  width: 100%;
  justify-content: space-between;
}
.welcome-box {
  width: 50%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border-right: 1px solid black;
}
.caption {
  text-align: center;
  width: 50%;
  padding-bottom: 1rem;
}
.adress-box {
  width: 20rem;
  height: auto;
  background-color: #D8FAE9;
  border-radius: 0.5rem;
  padding: 1rem 1rem;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}
.queue-data {
  border-left: 1px gray;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 1rem;
}
.waiting-details {
  width: 13rem;
  height: auto;
  background-color: #f1e4db;
  border-radius: 0.5rem;
  padding: 1rem 1rem;
}
.dr-name {
  text-align: center;
}
.queue-ewt-text {
  text-align: center;
  padding-bottom: 0.5rem;
}
.ewt-time {
  font-weight: bold;
  display: flex;
  justify-content: center;
  padding-bottom: 0.7rem;
}

.total-people {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}
.people-text {
  padding-left: 1rem;
  color: orangered;
}

.join-mark-buttons {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 13rem;
}
.buttonss {
  display: flex;
  flex-direction: column;
  gap: 1rem;

}
.join-live-button {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  width: 14rem;
  height: 3rem;
  border-radius: 2rem;
  background-color: #125836;
  color: white;
  font-weight: bold;
}
.mark-arrival-button {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  width: 14rem;
  height: 3rem;
  border-radius: 2rem;
  background-color: #fcfdfd;
  color: white;
  font-weight: bold;
  border: 2px solid rgb(136, 133, 133);
}
.arrival-text{
color: #03713c;
}
</style>
