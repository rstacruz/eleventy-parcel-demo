<h1 align='center'>
parcel-eleventy-demo
</h1>

<p align='center'>
A short barebones demo showing how Parcel can be integrated with Eleventy (11ty).
</p>

<p align='center'>
<img src='https://user-images.githubusercontent.com/74385/110925544-714ab380-8377-11eb-964f-ef0a6dc55c16.png' width='600'>
</p>

## How it works

```sh
yarn        # Install dependencies
yarn dev    # starts a dev server
yarn build  # builds to dist/
```

- [Eleventy] builds `src/` to `tmp/`.
- [Parcel] builds `tmp/` to `dist/`.
- Links to source files (eg, `<script src="~/styles/main.scss">`) are processed by Parcel.

[eleventy]: https://www.11ty.dev/
[parcel]: https://parceljs.org/

## FAQ

### Why is there [sirv]?

[sirv]: https://npmjs.com/package/sirv-cli

The [sirv-cli][sirv] package is used to run a web server rather than Parcel or 11ty. While it'd be ideal to use `parcel serve`, Parcel will serve 404 pages with the root index.html page, since it's geared towards that kind of single-page application setup.

### Why is `--no-cache` being passed to Parcel?

As `tmp/` gets regenerated everytime, it can mess with Parcel's caching.

### Why is there [sass]?

No reason, just an example of a CSS transform that one might use with Parcel. It's not needed for Parcel to work with Eleventy.

[sass]: https://sass-lang.com/

## Prior art

A lot of this code was patterned off of [vseventer/eleventy-parcel-boilerplate](https://github.com/vseventer/eleventy-parcel-boilerplate).

## Thanks

&copy;2021, MIT License
