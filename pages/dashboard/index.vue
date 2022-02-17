<template>
  <div id="main-content">
    <sidebar />
    <div id="dashboard-content" class="dashboard-content">
      <div id="dashboard-header-content" class="header">
        <div id="dashboard-group-head-content" class="head">
          <!-- title -->
          <span class="title">dashboard</span>

          <!-- group-icons -->
          <div id="dashboard-group-head-icon" class="group-icon">
            <!-- icon-comment -->
            <i class="icon icon-comment-discussion"></i>
            <!-- group-icons-notifications -->
            <div id="group-icon-notification" class="group-icon-notification">
              <!-- icon-notification -->
              <i class="icon icon-notification"></i>
              <i class="icon icon-bull-empty bull"></i>
            </div>

            <!-- group-search -->
            <div id="dashboard-group-input">
              <i class="icon-search"></i>
              <input id="dashboard-search-input" type="text" placeholder="SEARCH ..." />
            </div>

            <!-- group-profile -->
            <div id="dashboard-group-profile" class="dasboard-group-profile">
              <img src="~/assets/images/profile.png" class="profile" />
              <button id="btn-profile" class="btn-profile">
                <span>CAMILLE</span>
                <i class="icon-chevron-down"></i>
              </button>
            </div>
          </div>
        </div>
      </div>

      <div id="dashboard-main-content">
        <div id="dashboard-sub-main-content">
          <!-- menu: update athlete stat + create new client + document library -->
          <div id="sub-menu-btn">
            <button v-for="item in sub_menus_btn" class="btn-update">
              <i class="icon" :class="item.icon"></i>
              {{ item.label }}
            </button>
          </div>

          <!-- calendar: upcoming date + pending work -->
          <div id="calendar" class="card">
            <h3 class="card-title">UPCOMING DATES</h3>
            <div class="event">
              <div class="date">
                <span class="day">20</span>
                <br />
                <span class="month">MAY</span>
              </div>
              <div>
                <div class="text">
                  <span class="hour">09:00</span>
                  <div class="content-title">
                    <span class="title">MEETING WITH JAMES J. JUVENTUS</span>
                    <span class="sub-title">lorem ipsum dolor sit amet</span>
                  </div>
                </div>
                <div class="text">
                  <span class="hour">10:00</span>
                  <div class="content-title">
                    <span class="title">MEETING WITH JAMES J. JUVENTUS</span>
                    <span class="sub-title">lorem ipsum dolor sit amet</span>
                  </div>
                </div>
              </div>
            </div>

            <div class="event">
              <div class="date">
                <span class="day">25</span>
                <br />
                <span class="month">MAY</span>
              </div>
              <div>
                <div class="text">
                  <span class="hour">18:00</span>
                  <div class="container-title">
                    <div class="content-title">
                      <span class="title">MEETING WITH JAMES J. JUVENTUS</span>
                      <span class="sub-title">lorem ipsum dolor sit amet</span>
                    </div>
                  </div>
                </div>
              </div>
            </div>

            <div class="event">
              <div class="date">
                <span class="day">06</span>
                <br />
                <span class="month">JUNE</span>
              </div>
              <div>
                <div class="text">
                  <span class="hour">14:00</span>
                  <div class="container-title">
                    <div class="content-title">
                      <span class="title">MEETING WITH JAMES J. JUVENTUS</span>
                      <span class="sub-title">lorem ipsum dolor sit amet</span>
                    </div>
                  </div>
                </div>
              </div>
            </div>
            <a class="view-all" href="#view_all">VIEW ALL ...</a>
          </div>

          <div id="pending" class="card">
            <h3 class="card-title">PENDING WORK</h3>
            <div class="event">
              <div>
                <div class="text text-pending">
                  <i class="icon icon-document"></i>
                  <div class="content-title">
                    <span class="title">ENDORSEMENT CONTRACT</span>
                    <span class="sub-title">lorem ipsum dolor sit amet</span>
                  </div>
                </div>
              </div>
            </div>

            <div class="event">
              <div>
                <div class="text text-pending">
                  <i class="icon icon-document"></i>
                  <div class="content-title">
                    <span class="title">ENDORSEMENT CONTRACT</span>
                    <span class="sub-title">lorem ipsum dolor sit amet</span>
                  </div>
                </div>
              </div>
            </div>

            <div class="event">
              <div>
                <div class="text text-pending">
                  <i class="icon icon-document"></i>
                  <div class="content-title">
                    <span class="title">ENDORSEMENT CONTRACT</span>
                    <span class="sub-title">lorem ipsum dolor sit amet</span>
                  </div>
                </div>
              </div>
            </div>

            <a class="view-all" href="#view_all">VIEW ALL ...</a>
          </div>
        </div>

        <div id="sidebar-event">
          <div id="birth">
            <i class="icon-birthday-cake"></i>
            <div class="text">
              <div class="title">5 Birthdays this week</div>
              <div class="sub-title">Rosa BRUNA and others</div>
            </div>
          </div>

          <div id="recent-activity">
            <div id="recent-activity-head">
              <h3>RECENT ACTIVITIES</h3>
              <span>VIEW ALL</span>
            </div>
            <div id="recent-activity-main">
              <div class="recent-activity-main-item">
                <div class="img">
                  <img src="~/assets/images/profile.png" alt="">
                </div>
                <div class="text">
                  <div class="title">ANNA BANUTA</div>
                  <div class="sub-title">Anna has signed with a new club</div>
                </div>
              </div>
              <div class="recent-activity-main-item">
                <div class="img">
                  <img src="~/assets/images/profile.png" alt="">
                </div>
                <div class="text">
                  <div class="title">ANNA BANUTA</div>
                  <div class="sub-title">Anna has signed with a new club</div>
                </div>
              </div>

              <div class="recent-activity-main-item">
                <div class="img">
                  <img src="~/assets/images/profile.png" alt="">
                </div>
                <div class="text">
                  <div class="title">ANNA BANUTA</div>
                  <div class="sub-title">Anna has signed with a new club</div>
                </div>
              </div>

              <div class="recent-activity-main-item">
                <div class="img">
                  <img src="~/assets/images/profile.png" alt="">
                </div>
                <div class="text">
                  <div class="title">ANNA BANUTA</div>
                  <div class="sub-title">Anna has signed with a new club</div>
                </div>
              </div>

              <div class="recent-activity-main-item">
                <div class="img">
                  <img src="~/assets/images/profile.png" alt="">
                </div>
                <div class="text">
                  <div class="title">ANNA BANUTA</div>
                  <div class="sub-title">Anna has signed with a new club</div>
                </div>
              </div>

              <div class="more-new-notifs">
                <span>+99 NEW NOTIFICATIONS</span>
              </div>
              <div>

              </div>
            </div>

          </div>



          <div id="dashboard-time-n-chat">
            <i class="icon-chat-bubble chat-bubble"></i>
            <div class="login-time">
              <Time>
              </Time>
            </div>
          </div>

        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import Component from 'vue-class-component'


@Component({
  layout: 'connected',
  middleware: ['auth']
})

class Dashboard extends Vue {
  sub_menus_btn: any = []

  mounted () {
    this.sub_menus_btn = [
                {
                    icon: "icon-update",
                    label: "UPDATE ATHLETE STAT"
                },
                {
                    icon: "icon-gridicons_create",
                    label: "CREATE NEW CLIENT"
                },
                {
                    icon: "icon-documents-outline",
                    label: "DOCUMENT LIBRARY"
                },
            ]
  }
  
}

export default Dashboard
</script>
