---
title: Use Middleware to Handle Asynchronous Actions
---
## Use Middleware to Handle Asynchronous Actions

`
const handleAsync = () => {
  return function(dispatch) {
    // dispatch request action here
    dispatch(requestingData());

    setTimeout(function() {
      let data = {
        users: ['Jeff', 'William', 'Alice']
      }
      // dispatch received data action here
      dispatch(receivedData(data));
    }, 2500);
  }
};

`
