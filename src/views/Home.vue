<template>
  <div class="hero height-full">
    <Center>
      <span class="logo iconfont icon-steemconnect" />
      <h4 class="m-0">hivesigner</h4>
      <div class="mt-4 mb-7">
        <h1 class="mb-6">You're in control of your keys.</h1>
        <div class="columns mb-6 hide-sm">
          <div class="column one-half v-align-middle">
            <a
              :href="chromeExtensionUrl"
              target="_blank"
              class="d-block rounded-2 px-3 py-2 bg-primary text-white text-left"
            >
              <span class="iconfont icon-chrome float-right" />
              Download extension (coming soon)
            </a>
          </div>
          <div class="column one-half v-align-middle">
            <a
              :href="pkg.repository.url.replace('.git', '/releases')"
              target="_blank"
              class="d-block rounded-2 px-3 py-2 bg-primary text-white text-left"
            >
              <span class="iconfont icon-desktop-windows float-right" />
              Download Desktop app (coming soon)
            </a>
          </div>
        </div>
        <p>
          With HiveSigner, you're always in control of your private keys: we neither store nor have
          access to them.
        </p>
      </div>
      <Footer />
    </Center>
  </div>
</template>

<script>
import pkg from '@/../package.json';

const chromeExtensionUrl =
  'https://chrome.google.com/webstore/detail/hivesigner/ophihnhnfgcmhpbcennhppicomdeabip';

export default {
  data() {
    return {
      pkg,
      chromeExtensionUrl,
    };
  },
};
</script>

<style scoped lang="less">
.icon-chrome,
.icon-desktop-windows {
  font-size: 32px;
}
</style>
