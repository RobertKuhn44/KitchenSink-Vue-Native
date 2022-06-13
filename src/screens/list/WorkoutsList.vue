<template>
  <nb-container :style="{ backgroundColor: '#fff' }">
    <nb-header>
      <nb-left>
        <nb-button transparent :onPress="() => this.props.navigation.goBack()">
          <nb-icon name="arrow-back" />
        </nb-button>
      </nb-left>
      <nb-body>
        <nb-title>Workout Programs</nb-title>
      </nb-body>
      <nb-right />
    </nb-header>
    <nb-content padder>
      <nb-list>
        <nb-list-item v-for="item in listItemArr" :key="item">
          <nb-left>
            <nb-text>
              {{ item }}
            </nb-text>
          </nb-left>
          <nb-right>
            <nb-icon name="arrow-forward"></nb-icon>
          </nb-right>
        </nb-list-item>
      </nb-list>
    </nb-content>
  </nb-container>
</template>

<script>
export default {
  data() {
    return {
      listItemArr: [
        "LEG1-PUSH1-PULL1-LEG2-PUSH2-PULL2-CARDIO",
        "LEG1-CARDIO-PUSH-CARDIO-PULL-CARDIO-REST",
        "LEG1-PUSH1-PULL1-CARDIO-LEG2-PUSH2-PULL2-CARDIO",
        "UPPER-LOWER-CARDIO",
        "BRO PLAN",
        "CUSTOM-FULLBODY",
        "UPPER-LOWER",
        "UPPER1-LOWER1-CARDIO-UPPER2-LOWER2-CARDIO-REST"
      ]
    };
  }
};
</script>
