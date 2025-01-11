# Expo Linking Background Deep Link Issue

This repository demonstrates a bug in Expo's `Linking` API where deep link events are not consistently triggered when the app is in the background. The `backgroundLinkBug.js` file showcases the problem, and `backgroundLinkSolution.js` offers a potential workaround.  The issue primarily revolves around the unreliability of `Linking.addEventListener` in background situations.

## Reproducing the Bug

1. Run `backgroundLinkBug.js` using Expo Go.
2. Minimize the app or send it to the background.
3. Open a deep link intended for your app.
4. Observe that the app does not react to the deep link as expected.

## Potential Solution

`backgroundLinkSolution.js` presents a possible solution leveraging the Expo `AppLoading` and asynchronous handling of initial deep link retrieval.  This approach attempts to catch the link during app initialization.

**Note:** This workaround is not a guaranteed fix. The root cause lies within the Expo `Linking` API's behavior, and a more robust solution might require changes on the Expo side or using an alternative deep-linking library.