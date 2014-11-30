# Introduction to GCM

These are @avendael's slides for Introduction to GCM, generated with `yo reveal`.

## Building

Optional:

* Install yeoman globally: `npm install -g yeoman`
* Install the reveal generator globally: `npm install -g generator-reveal`

Mandatory:

* Install grunt-cli globally: `npm install -g grunt-cli`

Just run `grunt` in the root project directory.

## Slides

If you installed yeoman and the reveal generator, you can add slides by doing

```zsh
$ yo reveal:slide "Slide title" --markdown
```

Slides are written in markdown because ezmode.

## Deploying

You can deploy to github pages if you have commit access to this repository:

```shell
$ grunt deploy
```

Done.

## Web access

You can view the finished product in http://padc.github.io/gcm-slides
