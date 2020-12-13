# Build, Sign, and Push
cd ~/project_repos/singularity-rstudio-base
singularity build --fakeroot ~/container_images/singularity_rstudio_base_4_0_3.sif Singularity.4.0.3
singularity push -U ~/container_images/singularity_rstudio_base_4_0_3.sif library://granek/default/singularity-rstudio-base:4.0.3

# Run From Sylabs Cloud
singularity run library://granek/default/singularity-rstudio-base:4.0.3
