# React Native AsyncStorage Data Corruption Bug

This repository demonstrates a bug encountered when using AsyncStorage in React Native to store and retrieve large JSON objects. The retrieval is inconsistent; sometimes the data is complete, other times it's truncated or corrupted, making debugging challenging.  The bug's inconsistency adds to the difficulty. 

## Bug Description

The core issue lies in AsyncStorage's handling of large JSON objects. When attempting to retrieve data stored using `AsyncStorage.setItem`, the retrieved value is sometimes incomplete or altered. This inconsistency makes reproducing the problem and finding a straightforward solution challenging.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run the app on an emulator or device.
4. Observe the inconsistent retrieval of data from AsyncStorage.

## Solution

The recommended solution involves using a more robust storage mechanism such as MMKV, which is designed to handle larger datasets more effectively. This solution provides a more stable and reliable storage alternative, overcoming the limitations of AsyncStorage for large JSON objects.

## Files

- `bug.js`: Demonstrates the inconsistent data retrieval from AsyncStorage.
- `bugSolution.js`: Shows the implementation using MMKV for improved data handling.
