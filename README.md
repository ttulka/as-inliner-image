# as-inliner-image

[AssemblyScript](https://github.com/AssemblyScript/assemblyscript) transform to inline images as arrays of RGBA values 🚀

Based on https://github.com/surma/as-inliner

## Install

```sh
npm install as-inliner-image -D
```

## Use

```typescript
const image: StaticArray<u8> = Inliner.inlineImageAsRgbaStaticArray(
    "../assets/image.png"
);
```

Inlining works through [ASC transforms](https://www.assemblyscript.org/transforms.html#transforms):

```sh
npx asc assembly/index.ts --transform as-inliner-image
```

or place it in your `asconfig.json`:

```json
{
  ...
  "options": {
    "transform": ["as-inliner-image"]
  }
}
```

Or extend the `asconfig.json` here:

```json
{
  "extend": "as-inliner-image/asconfig.json"
}
```

## Licence

[MIT](https://github.com/ttulka/as-inliner-image/blob/main/LICENSE)