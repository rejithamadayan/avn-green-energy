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
          <div class="avn-home-page__image-text">
               <p class="avn-home-page__image-text-header">AVN Green Energy</p>
               <p class="avn-home-page__image-text-sub-header">This plant</p>
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
          navigationLabels: ['Home', 'About', 'Contact']
      }
  }
}
</script>
<style lang="scss">
    .avn-home-page {
        .avn-home-page__header {
            display: flex;
            align-items: center;
            padding: 8px 40px;
            // > * {
            //     flex: 50%;
            // }
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
            height: 670px;
            object-fit: cover;
            display: block;
            background-size: cover;
            background-image: url("./../assets/FloatingDrum.png");
            background-repeat: no-repeat;
            background-position: 50% 50%;
            position: relative;
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
                    margin: 0;
                }
                .avn-home-page__image-text-header {
                     font-size: 5.625rem;
                }
                .avn-home-page__image-text-sub-header {
                     font-size: 2rem;
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
                     font-size: 1.65rem !important;
                }
            }
        }
    }
</style>