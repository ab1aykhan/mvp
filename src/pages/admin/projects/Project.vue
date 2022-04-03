<template>
  <div class="page project-page">
    <div class="project-page__inner">
      <div class="project-page__header pa-2">
        <div>
          <div class="ml-3">
            <b>Project Name</b>
          </div>
          <div>
            <va-tabs v-model="activeTabName">
              <template #tabs>
                <va-tab name="OverviewTab">
                  Home
                </va-tab>
                <va-tab name="BillingAddressTab">
                  Tasks
                </va-tab>
                <va-tab name="BankDetailsTab">
                  Discussions
                </va-tab>
                <va-tab name="BankDetailsTab">
                  Docs
                </va-tab>
              </template>
            </va-tabs>
          </div>
        </div>
      </div>
      <div class="project-page__body">
        <div class="project-page__card">
          <va-card class="mb-4">
            <va-list-label >
              <h1 style="font-size: 22px">Tasks</h1>
            </va-list-label>
            <va-list-item>
              <va-checkbox class="mr-2" v-model="appBanners" />
              <va-list-item-section>
                <va-list-item-lab>
                  Task’s name
                </va-list-item-lab>
                <va-list-item-label caption>
                  You can send invitations via email or any messenger.
                </va-list-item-label>
              </va-list-item-section>
            </va-list-item>
            <va-list-item>
              <va-checkbox class="mr-2" v-model="appBanners" />
              <va-list-item-section>
                <va-list-item-lab>
                  Task’s name
                </va-list-item-lab>
                <va-list-item-label caption>
                  You can send invitations via email or any messenger.
                </va-list-item-label>
              </va-list-item-section>
            </va-list-item>
            <va-list-item>
              <va-checkbox class="mr-2" v-model="appBanners" />
              <va-list-item-section>
                <va-list-item-lab>
                  Task’s name
                </va-list-item-lab>
                <va-list-item-label caption>
                  You can send invitations via email or any messenger.
                </va-list-item-label>
              </va-list-item-section>
            </va-list-item>
          </va-card>
        </div>
        <div class="project-page__card">
          <va-card class="mb-4">
            <va-list>
              <va-list-label>
                <h1 style="font-size: 22px">Docs</h1>
              </va-list-label>
              <va-list-item class="ml-2" clickable>
                <va-list-item-section>
                  <va-list-item-label>
                    Document #1 
                  </va-list-item-label>   
                  <va-list-item-label caption>
                    Instructor
                  </va-list-item-label>
                </va-list-item-section>
              </va-list-item>
              <va-list-item class="ml-2" clickable>
                <va-list-item-section>
                  <va-list-item-label>
                    Document #2 
                  </va-list-item-label>   
                  <va-list-item-label caption>
                    Instructor
                  </va-list-item-label>
                </va-list-item-section>
              </va-list-item>
              <va-list-item class="ml-2" clickable>
                <va-list-item-section>
                  <va-list-item-label>
                    Document #3
                  </va-list-item-label>   
                  <va-list-item-label caption>
                    Instructor
                  </va-list-item-label>
                </va-list-item-section>
              </va-list-item>
            </va-list>
          </va-card>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.project-page{
    &__header{
        background-color: #fff;
    }
    &__body{
        padding-top: 40px;
        display: flex;
        justify-content:space-around;
    }
    &__card{
        width: 520px;
    }
}
</style>