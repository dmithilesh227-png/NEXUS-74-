#!/bin/bash

# --- NEXUS-74 का शाही बैनर ---
clear
echo -e "\e[1;32m"
echo " ███╗   ██╗███████╗██╗  ██╗██╗   ██╗███████╗"
echo " ████╗  ██║██╔════╝╚██╗██╔╝██║   ██║██╔════╝"
echo " ██╔██╗ ██║█████╗   ╚███╔╝ ██║   ██║███████╗"
echo " ██║╚██╗██║██╔══╝   ██╔██╗ ██║   ██║╚════██║"
echo " ██║ ╚████║███████╗██╔╝ ██╗╚██████╔╝███████║"
echo " ╚═╝  ╚═══╝╚══════╝╚═╝  ╚═╝ ╚═════╝ ╚══════╝"
echo -e "\e[1;36m       BUILDING THE EMPIRE - v1.3 \e[0m"
echo -e "\e[1;33m       Created by: Mithilesh Dubey \e[0m"
echo "--------------------------------------------"

echo "⏳ आपके 'NEXUS' पैकेज का सेटअप शुरू हो रहा है..."

# सिस्टम टूल्स इंस्टॉल करना
pkg update -y
pkg install python tmux sqlite python-lxml clang binutils -y

# पाइथन लाइब्रेरीज़ डालना 
echo "📦 लाइब्रेरीज़ लोड हो रही हैं..."
pip install pyTelegramBotAPI wikipedia
pip install search-engine-parser --no-deps

# आपके दिमाग (bot.py) को डाउनलोड करना
curl -o ~/bot.py https://raw.githubusercontent.com/dmithilesh227-png/-NEXUS-74/main/bot.py

# 🔥 असली 'PKG' कमांड बनाना
echo "python ~/bot.py" > $PREFIX/bin/nexus
chmod +x $PREFIX/bin/nexus

echo -e "\e[1;32m\n✅ बधाई हो! NEXUS-74 पैकेज इंस्टॉल हो गया है।\e[0m"
echo -e "अब आप सिर्फ \e[1;33mnexus\e[0m टाइप करके जादू देख सकते हैं।"

