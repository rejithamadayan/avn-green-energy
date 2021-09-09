<template>
  <div class="avn-home-page">
      <div class="avn-home-page__header">
          <div class="avn-home-page__header-left">
               <img class="" src="../img/logo.png" alt="LOGO">
          </div>
          <div class="avn-home-page__header-right">
              <ul class="avn-home-page__header-right-labels">
                  <li v-for="(label, index, key) in navigationLabels" :key="key">
                      <a href="javascript:void(0)" id="tab" class="avn-home-page__header-label" :class="activeTab === index ? 'active-tab' : ''" @click="getActiveTab(index)">{{label}}</a>
                  </li>
              </ul>
          </div>
      </div>
      <div class="avn-home-page__image">
          <img src="../img/FloatingDrum.png" alt="">
          <div class="avn-home-page__image-text">
               <p class="avn-home-page__image-text-header">AVN GREEN Energy</p>
               <p class="avn-home-page__image-text-sub-header">Transforming Waste to Green Energy</p>
          </div>
      </div>
      <div class="avn-home-page__question">
            <div class="avn-home-page__question-left">
                <p class="avn-home-page__question-title">Have Any Questions !</p>
                <p class="avn-home-page__question-text">Don't Hesitate to Contact Us Any Time.</p>
            </div>
            <div class="avn-home-page__question-right">
                <button class="avn-home-page__question-button">REQUEST A QUOTE</button>
                <button>CONTACT US</button>
            </div>
      </div>
      <div class="avn-home-page__image-list">
          <div class="avn-home-page__imag-desc avn-home-page__image-biogas">
              <div class="div-block">
                  <img src="../img/Plantn.jpg" alt="">
              </div>
              <div class="avn-home-page__text-desc avn-home-page__image-biogas-desc">
                  <h4>Biogas Plant</h4>
                  <ul>
                      <li v-for="(item, key) in biogasDesc" :key="key">
                          <p>{{item.title}}</p>
                          <ul>
                              <li v-for="(data, key) in item.list" :key="key">
                                  <p>{{data}}</p>
                              </li>
                          </ul>
                      </li>
                  </ul>
              </div>
          </div>
          <div class="avn-home-page__imag-desc avn-home-page__image-process">
              <div class="div-block">
                  <img src="../img/Process.jpg" alt="">
              </div>
              <div class="avn-home-page__text-desc avn-home-page__image-process-desc">
                  <h4>Production of Biogas</h4>
                  <ul>
                      <li v-for="(item, key) in processDesc" :key="key">
                          <p>{{item.title}}</p>
                          <ul>
                              <li v-for="(data, key) in item.list" :key="key">
                                  <p>{{data}}</p>
                              </li>
                          </ul>
                      </li>
                  </ul>
              </div>
          </div>
          <div class="avn-home-page__imag-desc avn-home-page__image-fixed">
              <div class="div-block">
                   <img src="../img/Fixed_Dome.jpg" alt="">
              </div>
              <div class="avn-home-page__text-desc avn-home-page__image-fixed-desc">
                  <h4>Fixed Dome type Plant</h4>
                  <ul>
                      <li v-for="(item, key) in fixedDesc" :key="key">
                          <p>{{item.title}}</p>
                          <ul>
                              <li v-for="(data, key) in item.list" :key="key">
                                  <p>{{data}}</p>
                              </li>
                          </ul>
                      </li>
                  </ul>
              </div>
          </div>
      </div>
      <div class="avn-home-page__our-story">
          <div class="avn-home-page__our-story-top">
            <h4>Our Story</h4>
            <p>AVN green energy plant has been established in Green Agra City as passion and founded in collaboration with 3 partners having distinct knowledge and experience in the field of Green and Renewable energy solutions.</p>
          </div>
          <div class="avn-home-page__our-story-middle">
              <div class="our-story-middle__left">
                  <div>
                      <p class="story-title">About</p>
                      <p>AVN green energy plant has been established in the Agra City, UttarPradesh. This renewable power generation company has been co-founded by 3 partners having distinct knowledge and experience in the field of Green and Renewa.ble energy solutions.</p>
                  </div>
                  <div>
                    <p class="story-title">Vision</p>
                    <p>Driven by passion to promote </p>
                    <ul>
                        <li>
                            <span>Sustainable  green energy for the protection of the climate.</span>
                        </li>
                        <li>
                            <span>Eco friendly and low cost energy to Smart Cities and Smart Village</span>
                        </li>
                        <li>
                            <span>Recycle waste and organic Manure</span>
                        </li>
                    </ul>
                  </div>
                  <div>
                    <p class="story-title">Our Goals</p>
                    <p>Efficient recovery value with organic energy.</p>
                  </div>
              </div>
              <div class="our-story-middle__center">
                <img src="../img/people.jpeg" alt="">
              </div>
              <div class="our-story-middle__right">
                 <div>
                      <p class="story-title">Reliability</p>
                      <p>AVN Green Energy has a cutting edge quality management system which ensures high quality standards at all sites.</p>
                  </div>
                  <div>
                    <p class="story-title">Expertise</p>
                    <p>We have a team of specialists capable of maximizing the result and delivering the projects on time.</p>
                  </div>
                  <div>
                    <p class="story-title">Quality</p>
                    <p>The control mechanism allows secure & integrated monitoring of all stages of the works.</p>
                  </div>
              </div>
          </div>
          <div class="avn-home-page__services">
              <h4>Biogas services  and products</h4>
              <div>
                  <div>
                      <p>Biomethane</p>
                      <p>Today, biogas is generally used directly at the place where it is produced</p>
                  </div>
                  <div>
                      <p>General information</p>
                      <p>Biogas is actually a mixture of gases - Carbon dioxide (CO2) and methane.</p>
                  </div>
                  <div>
                      <p>Benefits of biogas</p>
                      <p>Biogas is a very efficient in all  and can be converted into lectricity and heat or organic fertilizer</p>
                  </div>
                  <div>
                      <p>Green organic fertilizer solution</p>
                      <p>Slurry and manure as cheap substrate and by products as organic fertilizer alongside green energy generation</p>
                  </div>
                  <div>
                      <p>Industry focus</p>
                      <p>biogas plant focus is to reduce waste, reduce energy costs and climate impact by using green energy.</p>
                  </div>
                  <div>
                      <p>Waste to Energy</p>
                      <p>The digestion of waste could complete a cycle of raw materials based on food production or food waste</p>
                  </div>
              </div>
          </div>
          <div class="avn-home-page__our-story-bottom">
              <div class="visit contact-box">
                  <img src="../img/visit.svg" alt="">
                  <div>
                      <a href="">
                        <p>Visit Us</p>
                        <p>Thane, Mumbai India</p>
                      </a>
                  </div>
              </div>
              <div class="mail contact-box">
                  <img src="../img/mail.svg" alt="">
                  <div>
                      <a href = "mailto: abc@example.com">
                        <p>Email Us</p>
                        <p>youremail@biogas.com</p>
                      </a>
                  </div>
              </div>
              <div class="call contact-box">
                  <img src="../img/call.svg" alt="">
                  <div>
                      <a href="tel:74873287483">
                        <p>Call Us</p>
                        <p>+ 91 74873287483</p>
                       </a>
                  </div>
              </div>
          </div>
      </div>
  </div>
</template>

<script>
export default {
  name: 'AvnHomePAge',
  components:{
  },
  data () {
      return {
          activeTab: 0,
          navigationLabels: ['Home', 'About', 'Contact'],
          biogasDesc: [
              {
                  title: 'Biogas is a clean and efficient fuel.',
                  list: []
              },
              {
                 title: 'It is a mixture of ',
                 list: ['Methane (CH4)', 'Carbon dioxide (CO2)', 'Hydrogen (H2)', 'Hydrogen sulphide (H2S)'] 
              },
              {
                  title: 'The chief constituent of biogas is methane (65%).',
                  list: []
              },
          ],
          processDesc: [
              {
                  title: 'There are two types of biogas plants in usage for the production of biogas. These are:',
                  list: ['The fixed- dome type of biogas plant', 'The floating gas holder type of biogas plant']
              }
          ],
          fixedDesc: [
              {
                  title: 'Requires only locally and easily available materials for construction.',
                  list: []
              },
              {
                 title: 'Inexpensive',
                 list: []
              },
              {
                  title: 'Easy to construct',
                  list: []
              },
          ]
      }
  },
  methods : {
      getActiveTab (index) {
          this.activeTab = index
          if (index === 0) {
              const homeElement = document.querySelector('.avn-home-page__header')
              homeElement.scrollIntoView({behavior: 'smooth'})
          }
          if (index === 1) {
              const aboutElement = document.querySelector('.avn-home-page__our-story')
              aboutElement.scrollIntoView({behavior: 'smooth'})
          }
          if (index === 2) {
              const contactElement = document.querySelector('.avn-home-page__our-story-bottom')
              contactElement.scrollIntoView({behavior: 'smooth'})
          }
      }
  }
}
</script>
<style lang="scss">

    .avn-home-page {
        h4 {
            font-size: 26px;
            padding: 0 24px;
            margin: 0;
        }
        .avn-home-page__header {
            display: flex;
            align-items: center;
            padding: 8px 40px;
            .avn-home-page__header-left{
                flex: 1;
                img {
                    width: 48px;
                    height: 48px;
                }
            }
            .active-tab {
               color: #478ac9;
            }
        }
        .avn-home-page__header-right-labels {
            display: flex;
            list-style: none;
            > * {
                margin-right: 12px;
            }
        }
        .avn-home-page__header-label {
            color: black;
            text-decoration: none;
        }
        .avn-home-page__image {
            margin-bottom: -8px;
            position: relative;
            img {
                width: 100%;
            }
            .avn-home-page__image-text {
                display: flex;
                flex-direction: column;
                align-items: center;
                position: absolute;
                top: 50%;
                left: 50%;
                transform: translate(-50%, -50%);
                z-index: 2;
                color: white;
                font-family: patua-one;
                white-space: nowrap;
                > * {
                    padding: 8px 0;
                }
                .avn-home-page__image-text-header {
                     font-size: 3.625rem;
                }
                .avn-home-page__image-text-sub-header {
                     font-size: 1.25rem;
                }
            }
        }
        .avn-home-page__question {
            display: flex;
            color: #ffffff;
            background-color: #2cccc4;
            align-items: center;
            padding: 40px 60px;
            justify-content: space-between;
            .avn-home-page__question-title {
                font-size: 1.25rem;
                margin-bottom: 16px;
                white-space: nowrap;
            }
            .avn-home-page__question-text {
                font-size: 2 rem;
                line-height: 1.1;
            }
            .avn-home-page__question-right {
                display: flex;
                .avn-home-page__question-button {
                    margin-right: 16px;
                    background-color: black;
                    color: white;
                    font-weight: 600;
                }
                button {
                    padding:12px 16px;
                    background: transparent;
                    border: 1px solid black;
                    cursor: pointer;
                    width: 175px;
                }
            }
        }
        .avn-home-page__image-list {
            display: flex; 
            padding-bottom: 32px;
        }
        .avn-home-page__image-list > div {
            flex: 1; /*grow*/
            img {
                width: 100%;
                width: 100%;
            }
        }
        .div-block {
            height: 440px;
            display: flex;
            align-items: center;
        }
        .avn-home-page__our-story {
            background-color: #f2f2f2;
            .avn-home-page__our-story-top {
                padding: 32px;
                text-align: center;
                margin-bottom: 32px;
                h4 {
                    margin-bottom: 16px;
                }
            }
            .avn-home-page__our-story-middle{
                 display: flex;
                 padding: 0 46px;
                > * {
                    margin-right: 32px;
                }
                .our-story-middle__left {
                    width: 45%;
                    > * {
                        margin-bottom: 64px;
                    }
                }
                .our-story-middle__center{
                    width: 25%;
                    img {
                    width: 100%;
                    }

                }
                .our-story-middle__right {
                    width: 20%;
                     > * {
                        margin-bottom: 64px;
                    }
                }
                .story-title {
                    font-size: 1.25rem;
                    margin-bottom: 16px;
                }
            }
            .avn-home-page__our-story-bottom {
                background: black;
                display: flex;
                justify-content: space-around;
                padding:64px 32px;
                > div > img {
                    height: 60px;
                    width: 80px;
                    margin-right: 16px;
                }
                >div > div {
                    color: white;
                }
                .contact-box {
                    display: flex;
                    align-items: center;
                    > div > a> p:first-child {
                        font-size: 1.25rem;
                        color: #2ccc;
                        margin-bottom: 8px;
                    }
                    > div > a {
                        text-decoration: none;
                        color: white;
                    }
                }
            }
        }
        .avn-home-page__services {
            padding: 24px;
            background-color: white;
            h4 {
                font-size: 1.35rem;
                padding: 0;
                margin-bottom: 16px;
            }
            > div {
                display: flex;
                flex-wrap: wrap;
                justify-content: space-between;
                > div {
                    padding: 16px;
                   width: 30%;
                   background-color: #f2f2f2;
                   margin-bottom: 16px;
                   border: 1px solid;
                    padding: 10px;
                    border-radius: 4px;
                    box-shadow: 5px 5px #888888;
                }
                >div > p:first-child {
                    font-size: 1rem;
                    font-weight: 600;
                    margin-bottom: 12px;
                }
            }
        }
    }
    @media only screen and (max-width: 600px) {
        .avn-home-page__image{
            .avn-home-page__image-text{
                .avn-home-page__image-text-header {
                    font-size: 2.65rem !important;
                }
                .avn-home-page__image-text-sub-header {
                     font-size: 1rem !important;
                }
            }
        }
        .avn-home-page__question {
            flex-direction: column !important;
            align-items: stretch !important;
            padding: 24px !important;
            .avn-home-page__question-text {
                font-size: 1.5rem !important;
            }
            .avn-home-page__question-right {
                flex-direction: column !important;
                margin-top: 36px !important;
                .avn-home-page__question-button {
                    margin-bottom: 16px !important;
                }
            }
        }
         .avn-home-page__image-list  {
                flex-direction: column !important;
        }
        .div-block {
            height: inherit !important;
            margin-bottom: 32px !important;
        }
        .avn-home-page__text-desc {
          margin-bottom: 64px !important;
        }
        .avn-home-page__our-story-middle{
            padding: 0 16px !important;
            flex-direction: column !important;
            > div {
                width: 100% !important;
                flex: 1 !important;
            }
        }
        .our-story-middle__center {
            margin-bottom: 32px !important;
        }
        .avn-home-page__our-story-bottom {
            flex-direction: column  !important;
            justify-content:flex-start !important;
            padding:32px 16px !important;
            > div > img {
                    height: 50px !important;
                    width: 60px !important;
                    margin-right: 16px !important;
                }
            .contact-box {
                margin-bottom: 64px;
                > div > p:first-child {
                    font-size: 1.2rem !important;
                }
                &:last-child {
                    margin-bottom: 16px !important;
                }
            }
        }
        .avn-home-page__services {
            h4 {
                font-size: 1rem;
            }
            > div {
              flex-direction: column;
              align-items: center;
              flex-wrap: unset !important;
                
                > div {
                   width: 100% !important;
                }
                >div > p:first-child {
                    font-size: 1.25rem !important;
                }
            }
        }
    }
</style>