<template>
  <div class="container">
    <div class="row">
      <div class="col-lg-12 col-xs-12">
        <topBar />
      </div>
    </div>
    <div class="row">
      <div class="col-lg-12 col-xs-12 mt-5">
        <div class="row font-montserrat">
          <div
            class="d-flex justify-content-between align-items-center col-lg-12 col-xs-12"
          >
            <div>
              <span class="title">
                <b>Stays in Finland</b>
              </span>
            </div>
            <div>
              <span class="value-search"> 12+ stays </span>
            </div>
          </div>
        </div>
        <div class="row mt-3">
          <div
            class="col-lg-4 col-xs-12 mb-2"
            v-for="item in places"
            :key="item.id"
          >
            <div class="d-flex align-items-center">
              <div class="description-place">
                <img
                  :src="item.photo"
                  class="mb-1"
                  width="100%"
                  height="300px"
                  alt=""
                />

                <span class="super-host" v-if="item.superHost">
                  SUPER HOST
                </span>
                <span class="type">{{ item.type }}</span>
                <span style="float: right; font-size: 14px; color: #4f4f4f">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    width="16"
                    height="16"
                    color="#EB5757"
                    fill="currentColor"
                    class="bi bi-star-fill"
                    viewBox="0 0 16 16"
                  >
                    <path
                      d="M3.612 15.443c-.386.198-.824-.149-.746-.592l.83-4.73L.173 6.765c-.329-.314-.158-.888.283-.95l4.898-.696L7.538.792c.197-.39.73-.39.927 0l2.184 4.327 4.898.696c.441.062.612.636.283.95l-3.523 3.356.83 4.73c.078.443-.36.79-.746.592L8 13.187l-4.389 2.256z"
                    />
                  </svg>
                  {{ item.rating }}
                </span>

                <div>
                  <span class="decription-text">
                    {{ item.title }}
                  </span>
                </div>
              </div>
            </div>
          </div>
        </div>
        <author />
      </div>
    </div>
  </div>
</template>

<script>
import author from "@/components/footer.vue";
import Stays from "../../../../back/stays.json";
import topBar from "@/components/topBar.vue";
export default {
  components: { topBar, author },
  data: () => ({
    places: [],
  }),
  mounted() {
    this.places = Stays;
    console.log(this.places);
  },
};
</script>

<style lang="scss" scoped>
.description-place {
  .type {
    font-size: 14px;
    line-height: 17px;
    color: #828282;
  }

  .super-host {
    border: 1px solid #4f4f4f;
    width: 100px;
    height: 28px;
    border-radius: 12px;
    font-size: 12px;
    padding: 1px 5px;
    color: #4f4f4f;
    text-transform: uppercase;
    box-sizing: border-box;
    margin: 0px 3px;
  }
}

.title {
  font-size: 24px;
  color: #333333;
  line-height: 29px;
}

.value-search {
  font-weight: 500;
  font-size: 14px;
  line-height: 17px;
  float: right;
  color: #4f4f4f;
}

.decription-text {
  color: #333333;
  font-size: 16px;
  font-family: Montserrat;
  font-style: normal;
  font-weight: 600;
}
</style>