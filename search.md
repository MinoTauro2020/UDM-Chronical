# user:"alice"

# Búsqueda de eventos relacionados con una dirección IP específica:
source_ip:"192.168.0.1"

# Búsqueda de eventos en un rango de fechas específico:
event_timestamp >= "2022-01-01T00:00:00Z" AND event_timestamp <= "2022-01-31T23:59:59Z"

# Búsqueda de eventos HTTP con un código de estado determinado:
http.status_code:200

# Búsqueda de eventos relacionados con un archivo específico según su hash:
file_hash:"abcdef123456"

# Búsqueda de eventos que contienen un mensaje de error específico:
"error message"

# Búsqueda de eventos relacionados con un tipo de ataque conocido:
attack_type:"SQL injection"

# Búsqueda de eventos que involucran una dirección IP y un puerto específicos:
source_ip:"192.168.0.1" AND destination_port:22

# Búsqueda de eventos que involucran múltiples usuarios:
user:"alice" OR user:"bob"

# Búsqueda de eventos con una cadena específica en cualquier campo:
"sensitive information"

# Buscador
.* en el buscador para filtrar por provedor o darle a la lupa UDM y ahcer la querie
metadata.event_type = "NETWORK_CONNECTION" AND metadata.vendor_name = "Crowdstrike"

To run a raw log search against Windows Event Logs, you can use the following query in Chronicle SIEM:
log_name:"Windows Event Logs"

metadata.product_name:"<product_name>" AND metadata.vendor_name:"<vendor_name>"
metadata.vendor_name = "LimaCharlie" and target.process.file.sha256 !=""


