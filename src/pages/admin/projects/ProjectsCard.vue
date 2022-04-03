<template>
  <div class="project-card">
    <div class="project-card__aside">
      <div class="project-card____aside">
        <img class="project-card__image" src="https://via.placeholder.com/300x150" alt="">
      </div>
    </div>
    <div class="project-card__header">
      <div class="project-card__title">Project name</div>
      <div class="project-card__subtitle">Instructor name</div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.project-card{
    width: 310px;
    border-radius:10px;
    &:hover{
        cursor: pointer;
    }
    &__image{
        width: 100%;
        height: 100%;
    }
    &__title{
        margin-bottom: 10px;
    }
    &__header{
        background-color: #fff;
        padding: 8px 16px 24px 16px;
    }
}
</style>