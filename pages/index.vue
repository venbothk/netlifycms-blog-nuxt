<template>
  <main>
    <section class="page-banner-area rel z-1 pt-220 pb-145 rpb-125 bg-dark-blue text-white">
      <div class="container">
        <div class="row align-items-center">
          <div class="col-md-6">
            <h2 class="page-title wow fadeInRight delay-0-2s">Blog</h2>
          </div>
          <div class="col-md-6">
            <ul class="breadcrumb-nav wow fadeInLeft delay-0-2s">
              <!-- <li><a href="index.html">Home</a></li>
              <li>Blog Details</li> -->
            </ul>
          </div>
        </div>
      </div>
    </section>

    <!-- <section class="mt-8">
      <h3 class="text-primary-600 dark:text-primary-400 max-w-5xl mx-auto">Latest blog post</h3>
    </section> -->

    <section class="blog-single-area py-130 rpt-100 rpb-90">
      <div class="container">
        <div class="row">
          <div class="col-lg-12">
            <div class="widget latest-post-widget wow fadeInUp delay-0-2s">
              <h4 class="widget-title">Latest Blog Post</h4>
              <div class="popular-posts-wrapper">
                <posts post-type="blog" :amount="3" />
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </main>
</template>
