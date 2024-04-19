# jupyter_chat

[![Github Actions Status](https://github.com/jupyterlab-contrib/jupyter-chat/workflows/Build/badge.svg)](https://github.com/jupyterlab-contrib/jupyter-chat/actions/workflows/build.yml)

This project is a monorepo containing the frontend components and extensions to build
a chat in Jupyter.

A lot of the components of this chat project come from
[jupyter-ai](https://github.com/jupyterlab/jupyter-ai).

## Composition

### Typescript package

The typescript package is located in *packages/jupyter-chat* and builds an NPM
package named `@jupyter/chat`.

This package provides a frontend library (using react), and is intended to be
used by a jupyterlab extension to create a chat.

### Jupyterlab extensions

#### Chat extension based on shared document: *packages/jupyterlab-collaborative-chat*

This extension is an implementation of the `@jupyter/chat` package, relying on
shared document (see [jupyter_ydoc](https://github.com/jupyter-server/jupyter_ydoc)).

It is composed of:

- a Python package named `jupyterlab_collaborative_chat`, which register
  the `YChat` shared document in jupyter_ydoc
- a NPM package named `jupyterlab-collaborative-chat`.

#### Chat extension based on websocket: *packages/jupyterlab-ws-chat*

This extension is an implementation of the `@jupyter/chat` package, relying on
websocket for the communication between server and front end.

It is composed of a Python package named `jupyterlab_ws_chat`
for the server side and a NPM package named `jupyterlab-ws-chat`.

## Contributing

See the contributing part of each package for details.
