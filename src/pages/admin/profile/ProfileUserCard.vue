<template>
    <div class="profile-card">
        <div class="profile-card__inner">
            <div class="profile-card__img">
                <img src="https://upload.wikimedia.org/wikipedia/commons/8/89/Portrait_Placeholder.png" alt="" srcset="">
            </div>
            <div class="profile-card__info">
                <h2 class="profile-card__name">Name Surname</h2>
                <div class="profile-card__id">Student ID </div>
                <div class="profile-card__projects">2 Project</div>
            </div>
        </div>
    </div>
</template>
<style lang="scss" scoped>
.profile-card{
    &__inner{
        display: flex;
    }
    &__info{
        display: flex;
        flex-direction: column;
        justify-content: center;
    }
    &__img{
        margin-right: 50px;
        img{
            height: 200px;
            width: 200px;
        }
    }
    &__name{
        font-weight: 500;
        font-size: 24px;
        line-height: 28px;
        margin-bottom: 10px;
    }
    &__id{
        font-weight: 500;
        font-size: 15px;
        line-height: 18px;
        margin-bottom: 10px;
    }
}
</style>