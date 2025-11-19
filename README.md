# Termux-vs-code-and-React-Setup-on-android
You can install vs code and React in Termux in Just Few Commands And Enjoy Creating Beautiful and Advance Website on<strong><b>Vs code + React</b></strong>
<img src="1c.png" height="100%" width="100%">

1 :- <p stle="color: red;">command </p>


```bash
<code>nano build-mrb.sh</code>
```



2 :- command 


<code>#!/data/data/com.termux/files/usr/bin/bash
clear

RED="\033[1;31m"
CYAN="\033[1;36m"
BOLD="\033[1m"
RESET="\033[0m"

echo -e "${RED}${BOLD}"
echo "██████╗ ██╗   ██╗██╗██╗     ███╗   ███╗"
echo "██╔══██╗██║   ██║██║██║     ████╗ ████║"
echo "██████╔╝██║   ██║██║██║     ██╔████╔██║"
echo "██╔══██╗██║   ██║██║██║     ██║╚██╔╝██║"
echo "██████╔╝╚██████╔╝██║███████╗██║ ╚═╝ ██║"
echo "╚═════╝  ╚═════╝ ╚═╝╚══════╝╚═╝     ╚═╝"
echo -e "${RESET}"
sleep 1

echo -e "${CYAN}🔥 Creating FINAL MRB Script...${RESET}"
sleep 1

cat << 'EOF' > mrb-ultimate.sh
#!/data/data/com.termux/files/usr/bin/bash
clear

RED="\033[1;31m"
CYAN="\033[1;36m"
YELLOW="\033[1;33m"
BOLD="\033[1m"
RESET="\033[0m"

echo -e "${RED}${BOLD}"
echo "███╗   ███╗██████╗ ██████╗ "
echo "████╗ ████║██╔══██╗██╔══██╗"
echo "██╔████╔██║██║  ██║██║  ██║"
echo "██║╚██╔╝██║██║  ██║██║  ██║"
echo "██║ ╚═╝ ██║██████╔╝██████╔╝"
echo "╚═╝     ╚═╝╚═════╝ ╚═════╝ "
echo -e "${RESET}"

sleep 1
echo -e "${CYAN}🚀 MRB Auto Installer Starting...${RESET}"
sleep 1

progress(){
    for i in $(seq 1 40); do
        echo -ne "${RED}█${RESET}"
        sleep 0.04
    done
    echo ""
}

echo -e "${YELLOW}⚙ Updating Packages...${RESET}"
progress
apt update -y && apt upgrade -y

echo -e "${YELLOW}📦 Installing tur-repo...${RESET}"
progress
pkg install tur-repo -y

echo -e "${YELLOW}📦 Installing Code-Server...${RESET}"
progress
pkg install code-server -y

echo -e "${YELLOW}📦 Installing NodeJS + Git + Yarn...${RESET}"
progress
pkg install nodejs git yarn -y

echo -e "${YELLOW}📦 Installing Create-React-App...${RESET}"
progress
npm install -g create-react-app

echo -e "${CYAN}📁 Creating React Project: myapp...${RESET}"
progress
create-react-app myapp

echo -e "${CYAN}💻 Launching Code-Server...${RESET}"
progress
code-server --auth none --bind-addr 127.0.0.1:8080 &

echo -e "${CYAN}⚡ Starting React Dev Server...${RESET}"
cd ~/myapp
npm start &

echo -e "${RED}${BOLD}"
echo "🎉 MRB ULTIMATE INSTALL DONE!"
echo "🔥 Code-Server @ 127.0.0.1:8080"
echo "🔥 React App @ 127.0.0.1:3000"
echo -e "${RESET}"
EOF

chmod +x mrb-ultimate.sh

echo -e "${RED}${BOLD}✔ DONE!"
echo -e "Run installer with: ./mrb-ultimate.sh${RESET}"</code>





3 :- command 

<code>chmod +x build-mrb.sh</code>




4 :- command 

<code>./build-mrb.sh</code>
