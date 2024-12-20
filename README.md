# React + TypeScript + Vite + Helm + Kubernetes

This example project's primary goal is to explain how to deploy a `vite` `react` app to kubernetes the `RIGHT WAY`.

We will be using an `nginx` container as the base for our pod and we will be serving the built assets from the `dist` directory.

`THIS` is the `RIGHT WAY` to host your application on kubernetes. There are a lot of `BAD` examples out there that will have you run the app with `vite preview` or some other method that is both less secure and more resource intensive.

**ADDITIONALLY:**

It is common to use a different path for each app in your apps namespace and having those paths resolve to different pods with your ingress controller. So we will be using that pattern in this example.

## Assumptions
- you understand git
- you understand npm
- you have a running k8s cluster
- you have an understanding of Helm

## Getting Started
- Clone this repo
- npm install
- npm run dev

## Deploying to your cluster

## Whats going on here