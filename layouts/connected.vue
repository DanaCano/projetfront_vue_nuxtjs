<template>
  <div id="main-content">
    <!--<sidebar /> -->
    <div id="dashboard-content" class="dashboard-content">
      <div  id="dashboard-header-content"  class="header">
        <div id="dashboard-group-head-content" class="head">
          <!-- title -->
          <span class="title">dashboard</span>

          <!-- group-icons -->
          <div id="dashboard-group-head-icon" class="group-icon">  
          <!-- icon-comment -->  
            <i class="icon icon-comment-discussion" ></i>
          <!-- group-icons-notifications -->
            <div id="group-icon-notification" class="group-icon-notification">
              <!-- icon-notification -->  
              <i class="icon icon-notification"></i>
              <i class="icon icon-bull-empty bull"></i>
            </div>

          <!-- group-search -->
            <div id="dashboard-group-input">
                <i class="icon-search"></i>
                <input id="dashboard-search-input" type="text" placeholder="SEARCH ...">
            </div>

          <!-- group-profile -->
          <div id="dashboard-group-profile" class="dasboard-group-profile">
            <img src="~/assets/images/profile.png" class="profile">
            <button class="">
              <span>CAMILLE</span>
              <i class="icon-chevron-down"></i>
              </button>
          </div>


        </div>

      </div>
    </div>

  </div>
  </div>
</template>