Docker image for viewing Markdown pages
---------------------------------------

This is a Docker image for running [joeyespo/grip](https://github.com/joeyespo/grip), the Markdown viewer.

Usage
-----

Example: If you have a `README.md` file in `$HOME/docs/`, run the docker image as follows:

```bash
docker run \
    --rm \
    -v $HOME/docs:/root/docs \
    -p 6419:6419 \
    -t \
    -i fstab/grip \
    grip /root/docs/README.md 0.0.0.0:6419
```

Then point your browser to [http://localhost:6419](http://localhost:6419).
