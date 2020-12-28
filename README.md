# ai-704

this is a repro for https://github.com/microsoft/ApplicationInsights-node.js/issues/704

commits are the same as in original issue description, e.g.:

- `ng new` [4b019e1](https://github.com/mac2000/ai-704/commit/4b019e1)
- add some api calls [ba7d369](https://github.com/mac2000/ai-704/commit/ba7d369)
- `ng add @nguniversal/express-engine` [7ec12cc](https://github.com/mac2000/ai-704/commit/7ec12cc)
- add and configure appinsights [7c110aa](https://github.com/mac2000/ai-704/commit/7c110aa)

for test:

```bash
git clone https://github.com/mac2000/ai-704
cd ai-704
npm install
export APPINSIGHTS_INSTRUMENTATIONKEY=your-instumentation-key
npm run dev:ssr
open localhost:4200
```

after a while you shold see both requests and dependencies in appinsights portal, but because dependencies have no correlation they wont be attached to requests
