# bandwidth-mininet-analysis

# Bandwidth Measurement using Mininet and iperf

## 📌 Objective
To measure and analyze network bandwidth under different configurations using Mininet and iperf.

---

## 🛠 Tools Used
- Ubuntu OS
- Mininet
- iperf

---

## ⚙️ Setup Instructions

Install Mininet:

sudo apt update
sudo apt install mininet -y


Install iperf:

sudo apt install iperf -y


---

## 🌐 Topology
Single switch with 3 hosts:

sudo mn --topo single,3


---

## 🧪 Experiments

### 1. Normal Throughput

h1 iperf -s &
h2 iperf -c h1


### 2. Parallel Streams

h2 iperf -c h1 -P 4


### 3. Network Delay

sudo mn --topo single,3 --link tc,delay=10ms


### 4. Limited Bandwidth

sudo mn --topo single,3 --link tc,bw=10


---

## 📊 Results

| Scenario | Bandwidth | Observation |
|----------|----------|------------|
| Normal | XX Mbps | Stable |
| Parallel | XX Mbps | Improved |
| Delay | XX Mbps | Reduced |
| Limited | ~10 Mbps | Restricted |

---

## 📸 Screenshots
Screenshots are available in the `/screenshots` folder.

---

## 📈 Analysis
- Parallel streams improve throughput
- Delay reduces performance
- Bandwidth limiting controls speed
- Mininet simulates real network conditions

---

## ✅ Conclusion
The experiment successfully demonstrated how network conditions affect bandwidth using Mininet and iperf.

---

## 👨‍🎓 Author
Manjunatha H J  
SRN: PES1UG24AM157
