<template>
  <section class="o-section  t-section  ">
    <div class="o-section__header-bg  t-section__header" />
    <div class="o-section__content-bg  t-section__content" />

    <div class="o-container">
      <div class="o-section__container">
        <header class="o-section__header  t-section__header">
          <div class="o-content">
            <h2 class="o-section__heading">
              {{ $t("Projects") }}
            </h2>
            <div class="o-content__body  o-section__description">
              {{ $t("opensource_quote") }}
            </div>
          </div>
        </header>
        <!-- /o-section__header -->

        <div class="o-section__content  t-section__content  ">
          <div class="o-grid">
            <div
              v-for="(expertise, index) in exps"
              :key="index"
              class="o-grid__col-sm-6"
            >
              <div class="o-media  o-media--block  o-content">
                <div class="o-media__figure">
                  <div class="c-number  t-primary-color">
                    {{ expertise.num }}
                  </div>
                </div>
                <div class="o-media__body  o-content__body">
                  <h3>{{ expertise.title }}</h3>
                  <p>
                    {{ expertise.desc }}
                  </p>
                  <p>
                    <a :href="expertise.link" target="_blank">
                      > {{ expertise.linkText }}
                    </a>
                  </p>
                </div>
              </div>
              <!-- /o-media o-content -->
            </div>
            <!-- /o-grid__col -->
          </div>
          <!-- /o-grid -->
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
  name: "SectionProjects",
  data() {
    return {
      exps: [
        {
          num: "01",
          title: "Companion",
          desc: `Honorable Mention at nwHacks2021, a social media messaing web app built with Node, Firebase, Fetch and Socket.io using Google OAUTH to create accounts.`,
          link: "https://devpost.com/software/companion-m2lg9t",
          linkText: "DevPost Link",
        },
        {
          num: "02",
          title: "Dotfiles",
          desc:
            "Personal config files for my installation of Manjaro Linux, running on i3wm with custom CSS themes for Spotify, Discord, Firefox and VSCode that dynamically change based on system-wide wallpaper changes.",
          link: "https://github.com/Vinhocent/dotfiles",
          linkText: "GitHub Repository",
        },
        {
          num: "03",
          title: "CoronaJSON",
          desc:
            "Provides coronavirus statistic in a .json format through webscraping with BeautifulSoup for opensource use",
          link: "https://github.com/Vinhocent/CoronaJSON",
          linkText: "GitHub Repository",
        },
        {
          num: "04",
          title: "This Website",
          desc:
            "Website built with Nuxt.js (based on Vue.js, Node.js, Webpack and Babel.js) and hosted on Netlify.",
          link: "https://github.com/Vinhocent/vinhocent.github.io/",
          linkText: "GitHub Repository",
        },
      ],
    };
  },
};
</script>
