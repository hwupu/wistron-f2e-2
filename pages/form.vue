<template>
  <article class="CUB-signup">
    <aside class="CUB-signup-steps">
      <b-steps type="is-info" :mobile-mode="null" :has-navigation="false">
        <b-step-item step="1" label="登錄服務" header-class="CUB-signup-steps-item">
          <p class="is-hidden-tablet has-text-info is-size-6 has-text-centered">
            登錄服務
          </p>
        </b-step-item>
        <b-step-item label="確認資訊" header-class="CUB-signup-steps-item">
          <p class="is-hidden-tablet has-text-info is-size-6 has-text-centered">
            確認資訊
          </p>
        </b-step-item>
      </b-steps>
    </aside>

    <form>
      <section class="container is-max-desktop section">
        <b-field horizontal label="持卡人身分證後5碼">
          <b-input
            autofocus
            name="social_id"
            pattern="[\d]{5}"
            maxlength="5"
            :has-counter="false"
            validation-message="身分證格式輸入錯誤"
            required
            expanded
          />
        </b-field>

        <b-field horizontal label="開通的信用卡／ｉ刷金融卡卡號">
          <div class="field is-grouped">
            <b-input
              name="card1"
              pattern="[\d]{4}"
              maxlength="4"
              :has-counter="false"
              validation-message="卡號格式輸入錯誤"
              required
              expanded
            />
            <b-input
              name="card2"
              pattern="[\d]{4}"
              maxlength="4"
              :has-counter="false"
              validation-message="卡號格式輸入錯誤"
              required
              expanded
            />
            <b-input
              name="card3"
              pattern="[\d]{4}"
              maxlength="4"
              :has-counter="false"
              validation-message="卡號格式輸入錯誤"
              required
              expanded
            />
            <b-input
              name="card4"
              pattern="[\d]{4}"
              maxlength="4"
              :has-counter="false"
              validation-message="卡號格式輸入錯誤"
              required
              expanded
            />
          </div>
        </b-field>

        <b-field horizontal label="生日">
          <b-input
            type="date"
            name="birthday"
            validation-message="日期格式輸入錯誤"
            required
            expanded
          />
        </b-field>

        <b-field horizontal label="識別碼">
          <b-input
            name="birthday"
            pattern="CAPTCHA"
            validation-message="識別碼輸入錯誤"
            required
            expanded
          />
          <div class="field is-grouped">
            <figure class="image mr-3" style="width: 9rem">
              <img src="~/assets/images/img-validate.jpg">
            </figure>
            <button class="button is-rounded is-outlined is-info">
              重新發送
            </button>
          </div>
        </b-field>
      </section>

      <section class="container is-max-desktop section">
        <b-collapse class="card mb-3" :open="false" animation="slide">
          <template #trigger="props">
            <div class="card-header" role="button">
              <p class="card-header-title is-size-6">
                共同行銷條款
              </p>
              <a class="card-header-icon">
                <span :class="{'CUB-icon-menu': true, 'is-active': props.open}">&nbsp;</span>
              </a>
            </div>
          </template>

          <div class="card-content">
            <div class="content is-size-7">
              共同行銷條款
            </div>
          </div>
        </b-collapse>

        <b-field class="mb-6">
          <b-checkbox v-model="isChecked" type="is-info">
            本人已閱讀並同意上述共同行銷條款。
          </b-checkbox>
        </b-field>

        <div class="level increase_space">
          <div class="level-item">
            <input type="submit" value="確認送出" :disabled="!isChecked" class="button is-primary is-rounded CUB-wide-button">
          </div>
        </div>
      </section>
    </form>
  </article>
</template>

<script>
export default {
  name: 'SignUp',
  data () {
    return {
      isChecked: false
    }
  }
}
</script>

<style scroped>
/* to make it look similar to mock image */
.increase_space {
  margin-bottom: 50pt;
}
</style>
