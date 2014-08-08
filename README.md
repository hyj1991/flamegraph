# flamegraphs [![build status](https://secure.travis-ci.org/thlorenz/flamegraphs.png)](http://travis-ci.org/thlorenz/flamegraphs) 

[![testling badge](https://ci.testling.com/thlorenz/flamegraphs.png)](https://ci.testling.com/thlorenz/flamegraphs)

Generate flamegraphs with Node.js or in the browser.

```
cat instruments-callgraph.csv | flamegraph -t instruments > flamegraph.svg
```


## Installation

    npm install flamegraph

## Usage

```
flamegraph <options>

Generates a flamegraph from the callgraph data of the given `inputtype` that is streamed into it.

OPTIONS:

  -h --help       print this help message 
  -t --inputtype  the type of callgraph (only 'instruments' supported at this point)
  --fonttype      font family used                  default: 'Verdana'
  --fontsize      base text size                    default: 12
  --imagewidth    max width, pixels                 default: 1200
  --frameheight   max height is dynamic             default: 16.0
  --fontwidth     avg width relative to fontsize    default: 0.59
  --minwidth      min function width, pixels        default: 0.1
  --countname     what are the counts in the data?  default: 'samples'
  --colors        color theme                       default: 'hot'
  --bgcolor1      background color gradient start   default: '#eeeeee'
  --bgcolor2      background color gradient stop    default: '#eeeeb0'
  --timemax       (override the) sum of the counts  default: Infinity
  --factor        factor to scale counts by         default: 1
  --hash          color by function name            default: true
  --titletext     centered heading                  default: 'Flame Graph'
  --nametype      what are the names in the data?   default: 'Function:'

EXAMPLE:

  cat instruments-callgraph.csv | flamegraph -t instruments > flamegraph.svg
```

## API

## Kudos

This library is an adaptation of @brendangregg's [FlameGraph perl scripts](https://github.com/brendangregg/FlameGraph).

## License

MIT
