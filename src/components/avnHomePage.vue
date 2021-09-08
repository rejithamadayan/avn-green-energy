<template>
  <div class="avn-home-page">
      <div class="avn-home-page__header">
          <div class="avn-home-page__header-left">
               <img class="" src="" alt="LOGO">
          </div>
          <div class="avn-home-page__header-right">
              <ul class="avn-home-page__header-right-labels">
                  <li v-for="(label, key) in navigationLabels" :key="key">
                      <a href="javascript:void(0)"  class="avn-home-page__header-label">{{label}}</a>
                  </li>
              </ul>
          </div>
      </div>
      <div class="avn-home-page__image">
          <img src="../assets/FloatingDrum.png" alt="">
          <div class="avn-home-page__image-text">
               <p class="avn-home-page__image-text-header">AVN Green Energy</p>
               <p class="avn-home-page__image-text-sub-header">This plant</p>
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
                  <img src="../assets/Plant.jpg" alt="">
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
                  <img src="../assets/Process.jpg" alt="">
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
                   <img src="../assets/Fixed_Dome.jpg" alt="">
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
  </div>
</template>

<script>
export default {
  name: 'AvnHomePAge',
  components:{
  },
  data () {
      return {
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
                     font-size: 5.625rem;
                }
                .avn-home-page__image-text-sub-header {
                     font-size: 2rem;
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
                font-size: 2.25rem;
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
                    padding: 16px;
                    background: transparent;
                    border: 1px solid black;
                    cursor: pointer;
                }
            }
        }
        .avn-home-page__image-list {
            display: flex; 
            // align-items: center;
            // margin-top: 32px;
        }
        .avn-home-page__image-list > div {
            flex: 1; /*grow*/
            img {
                width: 100%;
            }
        }
        .avn-home-page__text-desc {
            // margin-top: 64px;
        }
        .div-block {
            height: 440px;
            display: flex;
            align-items: center;
        }
    }
    @media only screen and (max-width: 600px) {
        .avn-home-page__image{
            .avn-home-page__image-text{
                .avn-home-page__image-text-header {
                    font-size: 2.65rem !important;
                }
                .avn-home-page__image-text-sub-header {
                     font-size: 1.65rem !important;
                }
            }
        }
        .avn-home-page__question {
            flex-direction: column !important;
            align-items: stretch !important;
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
    }
</style>