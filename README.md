# Testem Selenium Launcher

This project provides a testem launcher which can connect to an existing selenium hub.

## Getting Started

1. Install the launcher

```
$ npm install testem-selenium-launcher --save-dev
```

2. Add the launcher configuration to your testem config. NOTE: the '&lt;url&gt;' needs to be as is, this is how testem knows where to put the test url.

```json
{
  ...
  "launchers": {
        "Chrome_iPhone7-portrait": {
      "exe": "node_modules/.bin/testem-selenium-launcher",
      "args": [
        "<url>",
        "http://localhost:9515",
        {
          "browserName": "chrome",
          "chromeOptions": {
            "args": [
              "--test-type",
              "--window-size=414,736"
            ]
          }
        }
      ],
      "protocol": "browser"
    }
  }
  ...
}
```

3. Run the suite 
```
$ testem -l Selenium
```

For a working example look at the [Example](./example).
