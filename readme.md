# League\Flysystem\GridFS [BETA]

[![Author](http://img.shields.io/badge/author-@frankdejonge-blue.svg?style=flat-square)](https://twitter.com/frankdejonge)
[![Build Status](https://img.shields.io/travis/thephpleague/flysystem-gridfs/master.svg?style=flat-square)](https://travis-ci.org/thephpleague/flysystem-gridfs)
[![Coverage Status](https://img.shields.io/scrutinizer/coverage/g/thephpleague/flysystem-gridfs.svg?style=flat-square)](https://scrutinizer-ci.com/g/thephpleague/flysystem-gridfs)
[![Quality Score](https://img.shields.io/scrutinizer/g/thephpleague/flysystem-gridfs.svg?style=flat-square)](https://scrutinizer-ci.com/g/thephpleague/flysystem-gridfs)
[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE)
<!--
[![Packagist Version](https://img.shields.io/packagist/v/league/flysystem-gridfs.svg?style=flat-square)](https://packagist.org/packages/league/flysystem-gridfs)
[![Total Downloads](https://img.shields.io/packagist/dt/league/flysystem-gridfs.svg?style=flat-square)](https://packagist.org/packages/league/flysystem-gridfs)
-->

This is a Flysystem adapter for the MongoDB's GridFS.

# Bootstrap

``` php
<?php
use Aws\S3\S3Client;
use League\Flysystem\GridFS\Adapter;
use League\Flysystem\Filesystem;

include __DIR__ . '/vendor/autoload.php';

$mongoClient = new MongoClient();
$gridFs = $mongoClient->selectDB('db_name')->getGridFS();

$adapter = new Adapter($gridFs);
```
