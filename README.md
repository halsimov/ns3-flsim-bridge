# ns3-fl-sim-bridge

Properties in `config.json` in fl-sim project folder 

### Available datasets

DataSet has hard setup in `wifi_exp/fl-server.cc`

 - CIFAR-10
 - FashionMNIST
 - MNIST

### Available Algorithm

You can configure a number of round to go and limit to a certain target accuracy.

 - FedAvg
 - FedAsync

### Clients

You can instantiate an indefinite number of clients but they are all of the same type.
You choose a number of selected clients per Fed round playing on distribution and selection

 - Raspberry Pi 4
 - Raspberry Pi 400

### Network

Communication has only star topology implemented.Communication has only star topology implemented.
You can play on link :
 - `type`  : ethernet / wifi
 - `speed` : min / max / standard deviation

---

## fl-sim Server Attributes

You can find those attributes in `wifi_exp/fl-server.cc`

 - `Data Rate`     : The data rate in on state (default = 1b/s)
 - `Local`         : The Address on which to Bind the rx socket (default = Handled by ns3)
 - `Protocol`      : The type id of the protocol to use for the rx socket (default = UDP)
 - `MaxPacketSize` : The maximum packet size to send to client
 - `Async`         : Decide if client-server communication is asynchronous (default = false)
 - `BytesModel`    : Number of bytes in model
 - `TimeOffset`    : Time offset to add to simulation time reported

### TODO Server

---

## fl-sim Client Attributes

You can find those attributes in `wifi_exp/fl-client-application.cc`

 - `Data Rate`     : The data rate in on state (default = 500kb/s)
 - `MaxPacketSize` : The maximum packet size to send to client
 - `BytesModel`    : Number of bytes in model
 - `BytesSent`     : Number of bytes sent from Client
 - `BytesReceived` : Number of bytes received from server
 - `BeginDownLink` : Time when client start receiving model from server
 - `EndDownLink`   : Time when client finish receiving model from server

### TODO Client