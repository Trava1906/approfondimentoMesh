# Approfondimento Tecnico sulle Reti Mesh  

## Introduzione  
Le **reti mesh** sono infrastrutture di rete in cui ogni nodo può trasmettere e ricevere dati, creando una topologia decentralizzata (priva di un nodo centrale).  
Utilizzate in ambiti wireless e wired, permettono comunicazioni robuste e dinamiche senza un punto centrale di guasto.  

---

## Topologie delle Reti Mesh  
Le reti mesh possono essere strutturate in due principali configurazioni:  

### **Full Mesh**
- Ogni nodo è direttamente connesso a tutti gli altri.  
- **Vantaggi**: Massima ridondanza, tolleranza ai guasti elevata.  
- **Svantaggi**: Costo elevato, gestione complessa, overhead di routing.  

### **Partial Mesh**
- Solo alcuni nodi sono connessi direttamente, gli altri si affidano a percorsi alternativi.  
- **Vantaggi**: Bilanciamento tra ridondanza e costo.  
- **Svantaggi**: Minor tolleranza ai guasti rispetto alla full mesh.  

---

## Protocollo di Comunicazione nelle Reti Mesh  
I protocolli di routing in una rete mesh devono gestire instradamento dinamico, tolleranza ai guasti e bilanciamento del carico.  
Alcuni protocolli comuni:  

### **Routing Proattivo (Table-Driven)**
- Ogni nodo mantiene una tabella di routing costantemente aggiornata.  
- **Esempi**:  
  - **OLSR (Optimized Link State Routing)** – Basato su shortest path, utilizzato in reti MANET.  
  - **BATMAN (Better Approach to Mobile Adhoc Networking)** – Sviluppato per reti wireless distribuite.  

### **Routing Reattivo (On-Demand)**
- Le rotte vengono calcolate solo quando necessario per ridurre overhead.  
- **Esempi**:  
  - **AODV (Ad hoc On-Demand Distance Vector)** – Costruisce percorsi solo quando richiesti.  
  - **DSR (Dynamic Source Routing)** – Il pacchetto contiene l'intero percorso fino alla destinazione.  

### **Routing Ibrido**
- Combinazione di protocolli proattivi e reattivi per ottimizzare prestazioni.  
- **Esempio**: **HSRP (Hybrid Wireless Mesh Protocol)**  

---

## Implementazione di una Rete Mesh Wi-Fi  
###  **Dispositivi Necessari**
- **Access Point Mesh** compatibili (es. Google Nest, TP-Link Deco, Ubiquiti AmpliFi).  
- **Controller Mesh** (opzionale) per gestione centralizzata.  

### **Configurazione Base**
1. **Configurare un nodo principale** collegato al router via Ethernet.  
2. **Abilitare il protocollo mesh** (IEEE 802.11s per Wi-Fi Mesh).  
3. **Aggiungere nodi secondari** che si connettono in automatico.  
4. **Ottimizzare la topologia** con algoritmi di bilanciamento del traffico.  

---

## Vantaggi e Svantaggi Tecnici  
### **Vantaggi**
 **Alta Scalabilità** – Aggiungere nodi aumenta la copertura senza cablaggi aggiuntivi.  
 **Tolleranza ai guasti** – Se un nodo si guasta, il traffico viene reindirizzato automaticamente.  
 **Load Balancing** – I protocolli mesh distribuiscono il carico dinamicamente e in maniera automatica.  

### **Svantaggi**
 **Overhead di Routing** – Nelle reti con tanti dispositivi, la gestione delle tabelle di instradamento può causare interferenze.  
 **Interferenza e Congestione** – Troppi nodi wireless possono causare interferenze.  
 **Consumo Energetico Elevato** – I nodi devono essere sempre attivi per il routing.  

---

## Applicazioni delle Reti Mesh  
 **Reti IoT (Internet of Things)** – Zigbee, Z-Wave e LoRaWAN usano mesh per connettere sensori in ambienti industriali.  
 **Wireless Community Networks** – Progetti come **Freifunk** e **Guifi.net** usano mesh per reti cittadine.  
 **Comunicazioni d'emergenza** – Reti mesh sono impiegate in scenari di emergenza per garantire connettività in assenza di strutture fisse.  
 **Reti Mesh Militari** – US Army e NATO utilizzano protocolli mesh per comunicazioni in modo sicuro sul campo.  

---

## Conclusione  
Le reti mesh sono una soluzione per ambienti he hanno bisogno di alta affidabilità e copertura estesa.  
Tuttavia, per garantire prestazioni ottime, è necessario scegliere il giusto protocollo di routing e ottimizzare la gestione della rete per ridurre interferenze.  

---

## Risorse Utili  
 **[IEEE 802.11s Standard](https://standards.ieee.org/standard/802_11s-2011.html)**  
 **[BATMAN Protocol](https://www.open-mesh.org/projects/open-mesh/wiki)**  
 **[AODV Routing](https://tools.ietf.org/html/rfc3561)**  
