# Expo Constants.manifest Returns Undefined or Partial Data

This repository demonstrates a bug where `Constants.manifest` in an Expo managed workflow app returns `undefined` or a partially populated object under certain conditions (e.g., immediately after app installation or due to caching). This can lead to unexpected app behavior or crashes if your code depends on the manifest data.

## Steps to Reproduce

1. Clone this repository.
2. Run `expo start`.
3. Observe that `Constants.manifest` might return `undefined` or a partial object when the app first loads, but often works later. 

## Solution

A robust solution involves employing asynchronous operations and handling potential errors. The provided `bugSolution.js` example showcases a better approach.