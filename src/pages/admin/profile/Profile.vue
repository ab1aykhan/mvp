<template>
    <div>
        <div class="xs12 mb-5 px-auto">
            <ProfileUserCard />
        </div>
        <div class="xs12">
            <ProfileInfoCard />
        </div>
    </div>
</template>
<script lang="ts">
import { defineComponent } from 'vue'
import ProfileUserCard from './ProfileUserCard.vue'
import ProfileInfoCard from './ProfileInfoCard.vue'


export default defineComponent({
    components: {ProfileUserCard, ProfileInfoCard},
    setup() {
        
    },
})
</script>
<style lang="scss">

</style>