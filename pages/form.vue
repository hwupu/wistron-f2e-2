<template>
  <article class="CUB-signup">
    <aside class="CUB-signup-steps">
      a
    </aside>

    <section class="container is-max-desktop section">
      <b-field horizontal label="持卡人身分證後5碼" type="is-danger" message="身分證格式輸入錯誤">
        <b-input name="social_id" expanded />
      </b-field>

      <b-field horizontal label="開通的信用卡／ｉ刷金融卡卡號">
        <div class="field is-grouped">
          <b-input name="card1" expanded />
          <b-input name="card2" expanded />
          <b-input name="card3" expanded />
          <b-input name="card4" expanded />
        </div>
      </b-field>

      <b-field horizontal label="生日">
        <b-input name="birthday" expanded />
      </b-field>

      <b-field horizontal label="識別碼" type="is-danger" message="識別碼輸入錯誤">
        <b-input name="birthday" expanded />
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
        <b-checkbox type="is-info">
          本人已閱讀並同意上述共同行銷條款。
        </b-checkbox>
      </b-field>

      <div class="level increase_space">
        <div class="level-item">
          <a class="button is-primary is-rounded CUB-wide-button">
            確認送出
          </a>
        </div>
      </div>
    </section>
  </article>
</template>

<script>
export default {
  name: 'SignUp'
}
</script>

<style scroped>
/* to make it look similar to mock image */
.increase_space {
  margin-bottom: 50pt;
}
</style>
