<template>
  <footer class="footer">
    <div class="container">
      <div class="footer-content">
        <div class="left">
          <div class="left-line">
            <strong>链接</strong>
            <a target="_blank" rel="external nofollow" href="https://github.com/daker-china">
              <i class="iconfont icon-github"/>
              </i>
            </a>
            <a rel="external nofollow" href="mailto:daker.zhou@gmail.com">
              <i class="iconfont icon-mail"/>
            </a>
          </div>
          <div class="left-line">
            <strong>备案</strong>
            <a target="_blank" rel="external nofollow" href="http://www.miitbeian.gov.cn/">
              <span class="content">{{globalOption.site_icp}}</span>
            </a>
          </div>
          <div class="left-line">
            <strong><img src="/gov.png" style="vertical-align: sub; width: 16px; height: 16px; display: inline-block"/> 粤公网安备</strong>
            <a target="_blank" rel="external nofollow" href="http://www.beian.gov.cn/portal/registerSystemInfo?recordcode=44030502002101">
              <span class="content">44030502002101号</span>
            </a>
          </div>
        </div>
        <div class="right">
          <div class="right-line">
          <span>© 2018 ❤
            <a target="_blank" rel="external nofollow" href="https://daker.xin/">DakerZhou</a> |
            <a target="_blank" rel="external nofollow" href="https://api.daker.xin/sitemap.xml">sitemap</a>
          </span>
          </div>
          <div class="right-line">
            <i>做最坏的打算，做最多的努力</i>
          </div>
          <div class="right-line">
            <i>POWERED BY <a href="/project">NUXT.JS</a> AND SOLITARILY.   DESIGNED BY
              <a href="/about">ME</a></i>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
  export default {
    name: 'Footer',
    computed: {
      globalOption() {
        return this.$store.state.option.globalOption.data
      }
    },
  }
</script>

<style lang="scss" scoped>
  footer {
    margin-top: 1em;
    background-color: $module-bg;
    .footer-content {
      display: flex;
      font-size: .9em;
      justify-content: space-between;
      text-transform: uppercase;
      .left {
        .left-line {
          text-align: left;
          height: 2em;
          line-height: 2em;
          i, .content {
            display: inline-block;
            margin-left: 1em;
            font-size: .9em;
          }
        }
      }
      .right {
        .right-line {
          text-align: right;
          height: 2em;
          line-height: 2em;
        }
      }
    }
    @media screen and (max-width: 640px) {
      .footer-content {
          width: 100%;
          display: block;
          .left {
            .left-line {
              text-align: center;
            }
          }
          .right {
            .right-line {
              text-align: center;
            }
          }
        }
    }
  }
</style>