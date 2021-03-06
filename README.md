# (বাংলা)Bengali sentence dataset
This is a repository to form a bengali data set scraping the bengali wikipedia. This is primarily done for the [Mozzila Common Voice Bengali](https://voice.mozilla.org/bn) and will contain the [বাংলা উইকিপেডিয়া(bengali wikipedia)](https://bn.wikipedia.org) for now. But it will contain sentences from other public domain in the future.

# To Do list
 - [ ] create usable languge rules and a blacklist.

# Setup

This is supposed to work with [cv-sentence-extractor](https://github.com/Common-Voice/cv-sentence-extractor).

Clone common-voice-wiki-scraper repo:

git clone https://github.com/Common-Voice/common-voice-wiki-scraper.git

You need to download the WikiExtractor:
```bash
git clone https://github.com/attardi/wikiextractor.git
```
clone this repo

```bash
git clone https://github.com/mm-crj/bn-wiki-scraper.git
cd bn-wiki-scraper
```
extract the `text.tar.bz2` file.

then place the text folder from this repo in `wikiextractor` folder(cloned or downloaded).

Place the files from the rules folder in this repo in appropiate places in the common-voice-wiki-scraper folder.

then execute

```bash
cargo run -- extract -l bn -d ../wikiextractor/text/ >> ./sentences/wiki.bn.txt
```
