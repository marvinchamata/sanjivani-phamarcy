<template>
  <div id="about-page" class="page-wrapper about-page content-page">
    <site-hero
      title="About Us"
      subtitle="About Sanjivani Pharmaceuticals"
      image="/uploads/about-hero.jpg"
    ></site-hero>
    <main-section theme="sidebar-right">
      <template v-slot:default>
        <div class="content">
          <h3> About Us</h3>
          <p>
            <strong>
              Edit this page in<code>/pages/about.vue</code>to fit your needs.
            </strong>
          </p>
          <p>
            With offices in SADC regions, Sanjivani Pharmaceutical works with many of the world’s leading
companies through various agreements, partnerships and joint ventures, the group is a leading
healthcare, medical equipment and consumer care company in Zambia , Botswana, Mauritius
India and is committed to meeting the growing needs of healthcare and pharmaceutical
distribution in the regions
Sanjivani Pharmaceutical has a unique distribution and marketing network of more than 50 sales
and medical representatives(comprising mostly of doctors), as well as wholesale organization and
chain of local pharmacies, the company is managed by a highly experienced team consiting of
SADC regions and expatriates with diverse backgrounds and skill sets
          </p>

          <h3>Another Fake Heading</h3>
          <p>Sanjivani Pharmaceuticals is a pharmaceutical wholesaler and distributor committed to delivering
a high standard of service to national and international partners in the healthcare sector.

     </p> 
     
     <p> Our long term experience in trading pharmaceutical
products worldwide makes us a reliable partner in
sourcing pharmaceutical products with the highest level
of quality and safety.
     </p>
          <quote-card />
          <h3>Still More Fake Content</h3>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Adipisci
            eligendi impedit inventore ipsa laboriosam libero magnam modi odio,
            sunt temporibus. Distinctio doloremque eum magni nostrum quasi
            ratione rem repudiandae sit! Lorem ipsum dolor sit amet, consectetur
            adipisicing elit.
            <strong>Alias aut facere harum ipsam</strong> quibusdam quidem
            quisquam saepe? Alias architecto blanditiis consequatur consequuntur
            dicta ipsa iste modi provident, quod, similique veritatis.
          </p>
        </div>

        <div class="tile is-ancestor">
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">
                Cool Stuff We Do
              </p>
              <p class="subtitle">
                Sooo Cool
              </p>
              <figure class="image is-1by1">
                <opti-image width="500" height="500" />
              </figure>
            </article>
          </div>
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">
                Other Cool Things
              </p>
              <p class="subtitle">
                Just as cool
              </p>
              <figure class="image is-1by1">
                <opti-image width="500" height="500" />
              </figure>
            </article>
          </div>
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">
                All the cool
              </p>
              <p class="subtitle">
                that is all
              </p>
              <figure class="image is-1by1">
                <opti-image width="500" height="500" />
              </figure>
            </article>
          </div>
        </div>
      </template>

      <template v-slot:sidebar>
        <h3 class="subtitle is-4">
          Latest Posts
        </h3>
        <posts-grid :per-row="1" :number="2" />
      </template>
    </main-section>
  </div>
</template>
<script>
import QuoteCard from '~/components/cards/QuoteCard'
export default {
  head() {
    return {
      title: `About | ${this.$siteConfig.siteName}`
    }
  },
  components: { QuoteCard }
}
</script>
