Para usar la libreria:
import json

Para abrir el archivo .json como la variable json_example:

with open("json_example.json") as f:
    json_example = f.read()

Para crear un objeto (diccionario) con el archivo json:

json_dict = json.loads(json_example)

Para imprimir un valor del diccionario:

int_name = json_dict["interface"]["name"]
print(int_name)

Para cambiar un valor del diccionario:

json_dict["interface"]["ipv4"]["address"][0]["ip"] = "192.168.0.2"
print(json.dumps(json_dict))

Para devolver el objeto al formato .json:

json.dumps(json_dict)
