<template>
  <Page>
    <ActionBar>
      <Label text="Home"/>
    </ActionBar>
    <MDBottomNavigation selectedIndex="0">
      <MDTabContentItem style="background-color: yellow">
        <GridLayout><Label text="1" @tap="navigate"></Label></GridLayout>
      </MDTabContentItem>
      <MDTabContentItem>
        <Label text="2"></Label>
      </MDTabContentItem>
    </MDBottomNavigation>

  </Page>
</template>

<script>
import NavigateChild from "~/components/NavigateChild";

export default {
  methods: {
    navigate() {
      this.$navigateTo(NavigateChild)
    }
  }
};
</script>

<style scoped lang="scss">
@import '@nativescript/theme/scss/variables/blue';

// Custom styles
.fas {
  @include colorize($color: accent);
}

.info {
  font-size: 20;
  horizontal-align: center;
  vertical-align: center;
}
</style>
