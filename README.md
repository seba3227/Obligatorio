# Instalación de aplicación 'TODO'

Se detallará el paso por paso para la correcta instalación de todo el conjunto de aplicacion y base de datos. 

## 1- Instalar módulo de Python en el controller
```bash
sudo dnf install python3-PyMySQL
```

Colocarse en el directorio del playbook para ejecutar todos .yml 
```bash
cd .\{directorio}\TallerJulio2024
```

## 2- Instalación de Base de datos e importación de base 'todo'

```bash
ansible-playbook -i Inventory/host_vars/servidores.toml database.yml --ask-become-pass
```

## 3- instalacion de los requirements 

```bash
ansible-galaxy collection install -r collections/requirements.yml 
```

## 4- Instalacion de tomcat y aplicacion todo.war

```bash
ansible-playbook -i Inventory/host_vars/servidores.toml instalacion_todo_app.yml --ask-become-pass
```



