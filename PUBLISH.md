## Publishing an extension

You can use the official [instructions](https://code.visualstudio.com/api/working-with-extensions/publishing-extension) for publishing extensions

or

you can use a docker container which is created from the [Dockerfile](https://raw.githubusercontent.com/gozoro/vscode-greybird-theme/main/Dockerfile) given here  to avoid installing `nodejs`, `npm`, `vsce` on your machine.

Build image:

```bash
docker build -t vsce .
```

Run container from image:

```bash
docker run -it vsce
```

Create package inside container:

```bash
vsce package
```

Logining into markerplace

```bash
vsce login <your_publisher>
```

Publishing extension

```bash
vsce publish
```
