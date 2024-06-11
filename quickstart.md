# Quickstart

The Syncstream-ai is the easiest way to onboard your users to web3 in your React App.\


## 0. Prerequsites

In order to integrate the [**syncstream-ai**](https://www.npmjs.com/package/syncstream-ai), your project must be on:

* a [**minimum React version of 18**](https://github.com/facebook/react/blob/main/CHANGELOG.md#1800-march-29-2022)
* a [**minimum TypeScript version of 5**](https://github.com/microsoft/TypeScript/releases/tag/v5.0.2)

## 1. Installation[​](https://docs.privy.io/guide/react/quickstart#\_1-installation) <a href="#id-1-installation" id="id-1-installation"></a>

{% tabs %}
{% tab title="npm" %}
npm install syncstream-ai
{% endtab %}

{% tab title="yarn" %}
yarn add syncstream-ai
{% endtab %}
{% endtabs %}

## 2. Set up your app with syncstream-ai

Once you install package, import the SyncstreamProvider component into your project, and wrap your app with it.

Concretely, the SyncstreamProvider must wrap any component or page that will use the syncstream-ai. It is generally recommended to render it as close to the root of your application as possible.



For example, in a [NextJS](https://nextjs.org/) or [Create React App](https://create-react-app.dev/) project, you may wrap your components like so:

{% tabs %}
{% tab title="NextJS" %}
```tsx
'use client';

import { OneTap, SyncstreamProvider } from "syncstream-ai";
import "syncstream-ai/dist/index.css";

export default function App() {
  return (
    <SyncstreamProvider
      clientId="EXAMPLE_CLIENT_ID"
    >
      <OneTap contextUri="spotify:artist:2hlmm7s2ICUX0LVIhVFlZQ" />
    </SyncstreamProvider>
  );
}
```
{% endtab %}

{% tab title="Create React App" %}
```tsx
import React from 'react';
import { OneTap, SyncstreamProvider } from "syncstream-ai";
import "syncstream-ai/dist/index.css";

export default function App() {
  return (
    <SyncstreamProvider
      clientId="EXAMPLE_CLIENT_ID"
    >
      <OneTap contextUri="spotify:artist:2hlmm7s2ICUX0LVIhVFlZQ" />
    </SyncstreamProvider>
  );
}
```
{% endtab %}
{% endtabs %}

In the examples above, notice that the `SyncstreamProvider` component takes one property:

| Property   | Description                   |
| ---------- | ----------------------------- |
| `clientId` | (Required) your app clientID. |



In the examples above, notice that the `OneTap` component takes 2 properties:\
Please refer to the [Spotify documentation](https://developer.spotify.com/documentation/web-api/reference/start-a-users-playback) to learn more about this.

| Property   | Description                                                                                                                                                                     |
| ---------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| contextUri | <p>Optional. Spotify URI of the context to play. Valid contexts are albums, artists &#x26; playlists. <code>{context_uri:"spotify:album:1Je1IMUlBXcx1Fz0WE7oPT"}</code><br></p> |
| uris       | Optional. A JSON array of the Spotify track URIs to play. For example: `{"uris": ["spotify:track:4iV5W9uYEdYUVa79Axb7Rh", "spotify:track:1301WleyT98MSxVHPZCA6M"]}`             |

## 3. Just `use syncstream-ai`! 🎉[​](https://docs.privy.io/guide/react/quickstart#\_4-just-useprivy-%F0%9F%8E%89) <a href="#id-4-just-useprivy" id="id-4-just-useprivy"></a>

Once you've wrapped your app with the SyncstreamProvider, you can now use the it throughout your components and pages via the `OneTap`!

