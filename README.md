# 🚀 AWS Scalable Web Deployment — EC2 + Auto Scaling + Load Balancer

Este projeto foi desenvolvido como parte do meu processo de aprendizado em **Cloud Computing** e **arquiteturas escaláveis** na AWS.  
O objetivo foi transformar um simples site estático hospedado no GitHub Pages em um **ambiente de alta disponibilidade**, **balanceado** e **escalável automaticamente**, utilizando apenas serviços dentro do **Free Tier da AWS**.

---

## 🧩 Objetivo

Construir uma infraestrutura **resiliente e escalável** na AWS capaz de:

- Hospedar um site estático via EC2 com Nginx.  
- Balancear tráfego HTTP automaticamente com o **Application Load Balancer (ALB)**.  
- Redimensionar instâncias conforme a demanda via **Auto Scaling Group (ASG)**.  
- Garantir **alta disponibilidade** entre múltiplas zonas (AZs).  

---

## ⚙️ Arquitetura

A solução implementada é composta por:

- **Amazon EC2** → Servidor web com Nginx e site hospedado.  
- **Launch Template** → Modelo de inicialização das instâncias.  
- **Auto Scaling Group (ASG)** → Ajuste automático de capacidade.  
- **Application Load Balancer (ALB)** → Distribuição automática de tráfego HTTP.  
- **Target Group** → Encaminha o tráfego e realiza health checks.  
- **Health Checks** → Monitoramento contínuo das instâncias.  

📍 **Região:** us-east-1  
📍 **AZs:** us-east-1a, us-east-1b  
📍 **VPC:** default  

---

## 🧠 Etapas de Implementação

1. **Hospedagem inicial** do site no GitHub.  
2. **Criação da instância EC2** e instalação do Nginx.  
3. **Configuração do Launch Template** (`nginx-webserver-template`).  
4. **Criação do Application Load Balancer** (`nginx-alb`).  
5. **Criação do Target Group** (`nginx-target-group`).  
6. **Implementação do Auto Scaling Group** (`nginx-asg`).  
7. **Testes de Resiliência** — desligar manualmente instâncias e validar a criação automática de novas.  

---

## 🧩 Desafios e Soluções

- ⚠️ **Atualização inesperada** do curso AWS Cloud Practitioner Essentials durante o aprendizado.  
- 🛠️ Problemas de roteamento e “Unhealthy” resolvidos ajustando **path `/`** e **Security Groups**.  
- 💰 Ajuste do **ASG** para respeitar limites do Free Tier (1 instância mínima, 2 máxima).  

Cada obstáculo representou uma oportunidade real de aprendizado prático.  

---

## 🧠 Lições Aprendidas

- A prática é o verdadeiro caminho para dominar AWS.  
- Ler a **documentação oficial** da AWS é indispensável.  
- Ferramentas como **ChatGPT (GPT-5)** ajudam a resolver dúvidas técnicas de forma contextual.  
- **Resiliência** é essencial: configurar corretamente demanda paciência e ajustes contínuos.  

⏱️ **Tempo total de execução:** 8 horas (do deploy no GitHub à configuração final).  

---

## 🌐 Demonstração Online

A aplicação está ativa e acessível via **Load Balancer da AWS**:  
🔗 [Acesse aqui o site funcionando](https://lnkd.in/dPknK7ai)

---

## 📘 Tecnologias Utilizadas

- AWS EC2  
- AWS Auto Scaling Group  
- AWS Application Load Balancer  
- AWS Target Groups  
- AWS VPC  
- Nginx  
- GitHub Pages  

---

## 📸 Diagrama da Arquitetura

![AWS Architecture Diagram](https://github.com/romariodomingos/aws-scalable-deploy-ec2-asg-alb/blob/main/Architecture-Diagram.png?raw=true)

---

## 👨🏽‍💻 Autor

**Romão Gando Domingos**  
AWS Cloud Enthusiast ☁️ | Cloud | Finance Analytics | Computer Engineering Student | Project Management
🔗 [LinkedIn](https://www.linkedin.com/in/rom%C3%A3o-domingos-948003217/)  

---

## 📜 Licença

Distribuído sob a licença MIT. Consulte `LICENSE` para mais informações.

---

