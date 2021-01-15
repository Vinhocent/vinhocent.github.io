<template>
  <section class="o-section  t-section  ">
    <div class="o-section__header-bg  t-section__header" />
    <div class="o-section__content-bg  t-section__content" />

    <div class="o-container">
      <div class="o-section__container">
        <header class="o-section__header  t-section__header">
          <div class="o-content">
            <h2 class="o-section__heading">
              {{ $t("Education") }}
            </h2>
            <div class="o-content__body  o-section__description">
              {{ $t("Yes, I have been around.") }}
            </div>
          </div>
        </header>
        <!-- /o-section__header -->

        <div class="o-section__content  t-section__content  u-pb-0">
          <div class="a-experience-timeline  c-timeline  t-border-color">
            <div
              v-for="(edu, index) in educations"
              :key="index"
              class="c-timeline__item"
            >
              <div class="c-timeline__point  t-timeline__point  t-primary-bg" />
              <div class="o-content">
                <div class="o-grid">
                  <div class="o-grid__col-md-5">
                    <div class="c-work__timeframe">
                      {{ edu.from }} &ndash; {{ edu.to }}
                    </div>
                    <h3 class="c-work__heading">
                      {{ edu.company }}
                    </h3>
                    <h4 class="c-work__title">
                      {{ edu.role }}
                    </h4>
                    <h4 class="c-work__title">
                      {{ edu.marks }}
                    </h4>
                    <div class="c-work__location">
                      {{ edu.location }}
                    </div>
                  </div>
                  <div class="o-grid__col-md-7">
                    <p>
                      {{ edu.description }}
                    </p>
                  </div>
                </div>
                <!-- /o-grid -->
              </div>
              <!-- /o-content -->
            </div>
            <!-- /c-timeline__item -->
          </div>
          <!-- /c-timeline -->
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
      educations: [
        {
          from: "09.2020",
          to: "Ongoing",
          company: this.$t("University of Waterloo"),
          role: this.$t(
            "Candidate for Bachelor of Computer Science | Faculty Average: 97% "
          ),
          marks: this.$t("(CS135:  97%, MATH135:  99%, MATH137:  95%)"),

          location: this.$t("Waterloo, Canada"),
        },
        {
          from: "00.2016",
          to: "06.2020",
          company: this.$t("Martingrove Collegiate Institute"),
          role: this.$t("Ontario Secondary School Diploma"),

          location: this.$t("Toronto, Ontario"),
        },
      ],
    };
  },
};
</script>
