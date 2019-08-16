# Build, Sign, and Push
cd ~/project_repos/singularity-rstudio-base
singularity build --fakeroot ~/container_images/singularity-rstudio-base.3.6.1.sif Singularity.3.6.1
singularity push -U ~/container_images/singularity-rstudio-base.3.6.1.sif library://granek/default/singularity-rstudio-base:3.6.1

# Run From Sylabs Cloud
singularity run library://granek/default/singularity-rstudio-base:3.6.0
