<template>
  <main>
    <section class="page-banner-area rel z-1 pt-220 pb-145 rpb-125 bg-dark-blue text-white">
      <div class="container">
        <div class="row align-items-center">
          <div class="col-md-6">
            <h2 class="page-title wow fadeInRight delay-0-2s">{{ post.title }}</h2>
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

    <section class="blog-single-area py-130 rpt-100 rpb-90" v-if="post">
      <div class="container">
        <div class="row">
          <div class="col-lg-12">
            <div class="single-blog-post blog-details-content pr-xl-5">
              <div class="post-content">
                <div class="post-categories" v-if="post.category">
                  <a href="#">{{ post.category }}</a>
                </div>
                <ul class="post-meta">
                  <!-- <li>
                                        <a href="#"><i class="far fa-user-circle"></i> David D. Ansley</a>
                                    </li> -->
                  <li>
                    <a href="#"><i class="far fa-calendar-alt"></i> {{ formatDate(post.createdAt) }}</a>
                  </li>
                </ul>
                <h3 class="post-title">{{ post.description }}</h3>
                <nuxt-content :document="post" />

                <div class="content-footer" hidden>
                  <ul class="related-tags">
                    <li class="title">Tags:</li>
                    <li><a href="#">Agency</a></li>
                    <li><a href="#">Cosmetics</a></li>
                    <li><a href="#">Beauty</a></li>
                  </ul>
                  <ul class="post-share">
                    <li class="title">Share:</li>
                    <li>
                      <a href="#"><i class="fab fa-facebook-f"></i></a>
                    </li>
                    <li>
                      <a href="#"><i class="fab fa-twitter"></i></a>
                    </li>
                    <li>
                      <a href="#"><i class="fab fa-instagram"></i></a>
                    </li>
                  </ul>
                  <div class="post-author mb-50 wow fadeInUp delay-0-2s">
                    <div class="author-photo">
                      <img src="assets/images/blog/author.jpg" alt="Image" />
                    </div>
                    <div class="author-content">
                      <h5 class="name">Rasalina Wilimson</h5>
                      <p>
                        Quis autem eum reprehenderit voluptate esse quam molestiae consequatu dolorem voluptas nulla
                        pariano rejects
                      </p>

                      <div class="share-links">
                        <a href=""><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-behance"></i></a>
                        <a href="#"><i class="fab fa-dribbble"></i></a>
                      </div>
                    </div>
                  </div>
                  <hr />
                  <div class="post-nav pt-35 pb-30">
                    <div class="prev-post wow fadeInLeft delay-0-2s">
                      <div class="post-thumb">
                        <a href="blog-details.html"><img src="assets/images/blog/post-nav-prev.jpg" alt="Image" /></a>
                      </div>
                      <div class="content">
                        <h6><a href="blog-details.html">How Deal With Back During Pregn</a></h6>
                        <span>25 May 2021</span>
                      </div>
                    </div>
                    <div class="next-post wow fadeInRight delay-0-2s">
                      <div class="post-thumb">
                        <a href="blog-details.html"><img src="assets/images/blog/post-nav-next.jpg" alt="Image" /></a>
                      </div>
                      <div class="content">
                        <h6><a href="blog-details.html">Online Environme Work Older See</a></h6>
                        <span>25 May 2021</span>
                      </div>
                    </div>
                  </div>
                  <hr />
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
export default {
  async asyncData({ $content, params, error }) {
    let post
    try {
      post = await $content('blog', params.blog).fetch()
    } catch (e) {
      error({ message: 'Blog post not found' })
    }
    return { post }
  },
  methods: {
    formatDate(dateString) {
      const date = new Date(dateString)
      return date.toLocaleDateString(process.env.lang) || ''
    },
  },
}
</script>
