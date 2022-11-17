<template>
  <div class="font">
    <section class="my-3 header header-font">
      <span class="s1 upper-case text-dark center-margin">
        Reasons to Buy
      </span>
    </section>
    <section class="bg-light features center-margin">
      <div class="avatar-container center-margin my-2">
        <div class="avatar bg-secondary center-margin">
          <img class="d-block pt-1_5 center-margin" src="../../../assets/png/warranty.png" alt="Warranty"/>
        </div>
        <span class="mt-1 features1 upper-case text-block-center">1 Year Warranty</span>
        <br/>
        <span class="d-block sub-heading sub-features text-light-dark text-block-center">
          Seller / Manufacture
        </span>
      </div>
      <div class="avatar-container center-margin my-2">
        <div class="avatar bg-secondary center-margin">
          <img class="d-block pt-1_5 center-margin" src="../../../assets/png/unlocked.png" alt=""/>
        </div>
        <span class="mt-1 features1 upper-case text-block-center">Unlocked / Free SIM</span>
        <br/>
        <span class="d-block sub-heading sub-features text-light-dark text-block-center">
          Work with all networks
        </span>
      </div>
      <div class="avatar-container center-margin my-2">
        <div class="avatar bg-secondary center-margin">
          <img class="d-block pt-1_5 center-margin" src="../../../assets/png/delivery.png" alt=""/>
        </div>
        <span class="mt-1 features1 upper-case text-block-center">Next Day Delivery</span>
        <br/>
        <span class="d-block sub-heading sub-features text-light-dark text-block-center">
          On your Door Step
        </span>
      </div>
      <div class="avatar-container center-margin my-2">
        <div class="avatar bg-secondary center-margin">
          <img class="d-block pt-1_5 center-margin" src="../../../assets/png/free_delivery.png" alt=""/>
        </div>
        <span class="mt-1 features1 upper-case text-block-center">
          Free Delivery
        </span>
        <br/>
        <span class="d-block sub-heading sub-features text-light-dark text-block-center">
          All Over United Kingdom
        </span>
      </div>
    </section>
    <section class="specification py-3 bg-grey center-margin h-auto">
      <span class="specification-header header-font text-dark">
        Specification
      </span>
      <section class="bg-light features center-margin specification1 py-3 mt-3 pb-none">
        <div class="avatar-container sub-avatar-container center-margin d-inherit">
          <img class="spec-img d-block center-margin" style="--imgWidth: 45%" src="../../../assets/png/phone.png" alt=""/>
          <div class="spec-details">
            <span class="features1 text-left-align ml-1 mt-05 upper-case">{{ phone.display ? phone.display : 'Not Available' }}</span>
            <br/>
            <span class="d-block sub-heading sub-features text-light-dark text-left-align ml-1">
              Display
            </span>
          </div>
        </div>
        <div class="avatar-container sub-avatar-container center-margin d-inherit">
          <img class="spec-img d-block center-margin" style="--imgWidth: 55%" src="../../../assets/png/memory.png" alt=""/>
          <div class="spec-details">
            <span class="features1 text-left-align ml-1 mt-05 upper-case">{{phone.ram}}</span>
            <br/>
            <span class="d-block sub-heading sub-features text-light-dark text-left-align ml-1">
              RAM
            </span>
          </div>
        </div>
        <div class="avatar-container sub-avatar-container center-margin d-inherit">
          <img class="spec-img d-block center-margin" style="--imgWidth: 40%" src="../../../assets/png/battery.png" alt=""/>
          <div class="spec-details">
            <span class="features1 text-left-align ml-1 mt-05">{{phone.battery ? phone.battery : 'Not Available'}}</span>
            <br/>
            <span class="d-block sub-heading sub-features text-light-dark text-left-align ml-1">
              Battery
            </span>
          </div>
        </div>
        <div class="avatar-container sub-avatar-container center-margin d-inherit">
          <img class="spec-img d-block center-margin" style="--imgWidth: 37%" src="../../../assets/png/camera.png" alt=""/>
          <div class="spec-details">
            <span class="features1 text-left-align ml-1 mt-05">
              {{ phone.back_camera ? phone.back_camera : 'Not Available' }}
            </span>
            <br/>
            <span class="d-block sub-heading sub-features text-light-dark text-left-align ml-1">
              Back Camera
            </span>
          </div>
      </div>
      </section>
      <section class="sub-section">
        <div class="bg-light general-features p-1 pb-2 my-1">
          <div class="mt-05 mx-1_5">
            <span class="sub-specification text-dark">
              General Features
            </span>
            <div class="mt-1 details py-03">
              <span class="text-primary details-head sub-heading">Release Date</span>
              <span class="d-block text-dark sub-details sub-heading">{{ phone.release_date ? phone.release_date : 'Not Available' }}</span>
            </div>
            <div class="details py-03">
              <span class="text-primary details-head sub-heading">SIM Support</span>
              <span class="d-block text-dark sub-details sub-heading">{{ phone.sim_support ? phone.sim_support : 'Not Available' }}</span>
            </div>
            <div class="details py-03">
              <span class="text-primary details-head sub-heading">Phone Dimensions</span>
              <span class="d-block text-dark sub-details sub-heading">{{phone.phone_dimensions ? phone.phone_dimensions : 'Not Available'}}</span>
            </div>
            <div class="details py-03">
              <span class="text-primary details-head sub-heading">Phone Weight</span>
              <span class="d-block text-dark sub-details sub-heading">{{phone.phone_weight ? phone.phone_weight : 'Not Available'}}</span>
            </div>
            <div class="py-03">
              <span class="text-primary details-head sub-heading">Operating System</span>
              <div class="sub-details sub-heading f-w-60"><span class="d-block text-dark">{{phone.operating_system ? phone.operating_system : 'Not Available'}}</span></div>
            </div>
          </div>
        </div>
        <div class="bg-light general-features p-1">
          <div class="mt-05 mx-1_5">
            <span class="sub-specification text-dark">
              Display
            </span>
            <div class="mt-1 details py-03">
              <span class="text-primary details-head sub-heading">Screen Size</span>
              <span class="d-block text-dark sub-details sub-heading">{{ phone.screen_size ? phone.screen_size : 'Not Available'}}</span>
            </div>
            <div class="details py-03">
              <span class="text-primary details-head sub-heading">Screen Resolution</span>
              <span class="d-block text-dark sub-details sub-heading">{{phone.screen_resolution ? phone.screen_resolution : 'Not Available'}}</span>
            </div>
            <div class="details py-03">
              <span class="text-primary details-head sub-heading">Screen Type</span>
              <span class="d-block text-dark sub-details sub-heading">{{ phone.screen_type ? phone.screen_type : 'Not Available' }}</span>
            </div>
            <div class="py-03">
              <span class="text-primary details-head sub-heading">Screen Protection</span>
              <span class="d-block text-dark sub-details sub-heading">{{ phone.screen_protection ? phone.screen_protection : 'Not Available' }}</span>
            </div>
          </div>
        </div>
        <div class="bg-light general-features p-1 mt-1">
          <div class="mt-05 mx-1_5">
            <span class="sub-specification text-dark">
              Memory
            </span>
            <div class="mt-1 details  py-03">
              <span class="text-primary details-head sub-heading">Internal Memory</span>
              <span class="d-block text-dark sub-details sub-heading">{{phone.internal_memory ? phone.internal_memory : 'Not Available'}}</span>
            </div>
            <div class="details py-03">
              <span class="text-primary details-head sub-heading">RAM</span>
              <span class="d-block text-dark sub-details sub-heading">{{ phone.ram ? phone.ram : 'Not Available' }}</span>
            </div>
            <div class="py-03">
              <span class="text-primary details-head sub-heading">Card Slot</span>
              <span class="d-block text-dark sub-details sub-heading">{{ phone.card_slot ? 'Yes' : 'No' }}</span>
            </div>
          </div>
        </div>
        <div class="bg-light general-features p-1 pb-2 mt-1">
          <div class="mt-05 mx-1_5">
          <span class="sub-specification text-dark">
              Battery
            </span>
            <div class="pt-1">
              <span class="text-primary details-head sub-heading">Type</span>
              <span class="d-block text-dark sub-details sub-heading f-w-60">{{phone.battery ? phone.battery : 'Not Available'}} {{phone.battery_type ? phone.battery_type : 'Not Available'}}</span>
            </div>
          </div>
        </div>
      </section>
      <section class="ml-1 sub-section">
        <div class="bg-light general-features p-1 my-1">
          <div class="mt-05 mx-1_5">
            <span class="sub-specification text-dark">
              Performance
            </span>
            <div class="mt-1 details py-03">
              <span class="text-primary details-head sub-heading">Processor</span>
              <span class="d-block text-dark sub-details sub-heading">{{phone.processor ? phone.processor : 'Not Available'}}</span>
            </div>
            <div class="py-03">
              <span class="text-primary details-head sub-heading">GPU</span>
              <span class="d-block text-dark sub-details sub-heading">{{phone.gpu ? phone.gpu : 'Not Available'}}</span>
            </div>
          </div>
        </div>
        <div class="bg-light general-features p-1">
          <div class="mt-05 mx-1_5">
            <span class="sub-specification text-dark">
              Camera
            </span>
            <div class="mt-1 details py-03">
              <span class="text-primary details-head sub-heading">Front Camera</span>
              <span class="d-block text-dark sub-details sub-heading">{{phone.front_camera ? phone.front_camera : 'Not Available'}}</span>
            </div>
            <div class="details py-03">
              <span class="text-primary details-head sub-heading">Front Flash Light</span>
              <span class="d-block text-dark sub-details sub-heading">{{phone.front_flashlight ? phone.front_flashlight : 'Not Available'}}</span>
            </div>
            <div class="details py-03">
              <span class="text-primary details-head sub-heading">Front Video Recording</span>
              <span class="d-block text-dark sub-details sub-heading">{{phone.front_video_recording ? phone.front_video_recording : 'Not Available'}}</span>
            </div>
            <div class="details py-03">
              <span class="text-primary details-head sub-heading">Back Flash Light</span>
              <span class="d-block text-dark sub-details sub-heading">{{phone.back_flashlight ? phone.back_flashlight : 'Not Available'}}</span>
            </div>
            <div class="details py-03">
              <span class="text-primary details-head sub-heading">Back Camera</span>
              <span class="d-block text-dark sub-details sub-heading">{{phone.back_camera ? phone.back_camera : 'Not Available'}}</span>
            </div>
            <div class="py-03">
              <span class="text-primary details-head sub-heading">Back Video Recording</span>
              <span class="d-block text-dark sub-details sub-heading">{{phone.back_video_recording ? phone.back_video_recording : 'Not Available'}}</span>
            </div>
          </div>
        </div>
        <div class="bg-light general-features p-1 mt-1">
          <div class="mt-05 mx-1_5">
            <span class="sub-specification text-dark">
              Connectivity
            </span>
            <div class="mt-1 details py-03">
              <span class="text-primary details-head sub-heading">Bluetooth</span>
              <span class="d-block text-dark sub-details sub-heading">{{ phone.bluetooth ? 'Yes' : 'No' }}</span>
            </div>
            <div class="details py-03">
              <span class="text-primary details-head sub-heading">3G</span>
              <span class="d-block text-dark sub-details sub-heading">{{ phone.G3 ? 'Yes' : 'No' }}</span>
            </div>
            <div class="details py-03">
              <span class="text-primary details-head sub-heading">4G/LTE</span>
              <span class="d-block text-dark sub-details sub-heading">{{ phone.G4 ? 'Yes' : 'No' }}</span>
            </div>
            <div class="details py-03">
              <span class="text-primary details-head sub-heading">5G</span>
              <span class="d-block text-dark sub-details sub-heading">{{ phone.G5 ? 'Yes' : 'No' }}</span>
            </div>
            <div class="details py-03">
              <span class="text-primary details-head sub-heading">Radio</span>
              <span class="d-block text-dark sub-details sub-heading">{{ phone.radio ? 'Yes' : 'No' }}</span>
            </div>
            <div class="details py-03">
              <span class="text-primary details-head sub-heading">WiFi</span>
              <span class="d-block text-dark sub-details sub-heading">{{ phone.wifi ? 'Yes' : 'No' }}</span>
            </div>
            <div class="py-03">
              <span class="text-primary details-head sub-heading">NFC</span>
              <span class="d-block text-dark sub-details sub-heading">{{ phone.nfc ? 'Yes' : 'No' }}</span>
            </div>
          </div>
        </div>
      </section>
    </section>
    
    <section class="faq bg-grey">
      <div class="w-85 center-margin py-3">
        <span class="header-font text-dark specification-header">
          FAQ
        </span>
      </div>
      <div class="bg-light w-100 py-3">
        <div v-for="(qa,index) in Faq" :key="qa.id">
          <div class="w-85 center-margin p-1">
            <input :id="'faqs' + index" type="checkbox" class="d-none"/>
            <label :for="'faqs' + index" class="d-block header-font features1">Q. {{qa.question}}</label>
            <div class="sub-heading features1 faq-answer">A. {{qa.answer}}</div>
          </div>
        </div>
      </div>
    </section>

    <section class="faq bg-grey">
      <div class="w-85 center-margin py-3">
        <span class="header-font text-dark specification-header">
          What’s in the Box
        </span>
      </div>
      <div class="bg-light w-100 py-3">
        <div v-for="bx in Box" :key="bx.id">
          <div class="w-85 center-margin">
            <img src="../../../assets/png/bullet.png"/>
            <span class="ml-1 features1">{{ bx.in_box }}</span> 
          </div>
        </div>
      </div>
    </section>

    <section class="faq bg-grey">
      <div class="w-85 center-margin py-3">
        <span class="header-font text-dark specification-header">
          Condition
        </span>
      </div>
      <div class="bg-light w-100 py-3">
        <div v-for="cond in Condition" :key="cond.id">
          <div class="w-85 center-margin">
            <img src="../../../assets/png/bullet.png"/>
            <span class="ml-1 features1">{{cond.condition}}</span> 
          </div>
        </div>
      </div>
    </section>

    <section class="specification bg-grey center-margin">
      <section class="sub-section ">
        <span class="specification-header header-font text-dark text-block-center py-3">
          Shipping Policy
        </span>
        <div class="bg-light general-features p-1 my-1 m-h-50 mb-3">
          <div class="p-1">
            <span class="features1">Items will be shipped out same day if ordered before 3 pm.       
              <br /><br />
            Delivery Address: It is the buyer's responsibility to provide the correct delivery address. The goods are dispatched to the Buyer's address in eBay records. If there is any change in your personal details, please update your address before checkout, if you want to arrange a delivery to a different address than your own, please add the new address for delivery at checkout.                          
              <br /><br />
            The Delivery Time depends on the type of delivery service selected by the buyer. Mostly Royal Mail used, so parcel will arrive within 1-2 days. </span>
          </div>
        </div>
      </section>
      <section class="ml-1 sub-section">
        <span class="specification-header header-font text-dark text-block-center py-3">
          Return Policy
        </span>
        <div class="bg-light general-features p-1 my-1 m-h-50 mb-3">
          <div class="p-1">
            <span class="features1">
              We offer 30 Days Money Back service of the receipt of goods for an exchange or a refund. 
                <br /><br />
              All returns must include all original items undamaged, in re-saleable condition, all original packaging including manuals, warranty forms FREE OF ANY WEAR OR TEAR AND UNUSED IN A GOOD SALABLE CONDITION. Please Note: In case of exchange or return Seller will pay the postage. In case of refund seller only refund the actual item price. 
                <br /><br />
              Postage will not be refunded. Please contact us before returning item(s).
            </span>
          </div>
        </div>
      </section>
    </section>
  </div>
</template>

<script>
export default {
  name: 'listingPage',
  props: ["phone"],
  computed: {
    Faq(){
      return JSON.parse(this.phone.faq)
    },
    Condition(){
      return JSON.parse(this.phone.cond)
    },
    Box(){
      return JSON.parse(this.phone.box)
    }
  }
}
</script>
<style>
  .text-block-center{
    display: inline-block;
    width: 100%;
    text-align: center;
  }
  .text-left-align{
    display: inline-block;
    width: 100%;
    text-align: left;
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
  .s1{
    margin-top: 1rem;
  }
  .avatar-container{
    align-content: center;
  }
  .avatar{
    width: 84px;
    height: 84px;
    border-radius: 100%;
  }
  .features{
    display: flex;
    flex-direction: row;
    align-items: center;
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
    width: 49%;
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
    width:90px;
  }
  .general-features{
    border-radius: 0.8rem;
  }
  .details{
    border-bottom: 1px solid rgba(0, 0, 0, 0.08);
  }
  .details-head{
    font-weight: 500;
    font-size: 11px;
    width: 30%;
    float: left;
    border-radius: 0.8rem;
  }
  .sub-details{
    font-weight: 500;
    font-size: 11px;
  }
  .faq{
    clear:both;
  }
</style>
