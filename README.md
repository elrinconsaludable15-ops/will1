#!/bin/bash

clear

echo "=================================="
echo "      INSTALADOR WILL1 VPN"
echo "=================================="
echo ""

KEY_CORRECTA="WLFD-8X7K-29QP-LCSM-2026"

read -p "Ingrese su Key: " KEY

if [ "$KEY" != "$KEY_CORRECTA" ]; then
    echo ""
    echo "❌ Key incorrecta"
    exit 1
fi

echo ""
echo "✅ Key válida"
echo "🚀 Iniciando instalación..."
sleep 2

apt update -y
apt upgrade -y

wget --no-check-certificate https://raw.githubusercontent.com/lacasitamx/SCRIPTMOD-LACASITA/master/Instalador/LACASITA.sh

chmod 777 LACASITA.sh
./LACASITA.sh
