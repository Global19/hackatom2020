<template>
  <div class="section starport-banner">
    <div class="text">
      <div
        class="text__overline tm-rf-1 tm-rf0-m-up tm-medium tm-lh-title tm-overline"
      >
        Starport
      </div>
      <div class="text__title tm-rf3 tm-bold tm-lh-title">
        Start hacking your own chain
      </div>
      <div class="text__btn-container">
        <tm-button
          to-link="external"
          href="https://github.com/tendermint/starport"
          background-color="linear-gradient(316.23deg, #38769B 0%, #A43E28 100%)"
          color="var(--white)"
          glow
          class="text__btn-container__btn"
          >Get started</tm-button
        >
        <tm-button
          to-link="external"
          href="https://www.youtube.com/watch?v=rmbPjCGDXek"
          color="var(--white)"
          variant="text"
          glow
          class="text__btn-container__btn tm-rf0 tm-lh-copy"
          ><span class="icon__left" aria-hidden="true">▶</span>Watch
          demo</tm-button
        >
      </div>
    </div>
  </div>
</template>

<style lang="stylus" scoped>
/deep/
.text__btn-container__btn
  margin-right var(--spacing-6)
  &:last-child
    margin-right 0

.starport-banner
  display grid
  grid-template-columns repeat(6, 1fr)
  grid-template-rows 1fr
  gap 0 var(--spacing-7)
  background url(/cards/starport-rocket.jpg), linear-gradient(180deg, #1D1D1D 0%, #2E2D2D 100%)
  background-repeat no-repeat
  background-size contain
  box-shadow var(--elevation-16)
  border-radius $border-radius-4
  center()

.text
  padding var(--spacing-8)
  grid-column 3 / span 6

  &__overline
    color var(--white-700)
    position relative

  &__title
    margin-top var(--spacing-3)
    color var(--white)
    position relative

.text__btn-container
  margin-top var(--spacing-8)
  max-width $max-width-6
  display flex
  flex-wrap wrap

.icon__left
  color var(--primary-600)

@media screen and (max-width: 768px)
  .starport-banner
    grid-template-columns 1fr

  .text
    padding var(--spacing-7)

@media screen and (max-width: 660px)
  .starport-banner
    max-width $max-width-7
    height 22rem
    background url(/cards/starport-rocket-small.jpg), linear-gradient(180deg, #1D1D1D 0%, #2E2D2D 100%)
    background-repeat no-repeat
    background-size contain

  .text
    grid-column unset
    grid-row 2
    padding var(--spacing-6)
    position relative
    &:before
      content ''
      position absolute
      top 0
      left 0
      right 0
      bottom 0
      border-radius $border-radius-4
      background linear-gradient(180deg, rgba(46, 45, 45, 0) 0%, #2E2D2D 39.9%)

  .text__btn-container__btn
    flex 1 0 auto
</style>
