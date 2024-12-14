# Node.js Server Concurrency Issue

This repository demonstrates a common issue in Node.js where a single-threaded server might fail to handle a high volume of concurrent requests.  The provided solution uses the `cluster` module to create a cluster of worker processes, improving concurrency and handling capacity.

## Bug Description

The `bug.js` file contains a basic HTTP server.  Under heavy load, this server will likely miss requests or respond slowly. This is because Node.js uses a single thread to handle all incoming requests.

## Solution

The `bugSolution.js` file demonstrates how to solve this problem by using the `cluster` module. This creates multiple worker processes that share the load, thus enabling the server to handle a larger number of concurrent requests more efficiently.

## How to Run

1. Clone the repository.
2. Navigate to the directory.
3. Run `node bug.js` for the buggy version.
4. Run `node bugSolution.js` for the improved solution.