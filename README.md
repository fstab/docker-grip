Docker image for viewing Markdown pages
---------------------------------------

This is a Docker image for running [joeyespo/grip](https://github.com/joeyespo/grip), the Markdown viewer.

Usage
-----

Example: In order to view `$HOME/myproj/README.md`, run the Docker image as follows:

```bash
docker run \
    --rm \
    -v $HOME/myproj:/root/docs \
    -p 6419:6419 \
    -t \
    -i fstab/grip \
    grip /root/docs/README.md 0.0.0.0:6419
```

If you run it for the first time, image will be pulled from [https://hub.docker.com/r/fstab/grip](https://hub.docker.com/r/fstab/grip).

Then point your browser to [http://localhost:6419](http://localhost:6419).

