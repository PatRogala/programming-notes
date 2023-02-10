# Deploy React App

First we need to get production build of our rails app by running

`npm run build`

This creates a directory called `build`

We need to copy production build to our backend

`cp -r build ../backend`