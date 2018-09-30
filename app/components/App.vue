<template>
    <Page>
        <ActionBar title="Welcome to NativeScript-Vue!"/>
		<GridLayout rows="*, auto">
    <StackLayout row="0">
			<button text="show Feed" col="0" row="0" @tap="showFeed" style="width:200 ; height : 50"></button>
    </StackLayout>
    <BottomNavigation activeColor="red"
                      inactiveColor="yellow"
                      backgroundColor="black"
                      keyLineColor="black"
                      @tabSelected="onBottomNavigationTabSelected"
                      row="1">
        <BottomNavigationTab title="First" icon="logo" />
        <BottomNavigationTab title="Second" icon="logo" />
        <BottomNavigationTab title="Third" icon="logo" />
    </BottomNavigation>
</GridLayout>
       
    </Page>
</template>

<script>
var FeedbackPlugin = require("nativescript-feedback");
var feedback = new FeedbackPlugin.Feedback();
  export default {
    data() {
      return {
        msg: 'Hello World!'
      }
    },
	methods: {
          showFeed(){
				feedback.show({
				  message: "Easiest thing ever, right?"
				});
          }
    }
	
  }
</script>

<style scoped>
    ActionBar {
        background-color: #53ba82;
        color: #ffffff;
    }

    .message {
        vertical-align: center;
        text-align: center;
        font-size: 20;
        color: #333333;
    }
</style>
