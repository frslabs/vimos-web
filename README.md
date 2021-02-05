# VIMOS WEB SDK

![version](https://img.shields.io/badge/version-v1.0.0-blue)

# Table Of Content
- [Quick Start](#quick-start)
- [Help](#help)

## Quick Start

Web SDK Integration

- Import [atlaskyc.js](https://github.com/frslabs/vimos-web/releases/download/v1.0.0/atlaskyc.js) script to your HTML file

```html
<script src="atlaskyc.js">
```

- Invoke AtlasKYC on a button click or on similar user input event

```html
<input type="button" onClick="openAtlasKYC()" value="AtlasKYC">
```

Method 1: To open AtlasKYC in a new window

```javascript
function openAtlasKYC(){
  let atlasKYC = new AtlasKYC({
    method: "window",
    onFinish: () => {
       // Callback function 
    }
  });
 
   atlasKYC.open(ATLAS_KYC_URL);

}
```

The onFinish function will be called once the KYC is done.

Method 2: To open AtlasKYC in an iframe

Create a DIV element like below

```html
<div class="atlas-kyc"></div>
```

```javascript
function openAtlasKYC(){
  let atlasKYC = new AtlasKYC({
    method: "iframe",
    containerClassName:"atlas-kyc",
    onFinish: () => {   
       // Callback function    
    }
  });

  atlasKYC.open(ATLAS_KYC_URL);
}
```

## Help
For any queries/feedback , contact us at `support@frslabs.com` 
