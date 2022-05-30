sio-smoltcp.rs [![Unlicensed work](https://raw.githubusercontent.com/unlicense/unlicense.org/master/static/favicon.png)](https://unlicense.org/)
==============
~~![GitLab Build Status](https://gitlab.com/KOLANICH-libs/sio-smoltcp.rs/badges/master/pipeline.svg)~~
~~![GitLab Coverage](https://gitlab.com/KOLANICH-libs/sio-smoltcp.rs/badges/master/coverage.svg)~~
[![GitHub Actions](https://github.com/KOLANICH-libs/sio-smoltcp.rs/workflows/CI/badge.svg)](https://github.com/KOLANICH-libs/sio-smoltcp.rs/actions/)
[![Libraries.io Status](https://img.shields.io/librariesio/github/KOLANICH-libs/sio-smoltcp.rs.svg)](https://libraries.io/github/KOLANICH-libs/sio-smoltcp.rs)

[Sans-IO-style](https://sans-io.readthedocs.io/how-to-sans-io.html) [FFI](https://en.wikipedia.org/wiki/Foreign_function_interface) for [smoltcp](https://github.com/smoltcp-rs/smoltcp).

Obviously, this lib wouldn't be possible without `smoltcp` existence.

This library reuses some portions of `smoltcp` source code.


Limitations
===========

* For fragmentation you need the branch of `smoltcp` used in the PR https://github.com/smoltcp-rs/smoltcp/pull/672 .
* You can also use https://github.com/smoltcp-rs/smoltcp/pull/634 , but for now it panics. It corresponds to https://github.com/KOLANICH-libs/sio-smoltcp.rs/tree/thvdveld_ipv6_frag branch of this repo, since that branch changes the API.
* We copy bytes back and forth, which is inefficient
* Currently it is early beta, not all the features are implemented, and API is not yet stabilized.
