Test the speed and throughput from macOS/Ubuntu

Speedtest CLI for Internet/WAN performance and iPerf3 for testing throughput inside your own nwtwork.

1. Speedtest CLI
Use Speedtest CLI to test your Internet connection: latency, download speed and upload speed.

Install on macOS

```brew install speedtest-cli```

Install on Ubuntu

```sudo update```
```sudo apt install speedtest-cli```

Run a speedtest

```speedtest-cli```

=======================================================

2. iPerf3
Use iPerf3 to measure network thtoughput between two devices, such as your Mac and an Ubuntu server.

Install on macOS

```brew install iperf3```

Install on Ubuntu

```sudo apt update```
```sudo apt install iperf3```

Using iPerf3

One device must operate as the server and the other as a client.

Step 1 - Start iPerf3 on the destination server

```iperf3 -s```

iperf3 uses TCP port 5201 by default, it should be up.

Step 2 - do the test from the source machine

```iperf3 -c x.x.x.x```

x.x.x.x -> IP of the destination server

Test the reverse direction (this test is done from the source also)

```iperf3 -c x.x.x.x -R```

Run a longer test (30 seconds):

```iperf3 -c x.x.x.x -t 30```

Reverse direction:
```iperf3 -c x.x.x.x -t 30 -R```