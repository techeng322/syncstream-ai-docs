# Getting Started with SyncStream 🪄

## Getting started

- Documentation can be found here: [docs.syncstream.ai](https://docs.syncstream.ai)

```bash
npm install syncstream
# or
yarn add syncstream
```

```
import { OneTap, SyncstreamProvider } from "syncstream-ai";
import "syncstream-ai/dist/index.css";

const App = () => {
  return (
    <div
      style={{
        background: "black",
        width: "100vw",
        height: "100vh",
      }}
    >
      <SyncstreamProvider clientId="EXAMPLE_CLIENT_ID">
        <OneTap contextUri="spotify:artist:2hlmm7s2ICUX0LVIhVFlZQ" />
      </SyncstreamProvider>
    </div>
  );
};

export default App;

```
