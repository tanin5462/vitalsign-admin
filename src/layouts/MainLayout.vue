<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar class="col-4 bg-primary-500 shadow-1">
        <q-toolbar-title>Title</q-toolbar-title>
        <q-btn flat round dense icon="search" />
        <q-space />
      </q-toolbar>
      <q-toolbar class="col bg-primary-500 shadow-1">
        <q-toolbar-title>Title</q-toolbar-title>
        <q-btn flat round dense icon="search" />
        <q-space />
      </q-toolbar>
    </q-header>

    <q-drawer
      v-model="drawer"
      show-if-above
      :width="70"
      :breakpoint="500"
      content-class="bg-black"
    >
      <q-scroll-area class="fit ">
        <q-list padding>
          <q-item class="color-white q-py-md" clickable v-ripple>
            <q-item-section>
              <div align="center">
                <q-icon name="inbox" size="26px" />
                <br />
                <span>name</span>
              </div>
            </q-item-section>
          </q-item>

          <q-item class="color-white q-py-md" clickable v-ripple>
            <q-item-section>
              <div align="center">
                <q-icon name="inbox" size="26px" />
                <br />
                <span>name</span>
              </div>
            </q-item-section>
          </q-item>

          <q-item class="color-white q-py-md" clickable v-ripple>
            <q-item-section>
              <div align="center">
                <q-icon name="inbox" size="26px" />
                <br />
                <span>name</span>
              </div>
            </q-item-section>
          </q-item>

          <q-separator />

          <q-item class="color-white q-py-md" clickable v-ripple>
            <q-item-section>
              <div align="center">
                <q-icon name="inbox" size="26px" />
                <br />
                <span>name</span>
              </div>
            </q-item-section>
          </q-item>
        </q-list>
      </q-scroll-area>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import EssentialLink from "components/EssentialLink";

export default {
  name: "MainLayout",
  data() {
    return {
      drawer: false,
      miniState: true,
      leftDrawerOpen: false
    };
  },
  methods: {
    drawerClick(e) {
      // if in "mini" state and user
      // click on drawer, we switch it to "normal" mode
      if (this.miniState) {
        this.miniState = false;

        // notice we have registered an event with capture flag;
        // we need to stop further propagation as this click is
        // intended for switching drawer to "normal" mode only
        e.stopPropagation();
      }
    }
  },
  components: {
    EssentialLink
  }
};
</script>
