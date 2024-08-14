#!/bin/bash

# Версия скрипта
VERSION="1.4"
REPO_URL="https://github.com/Admin90127/hastor.git" # Замените на ваш URL репозитория

# Функция для установки необходимых пакетов
install_packages() {
    echo "Проверка и установка необходимых пакетов..."

    # Список необходимых пакетов
    packages=("iputils-ping" "nmap" "dnsutils" "nikto" "curl" "traceroute" "whois" "tcpdump" "net-tools" "httpie")

    for package in "${packages[@]}"; do
        if ! command -v "$package" &> /dev/null; then
            echo "$package не установлен. Установка..."
            sudo apt-get install -y "$package"
        else
            echo "$package уже установлен."
        fi
    done
}

# Функция для отображения версии инструмента
show_version() {
    command -v "$1" &> /dev/null && "$1" --version || echo "$1 не установлен."
}

# Функция для обновления скрипта
update_script() {
    echo "Обновление скрипта из репозитория $REPO_URL..."
    git pull origin main # Замените "main" на вашу основную ветку, если необходимо
}

# Функция 1: Проверка доступности хоста
check_host() {
    read -p "Введите IP-адрес или доменное имя: " host
    ping -c 4 "$host"
}

# Функция 2: Сканирование открытых портов
scan_ports() {
    read -p "Введите IP-адрес или доменное имя для сканирования портов: " host
    show_version nmap
    nmap "$host"
}

# Функция 3: Извлечение информации о DNS
dns_info() {
    read -p "Введите доменное имя для получения информации о DNS: " domain
    show_version dig
    dig "$domain" ANY
}

# Функция 4: Проверка на уязвимости с помощью nikto
check_vulnerabilities() {
    read -p "Введите URL для проверки на уязвимости (например, http://example.com): " url
    show_version nikto
    nikto -h "$url"
}

# Функция 5: Проверка HTTP-заголовков
check_http_headers() {
    read -p "Введите URL для проверки HTTP-заголовков: " url
    curl -I "$url"
}

# Функция 6: Трассировка маршрута
trace_route() {
    read -p "Введите IP-адрес или доменное имя для трассировки маршрута: " host
    traceroute "$host"
}

# Функция 7: Информация о домене
whois_info() {
    read -p "Введите доменное имя для получения информации WHOIS: " domain
    whois "$domain"
}

# Новая функция: Проверка открытых портов с помощью netcat
check_open_ports() {
    read -p "Введите IP-адрес или доменное имя для проверки открытых портов с помощью netcat: " host
    nc -zv "$host" 1-1024
}

# Новая функция: Отправка HTTP-запроса с помощью httpie
send_http_request() {
    read -p "Введите URL для отправки HTTP-запроса: " url
    http "$url"
}

# Функция 8: Сниффинг трафика (требует sudo)
sniff_traffic() {
    echo "Сниффинг трафика... (нажмите Ctrl+C для остановки)"
    sudo tcpdump -i any -n
}

# Основное меню
install_packages

while true; do
    clear
    echo "Версия скрипта: $VERSION"
    
    echo "Выберите категорию:"
    echo "1. Сетевые утилиты"
    echo "2. Сканирование"
    echo "3. Информация о системе"
    echo "4. HTTP-инструменты"
    echo "5. Трассировка и информация о домене"
    echo "6. Сниффинг трафика"
    echo "7. Обновить скрипт"
    echo "8. Выход"
    
    read -p "Введите номер категории: " category

    case $category in
        1)
            echo "Сетевые утилиты:"
            echo "1. Проверка доступности хоста"
            read -p "Выберите функцию: " func
            if [ "$func" -eq 1 ]; then
                check_host
            fi
            ;;
        2)
            echo "Сканирование:"
            echo "1. Сканирование открытых портов"
            echo "2. Проверка открытых портов с помощью netcat"
            echo "3. Проверка на уязвимости"
            read -p "Выберите функцию: " func
            if [ "$func" -eq 1 ]; then
                scan_ports
            elif [ "$func" -eq 2 ]; then
                check_open_ports
            elif [ "$func" -eq 3 ]; then
                check_vulnerabilities
            fi
            ;;
        3)
            echo "Информация о системе:"
            echo "1. Извлечение информации о

ChatGPT 4 | Midjourney | Gemini | Claude, [14.08.2024 09:08]
DNS"
            read -p "Выберите функцию: " func
            if [ "$func" -eq 1 ]; then
                dns_info
            fi
            ;;
        4)
            echo "HTTP-инструменты:"
            echo "1. Проверка HTTP-заголовков"
            echo "2. Отправка HTTP-запроса"
            read -p "Выберите функцию: " func
            if [ "$func" -eq 1 ]; then
                check_http_headers
            elif [ "$func" -eq 2 ]; then
                send_http_request
            fi
            ;;
        5)
            echo "Трассировка и информация о домене:"
            echo "1. Трассировка маршрута"
            echo "2. Информация WHOIS"
            read -p "Выберите функцию: " func
            if [ "$func" -eq 1 ]; then
                trace_route
            elif [ "$func" -eq 2 ]; then
                whois_info
            fi
            ;;
        6)
            sniff_traffic
            ;;
        7)
            update_script
            ;;
        8)
            echo "Выход..."
            exit 0
            ;;
        *)
            echo "Некорректный выбор, попробуйте снова."
            ;;
    esac

    read -p "Нажмите Enter для продолжения..."
done
