# wkhtmltopdf

[wkhtmltopdf](https://wkhtmltopdf.org) is an open source (LGPLv3) command line tool to render HTML into PDF using the Qt WebKit rendering engine.

## Usage

```sh
$ docker run dtannock/wkhtmltopdf
$ docker run -v $PWD:/tmp/ dtannock/wkhtmltopdf http://www.google.com /tmp/output.pdf
```

