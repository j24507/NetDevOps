Para usar la libreria:
import csv

csv.reader() trata los datos csv como listas

#El with block es un context handeler, va a cerrar el archivo una vez terminado

with open("csv_example.csv") as f:
    csv_python = csv.reader(f)

    # Loop over each row in csv and leverage the date in code
    for row in csv_python:
      print("{device} is in {location} " \
      "and has IP {ip}.".format(
          device = row[0],
          location = row[2],
          ip = row[1]
          )
        )
