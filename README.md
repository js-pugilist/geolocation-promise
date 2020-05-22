
# Geolocation-promise

Too many we find ourselves unable to use javascript's geolocation API as promise. This package fixes that, geolocation's **`getCurrentPosition`** 
is implemented using promise and user can use function : **`getCurrentPositionPromise`** which returns a promise.


# Installation

    npm i geolocation-promise

> requires browser environment as it uses **navigator**

# Usage
## getCurrentPositionPromise

    import { getCurrentPositionPromise } = require('geolocation-promise');
    
    getCurrentPositionPromise()
	    .then((position) => {
		    console.log(position); 
	    })
	    .catch(e => console.log(e));
OR use async/await

    import { getCurrentPositionPromise } = require('geolocation-promise');
    
    try{
	    const position = await getCurrentPositionPromise();
	    console.log(position);
	}catch(e){
		console.log(e);
	}

> Incase of error promise gets rejected with an object like this: 

    { error: ERROR_INFORMATION_STRING }

# Parameters
While using getCurrentPositionPromise() user can pass option object in the function.

    const  options = {
	    enableHighAccuracy: false,//default
	    timeout: 5000,//default (milliseconds)
	    maximumAge: 10000 //default (milliseconds)
    }
# Suggestions/ Feedback
For any suggestions or feedback ping me on : [Abhishek Singh (Gmail)](mailto:abesingh1@gmail.com)