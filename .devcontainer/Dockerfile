# Using the specific ARM64 compatible image
FROM mcr.microsoft.com/devcontainers/base:ubuntu

# Set up the workspace
ARG WORKSPACE_DIR=/workspaces/vibe-coding-tools
RUN mkdir -p ${WORKSPACE_DIR}

# Ensure the 'vscode' user owns the workspace
RUN chown -R vscode:vscode ${WORKSPACE_DIR}

# --- THE FIX ---
# This removes the file that allows the 'vscode' user to use sudo without a password
RUN rm /etc/sudoers.d/vscode
# ----------------

# but we will lock it down in the json file.
USER vscode
