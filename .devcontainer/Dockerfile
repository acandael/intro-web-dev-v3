FROM mcr.microsoft.com/devcontainers/base:ubuntu-24.04

COPY --from=jdxcode/mise /usr/local/bin/mise /usr/local/bin/

# make sure mise is activated in both zsh and bash. Might be overridden by a user's dotfiles.
RUN echo 'eval "$(mise activate bash)"' >> /home/vscode/.bashrc && \
    echo 'eval "$(mise activate zsh)"' >> /home/vscode/.zshrc

# pre-create mise data directory so it doesn't fail on first SSH login
RUN mkdir -p /home/vscode/.local/share/mise/migrations && \
    chown -R vscode:vscode /home/vscode/.local
