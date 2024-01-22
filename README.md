# Solana RPC Benchmark Tool

This GoLang-built tool is designed to transmit multiple RPC transactions to a specified Solana RPC endpoint. Its core purpose is to assess the transaction throughput, enabling users to determine the maximum Transactions Per Second (TPS) that an RPC can handle.

## Download
-   [Get the latest version of the tool](https://github.com/thorlabsDev/rpc-bencmark/releases)
-   Make sure you choose the right version for your OS

## Features
- Send multiple transactions concurrently to an RPC endpoint.
- Set a delay between each transaction.
- Measure the success and failure rate of the transactions.
- Display the Transactions Per Second (TPS) for both successful and total transactions.
- Show detailed error reports for failed transactions.

## Configuration Options
Here are the configuration options you can specify when running the tool:
- `rpcEndpoint`: The URL of the RPC endpoint.
- `concurrentRequests`: The number of concurrent requests to send to the RPC endpoint.
- `testDurationSeconds`: The duration of the test in seconds.
- `showRPCOutput`: Whether to display detailed output for each RPC request.
- `transactionDelayMilliseconds`: The delay between sending each transaction in milliseconds. Adjusting this value can control the rate at which transactions are sent.

## Usage
- Execute the binary application in your command prompt or terminal, ensure that you have a valid configuration file located in the same folder as the executable.

## Output
The program provides a detailed report of:

- RPC Endpoint used.
- Number of workers (concurrent requests).
- Total successful transactions sent.
- Total failed transactions.
- Test duration in seconds.
- All jobs process duration in seconds.
- Sending Transactions Per Second (TPS).
- Successful Transactions Per Second (TPS).
- Ping Latency (ms).
- Minimum Response Time (ms).
- Maximum Response Time: (ms).
- Average Response Time: (ms).
- Detailed error reports for each HTTP error code encountered.

## Best Practices for Effective RPC Throughput Testing

- **Concurrent Overhead:** While the tool allows for multiple concurrent requests, it's essential to understand that every system has a concurrency limit beyond which additional requests might not lead to better performance. Instead, they could introduce overhead, causing the system to slow down. It's advisable to incrementally increase concurrency and observe the TPS to find an optimal point.

- **Network Latency:** The physical distance and network quality between the tool and the RPC endpoint can introduce latency. For more accurate results, consider running the tool from a location (or server) that's geographically closer to the RPC endpoint.

- **RPC Endpoint Capacity:** Different RPC endpoints might have varying capacities based on their underlying infrastructure. It's crucial to ensure that the endpoint you're testing is representative of a real-world scenario.

- **System Resources:** Ensure that the machine running the tool has sufficient resources (CPU, memory, and network bandwidth) to handle the desired concurrency level. A bottleneck in any of these resources can skew the results.

- **Error Analysis:** Pay close attention to the error codes and their frequency. A high number of specific errors might indicate a bottleneck or limitation in the RPC or the network.

- **Duration of Test:** Running the test for a very short duration might not give the system enough time to stabilize and show its true performance. Conversely, very long tests might lead to throttling or other limitations kicking in. Find a balance based on your specific needs.


## Disclaimer

The information, recommendations, and guidelines provided in this document are presented in good faith and believed to be accurate based on the current state of knowledge and technology. However, they are provided without any warranty or guarantee of any kind, either expressed or implied, including, without limitation, warranties of merchantability or fitness for a particular purpose. Users are advised to exercise their own judgment and discretion when implementing or using the tools and techniques described herein. The authors, contributors, and publishers of this document shall not be held liable for any damages, losses, or consequences, whether direct, indirect, special, incidental, or consequential, arising out of or in connection with the use or reliance on this documentation or any information contained within.

## Contact Us

For any inquiries, feedback, or to report bugs, please reach out to us via our official Discord server:

[Join ThorLabs Discord Server](https://discord.gg/thorlabs)

To report a bug or any other issue, kindly submit a ticket within the Discord server. Our dedicated team will review and address your concerns promptly.
