# SocketAPI
Easy Socket(UDP) Creating API for PocketMine Plugin developers. NSFE Codes.

## Documents

##### Create a Socket (in this example, binds on port 19133)

	$port = 19133;
	$socket = \drmyo\SocketAPI\SocketAPI::getInstance()->createSocket($port); //The method SocketAPI::createSocket(int $port) returns \drmyo\SocketAPI\UDPSocket.

##### Send a datapacket to somewhere (to use this, you must create your own socket firs)

	\drmyo\SocketAPI\SocketAPI::getInstance()->getSocket(19133)->sendPacket(new \drmyo\SocketAPI\DataPacket($ip, $port, $data));

##### Handle Received Packet(s)

	public function onSocketReceive(\drmyo\SocketAPI\events\SocketReceiveEvent $event){
		$event->getPacket(); //returns \drmyo\SocketAPI\DataPacet
		//do something you want !
	}

### Apologize for everyone

I'm sorry for providing you deficient informations, also not providing PHPDocs, example plugins. They will be added soon.
