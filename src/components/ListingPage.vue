<template>
  <div class="font">
    <div class="header header-font bg-dark">
      <span class=" upper-case text-white center-margin">Mr. Super Deals</span>
    </div>
    <section class="section1 header header-font">
      <span class="s1 upper-case text-dark center-margin">
        Reasons to Buy
      </span>
    </section>
    <section class="bg-light features center-margin">
      <div class="avatar-container center-margin">
        <div class="avatar bg-grey center-margin"></div>
        <span class="sub-heading features1 text-block-center">1 Year Warranty</span>
        <br/>
        <span class="sub-heading sub-features text-light-dark text-block-center">
          Seller / Manufacture Warranty
        </span>
      </div>
      <div class="avatar-container center-margin">
        <div class="avatar bg-grey center-margin"></div>
        <span class="sub-heading features1 text-block-center">Unlocked / Free SIM</span>
        <br/>
        <span class="sub-heading sub-features text-light-dark text-block-center">
          Work with all networks
        </span>
      </div>
      <div class="avatar-container center-margin">
        <div class="avatar bg-grey center-margin"></div>
        <span class="sub-heading features1 text-block-center">Next Day Delivery</span>
        <br/>
        <span class="sub-heading sub-features text-light-dark text-block-center">
          On your Door Step
        </span>
      </div>
      <div class="avatar-container center-margin">
        <div class="avatar bg-grey center-margin"></div>
        <span class="sub-heading features1 text-block-center">
          Free Delivery
        </span>
        <br/>
        <span class="sub-heading sub-features text-light-dark text-block-center">
          All Over United Kingdom
        </span>
      </div>
    </section>
    <section class="specification center-margin">
      <span class="specification-header header-font text-dark">
        Specification
      </span>
      <section class="bg-light features center-margin specification1">
        <div class="avatar-container center-margin">
          <div class="avatar bg-grey center-margin"></div>
          <span class="sub-heading features1 text-block-center">1 Year Warranty</span>
          <br/>
          <span class="sub-heading sub-features text-light-dark text-block-center">
            Seller / Manufacture Warranty
          </span>
        </div>
        <div class="avatar-container center-margin">
          <div class="avatar bg-grey center-margin"></div>
          <span class="sub-heading features1 text-block-center">Unlocked / Free SIM</span>
          <br/>
          <span class="sub-heading sub-features text-light-dark text-block-center">
            Work with all networks
          </span>
        </div>
        <div class="avatar-container center-margin">
          <div class="avatar bg-grey center-margin"></div>
          <span class="sub-heading features1 text-block-center">Next Day Delivery</span>
          <br/>
          <span class="sub-heading sub-features text-light-dark text-block-center">
            On your Door Step
          </span>
        </div>
        <div class="avatar-container center-margin">
          <div class="avatar bg-grey center-margin"></div>
          <span class="sub-heading features1 text-block-center">
            Free Delivery
          </span>
          <br/>
          <span class="sub-heading sub-features text-light-dark text-block-center">
            All Over United Kingdom
          </span>
        </div>
      </section>
      <section class="sub-section bg-light general-features p-1 my-1">
        <span class="sub-heading sub-specification text-dark">
          General Features
        </span>
      </section>
      <section class="sub-section bg-light general-features p-1 my-1 ml-1">
        <span class="sub-heading sub-specification text-dark">
          Performance
        </span>
      </section>
      <section class="sub-section bg-light general-features p-1 my-1">
        <span class="sub-heading sub-specification text-dark">
          Display
        </span>
      </section>
      <section class="sub-section bg-light general-features p-1 my-1 ml-1">
        <span class="sub-heading sub-specification text-dark">
          Camera
        </span>
      </section>
      <section class="sub-section bg-light general-features p-1 my-1">
        <span class="sub-heading sub-specification text-dark">
          Memory
        </span>
      </section>
      <section class="sub-section bg-light general-features p-1 my-1 ml-1">
        <span class="sub-heading sub-specification text-dark">
          Connectivity
        </span>
      </section>
      <section class="sub-section bg-light general-features p-1 my-1">
        <span class="sub-heading sub-specification text-dark">
          Performance
        </span>
      </section>
    </section>
  </div>
</template>

<script>
export default {
  name: 'listingPage',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .font{
    font-family: 'Poppins';
  }
  .header-font{
    font-weight: 600;
  }
  .sub-heading{
    font-weight: 500;
  }
  .text-dark{
    color: #000000;
  }
  .text-light-dark{
    color: rgba(0, 0, 0, 0.6);
  }
  .text-white{
    color: #FFFFFF;
  }
  .bg-dark{
    background-color: #000000;
  }
  .bg-light{
    background-color: #FFFFFF;
  }
  .bg-grey{
    background-color: #F1F3F6;
  }
  .center-margin{
    margin: 0 auto;
  }
  .text-block-center{
    display: inline-block;
    width: 100%;
    text-align: center;
  }
  .heading{
    margin-top: 0.5rem;
    margin-bottom: 0.5rem;
  }
  .p-1{
    padding: 1rem;
  }
  .m-1{
    margin: 1rem;
  }
  .my-1{
    margin-top: 1rem;
    margin-bottom: 1rem;
  }
  .mx-1{
    margin-left: 1rem;
    margin-right: 1rem;
  }
  .mt-1{
    margin-top: 1rem;
  }
  .mb-1{
    margin-bottom: 1rem;
  }
  .ml-1{
    margin-left: 1rem;
  }
  .header{
    display: flex;
    align-items: center;
    font-size: 42px;
    line-height: 63px;
    padding-top: 0.5rem;
    padding-bottom: 0.5rem;
  }
  .upper-case{
    text-transform: uppercase;
  }
  .capitalize{
    text-transform: capitalize;
  }
  .section1{
    margin-top: 1rem;
    margin-bottom: 1rem;
  }
  .s1{
    margin-top: 1rem;
  }
  .avatar-container{
    align-content: center;
  }
  .avatar{
    width: 100px;
    height: 100px;
    border-radius: 100%;
  }
  .features{
    flex-direction: row;
    display: flex;
    align-items: center;
    padding-top: 1.4rem;
    padding-bottom: 1.4rem;
  }
  .features1{
    font-size: 14px;
    line-height: 21px;
  }
  .sub-features{
    font-size: 12px;
    line-height: 18px;
  }
  .specification{
    width: 85%;
    padding-top: 3rem;
    padding-bottom: 3rem;
  }
  .specification-header{
    font-size: 24px;
    line-height: 36px;
  }
  .specification1{
    margin-top: 3rem;
    border-radius: 0.8rem;
  }
  .sub-section{
    width: 49.5%;
    float: left;
    border-radius: 0.8rem;
  }
  .sub-specification{
    font-size: 13px;
    line-height: 20px;
  }
</style>
