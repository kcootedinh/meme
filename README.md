# memes in a container

This fork puts [upstream](https://github.com/nomad-software/meme) in a container.

## Run it

The following will drop `meme.png` to your `$(PWD)`
```bash
docker run -v $(PWD):/tmp staff0rd/meme -i archer-do-you-want -t "do you want memes in a container?|because this is how you get memes in a container"
```
See what it can do
```bash
docker run staff0rd/meme --help
```

## Dev

```bash
docker run -it --entrypoint bash -v $(PWD):/src -p 5000:5000 staff0rd/meme
```

# Upstream docs
**A command line utility for creating [image macro style memes](https://en.wikipedia.org/wiki/Image_macro)**

[![Go report card](https://goreportcard.com/badge/github.com/nomad-software/meme)](https://goreportcard.com/report/github.com/nomad-software/meme)

---

![Am i the only one around here?](http://i.imgur.com/WP1TAzg.png)

## Features

* Create memes from built-in templates
* Create memes from image URL's
* Create memes from local image files
* Supports drawing on animated gifs
* Supports intensifing images by shaking them slightly
* Supports adding the 'triggered' banner
* Resizes oversized images
* Automatically upload to [imgur.com](http://imgur.com/) (when passed a client id)
* Works on Linux, Mac and Windows

## Simple example

To create a meme use the following command. The image can be an built-in
template, a URL or the path to a local file.

```
meme -i brace-yourselves -t "brace yourselves|the memes are coming"
```

When the command finishes, the location of the newly generated meme is printed
to the terminal. This location can be overriden using the `-o` flag.

## Installation

* [Install Go](https://golang.org/doc/install)
* Run `go get -u -v github.com/nomad-software/meme`

## Automatic uploads

If you supply an imgur client id when invoking the command, the meme will
automatically be uploaded to [imgur.com](http://imgur.com/). To get a client
id, follow these steps.

1. [Create an imgur account](https://imgur.com/register)
2. [Register this application for anonymous usage](https://api.imgur.com/oauth2/addclient)
3. Once registered, you get a client id for use when invoking the command. See `meme -help`
4. [Read the rate limits](https://api.imgur.com/#limits)

## Help

Run the following command for help and to list all of the available built-in templates.

```
meme -help
```

## Other examples

```
meme -i brace-yourselves -t "brace yourselves|the memes are coming"
```

![Brace yourselves](http://i.imgur.com/Bn1ANs5.png)

---

```
meme -gif -i http://www.reactiongifs.com/r/trmp.gif -t "|when somebody mentions china"
```

![When somebody mentions china](http://i.imgur.com/0aV1nfo.gif)

---

```
meme -shake -i kirk-khan -t "|khaaaaan"
```

![khaaaaan](http://i.imgur.com/PpGTRvN.gif)

---

```
meme -trigger -i https://i.giphy.com/3o7abKGM3Xa70I7jCU.gif
```

![triggered](http://i.imgur.com/D1pYHmC.gif)

---

## Built-in templates

To create a meme using one of the built-in templates, use one of the following
id's with the `-i` flag. (You can also list these using the `meme -help` command.)

* [advice-mallard](https://github.com/nomad-software/meme/blob/master/data/images/advice-mallard.jpg)
* [all-the-things](https://github.com/nomad-software/meme/blob/master/data/images/all-the-things.jpg)
* [am-i-the-only-one](https://github.com/nomad-software/meme/blob/master/data/images/am-i-the-only-one.jpg)
* [ancient-aliens](https://github.com/nomad-software/meme/blob/master/data/images/ancient-aliens.jpg)
* [archer-do-you-want](https://github.com/nomad-software/meme/blob/master/data/images/archer-do-you-want.jpg)
* [awkward-sealion](https://github.com/nomad-software/meme/blob/master/data/images/awkward-sealion.jpg)
* [baby-insanity-wolf](https://github.com/nomad-software/meme/blob/master/data/images/baby-insanity-wolf.jpg)
* [back-in-my-day](https://github.com/nomad-software/meme/blob/master/data/images/back-in-my-day.jpg)
* [bad-guy-boss](https://github.com/nomad-software/meme/blob/master/data/images/bad-guy-boss.jpg)
* [bad-luck-brian](https://github.com/nomad-software/meme/blob/master/data/images/bad-luck-brian.jpg)
* [brace-yourselves](https://github.com/nomad-software/meme/blob/master/data/images/brace-yourselves.jpg)
* [college-liberal](https://github.com/nomad-software/meme/blob/master/data/images/college-liberal.jpg)
* [condescending-wonka](https://github.com/nomad-software/meme/blob/master/data/images/condescending-wonka.jpg)
* [confession-bear](https://github.com/nomad-software/meme/blob/master/data/images/confession-bear.jpg)
* [confession-kid](https://github.com/nomad-software/meme/blob/master/data/images/confession-kid.jpg)
* [dicaprio-cheers](https://github.com/nomad-software/meme/blob/master/data/images/dicaprio-cheers.jpg)
* [disaster-girl](https://github.com/nomad-software/meme/blob/master/data/images/disaster-girl.jpg)
* [doge](https://github.com/nomad-software/meme/blob/master/data/images/doge.jpg)
* [dr-evil-lasers](https://github.com/nomad-software/meme/blob/master/data/images/dr-evil-lasers.jpg)
* [everywhere](https://github.com/nomad-software/meme/blob/master/data/images/everywhere.jpg)
* [first-world-problems](https://github.com/nomad-software/meme/blob/master/data/images/first-world-problems.jpg)
* [fuck-me-right](https://github.com/nomad-software/meme/blob/master/data/images/fuck-me-right.jpg)
* [futurama-fry](https://github.com/nomad-software/meme/blob/master/data/images/futurama-fry.jpg)
* [good-guy-boss](https://github.com/nomad-software/meme/blob/master/data/images/good-guy-boss.jpg)
* [good-guy-greg](https://github.com/nomad-software/meme/blob/master/data/images/good-guy-greg.jpg)
* [grumpy-cat](https://github.com/nomad-software/meme/blob/master/data/images/grumpy-cat.jpg)
* [high-guy](https://github.com/nomad-software/meme/blob/master/data/images/high-guy.jpg)
* [how-do-they-work](https://github.com/nomad-software/meme/blob/master/data/images/how-do-they-work.jpg)
* [i-should-buy-a-boat-cat](https://github.com/nomad-software/meme/blob/master/data/images/i-should-buy-a-boat-cat.jpg)
* [kirk-khan](https://github.com/nomad-software/meme/blob/master/data/images/kirk-khan.jpg)
* [laughing-men-in-suits](https://github.com/nomad-software/meme/blob/master/data/images/laughing-men-in-suits.jpg)
* [look-at-me](https://github.com/nomad-software/meme/blob/master/data/images/look-at-me.jpg)
* [minor-mistake-marvin](https://github.com/nomad-software/meme/blob/master/data/images/minor-mistake-marvin.jpg)
* [mocking-spongebob](https://github.com/nomad-software/meme/blob/master/data/images/mocking-spongebob.jpg)
* [morpheus](https://github.com/nomad-software/meme/blob/master/data/images/morpheus.jpg)
* [most-interesting-man](https://github.com/nomad-software/meme/blob/master/data/images/most-interesting-man.jpg)
* [none-of-my-business](https://github.com/nomad-software/meme/blob/master/data/images/none-of-my-business.jpg)
* [one-does-not-simply](https://github.com/nomad-software/meme/blob/master/data/images/one-does-not-simply.jpg)
* [oprah-you-get-a](https://github.com/nomad-software/meme/blob/master/data/images/oprah-you-get-a.jpg)
* [overly-attached-girlfriend](https://github.com/nomad-software/meme/blob/master/data/images/overly-attached-girlfriend.jpg)
* [pepperidge-farm-remembers](https://github.com/nomad-software/meme/blob/master/data/images/pepperidge-farm-remembers.jpg)
* [peter-griffin-news](https://github.com/nomad-software/meme/blob/master/data/images/peter-griffin-news.jpg)
* [philosoraptor](https://github.com/nomad-software/meme/blob/master/data/images/philosoraptor.jpg)
* [picard-facepalm](https://github.com/nomad-software/meme/blob/master/data/images/picard-facepalm.jpg)
* [picard-wtf](https://github.com/nomad-software/meme/blob/master/data/images/picard-wtf.jpg)
* [politically-correct-redneck](https://github.com/nomad-software/meme/blob/master/data/images/politically-correct-redneck.jpg)
* [satisfied-seal](https://github.com/nomad-software/meme/blob/master/data/images/satisfied-seal.jpg)
* [scumbag-stacy](https://github.com/nomad-software/meme/blob/master/data/images/scumbag-stacy.jpg)
* [scumbag-steve](https://github.com/nomad-software/meme/blob/master/data/images/scumbag-steve.jpg)
* [so-hot-right-now](https://github.com/nomad-software/meme/blob/master/data/images/so-hot-right-now.jpg)
* [so-i-got-that-goin-for-me](https://github.com/nomad-software/meme/blob/master/data/images/so-i-got-that-goin-for-me.jpg)
* [success-kid](https://github.com/nomad-software/meme/blob/master/data/images/success-kid.jpg)
* [sudden-clarity-clarence](https://github.com/nomad-software/meme/blob/master/data/images/sudden-clarity-clarence.jpg)
* [that-would-be-great](https://github.com/nomad-software/meme/blob/master/data/images/that-would-be-great.jpg)
* [third-world-skeptical-kid](https://github.com/nomad-software/meme/blob/master/data/images/third-world-skeptical-kid.jpg)
* [too-damn-high](https://github.com/nomad-software/meme/blob/master/data/images/too-damn-high.jpg)
* [unhelpful-highschool-teacher](https://github.com/nomad-software/meme/blob/master/data/images/unhelpful-highschool-teacher.jpg)
* [unpopular-opinion-puffin](https://github.com/nomad-software/meme/blob/master/data/images/unpopular-opinion-puffin.jpg)
* [waiting-skeleton](https://github.com/nomad-software/meme/blob/master/data/images/waiting-skeleton.jpg)
* [y-u-no](https://github.com/nomad-software/meme/blob/master/data/images/y-u-no.jpg)
* [yall-got-any-more-of](https://github.com/nomad-software/meme/blob/master/data/images/yall-got-any-more-of.jpg)
