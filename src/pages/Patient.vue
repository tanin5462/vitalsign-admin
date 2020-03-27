<template>
  <q-page>
    <div class="row color-white">
      <q-toolbar
        class="col-4 bg-primary-500 no-padding shadow-1"
        style="max-width:360px;width:100%;"
      >
        <q-toolbar-title>
          <q-btn flat dense="" size="20px">
            <q-icon name="chevron_left"></q-icon>
          </q-btn>
          <span clas>Title</span>
        </q-toolbar-title>
        <div class="q-pa-sm">
          <q-btn flat round dense icon="search" />
        </div>
      </q-toolbar>
      <!-- <q-separator vertical class="shadow-2" /> -->
      <q-toolbar class="col bg-primary-500 shadow-1"></q-toolbar>
    </div>
  </q-page>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped></style>
