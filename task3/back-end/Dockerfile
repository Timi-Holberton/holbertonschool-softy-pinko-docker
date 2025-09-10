FROM ubuntu:latest

# Met à jour et installe python3 + pip3
RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install -y python3 python3-pip

# Supprime la restriction pour installer des paquets Python
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED || true

# Installe Flask
RUN pip3 install flask
RUN pip3 install flask-cors

# Définit le répertoire de travail
WORKDIR /app

# Copie le script Python dans l’image
COPY ./api.py /app/api.py

# Commande de lancement du serveur Flask
CMD ["python3", "api.py"]
