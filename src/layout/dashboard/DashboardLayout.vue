<template>
  <div class="wrapper">
    <side-bar>
      <template slot="links">
        <sidebar-link
            to="/dashboard"
            :name="$t('sidebar.dashboard')"
            icon="tim-icons icon-chart-pie-36"
        />
        <sidebar-link
            to="/maps"
            :name="$t('sidebar.maps')"
            icon="tim-icons icon-pin"
        />
        <sidebar-link
            to="/notifications"
            :name="$t('sidebar.notifications')"
            icon="tim-icons icon-bell-55"
        />
        <sidebar-link
            to="/profile"
            :name="$t('sidebar.userProfile')"
            icon="tim-icons icon-single-02"
        />
        <sidebar-link
            to="/table-list"
            :name="$t('sidebar.tableList')"
            icon="tim-icons icon-puzzle-10"
        />
      </template>
    </side-bar>
    <div class="main-panel">
      <dashboard-content @click.native="toggleSidebar"></dashboard-content>
    </div>
  </div>
</template>
<style lang="scss"></style>
<script>
import DashboardContent from "./Content.vue";
export default {
  components: {
    DashboardContent,
  },
  methods: {
    toggleSidebar() {
      if (this.$sidebar.showSidebar) {
        this.$sidebar.displaySidebar(false);
      }
    },
  },
};
</script>
