<template>
  <div>
    <header class="main-header">
      <!--Header-Upper-->
      <div class="header-upper">
        <div class="container-fluid clearfix">
          <div class="header-inner d-flex align-items-center justify-content-between">
            <div class="logo-outer d-lg-flex align-items-center">
              <div class="logo">
                <a href="index.html"><img style="width: 100px" src="venbot.png" alt="Logo" title="Logo" /></a>
              </div>
              <select name="select-languages" id="select-languages">
                <option value="English">English</option>
                <option value="Spanish">中文</option>
              </select>
            </div>

            <div class="nav-outer clearfix">
              <!-- Main Menu -->
              <nav class="main-menu navbar-expand-lg">
                <div class="navbar-header">
                  <!-- Toggle Button -->
                  <button type="button" class="navbar-toggle" data-toggle="collapse" data-target=".navbar-collapse">
                    <span class="icon-bar"></span>
                    <span class="icon-bar"></span>
                    <span class="icon-bar"></span>
                  </button>

                  <div class="mobile-logo p-15 m-auto">
                    <a href="index.html">
                      <img src="venbot.png" style="width: 70px" alt="Logo" title="Logo" />
                    </a>
                  </div>
                </div>

                <div class="navbar-collapse collapse clearfix">
                  <ul class="navigation clearfix">
                    <li><a href="https://venbot.tech#about">About</a></li>
                    <li><a href="https://venbot.tech#pricing">pricing</a></li>
                    <li><a href="/">blog</a></li>
                    <li><a href="https://venbot.tech#contact">Contact</a></li>
                  </ul>
                </div>
              </nav>
              <!-- Main Menu End-->
            </div>

            <!-- Menu Button -->
            <div class="menu-btn-sidebar d-flex align-items-center">
              <a href="https://app.venbot.tech" class="theme-btn"
                >Dashboard<i class="fas fa-long-arrow-alt-right"></i
              ></a>

              <!-- menu sidbar -->
              <div class="menu-sidebar">
                <button>
                  <span class="icon-bar"></span>
                  <span class="icon-bar"></span>
                  <span class="icon-bar"></span>
                </button>
              </div>
            </div>
          </div>
        </div>
      </div>
      <!--End Header Upper-->
    </header>

    <!--Form Back Drop-->
    <div class="form-back-drop"></div>

    <!-- Hidden Sidebar -->
    <section class="hidden-bar">
      <div class="inner-box text-center">
        <div class="cross-icon"><span class="fa fa-times"></span></div>
        <div class="title">
          <h4>Get Appointment</h4>
        </div>

        <!--Appointment Form-->
        <div class="appointment-form">
          <form method="post" action="#">
            <div class="form-group">
              <input type="text" name="text" value="" placeholder="Name" required />
            </div>
            <div class="form-group">
              <input type="email" name="email" value="" placeholder="Email Address" required />
            </div>
            <div class="form-group">
              <textarea placeholder="Message" rows="5"></textarea>
            </div>
            <div class="form-group">
              <button type="submit" class="theme-btn">Submit now</button>
            </div>
          </form>
        </div>

        <!--Social Icons-->
        <div class="social-style-one">
          <a href="#"><i class="fab fa-twitter"></i></a>
          <a href="#"><i class="fab fa-facebook-f"></i></a>
          <a href="#"><i class="fab fa-instagram"></i></a>
          <a href="#"><i class="fab fa-pinterest-p"></i></a>
        </div>
      </div>
    </section>
    <!--End Hidden Sidebar -->
  </div>
</template>

<script>
export default {
  name: 'Header',
}
</script>

<style lang="postcss" scoped></style>
