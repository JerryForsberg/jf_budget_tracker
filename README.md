# jf_budget_tracker

The budget tracker app is a progressive web app that allows the user to add and subtract funds from their budget, and keep track of the updated amount available.

The signifigance of making this a progressive web app, is that the user does not need to be online to use it, once it is installed. The tracker uses the following technologies to allow users the ability to track their funds while offline. 

Please view the deployed version of the app here: https://jf-budget-tracker.herokuapp.com/

Technologies: 
  - IndexDB : keeps a pending record of transactions that will be able to be sent to the database once the app is able to come back online. 
  - Cache storage: Caches the static files needed to for the app to run. Gets any available data requested from the API.
  - Web manifest: Tells the PWA what type of window to open(in this case it will be standalone) when the app is installed, as well as gives it the statrting page and the icons. 
  - Service worker: Sets up the static files to cache, and provides the logic for the 3 states of the service worker, which are install, activate, and fetch.
  - Javascript: In particular, the db.js file creates functionality for the indexdb and the pending collection to create and store transactions.
