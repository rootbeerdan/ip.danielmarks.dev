# ip.danielmarks.dev

This website tests a browser's IPv6 happy eyeballs configuration. The JS code itself is simplisctic as it just looks for "." in the "ip=" field to determine if it's an IPv4 address, and considers anything that doesn't return an HTTP error or "." a success.

## Details

The web browser sends a request to "https://crypto.cloudflare.com/cdn-cgi/trace" and extracts the "ip=" value. If it's an IPv4 address, the test fails. If it's an IPv6 address, the test succeeds.

The endpoint was deliberately chosen to support QUIC and "Encrypted Client Hello" if a browser supports it.

## Issues

Please don't submit an issue if you fail this test, I am not tech support. This repo is just here to share the source code in case anyone else finds it useful.
