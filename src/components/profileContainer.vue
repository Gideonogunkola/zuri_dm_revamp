<template>
  <div>
    <div class="userContainer rounded shadow m-2 bg-white">
        <div
          class="
            header
            text-white
            primaryColor
            d-flex
            justify-content-between
            align-items-center
            py-2
            px-3
          "
        >
          <h5>Profile</h5>
          <div><i class="fa fa-times" aria-hidden="true"></i></div>
        </div>
        <div class="side-profile px-3">
          <div class="text-center">
            <b-img class="rounded-circle u_icon" :src="userData.profileImage"></b-img>
      
            <div style="font-size:23px"><b>{{userData.displayName}}</b></div>
            
            <div style="font-size:14px">
                {{userData.profession}}<br>
                {{userData.gender}}
          </div>
          
          <!-- <i class="my-4 fa fas fa-cat"></i> -->
              <img src="@/assets/Emoji.png" class="my-4" style="height:18px; width:18px;"  >   
          </div>
          <div class="profile_icons d-flex justify-content-around mb-4 m-0">
            <div class="text-center">
              <button class="btn btn-light btn-rounded shadow-sm mb-2">
                <i class="far fa-comment"></i>
              </button>
              <div class="text-muted">Message</div>
            </div>

            <div>
              <button class="btn btn-light btn-rounded shadow-sm mb-2">
                <i class="far fa-bell-slash" aria-hidden="true"></i>
              </button>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
              <div class="text-muted">Muted</div>
            </div>
            <div class="text-center">
              <button class="btn btn-light btn-rounded shadow-sm mb-2">
                <i class="fa fa-ellipsis-h"></i>
              </button>
              <div class="text-muted">More</div>
            </div>
          </div>

          <div class="text-left p-3 margin:26.18px 0 27px 0;  font-size:13px">
            <div class="mb-2">
              <div class="text-muted">Display Name</div>
              <div>{{ userData.displayName }}</div>
            </div>

            <div class="mb-2">
              <div class="text-muted">Local Time</div>
              <div>{{ userData.localTime }}</div>
            </div>

            <div class="mb-2">
              <div class="text-muted">Phone Number</div>
              <div>{{ userData.phoneNumber }}</div>
            </div>
          </div>
        </div>
      </div>
    </div>
</template>

<script>
export default {
  data() {
    return {
      userData: {
        displayName: "Mama Gee",
        profession: "Frontend Desing Mentor",
        gender: "he/her",
        localTime: "3:15PM",
        phoneNumber: "021345789",
        profileImage: require("@/assets/images/mamaGee.jpg"),
      },
    };
  },
};
</script>

<style scoped>
.primaryColor {
  background-color: #00b87c;
}
.userContainer {
  position: relative;
  width: 18rem;
  height: auto;
  font-family: "Lato", sans-serif;
  grid-column-start: 2;
  grid-column-end: 5;
}
.side-profile {
  
}

.userContainer img {
  width: 100%;
  height: 250px;
}
.btn-rounded {
  border-radius: 100%;
}

.profile_icons button {
  height: 65%;
}

.u_icon{
      width:280px;
      height: 380px;
      margin: 16px 0px 3px -3px;
      object-fit: cover;
    }
</style>