Para usar la libreria:
import yaml

Para abrir el archivo .yaml como la variable yaml_example:

with open("yaml_example.yaml") as f:
    yaml_example = f.read()

Para crear un objeto (diccionario) con el archivo yaml:

yaml_dict = yaml.load(yaml_example)

Para imprimir un valor del diccionario:

int_name = yaml_dict["interface"]["name"]
print(int_name)

Para cambiar un valor del diccionario:

yaml_dict["interface"]["ipv4"]["address"][0]["ip"] = "192.168.0.2"
print(yaml.dump(yaml_dict, default_flow_style=False))

Para devolver el objeto al formato .yaml:

yaml.dump(yaml_dict, default_flow_style=False)
