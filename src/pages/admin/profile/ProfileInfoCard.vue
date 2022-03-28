<template>
    <div class="profile-info-card">
        <h1 class="profile-info-card__title">Project Name Information</h1>
        <div class="profile-info-card__table">
            <div class="profile-info-card__table-row">
                <div class="profile-info-card__table-col profile-info-card__table-title">Instructor</div>
                <div class="profile-info-card__table-col">Name Surname</div>
            </div>
            <div class="profile-info-card__table-row">
                <div class="profile-info-card__table-col profile-info-card__table-title">Email Address</div>
                <div class="profile-info-card__table-col">example@mail.ru</div>
            </div>
            <div class="profile-info-card__table-row">
                <div class="profile-info-card__table-col profile-info-card__table-title">Work duration</div>
                <div class="profile-info-card__table-col">6 Sep - 18 Dec</div>
            </div>
        </div>
    </div>
</template>
<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    setup() {
        
    },
})
</script>
<style lang="scss" scoped>
.profile-info-card{
    &__title{
        font-weight: 500;
        font-size: 20px;
        line-height: 23px;
        margin-bottom: 16px;
    }
    &__table{
        width: 373px;
        border: 1px solid #AAA6A6;
        &-title{
            font-weight: 600;
            font-size: 15px;
            color: #000000;
        }
        &-col{
            flex: 1;
            padding: 18px 20px;
        }
        &-row{
            display: flex;
            border-bottom: 1px solid #AAA6A6;
            &:last-child{
                border-bottom: none;
            }
        }
    }
}
</style>
