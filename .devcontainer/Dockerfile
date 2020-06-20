FROM rubensa/ubuntu-tini-dev-chrome

# Change docker socket owner
RUN printf "\nsudo chmod a+rw /var/run/docker.sock\n" >> /home/${USER_NAME}/.bashrc

# Keep container running (for use in VSCode)
CMD [ "tail", "-f", "/dev/null" ]

# Allow vscode-server cache
RUN mkdir -p /home/${USER_NAME}/.vscode-server

# Allow node cache
RUN mkdir -p /home/${USER_NAME}/.npm

# Configure npx auto fallback
RUN printf "\nsource <(npx --shell-auto-fallback bash)\n" >> /home/${USER_NAME}/.profile
