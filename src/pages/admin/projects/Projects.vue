<template>
<div class="page projects-page">
    <div class="page__inner">
        <div class="page__header">
            <h3 class="projects-page__title">Projects</h3>
            <div class="projects-page__actions mt-3 pa-2">
                <div class="projects-page__views">
                    <va-icon name="glyphicon glyphicon-align-justify" size="20px" class="ma-1"/>
                    <va-icon name="glyphicon glyphicon-th-large" size="20px" class="ma-1"/>
                </div>
                <div class="projects-page__searchbox">
                    <va-input
                        placeholder="Search"
                    />
                </div>
                <div class="projects-page__filter"></div>
            </div>
        </div>
        <div class="page__body projects-page__body">
            <ProjectsCard class="projects-page__card" @click="go"/>
            <ProjectsCard class="projects-page__card"/>
            <ProjectsCard class="projects-page__card"/>
            <ProjectsCard class="projects-page__card"/>
            <ProjectsCard class="projects-page__card"/>
        </div>
    </div>
</div>
</template>

<script>
import ProjectsCard from './ProjectsCard.vue'
export default {
    components: {
        ProjectsCard
    },
    methods: {
        go(){
            this.$router.push({ name: 'project'})
        }
    }
}
</script>

<style lang="scss" scoped>
.page{
    &__body {
        padding-top:40px;
        display: flex;
        flex-wrap: wrap;
    }
}
.projects-page{
    &__card{
        margin: 0 20px 20px 0;
    }
    &__actions{
        border-radius: 5px;
        background-color: #fff;
        display: flex;
    }
    &__views{
        margin-right: 24px;
    }
}
</style>