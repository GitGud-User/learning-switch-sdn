# SDN Learning Switch using POX & Mininet

## 📌 Objective

Implement a controller that mimics a learning switch by dynamically learning MAC addresses and installing forwarding rules.

---

## ⚙️ Technologies Used

* Mininet
* POX Controller
* Open vSwitch

---

## 🚀 How to Run

### 1. Start Controller

```
cd pox
./pox.py openflow.of_01 forwarding.l2_learning
```

### 2. Start Mininet

```
sudo mn --topo single,3 --mac --controller remote,port=6633
```

### 3. Test

```
pingall
h1 ping h2
h1 ping h2
```

### 4. Check Flow Table

```
sudo ovs-ofctl dump-flows s1
```

---

## 🔍 Features Demonstrated

### ✅ MAC Address Learning

* Controller learns MAC → Port mapping dynamically

### ✅ Dynamic Flow Rule Installation

* Flow entries installed in switch after learning

### ✅ Packet Forwarding Validation

* Successful communication between hosts (0% loss)

### ✅ Flow Table Inspection

* Verified using `ovs-ofctl dump-flows`

---

## 📸 Screenshots

(Uploaded 4 images in Screenshots folder)

---

## 🧠 Key Concept

Initially packets are flooded. After learning MAC addresses, flow rules are installed and packets are forwarded directly.

---

## 📌 Conclusion

Successfully implemented and verified a learning switch using SDN principles.
