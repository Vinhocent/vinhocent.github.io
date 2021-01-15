<template>
  <section class="o-section  t-section  ">
    <div class="o-section__header-bg  t-section__header" />
    <div class="o-section__content-bg  t-section__content" />

    <div class="o-container">
      <div class="o-section__container">
        <header class="o-section__header  t-section__header">
          <div class="o-content">
            <h2 class="o-section__heading">
              {{ $t("About Me") }}
            </h2>
          </div>
        </header>
        <!-- /o-section__header -->

        <div class="o-section__content  t-section__content  ">
          <div class="o-content">
            <div class="c-intro">
              <!-- EN -->
              <div v-if="$i18n.locale === 'en'" class="o-content__body">
                <p>
                  I am currently a first year at the
                  <a
                    class="highlight"
                    href="https://uwaterloo.ca/future-students/programs/computer-science"
                    >University of Waterloo</a
                  >
                  where I am currently pursuing a degree in
                  <strong>Computer Science</strong>
                  with co-op.
                </p>
                <p>
                  I'm an avid member of the
                  <a
                    class="highlight blue"
                    href="https://www.reddit.com/r/unixporn/"
                    target="_blank"
                    >ricing community</a
                  >. I am currently dual-booting Windows 10 and Manjaro Linux.
                  You can also find my graphic design portfolio
                  <a class="highlight green" href="./portfolio" target="_blank"
                    >here</a
                  >
                </p>
                <p>
                  Offline, I take amateur pictures of nature and cityscapes,
                  listen to music, or hang out with my friends.
                </p>
              </div>
            </div>
          </div>
        </div>
        <!-- /o-section__content -->
      </div>
      <!-- /o-section__container -->
    </div>
    <!-- /o-container -->
  </section>
  <!-- /o-section -->
</template>

<script>
export default {
  data() {
    return {
      hover: false,
    };
  },
};
</script>
