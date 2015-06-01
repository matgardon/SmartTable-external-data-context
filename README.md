# SmartTable-external-data-context
A plugin for SmartTable to enable reloading the table on external data-context change, when using smart-table with the pipe() function.

It is only usefull if data is externally-loaded through a custom pipe function, in which case the call to ctrl.split() will trigger a re-fetch of the data from the server.

In case of a client side data-source, it does nothing and should not be used : simply re-fetch the data-source and update it accordingly.
