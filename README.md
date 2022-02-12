# vector-tile-builder

## Requirements

- git
- curl
- GNU sed
- GNU make
- Docker

I believe GNU, So I don't care about other `sed` or `make`.  
Why don't you believe GNU?

## Build your own free vector tile web maps on GitHub Pages

### Click `Use this template` button of this repository

Decide the name of repository of your new maps.
This name will use the URL of the GitHub Pages.

### `git clone` your new repository

```
git clone git@github.com:your-github-username/your-repo-name.git
cd your-repo-name
```

### Copy and edit `.env`

```
cp .env.sample .env
```

You MUST edit `REGION` and `TILES_URL` value in `.env` file.

`REGION` is some string like `asia/japan/kanto` that is the path of https://download.geofabrik.de/  
`TILES_URL` is determine by your GitHub username and repository name.

NOTE: **GitHub Pages has 1GB size limits.**  
So you MUST NOT choose very large `REGION`.

You can ignore `PORT` value when you deploy vector tile maps to GitHub Pages.
The `PORT` value will only use when launch local vector tile server.

### Just run `make`

```
make
```

...It will done everything you want, If you meets requirements and `.env` file has written correctly.

### Create `gh-pages` branch and Publish

```
make gh-pages
git push
```

### See GitHub Pages
