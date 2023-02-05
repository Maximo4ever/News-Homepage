<template>
  <main class="main">
    <picture>
      <source
        srcset="../assets/image-web-3-mobile.jpg"
        media="(max-width: 500px)"
      />
      <img src="../assets/image-web-3-desktop.jpg" alt="nose" />
    </picture>
    <h1 class="main__title">The Bright Future of Web 3.0?</h1>
    <article class="main__content">
      <p class="main__content__text">
        We dive into the next evolution of the web that claims to put the power
        Of the platforms back into the hands Of the people. But is it really
        fulfilling its promise?
      </p>
      <button class="main__content__btn">READ MORE</button>
    </article>
    <aside class="news">
      <h3 class="news__title">New</h3>
      <div class="news__new">
        <h4>Hydrogen VS Electric Cars</h4>
        <p>Will hydrogen-fueled cars ever catch up to EVs?</p>
      </div>
      <div class="news__new">
        <h4>The Downsides of AI Artistry</h4>
        <p>
          What are the possible adverse effects of on-demand Al image
          generation?
        </p>
      </div>
      <div class="news__new">
        <h4>Is VC Funding Drying Up?</h4>
        <p>
          Private funding by VC firms is down 50% YOY. We take a look at what
          that means.
        </p>
      </div>
    </aside>
    <section class="section">
      <img src="../assets/image-retro-pcs.jpg" alt="Retro pcs" />
      <div class="info">
        <span class="info__num">01</span>
        <h4 class="info__title">Reviving Retro PCs</h4>
        <p class="info__text">
          What happens when old PCs are given modern upgrades?
        </p>
      </div>
    </section>
    <section class="section">
      <img src="../assets/image-top-laptops.jpg" alt="Retro pcs" />
      <div class="info">
        <span class="info__num">02</span>
        <h4 class="info__title">Top 10 Laptops of 2022</h4>
        <p class="info__text">Our best picks for various needs and budgets.</p>
      </div>
    </section>
    <section class="section">
      <img src="../assets/image-gaming-growth.jpg" alt="Retro pcs" />
      <div class="info">
        <span class="info__num">03</span>
        <h4 class="info__title">The Growth of Gaming</h4>
        <p class="info__text">
          How the pandemic has sparked fresh opportunities.
        </p>
      </div>
    </section>
  </main>
</template>
<style>
.main {
  display: flex;
  flex-direction: column;
  max-width: 540px;
  margin: 15px;
}
.main source,
.main img {
  width: 100%;
  object-fit: cover;
}

/*  */
.main__title {
  margin-top: 15px;
  font-size: 44px;
  line-height: 1.1;
}
.main__content__text {
  margin-top: 10px;
  line-height: 1.6;
}
.main__content__btn {
  margin-top: 25px;
  font-size: 16px;
  letter-spacing: 4px;
  font-weight: 600;
  padding: 16px 30px;
  background-color: var(--Soft-red);
  border: none;
  transition: 0.3s background-color;
  cursor: pointer;
}
.main__content__btn:hover {
  background-color: var(--Very-dark-blue);
}

/*  */
.news {
  background-color: var(--Very-dark-blue);
  color: var(--Grayish-blue);
  padding: 25px 20px;
  margin-block: 60px 40px;
}
.news__title {
  font-size: 36px;
  font-weight: 600;
  color: var(--Soft-orange);
}
.news__new {
  cursor: pointer;
}
.news__new:not(.news__new:last-of-type) {
  margin-block: 40px;
  padding-bottom: 36px;
  border-bottom: 1px solid var(--Grayish-blue);
}
.news__new:last-of-type {
  margin-bottom: 15px;
}
.news__new h4 {
  font-size: 22px;
}
.news__new:hover h4 {
  color: var(--Soft-orange);
}
.news__new p {
  margin-top: 12px;
}

/*  */
.section {
  max-width: 450px;
  display: flex;
  align-items: center;
  justify-content: center;
  column-gap: 15px;
  margin-top: 20px;
  cursor: pointer;
}
.section:first-of-type {
  margin-top: 0;
}
.section img {
  height: 155px;
  width: 135px;
  padding-right: 5px;
}
.info__num {
  font-size: 32px;
  font-weight: 800;
  color: var(--Grayish-blue);
}
.info__title {
  margin-top: 10px;
  font-size: 20px;
  font-weight: 800;
}
.section:hover .info__title {
  color: var(--Soft-red);
}
.info__text {
  margin-top: 14px;
  font-size: 16px;
  line-height: 1.7;
}
@media (min-width: 580px) {
  .main {
    margin-inline: auto;
  }
}
@media (min-width: 1100px) {
  .nav {
    max-width: 1350px;
    padding: 20px 40px 10px;
    margin: 40px auto;
  }
  .main {
    max-width: 1350px;
    padding: 0 40px;
    margin-block: 0;
  }
  .main {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-areas:
      "picture picture aside"
      "article article aside"
      "section section section";
    gap: 35px;
  }
  .main picture {
    grid-area: picture;
  }
  .main__content {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: flex-start;
  }
  .main__title {
    font-size: 54px;
    margin-top: 0;
  }
  .main__content__text {
    font-size: 18px;
    margin-top: 0;
  }
  .news {
    grid-area: aside;
    margin-block: 0;
  }
}
</style>
