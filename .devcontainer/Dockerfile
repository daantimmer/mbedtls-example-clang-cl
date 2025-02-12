FROM ghcr.io/philips-software/amp-devcontainer-cpp:5.6.0@sha256:884732270a353e8446f813e649f2918ac53ce446a6c0dd4f7f84a6d58fb26bce

HEALTHCHECK NONE

RUN xwin --accept-license --manifest-version 17 splat --preserve-ms-arch-notation \
        --include-debug-libs && mv .xwin-cache/splat/ /winsdk
