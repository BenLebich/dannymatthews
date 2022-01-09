<script>
  export let goTo;
</script>

<div class="content">
  <div class="timeline">
    <div class="profile">
      <img
        class="video"
        src="http://placehold.jp/ffffff/621d1d/150x150.png"
        alt="video"
      />
    </div>
    <div class="desktop">
      <div class="row">
        <div>2018</div>
        <div>2019-2020</div>
        <div>2021-PRESENT</div>
      </div>
      <div class="row">
        <div>EDITED PROMOS</div>
        <div>CONTINUED EDITING FOR COMPANYS</div>
        <div>STARTED WORKING WITH ARTISTS</div>
        <div>EDITING FOR YOUTUBERS</div>
      </div>
      <div class="row">
        <div>BECAME A VIDEO EDITOR</div>
        <svg
          width="130"
          height="6"
          viewBox="0 0 100 6"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <line y1="3" x2="130" y2="3" stroke="white" stroke-width="3" />
        </svg>
        <div>STARTED AS A WEDDING VIDEOGRAPHER</div>
        <svg
          width="120"
          height="6"
          viewBox="0 0 120 6"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <line y1="3" x2="120" y2="3" stroke="white" stroke-width="3" />
        </svg>
        <div>CREATED COMPANY</div>
        <svg
          width="90"
          height="6"
          viewBox="0 0 90 6"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <line y1="3" x2="90" y2="3" stroke="white" stroke-width="3" />
        </svg>
        <div>TRAVELED THE USA FOR PROJECTS</div>
        <svg
          width="60"
          height="6"
          viewBox="0 0 60 6"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <line y1="3" x2="60" y2="3" stroke="white" stroke-width="3" />
        </svg>
        <div>STILL CREATING</div>
      </div>
      <div class="row">
        <div>BECAME A MOTION DESIGNER</div>
        <div>VISITED PAPUA NEW GUINEA FOR VIDEO PROJECT</div>
        <div>FOUND SMALL BRANDS TO WORK WITH</div>
        <div>CREATED OVER 100 VIDEOS</div>
      </div>
      <div class="row">
        <div>2017-2018</div>
        <div>2018-2019</div>
        <div>2020-2021</div>
      </div>
    </div>
    <div class="mobile">
      <div class="row">
        <div>EDITED PROMOS</div>
        <div>CONTINUED EDITING FOR COMPANYS</div>
        <div>STARTED WORKING WITH ARTISTS</div>
        <div>EDITING FOR YOUTUBERS</div>
      </div>
      <div class="row">
        <div>BECAME A VIDEO EDITOR</div>

        <div>STARTED AS A WEDDING VIDEOGRAPHER</div>

        <div>CREATED COMPANY</div>

        <div>TRAVELED THE USA FOR PROJECTS</div>

        <div>STILL CREATING</div>
      </div>
      <div class="row">
        <div>BECAME A MOTION DESIGNER</div>
        <div>VISITED PAPUA NEW GUINEA FOR VIDEO PROJECT</div>
        <div>FOUND SMALL BRANDS TO WORK WITH</div>
        <div>CREATED OVER 100 VIDEOS</div>
      </div>
      <div class="row">
        <div>2017-2018</div>
        <div>2018</div>
        <div>2018-2019</div>
        <div>2019-2020</div>
        <div>2020-2021</div>
        <div>2021-PRESENT</div>
      </div>
    </div>
  </div>

  <div class="footer">
    <div class="info">
      GOD CREATED ME TO BE A DESIGNER. THE CONTENT I CREATE IS TO HELP YOU WITH
      MARKETING AND TO GROW YOUR BRAND. I CREATE VISUALS BECAUSE I WAS CREATED
      TO. I'VE SEEN MANY VIDEOS AND FILMS, I'VE CREATED MANY VIDEOS AND FILMS,
      AND I KNOW WHAT WORKS FOR MARKETING AND WHAT DOESN'T. LET ME HELP YOU
      CREATE THE PERFECT VISUAL FOR YOUR BRAND.
    </div>
    <div
      class="contact swiper-button-disabled"
      on:click={() => {
        goTo(4);
      }}
    >
      CONTACT US
    </div>
  </div>
</div>

<style>
  .timeline {
    display: flex;
    flex-direction: row;
    margin: auto;
    align-items: center;
  }

  .mobile {
    display: none;
  }

  .timeline .desktop .row {
    display: flex;
    flex-direction: row;
    align-items: center;
  }

  .timeline .desktop .row:nth-of-type(2) {
    padding-left: 120px;
    padding-right: 50px;
    justify-content: space-between;
  }

  .timeline .desktop .row:nth-of-type(4) {
    justify-content: space-between;
    padding-left: 150px;
  }

  .timeline .desktop .row:nth-of-type(3) {
    color: white;
    padding-top: 20px;
    padding-bottom: 20px;
  }

  .timeline .desktop .row:nth-of-type(1) {
    justify-content: space-between;
    color: white;
    padding-left: 300px;
    padding-right: 50px;
    padding-bottom: 60px;
  }

  .timeline .desktop .row:nth-of-type(5) {
    justify-content: space-between;
    color: white;
    padding-left: 50px;
    padding-right: 240px;
    padding-top: 60px;
  }

  .timeline .desktop .row svg {
    padding: 10px;
  }
  .profile {
    padding-right: 30px;
  }

  .content {
    display: flex;
    height: 100%;
    flex-direction: column;
    padding-right: 50px;
    justify-content: space-between;
    align-items: center;
  }

  .footer {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    color: white;
    padding-top: 20px;
    margin-top: -20px;
    font-size: 20px;
    padding-bottom: 20px;
  }

  .info {
    padding-bottom: 50px;
    color: black;
    text-align: center;
    font-size: 16px;
    max-width: 1000px;
  }

  @media only screen and (max-width: 1750px) {
    .timeline {
      margin: unset;
    }

    .desktop {
      display: none;
    }
    .mobile {
      display: flex;
      margin-left: 160px;
      height: 70%;
    }

    .timeline {
      flex-direction: column;
    }

    .profile {
      padding-right: 0px;
    }

    .mobile .row {
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      align-items: center;
    }

    .timeline .mobile .row:nth-of-type(1) {
      padding-top: 50px;
      padding-bottom: 100px;
      margin-right: -200px;
    }

    .timeline .mobile .row:nth-of-type(2) {
      padding-top: 10px;
      color: white;

    }

    .timeline .mobile .row:nth-of-type(3) {
      margin-left: -200px;
      padding-top: 80px;
      padding-bottom: 50px;
    }

    .timeline .mobile .row:nth-of-type(4) {
      color: white;
      font-size: 12px;

    }
  }

  @media only screen and (max-width: 800px) {
    .content {
      padding-right: 30px;
    }


    .mobile {
      display: flex;
      margin-left: 0px;
      font-size: 10px;
    }

    .timeline .mobile .row:nth-of-type(1) {
      padding-top: 50px;
      padding-bottom: 100px;
      margin-right: -100px;
    }



    .timeline .mobile .row:nth-of-type(3) {
      margin-left: -100px;
      padding-top: 80px;
      padding-bottom: 50px;
    }

    .timeline .mobile .row:nth-of-type(4) {
      font-size: 10px;
    }

    .timeline {
      height: 80%;
    }

    .footer .info {
      font-size: 12px;
      padding-bottom: 10px;
    }
  }
</style>
