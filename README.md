# React Native: Runtime Error from Unlinked Native Library

This repository demonstrates a common React Native bug related to improperly linked native libraries.  The bug arises when a third-party library, particularly one relying on native modules, is not correctly linked during the installation process. This can lead to runtime errors that are difficult to diagnose, often manifesting as cryptic messages about missing modules or methods.

## Bug Description

The core issue stems from a mismatch between the library's native code and the React Native environment.  While the JavaScript bundler might seem to correctly include the library code, the connection to the native side is broken.  This usually happens with libraries utilizing platform-specific features (e.g., camera access, maps).  The errors might appear only at runtime, masking the underlying linking problem.

## How to Reproduce

1. Clone this repository.
2. Follow the instructions in `bug.js` to reproduce the error.  Observe the runtime error when the component renders.
3. Refer to `bugSolution.js` for the correct solution.

## Solution

The solution involves correctly linking the native library.  The process depends on the specific library; consult its documentation.  Usually, it involves using a command-line tool (like `react-native link`) or running platform-specific build steps.