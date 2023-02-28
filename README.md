# MintNFT Unity SDK

Minting your NFTs over the web and plugging APIs to mint it through your own DApps are all cool. What about being able to mint in-game NFTs directly from Unity? We have got you covered! Introducing our Unity SDK

## Implementation Steps

1. Download the contents from the repo
2. Open the project on Unity, preferably Unity 2021.3
3. There are 3 scene files namely "TestUpload", "TestMint" and "TestRefreshJWT" which you can use to test
4. The "TestUpload.cs", "TestMint.cs" and "TestRefreshJWT.cs" scripts can help you get started to write your own scripts
5. Main 3 methods in the "MintNFT.cs" class are "Upload", "Mint" and "RefreshJWT"

### Upload
```
string result = MintNFT.Upload(string APIKEY, List<IMultipartFormSection> formData);
```
### Mint
```
string result = MintNFT.Mint(string APIKEY, string JWT, string stringifiedJsonBody);
```
### Refresh JWT
```
string result = MintNFT.RefreshJWT(string APIKEY, string REFRESH_TOKEN, string stringifiedJsonBody);
```

To get the APIKEY, JWT and REFRESH_TOKEN a please go to API dashboard - https://app.0xmint.io/create/api

To check the formats of the formdata, json body, etc. please check our documentation here - https://docs.0xmint.io/

## External Feature Additions
This section will highlight all the third part SDKs or features added by community builders
### Unlock SDK
Easily add payments and NFTs to your Unity WebGL project - no coding necessary. Users can purchase NFTs to grant access to content, purchase in-game items, provide ad-free experiences, buy tickets to in-game events, and lots more!

You can use Unlock SDK features in two ways

1. If you are cloning this repository and using the project as is, the Unlock package will automatically be added to the project at the time of initialization. Then you can proceed by referring the official Unlock Unity SDK documentation(mentioned below).
2. If you are using the unitypackage from the releases, make sure that you add the Unlock package to your project. First, open the Package Manager by opening `Window/Package Manager`. Then click on the + button on the upper-left-hand corner of the Package Manager, select "Add package from git URL..." on the context menu, then paste the following: `https://github.com/thehen/unlock-unity-package.git?path=/Unlock%20Unity%20Package`

To continue implementing the Paywall functionality using Unlock protocol, refer the official package documentation here - [Link to Documentation](https://thehen.github.io/unlock-unity-package/getting-started.html)

## IMPORTANT
In v2 of the APIs, creating a custom contract from the API dashboard is mandatory.

WE ARE DEPRECATING V1 APIs AND SUGGEST THE USAGE OF ONLY V2 APIs!
