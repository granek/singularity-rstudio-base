[![https://www.singularity-hub.org/static/img/hosted-singularity--hub-%23e32929.svg](https://www.singularity-hub.org/static/img/hosted-singularity--hub-%23e32929.svg)](https://singularity-hub.org/collections/3197)


# Running Singularity Image
Run a singularity-rstudio-base container with `singularity run shub://granek/singularity-rstudio-base`

## /tmp issues
It is recommended to do one of the following when running this image. There is no need to do both:

1. Set "mount tmp = no" in `/etc/singularity/singularity.conf`.
2. If #1 is not an option, the following command can be used to bind mount `/tmp` in the container to a "private" tmp directory:
```
SINGTMP="/tmp/${USER}_$$_tmp"; mkdir -p $SINGTMP; singularity run --bind $SINGTMP:/tmp shub://granek/singularity-rstudio-base
```
### /tmp issues TLDR
If a second user tries on the same server tries to run an RStudio container they will have permission issues with `/tmp/rstudio-server`, which will be owned by the user who first ran an RStudio container.
