<template>
  <div class="font">
    <section class="section1 header header-font">
      <span class="s1 upper-case text-dark center-margin">
        Reasons to Buy
      </span>
    </section>
    <section class="bg-light features center-margin">
      <div class="avatar-container center-margin">
        <div class="avatar bg-secondary center-margin"></div>
        <span class="sub-heading features1 text-block-center">1 Year Warranty</span>
        <br/>
        <span class="sub-heading sub-features text-light-dark text-block-center">
          Seller / Manufacture Warranty
        </span>
      </div>
      <div class="avatar-container center-margin">
        <div class="avatar bg-secondary center-margin"></div>
        <span class="sub-heading features1 text-block-center">Unlocked / Free SIM</span>
        <br/>
        <span class="sub-heading sub-features text-light-dark text-block-center">
          Work with all networks
        </span>
      </div>
      <div class="avatar-container center-margin">
        <div class="avatar bg-secondary center-margin"></div>
        <span class="sub-heading features1 text-block-center">Next Day Delivery</span>
        <br/>
        <span class="sub-heading sub-features text-light-dark text-block-center">
          On your Door Step
        </span>
      </div>
      <div class="avatar-container center-margin">
        <div class="avatar bg-secondary center-margin"></div>
        <span class="sub-heading features1 text-block-center">
          Free Delivery
        </span>
        <br/>
        <span class="sub-heading sub-features text-light-dark text-block-center">
          All Over United Kingdom
        </span>
      </div>
    </section>
    <section class="specification py-3 bg-grey center-margin">
      <span class="specification-header header-font text-dark">
        Specification
      </span>
      <section class="bg-light features center-margin specification1">
        <div class="avatar-container center-margin d-inherit">
          <div class="avatar bg-secondary center-margin sub-avatar"></div>
          <div class="spec-details">
            <span class="sub-heading features1 text-block-center upper-case">6.7 inches</span>
            <br/>
            <span class="sub-heading sub-features text-light-dark text-block-center">
              Display
            </span>
          </div>
        </div>
        <div class="avatar-container center-margin d-inherit">
          <div class="avatar bg-secondary center-margin sub-avatar"></div>
          <div class="spec-details">
            <span class="sub-heading features1 text-block-center upper-case">8GB / 6GB</span>
            <br/>
            <span class="sub-heading sub-features text-light-dark text-block-center">
              RAM
            </span>
          </div>
        </div>
        <div class="avatar-container center-margin d-inherit">
          <div class="avatar bg-secondary center-margin sub-avatar"></div>
          <div class="spec-details">
            <span class="sub-heading features1 text-block-center">4352 mAh</span>
            <br/>
            <span class="sub-heading sub-features text-light-dark text-block-center">
              Battery
            </span>
          </div>
        </div>
        <div class="avatar-container center-margin d-inherit">
          <div class="avatar bg-secondary center-margin sub-avatar"></div>
          <div class="spec-details">
            <span class="sub-heading features1 text-block-center">
              12 MP + 12 MP
            </span>
            <br/>
            <span class="sub-heading sub-features text-light-dark text-block-center">
              Back Camera
            </span>
          </div>
      </div>
      </section>
      <section class="sub-section mt-1 bg-light general-features p-1 my-1">
        <span class="sub-heading sub-specification text-dark">
          General Features
        </span>
        <div>1</div>
        <div>2</div>
        <div>3</div>
        <div>4</div>
        <div>5</div>
      </section>
      <section class="sub-section ml-05 mt-1 bg-light general-features p-1 my-1">
        <span class="sub-heading sub-specification text-dark">
          Performance
        </span>
        <div>1</div>
        <div>2</div>
      </section>
      <section class="sub-section ml-05 mt-1 bg-light general-features p-1 my-1">
        <span class="sub-heading sub-specification text-dark">
          Display
        </span>
        <div>1</div>
        <div>2</div>
        <div>3</div>
        <div>4</div>
      </section>
      <section class="sub-section mt-1 bg-light general-features p-1 my-1">
        <span class="sub-heading sub-specification text-dark">
          Camera
        </span>
        <div>1</div>
        <div>2</div>
        <div>3</div>
        <div>4</div>
        <div>5</div>
        <div>6</div>
        <div>7</div>
      </section>
      <section class="sub-section ml-05 mt-1 bg-light general-features p-1 my-1">
        <span class="sub-heading sub-specification text-dark">
          Memory
        </span>
        <div>1</div>
        <div>2</div>
        <div>3</div>
      </section>
      <section class="sub-section mt-1 bg-light general-features p-1 my-1">
        <span class="sub-heading sub-specification text-dark">
          Connectivity
        </span>
        <div>1</div>
        <div>2</div>
        <div>3</div>
        <div>4</div>
        <div>5</div>
        <div>6</div>
        <div>7</div>
      </section>
      <section class="sub-section ml-05 mt-1 bg-light general-features p-1 my-1">
        <span class="sub-heading sub-specification text-dark">
          Battery
        </span>
        <div>1</div>
      </section>
    </section>
  </div>
</template>

<script>
export default {
  name: 'listingPage'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .text-block-center{
    display: inline-block;
    width: 100%;
    text-align: center;
  }
  .heading{
    margin-top: 0.5rem;
    margin-bottom: 0.5rem;
  }
  .header{
    display: flex;
    align-items: center;
    font-size: 42px;
    line-height: 63px;
    padding-top: 0.5rem;
    padding-bottom: 0.5rem;
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
    display: flex;
    flex-direction: row;
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
  .spec-details{
    width:100%;
    float: left;
  }
  .sub-avatar{
    height: 62px;
  }
</style>
