# Theme

Main colors are from `logo.jpg`

- F8931FFF (orange)
- 8DC540FF (green)


# run

```
$ hugo server -D --logLevel debug --disableFastRender --watch -v --theme hugo-scroll

$ docker run --net=host  -v .:/src hugomods/hugo:ci-0.131.0 hugo server -D --logLevel debug --disableFastRender --watch --theme hugo-scroll
```

# debug

```
{{ printf "%#v" . }}
```

# build

```
$ hugo --theme hugo-scroll -b https://ecobike.pt

$ docker run --net=host  -v .:/src hugomods/hugo:ci-0.131.0 hugo --theme hugo-scroll -b https://ecobike.pt -d /public
```

The content can be served from the `public` folder: 

```
python -m http.server --directory public
```

# upload

```
ncftpput -R -v -u website@meditarlisboa.pt -p $FTP_PASSWORD ftp.meditarlisboa.pt / public/*
```
