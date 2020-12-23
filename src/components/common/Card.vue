<template>
  <div class="card-wrapper">
    <img src="../../assets/image/sock.png" alt="" class="sock">
    <img src="../../assets/image/ring.png" alt="" class="ring">
    <div class="card-header" v-if="$slots.header">
      <slot name="header"></slot>
    </div>
    <div class="card-text">
      <slot></slot>
    </div>
  </div>
</template>

<style lang="stylus" rel="stylesheet/stylus" scoped>
.card-wrapper
  margin 25px 5px
  border-radius 5px
  border 1px solid #EBEEF5
  background-color rgba(27,63,45,.85);
  // overflow hidden
  color #303133
  transition box-shadow 0.25s
  position relative

  &:hover
    box-shadow 2px 2px 5px rgba(0, 0, 0, 0.1)

  .card-header
    border-bottom 1px solid #EBEEF5
    padding 5px

  .card-text
    padding 15px 10px

.ring,.sock
  position absolute
  width 60px
  top -20px
  right -30px
  -webkit-transform-origin top center
  -moz-transform-origin top center
  -o-transform-origin top center
  transform-origin top center
  animation swing 6s .15s linear infinite;
  -moz-animation swing 6s .15s linear infinite; /* Firefox */
  -webkit-animation swing 6s .15s linear infinite; /* Safari and Chrome */
  -o-animation swing 6s .15s linear infinite; /* Opera */

.sock{
  right unset
  left -20px
  width 50px
}

@-webkit-keyframes swing {
  10% {
    transform: rotate(15deg);
  }
  20% {
    transform: rotate(-10deg);
  }
  30% {
    transform: rotate(5deg);
  }
  40% {
    transform: rotate(-5deg);
  }
  50%,100% {
    transform: rotate(0deg);
  }
}
@-moz-keyframes swing {
  10% {
    transform: rotate(15deg);
  }
  20% {
    transform: rotate(-10deg);
  }
  30% {
    transform: rotate(5deg);
  }
  40% {
    transform: rotate(-5deg);
  }
  50%,100% {
    transform: rotate(0deg);
  }
}
@-o-keyframes swing {
  10% {
    transform: rotate(15deg);
  }
  20% {
    transform: rotate(-10deg);
  }
  30% {
    transform: rotate(5deg);
  }
  40% {
    transform: rotate(-5deg);
  }
  50%,100% {
    transform: rotate(0deg);
  }
}
@keyframes swing {
  10% {
    transform: rotate(15deg);
  }
  20% {
    transform: rotate(-10deg);
  }
  30% {
    transform: rotate(5deg);
  }
  40% {
    transform: rotate(-5deg);
  }
  50%,100% {
    transform: rotate(0deg);
  }
}

</style>
