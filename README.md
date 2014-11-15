docker-composer
===============

Used to create Docker images for running composer [https://getcomposer.org]


Usage
--------------------

1. Install the `denisura/composer` container (optional - this step is performed by Docker automatically when running the container):

    ``` sh
    $ docker pull denisura/composer
    ```

2. Define an bash alias that runs this container whenever `composer` is invoked on the command line:

	``` sh
	$ echo "alias composer='docker run --rm -it -v \$(pwd):/workspace denisura/composer'" >> ~/.bashrc
	$ source ~/.bashrc
	```

3. Run composer as always:

	``` sh
	$ composer init --require=foo/bar:1.0.0 -n
	```

	``` sh
	$ composer self-update
	```

	``` sh
    $ composer install -o
    ```

	``` sh
    $ composer require "foo/bar:1.0.0"
    ```
