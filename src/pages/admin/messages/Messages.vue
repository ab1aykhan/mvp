<template>
    <div class="messages">
        <div class="messages__inner">
            <div class="messages__header">
                <div class="messages-controls">
                    <va-icon name="fa-square-o"  class="messages-controls__icon" size="20px"/>
                    <va-icon name="archive" class="messages-controls__icon" size="20px"/>
                    <va-icon name="fa-trash"  class="messages-controls__icon" size="20px"/>
                </div>
            </div>
            <div class="messages__body">
                <aside class="messages__aside">
                    <va-list class="messages__list">
                        <template v-for="(customer, i) in customers" 
                                :key="'item' + customer.id"
                        >
                        <va-list-item clickable @click="notify(customer.name)" class="messages__list-item">
                            <va-list-item-section class="ml-2" avatar>
                                <va-avatar>
                                    <img :src="customer.picture" :alt="customer.name">
                                </va-avatar>
                                </va-list-item-section>
                                <va-list-item-section>
                                    <va-list-item-label>
                                        {{ customer.name }}
                                    </va-list-item-label>
                                    <va-list-item-label caption>
                                        {{ customer.address }}
                                </va-list-item-label>
                            </va-list-item-section>
                        </va-list-item>
                        <va-list-separator v-if="i < customers.length - 1" :key="'separator' + customer.id" />
                        </template>
                    </va-list>
                </aside>
                <div class="messages__content">
                    mail box
                </div>
            </div>
        </div>
    </div>
</template>
<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    setup() {
        const data = [
            {
              "id": "5d318282400cc272d72ff744",
              "starred": true,
              "balance": "$3,210.05",
              "picture": "https://randomuser.me/api/portraits/women/1.jpg",
              "age": 30,
              "name": "Marcia Neal",
              "gender": "female",
              "company": "BLUEGRAIN",
              "email": "marcianeal@bluegrain.com",
              "phone": "+1 (950) 575-2330",
              "address": "642 Overbaugh Place, Loretto, Rhode Island, 3756"
            },
            {
              "id": "5d318282da3af2a9bda573b7",
              "starred": false,
              "balance": "$3,961.47",
              "picture": "https://randomuser.me/api/portraits/women/2.jpg",
              "age": 21,
              "name": "Corrine Oliver",
              "gender": "female",
              "company": "QUALITERN",
              "email": "corrineoliver@qualitern.com",
              "phone": "+1 (955) 402-3254",
              "address": "532 Colin Place, Talpa, Connecticut, 7461"
            },
            {
              "id": "5d31828232ea44346bd45ee9",
              "starred": true,
              "balance": "$1,874.06",
              "picture": "https://randomuser.me/api/portraits/men/1.jpg",
              "age": 27,
              "name": "Tucker Kaufman",
              "gender": "male",
              "company": "PREMIANT",
              "email": "tuckerkaufman@premiant.com",
              "phone": "+1 (954) 475-2928",
              "address": "887 Winthrop Street, Tryon, Florida, 3912"
            },
            {
              "id": "5d3182822ebdb5c989bb3364",
              "starred": false,
              "balance": "$1,797.76",
              "picture": "https://randomuser.me/api/portraits/women/3.jpg",
              "age": 32,
              "name": "Daisy Kramer",
              "gender": "female",
              "company": "ORBIN",
              "email": "daisykramer@orbin.com",
              "phone": "+1 (858) 416-3088",
              "address": "821 Louise Terrace, Waterview, Indiana, 6960"
            },
            {
              "id": "5d318282e1e716000b687943",
              "starred": false,
              "balance": "$2,538.94",
              "picture": "https://randomuser.me/api/portraits/women/4.jpg",
              "age": 26,
              "name": "Mindy Potts",
              "gender": "female",
              "company": "SNACKTION",
              "email": "mindypotts@snacktion.com",
              "phone": "+1 (835) 508-2695",
              "address": "418 Broadway , Whitehaven, New York, 7690"
            },
            {
              "id": "5d318282a9a4a59adf96cdd0",
              "starred": false,
              "balance": "$3,143.43",
              "picture": "https://randomuser.me/api/portraits/men/2.jpg",
              "age": 35,
              "name": "Dotson Franks",
              "gender": "male",
              "company": "SATIANCE",
              "email": "dotsonfranks@satiance.com",
              "phone": "+1 (869) 559-3971",
              "address": "156 Lyme Avenue, Lupton, California, 1221"
            },
            {
              "id": "5d3182823227c20aabc4993f",
              "starred": false,
              "balance": "$2,601.91",
              "picture": "https://randomuser.me/api/portraits/women/5.jpg",
              "age": 29,
              "name": "Audrey Clay",
              "gender": "female",
              "company": "MIRACLIS",
              "email": "audreyclay@miraclis.com",
              "phone": "+1 (860) 565-2697",
              "address": "644 Vermont Court, Freelandville, Kentucky, 2619"
            },
            {
              "id": "5d318282b5127412e1761466",
              "starred": false,
              "balance": "$1,718.36",
              "picture": "https://randomuser.me/api/portraits/men/3.jpg",
              "age": 37,
              "name": "Aguirre Klein",
              "gender": "male",
              "company": "CALCU",
              "email": "aguirreklein@calcu.com",
              "phone": "+1 (924) 555-3247",
              "address": "626 Carroll Street, Roulette, Ohio, 1477"
            }
        ]
        return {
            customers: data.slice(0, 5),
        }
    },
})
</script>

<style lang="scss">
.messages {
    height:100%;
    &__body{
        display: flex;
    }
    *{
        border-radius: 5px;
    }
    &__header{
        padding: 10px 13px;
        background-color: #ffffff;
        margin-bottom: 10px;
        display: flex;
        align-items: center;
    }
    &__aside{
        background-color: #ffffff;
        flex: 1;
        margin-right: 10px;
    }
    &__content{
        background-color: #ffffff;
        flex: 2;
        padding: 5px;
    }
    &__list-item{
        cursor: pointer;
    }
}
.messages-controls{
    display: flex;
    &__icon{
        margin-right: 15px;
    }
}
</style>