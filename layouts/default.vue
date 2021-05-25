<template>
  <div>
    <header class="CUB-header">
      立即購
    </header>
    <article class="container">
      <nuxt />
    </article>
    <footer class="CUB-footer">
      <aside>
        <div class="CUB-footer-slogan">
          謹慎理財 信用無價
        </div>
        <div class="CUB-footer-description">
          信用卡暨預借現金之各級別循環信用年利率為6.75％~15％（依本行信用評分制度定期評估，循環利率之基準日為104年9月1日）。
          <span class="CUB-nobreak">預借現金手續費：</span>預借現金金額乘以3％加上新臺幣150元或美元5元，其他相關費用係依本行網站公告。
        </div>
      </aside>
      <div class="CUB-footer-legal">
        &copy;&nbsp;國泰世華商業銀行股份有限公司
      </div>
    </footer>
    <a class="CUB-scroll-top" @click="scrollTop()">往上滑</a>
  </div>
</template>

<script>
export default {
  methods: {
    scrollTop () {
      document.body.scrollTop = 0
      document.documentElement.scrollTop = 0
    }
  }
}
</script>
