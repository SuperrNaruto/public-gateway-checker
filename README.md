# IPFS Public Gateway Checker

**A site displaying public IPFS gateways and their online/offline status.**

View the Public Gateway Checker in action

* on GitHub Pages: https://ipfs.github.io/public-gateway-checker/

[![Screenshot of Public Gateway Checker](https://user-images.githubusercontent.com/157609/121263486-f7fb2800-c8b5-11eb-9061-0b6f586a6f25.png)](https://ipfs.github.io/public-gateway-checker/)

## SECURITY NOTES

- The list contains gateways operated by various parties, coordinated by loose mutual consensus, without a central governing authority. Protocol Labs operates and is responsible for only two of the listed gateways: `ipfs.io` and `dweb.link`.
- Gateways without origin isolation will be marked with ⚠️, indicating they are not safe for use cases that require private local storage of data or credentials. [Learn more](https://github.com/ipfs/public-gateway-checker/issues/150).

## Adding a new public gateway

If you'd like to add a new public gateway, please edit `./gateways.json`:

1. Add the gateway's address to the **top** of the list
2. If you care about security of websites loaded via your gateway, make sure it is set up as a [subdomain gateway](https://docs.ipfs.io/how-to/address-ipfs-on-web/#subdomain-gateway). See [config docs](https://github.com/ipfs/go-ipfs/blob/master/docs/config.md#gatewaypublicgateways) and [recipes](https://github.com/ipfs/go-ipfs/blob/master/docs/config.md#gateway-recipes) for go-ipfs, and [learn more here](https://github.com/ipfs/public-gateway-checker/issues/150).

Then, submit a pull request for this change. Be sure to follow all the directions in the pull request template so your PR can be triaged as quickly as possible.

## Testing locally

```bash
npm ci
npm run build
npm start
```
