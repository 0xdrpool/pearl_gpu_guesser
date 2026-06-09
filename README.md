# pearl_gpu_guesser

## **📌 Mining Tutorial**  

### **1️⃣ Mining Pool Address**  
```bash
-p stratum+tcp://pearl.drpool.io:30148
```

### **2️⃣ Latest Miner Releases**  
🔗 **[Download Here](https://github.com/0xdrpool/pearl_gpu_guesser/blob/main/download.md)**  

### **3️⃣ Mining Guide**  

#### **Basic Command**  
```bash
./dr_pearl_prover -p stratum+tcp://pearl.drpool.io:30148 -w drpoolaccount.xxx
```

### **4️⃣ Register a DRPool Account​**  

[drpool register](https://drpool.io/user/register)

### **5️⃣ USE GPU（Option）**

```bash
./dr_neptune_prover -p stratum+tcp://pearl.drpool.io:30148 -w drpoolaccount.xxx -g 0,1,2,3
```

---

### **⚙️ HiveOS**

**New Wallet**

Address input your drpool accountname

<img width="816" height="836" alt="image" src="https://github.com/user-attachments/assets/ce08efeb-0b6b-4475-86d6-3789bb0b8fb1" />


**Add New Flight Sheet**

<img width="1501" height="331" alt="image" src="https://github.com/user-attachments/assets/1906c4e5-14c3-4986-9a4d-a28525ae1b56" />


**Setup Miner Config**

Extra config arguments:
- Miner name: `pearlprover`
- Installation URL: `https://pub-7c2f8935763c410d8897cc0d6379670e.r2.dev/pearlprover-1.0.0.tar.gz`
- Hash algorithm: `----`
- Wallet and worker template: `%WAL%.%WORKER_NAME%`
- Pool URL: `stratum+tcp://pearl.drpool.io:30148`

<img width="815" height="840" alt="image" src="https://github.com/user-attachments/assets/bf5c9ea2-b0c8-4aa6-86d8-1809c5e68fb3" />


**View HiveOS logs**

`tail -f /root/hive/miners/custom/pearlprover/pearlprover.log -n 100`

### **⚙️ Setup on Ubuntu (v18.04+)**  

1. **Get a Mining Address**
   
todo

1. **Download the Miner**  
   - Get the latest `ubuntu-dr_pearl_prover-x.x.x.tar.gz` from **[Download](https://github.com/0xdrpool/pearl_gpu_guesser/blob/main/download.md)**
   ```bash
   # Ubuntu 18.04+
   wget https://pub-7c2f8935763c410d8897cc0d6379670e.r2.dev/ubuntu_20-dr_pearl_prover-1.0.0.tar.gz
   ```
     
2. **Extract & Prepare**  
   ```bash
   tar -zxvf ubuntu-dr_pearl_prover-x.x.x.tar.gz
   cd dr_pearl_prover && chmod +x inner_guesser.sh run_guesser.sh stop_guesser.sh dr_pearl_prover
   ```

3. **Configure Your Account**  
   - Edit `inner_guesser.sh` and update your **[drpool](https://drpool.io) account name**.  

4. **GPU Acceleration**
   - Edit `inner_guesser.sh` and update `./dr_pearl_prover --pool stratum+tcp://pearl.drpool.io:30148 --worker $accountname -g 0`

5. **Start Mining**  
   ```bash
   ./start_guesser.sh
   ```
  
6. **Stop Mining**
   ```bash
   ./stop_guesser.sh
   ```
