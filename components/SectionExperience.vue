<template>
  <section class="o-section t-section">
    <div class="o-section__header-bg t-section__header" />
    <div class="o-section__content-bg t-section__content" />

    <div class="o-container">
      <div class="o-section__container">
        <header class="o-section__header t-section__header">
          <div class="o-content">
            <h2 class="o-section__heading">{{ $t("Experience") }}</h2>
            <div class="o-content__body o-section__description">
              {{ $t("") }}
            </div>
          </div>
        </header>
        <!-- /o-section__header -->

        <div class="o-section__content t-section__content u-pb-0">
          <div class="a-experience-timeline c-timeline t-border-color">
            <div
              v-for="(ex, index) in experiences"
              :key="index"
              class="c-timeline__item"
            >
              <div class="c-timeline__point t-timeline__point t-primary-bg" />
              <div class="o-content">
                <div class="o-grid">
                  <div class="o-grid__col-md-5">
                    <div class="c-work__timeframe">
                      {{ ex.from }} &ndash; {{ ex.to }}
                    </div>
                    <h3 class="c-work__heading">{{ ex.company }}</h3>
                    <h4 class="c-work__title">{{ ex.role }}</h4>
                    <div class="c-work__location">{{ ex.location }}</div>
                  </div>
                  <div class="o-grid__col-md-7">
                    <p>{{ ex.description }}</p>
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
      experiences: [
        {
          company: "1Password",
          role: "Incoming Software Developer",

          location: this.$t("Remote from Toronto, Canada"),
        },
        {
          from: "04.2019",
          to: "12.2019",
          company: "University of Toronto Department of Civil Engineering",
          role: "Summer Research Assistant",
          description: this.$t(
            "Assisted Prof. Eric Miller in modelling traffic flow within Toronto Traffic Systems to improve the practice of travel demand forecasting. Developing cellular automata models in Python for CEM1004H, Cities as Complex Systems"
          ),
          location: this.$t("Toronto, Canada"),
        },
        {
          from: "02.2019",
          to: "05.2019",
          company: "University of Toronto Department of Mathematics",
          role: "Research Assistant",
          description: this.$t(
            "Researched Galois Fields with a graduate student at the University of Toronto Department of Mathematics. Peformed computational algebra between the additive and multiplicative groups of Galois fields, using MATLAB and SAGEMATH."
          ),
          location: this.$t("Toronto, Canada"),
        },
        {
          from: "07.2018",
          to: this.$t("Present"),
          company: "Conchordium",
          role: "Director of Communications",
          description: this.$t(
            "Conchordium is a youth not-for-profit organization that aims to provide a space for young musicians of all types to connect and interact with each other. "
          ),
          location: this.$t("Toronto, Canada"),
        },
        {
          from: "07.2018",
          to: "Present",
          company: "SHAD",
          role: "SHAD Fellow",
          description: this.$t(
            "Earned the SHAD Fellow designation after being nominated to attend the award-winning enrichment and entrepreneurship program."
          ),
          location: this.$t("Sackville, Canada"),
        },
      ],
    };
  },
};
</script>
