FROM node:22.3-bookworm-slim

ENV PNPM_HOME="/pnpm"
ENV PATH="$PNPM_HOME:$PATH"
RUN corepack enable

WORKDIR /node
COPY . .

RUN pnpm i
RUN chmod +x /node/entrypoint.sh

ENTRYPOINT ["/bin/bash", "/node/entrypoint.sh"]
