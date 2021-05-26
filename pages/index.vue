<template>
  <article>
    <section class="CUB-banner">
      <div class="container is-max-desktop section content">
        <h3>立即購</h3>
        <p class="is-hidden-mobile">
          不必輸入信用卡資料<br>不必輸入寄送地址
        </p>
      </div>
    </section>
    <section class="container is-max-desktop section">
      <p class="has-text-weight-medium">
        立即夠快捷支付，登錄開通好康多！
      </p>
      <ol class="CUB-flex">
        <li>
          <figure class="image is-128x128">
            <img src="~/assets/images/prepare-paper.png" alt="國泰世華銀行登錄立即購服務">
          </figure>
          <div class="CUB-flex-steps">
            Step 1
          </div>
          <div>
            國泰世華銀行登錄立即購服務
          </div>
        </li>
        <li class="CUB-flex-arrow">
          &gt;
        </li>
        <li>
          <figure class="image is-128x128">
            <img src="~/assets/images/upload-success-pc.png" alt="TreeMail 開通立即購服務">
          </figure>
          <div class="CUB-flex-steps">
            Step 2
          </div>
          <div>
            TreeMail 開通立即購服務
          </div>
        </li>
        <li class="CUB-flex-arrow">
          &gt;
        </li>
        <li>
          <figure class="image is-128x128">
            <img src="~/assets/images/shopping-bag.png" alt="TreeMail 開始使用立即購服務">
          </figure>
          <div class="CUB-flex-steps">
            Step 3
          </div>
          <div>
            TreeMail 開始使用立即購服務
          </div>
        </li>
      </ol>
      <div class="level increase_space">
        <div class="level-item">
          <NuxtLink to="/form" class="button is-primary is-rounded CUB-wide-button">
            立即購服務登錄
          </NuxtLink>
        </div>
      </div>
    </section>
  </article>
</template>

<script>
export default {
  name: 'HomePage'
}
</script>

<style scroped>
/* to make it look similar to mock image */
.increase_space {
  margin-bottom: 80pt;
}
</style>
