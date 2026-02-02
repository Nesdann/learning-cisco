XYZ company is a fast-growing company in Eastern Australia with more than 2 million customers globally.
The company deals with selling and buying of food items, which are basically operated from the
headquarters. The company is intending to open a branch near the local village Bonalbo. Thus, the company
requires young IT graduates to design the network for the branch. The network is intended to operate
separately from the HQ network.
Being a small network, the company has the following requirements during implementation;
a) One router and one switch to be used (all CISCO products).
b) 3 departments (Admin/IT, Finance/HR and Customer service/Reception)
¢) Each department is required to be in different VLANS.
d) Each department is required to have wireless network for the users.
©) Host devices in the network are required to obtain 1Pva address automatically. |.
f) Devices in all the departments are required to communicate with each other.
Assume the ISP gave out a base network of 192.168.1.0, you as the young network engineer who has been
hired, design and implement a network considering the above requirements.

ejercicio de gurutech networking training
voy a modificarlo y hacerlo con 4 departamentos 


no de vlans=4
network:192.168.1.0
para que la network base sea 192.168.1.0 se va a necesitar una mascara
255.255.255.192
ya que 
255.255.255.192 <=> 11111111.11111111.11111111.11000000
                                               ++
esos dos bits mas marcados por ++ van a diferenciar las redes
por lo cual la cantidad de dispositivos conectados va a ser de 2**6
sin contar la ip broadcast ni la inicial ej
192.168.1.0-192.168.1.63
hay 64 direciones ips pero la 192.168.1.0 y la 192.168.1.63 se reservan
inclusive se puede reservar la 192.168.1.1 para el router
si pasamos esto a bits vemos que 
192.168.1.0=11000000.10101000.00000001.00000000
 				       ++
y 
192.168.1.63=11000000.10101000.00000001.00111111
                                        ++
vemos como efectivamente marcan la misma red si sumamos 1 pasa a la siguiente que seria

192.168.1.64= 11000000.10101000.00000001.01000000
                                         ++
lo cual cambia de red se puede hacer esto un total de 4 veces sin modificar la 
red base por lo cual es justo poner 4 departamentos 

ahora como solo tenemos un switch debemos configurar VLANs 
ya que por defecto no vienen separadas
luego configuro el router con el canal trunk
aprendi conf vlans en switch 
conf router para conectar vlans y para un servicio dhcp
