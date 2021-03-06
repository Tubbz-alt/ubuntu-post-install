# Logs

Logs are written to a file `<current-dir>/logs/after-effects.log`.

## Debugging the script

You can chose from multiple debug modes. by setting DEBUG variable to one of the following

- `DEBUG=1` Print debug messages
- `DEBUG=trace` Print debug messages and apt/dpkg/snap/ppa/pip logs.
Please note that This can generate a lot of output.

## Local testing

You can use `./tests/local.sh --help` to test the scripts locally. It uses docker to build and test the script in simulate mode inside
containers. This script requires two arguments __--distro__ and __--release__. They are used as parameters to build the Docker image from dockerfile in `dockerfiles/tests`.eg. to test the script on Ubuntu 18.04 bionic, run it as
`./tests/local.sh --distro ubuntu --release bionic`.

!!! tip
    This assumes that you can run docker without using sudo. Add yourself yo docker group or refer to docker documentation
    for more info.

## Documentation

Docs are built using mkdocs. If you spot a mistake or a typo, you can submit a Pull request to fix it.
You can test the docs locally with provided docker-compose file.

```bash
docker-compose up
```

and navigate to localhost:8000 to view the documentation.
