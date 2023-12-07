# .NET 7 Demo Snap

A snap packaging demonstartion that packages a simple .NET 7 hello world application.

## Prerequisite

To build the snap we need to install `snapcraft`:

```bash
snap install snapcraft --classic
```

## Building the snap

To build the snap simply run:

```bash
snapcraft
```

- On `amd64`: A `dotnet7-demo-snap_1.0.0_amd64.snap` file should be created.
- On `arm64`: A `dotnet7-demo-snap_1.0.0_arm64.snap` file should be created.

**NOTE:** I only tested this on `amd64`, but it should work on `arm64` too.

## Install the snap

```bash
snap install --devmode dotnet7-demo-snap_1.0.0_*.snap
```

The `--devmode` flag is needed, because the `.snap` file has no digital signature.

## Other

Note that we stage `libicu70` in the `snapcraft.yaml` file to get globalization support and therefore have to tell the linter to ignore `library` detection warnings.

## License

The MIT License (MIT)

Copyright © 2023 Dominik Viererbe

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the “Software”), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
