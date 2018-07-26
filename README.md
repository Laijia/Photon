# Photon [![python](https://img.shields.io/badge/Python-2.x|3.x-green.svg?style=style=flat-square)](https://www.python.org/downloads/)  [![license](https://img.shields.io/badge/License-GPL--v3-orange.svg?style=style=flat-square)](https://www.gnu.org/licenses/gpl-3.0.en.html) [![version](https://img.shields.io/badge/Version-1.0.4-blue.svg?style=style=flat-square)](https://github.com/s0md3v/Photon/blob/master/CHANGELOG.md) [![plugins](https://img.shields.io/badge/Plugins-1-yellow.svg?style=style=flat-square)](https://github.com/s0md3v/Photon/tree/master/plugins) [![twitter](https://img.shields.io/badge/Twitter-@s0md3v-skyblue.svg?style=style=flat-square)](https://twitter.com/s0md3v/)

Photon is a lightning fast web crawler which extracts URLs, files, intel & endpoints from a target.

![demo](https://image.ibb.co/bTNwBy/Screenshot_2018_07_22_12_07_30.png)

## Main Features

#### Data Extraction
Photon extracts the following data while crawling by default:

- URLs (in-scope & out-of-scope)
- URLs with parameters (`example.com/gallery.php?id=2`)
- Intel (emails, social media accounts, amazon buckets etc.)
- Files (pdf, png, xml etc.)
- JavaScript files & Endpoints present in them
- Strings based on custom regex pattern

The extracted information is saved in an organized manner.\
![save demo](https://image.ibb.co/ezTEyd/Screenshot_2018_07_22_12_24_44.png)

Photon also allows custom data extraction with [regex patterns](https://github.com/s0md3v/Photon/wiki/Usage#custom-regex-pattern).

#### Intelligent Multithreading
Here's a secret, most of the tools floating on the internet aren't properly multi-threaded even if they are supposed to. They either supply a list of items to threads which results in multiple threads accessing the same item or they simply put a thread lock and end up rendering multi-threading useless.\
But Photon is different or should I say "genius"? Take a look at [this](https://github.com/s0md3v/Photon/blob/aaf5ab3b2a2a168a8eb625eb2a6feb4307521f22/photon.py#L315-L339) and decide yourself.

#### Ninja Mode
In Ninja Mode, 3 online services are used to make requests to the target on your behalf.\
So basically, now you have 4 clients making requests to the same server simultaneously which gives you a speed boost, minimizes the risk of connection reset as well as delays requests from a single client.\
Here's a comparison generated by [Quark](https://github.com/s0md3v/Quark) where the lines represent threads:

![ninja demo](https://image.ibb.co/jJSDg8/ninja.png)

#### Plugins
Photon's capabilites can be further extended by using plugins.

Available plugins:

- **[dnsdumpster](https://github.com/s0md3v/Photon/wiki/Usage#dumping-dns-data)**: Generates an image containing the DNS data of the target doman.

Plugins in active development:

- **Quark**: A plugin to plot a graph making it easier to inspect relationships between different webpages using [Quark](https://github.com/s0md3v/Quark).
- **Exporter**: Plugin to export results in JSON, more formats will be added later.
- **dnsdumpster**: A new version of the plugin is in development which will save the DNS data in a nicely formatted HTML file.

#### Support
The project is under heavy development and any submitted issues or pull requests will be acknowledged within min 5 minutes and max 9 hours.

### Documentation
- [Using Photon](https://github.com/s0md3v/Photon/wiki/Usage)
- [Compatibility & Dependencies](https://github.com/s0md3v/Photon/wiki/Compatibility-&-Dependencies)

### Contribution & License
You can contribute in following ways:

- Report bugs
- Develop plugins
- Add more "APIs" for ninja mode
- Give suggestions to make it better
- Fix issues & submit a pull request

**Photon** is licensed under [GPL v3.0 license](https://www.gnu.org/licenses/gpl-3.0.en.html)
