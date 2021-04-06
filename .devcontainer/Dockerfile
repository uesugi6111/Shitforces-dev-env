
ARG VARIANT=14
FROM mcr.microsoft.com/vscode/devcontainers/typescript-node:${VARIANT}

ARG USER_UID=1000
ARG USER_GID=$USER_UID
RUN if [ "$USER_GID" != "1000" ] || [ "$USER_UID" != "1000" ]; then \
    groupmod --gid $USER_GID node \
    && usermod --uid $USER_UID --gid $USER_GID node \
    && chown -R $USER_UID:$USER_GID /home/node \
    && chown -R $USER_UID:root /usr/local/share/nvm /usr/local/share/npm-global; \
    fi


CMD ["bash"]