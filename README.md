# mlafeldt/fpm-cook

Docker images that provide [fpm-cookery](https://github.com/bernd/fpm-cookery)
for package building.

Usage:

    $ vim recipe.rb # create recipe
    $ docker run -it --rm -v $PWD:/data mlafeldt/fpm:ubuntu
    $ ls pkg/ # packages go here
