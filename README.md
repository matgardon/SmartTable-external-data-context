# SmartTable-external-data-context
A plugin for SmartTable to enable reloading the table on external data-context change, when using smart-table with the pipe() function.

### Usage
It is only usefull if data is externally-loaded through a custom pipe function, in which case the call to ctrl.split() will trigger a re-fetch of the data from the server (at page 1).

In case of a client side data-source, it does nothing and should not be used : simply re-fetch the data-source and update it accordingly.

Example code :

```HTML
<table class="table  table-striped" 
           st-pipe="searchQuoteVM.updateDisplayedQuotes" 
           st-table="searchQuoteVM.displayedQuotes"
           st-current-external-data-context="searchQuoteVM.currentUserVM.currentUserRole">
```

### Behavior
This directive will simply use the default angular comparison of scope.$watch() on the given parameter to check for a change, and trigger the reload accordingly.
