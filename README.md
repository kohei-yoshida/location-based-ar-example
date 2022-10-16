# location-based-ar-example

## Environment

- macos: monterey 12.6
- node.js: 18.10.0
- aframe.min.js: 1.2.0
- aframe-look-at-component 0.8.0
- docker desktop: 4.12.0
- docker engine: 20.10.17
- docker compose: 2.10.2

## WebXR Library

[A-Frame](https://aframe.io/)

[aframe-look-at-component](https://github.com/matrix-org/aframe-look-at-component)

## Directory

```txt
./a-frame-demo1
├── node_modules
├── .dockerignore
├── .gitignore
├── docker-compose.yaml
├── package-lock.json
├── package.json
├── README.md
└── src
    ├── index.html  # a-frame描画用のHTML
    └── index.js    # nodeのmainスクリプト
```

## Usage with docker

start: docker container

```bash
% docker-compose up -d
```

end: docker container

```bash
% docker-compose down
```

## Usage without docker

start: When specifying from the root directory

```bash
% node ./src/index.js 
# > Node.js is listening to PORT:3000
```

end: (control + c)

```bash
# > Node.js is listening to PORT:3000
^C
```

## View in browser, After Start

```blowser
http://localhost:3000
```

## Remark

https://github.com/kohei-yoshida/location-based-ar-example/blob/master/src/index.html#L21

gps-entity-place属性を指定して、GPSの圏内でアクセスすると文字が表示される。

```html
<a-text
  value="Tokyo Tower"
  look-at="[gps-camera]"
  scale="5 5 0"
  gps-entity-place="latitude: 35.658706880003145; longitude: 139.74542216936783;"
></a-text>
```

![GoogleMap](https://user-images.githubusercontent.com/43778602/195981420-f8e65e6a-9052-4ecf-ba16-0458c16fd0b7.png)
