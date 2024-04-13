import { TonConnectServer, AuthRequestTypes } from '@tonapps/tonconnect-server';

// Create a TonConnectServer instance configured with a static secret.
const tonconnect = new TonConnectServer({ 
    staticSecret: process.env.TONCONNECT_SECRET 
});

// When we need to authenticate the user, create an authentication request:
const request = tonconnect.createRequest({
    image_url: 'https://ddejfvww7sqtk.cloudfront.net/images/landing/ton-nft-tegro-dog/avatar/image_d0315e1461.jpg',
    callback_url: `${hostname}/tonconnect`,
    items: [{
        type: AuthRequestTypes.ADDRESS,
        required: true
    }, {
        type: AuthRequestTypes.OWNERSHIP,
        required: true
    }],
});


res.send(request);
 
// Example: Tonkeeper deeplink:
// Provide the user with the URL to download that request.
const requestURL = `example.com/myrequest`;
const deeplinkURL = `https://app.tonkeeper.com/ton-login/${requestURL}`;
