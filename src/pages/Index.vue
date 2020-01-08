<template>
  <q-page class="flex flex-center">
    <div class="q-pa-md">
      <q-layout view="hhh LpR lff" container style="height: 600px; width: 800px;" class="shadow-2 rounded-borders">
        <q-header reveal :style="uccolor">
          <q-toolbar>
            <q-toolbar-title>Telephony Bar</q-toolbar-title>
              <div v-for="item in buttons" :key="item" class="caption">
                <q-btn :label="item" />
              </div>
          </q-toolbar>
        </q-header>
        <q-page-container>
          <q-page class="q-pa-md">
            <div class="row">
              <div class="col-4">
                <q-list bordered style="height:505px; width:250px;">
                  <q-item v-ripple>
                    <q-item-section>
                      <q-item-label>GUS GUS GUS GUS GUS GUS GUS GUS ...</q-item-label>
                    </q-item-section>
                  </q-item>
                </q-list>
              </div>
              <div class="col-8" style="padding-left: 5px;">
                <div class="row">
                  <div class="col-3">
                    <q-avatar rounded size="100px" font-size="82px" color="teal" text-color="white">
                      J
                    </q-avatar>
                  </div>
                  <div class="col-9">
                    <q-list bordered separator>
                      <q-item v-ripple>
                        <q-item-section>Customer Info</q-item-section>
                      </q-item>
                      <q-item v-ripple>
                        <q-item-section>
                          <q-item-label>Customer Info</q-item-label>
                        </q-item-section>
                      </q-item>
                    </q-list>
                  </div>
                </div>
                <div class="row">
                  <q-list bordered style="height:400px; width:550px; margin-top:5px;">
                    <q-item clickable v-ripple>
                      <q-item-section>
                        <q-item-label>Business Panel</q-item-label>
                      </q-item-section>
                    </q-item>
                  </q-list>
                </div>
              </div>
            </div>
          </q-page>
        </q-page-container>
      </q-layout>
    </div>
  </q-page>
</template>

<script>
export default {
  name: 'Index',
  data () {
    return {
      buttons: []
    }
  },
  mounted: function () {
    this.buttons = ['CALL', 'ON-HOLD', 'CANCEL']
    // this.uccolor = 'pink'
  },
  methods: {
    getColor () {
      return 'purple'
    }
  },
  computed: {
    uccolor () {
      return {
        background: this.getColor()
      }
    }
  }
}
</script>
