<template>
  <transition name="fade" appear>
    <div class="index">
      <voice />
      <!-- <card>
        <div style="text-align: center">
          {{ t(INFO_I18N.voiceTotalTip) }}: {{ t(INFO_I18N.voiceTotal) }}
        </div>
      </card> -->
    </div>
  </transition>
</template>

<script lang="ts">
import { useI18n } from 'vue-i18n'
import { INFO_I18N } from '@/assets/script/option'
import Voice from '@/components/Voice.vue'

export default {
  components: {
    Voice
  },
  setup() {
    const { t } = useI18n()

    return {
      t,
      INFO_I18N
    }
  }
}
</script>

<style lang="stylus" scoped>
a
  margin 0 5px

.index
  margin 0 auto
  width 90%

  .content
    display flex
    flex-wrap wrap

    .btn
      margin 5px
      transition background 0.2s

@media only screen and (max-width 600px)
  .index
    width 95%

@media only screen and (max-width 768px)
  .index
    overflow hidden
</style>
