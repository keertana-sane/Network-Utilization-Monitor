# Network Utilization Monitor using Mininet

##  Objective

To monitor network utilization by measuring bandwidth, packet transmission, and connectivity using Mininet.

---

## 🛠 Tools Used

* Mininet
* Ubuntu VM
* iperf
* ping

---

## 🌐 Network Topology

Single switch with 3 hosts:

```
sudo mn --topo single,3
```

---

## ▶️ Steps to Run

### 1. Start Mininet

```
sudo mn --topo single,3
```

### 2. Test Connectivity

```
pingall
```

### 3. Ping between hosts

```
h1 ping -c 5 h2
```

### 4. Measure Bandwidth (Network Utilization)

Start server on h2:

```
h2 iperf -s &
```

Run client on h1:

```
h1 iperf -c 10.0.0.2
```

---

##  Results

###  Connectivity

* All hosts successfully connected
* 0% packet loss

### 📈 Bandwidth

* Achieved high throughput (~123 Gbits/sec)

---


##  Conclusion

The network utilization was successfully monitored using Mininet. Bandwidth and connectivity between hosts were analyzed using ping and iperf tools.

---

##  Future Scope

* Add real-time graphs
* Integrate Wireshark for packet analysis
* Use SDN controllers for advanced monitoring

