Para usar la libreria:
import xmltodict

Para abrir el archivo .xml como la variable xml_example:

with open("xml_example.xml") as f:
    xml_example = f.read()

Para crear un objeto (diccionario) con el archivo xml:

xml_dict = xmltodict.parse(xml_example)

Para imprimir un valor del diccionario:

int_name = xml_dict["interface"]["name"]
print(int_name)

Para cambiar un valor del diccionario:

json_dict["interface"]["ipv4"]["address"]["ip"] = "192.168.0.2"
print(xml.unparse(xml_dict))

Para devolver el objeto al formato .xml:

xml.unparse(xml_dict)
