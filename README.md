# ip.danielmarks.dev

This website tests a browser's IPv6 happy eyeballs configuration. The JS code itself is simplisctic as it just looks for "." in the "ip=" field to determine if it's an IPv4 address, and considers anything that doesn't return an HTTP error or "." a success.

## Details

The web browser sends a request to "https://crypto.cloudflare.com/cdn-cgi/trace" and extracts the "ip=" value. If it's an IPv4 address, the test fails. If it's an IPv6 address, the test succeeds.

The endpoint was deliberately chosen to support QUIC and "Encrypted Client Hello" if a browser supports it.

**It is possible to have working IPv6 and fail this test**, especially if you get your IPv6 access through a VPN or through a tunnel (i.e. link local tunnel endpoints). For my purposes, this page is just an easy way to see if friends/family can connect to my IPv6-only servers without explaining anything.

## Issues

Please don't submit an issue if you fail this test and need tech support on how to enable v6. This repo is just here to share the source code in case anyone else finds it useful. Please email me directly if you find security flaws.
