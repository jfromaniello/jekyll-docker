## Install

```
docker pull jfromaniello/jekyll
```

## Usage

Run your jekyll project as follows:

```
docker run -i -t -p 5000:5000 -v ~/myblog:/data jfromaniello/jekyll
```

Or dockerize your blog with a Dockerfile as follows:

```
FROM jfromaniello/jekyll

ADD . /data
WORKDIR /data

ENV PORT 5000

CMD jekyll serve --port $PORT
```

## License

MIT 2014 - José F. Romaniello