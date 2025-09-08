# ☁️ AWS EC2 Notes – Desafio DIO

![AWS Banner](https://user-images.githubusercontent.com/placeholder/aws-banner.png)

Repositório com **anotações, resumos e práticas** sobre gerenciamento de instâncias **Amazon EC2 (Elastic Compute Cloud)** e serviços relacionados (**EBS, S3, IAM, otimização de custos e segurança**), desenvolvidos durante o **Bootcamp Santander CodeGirls (DIO)**.  

---

## 🎯 Objetivos
- Consolidar conhecimento prático e teórico sobre EC2 e serviços associados.  
- Documentar os **laboratórios da DIO** com exemplos práticos.  
- Servir como **guia de consulta rápida** para estudos, certificações e projetos.  
- Registrar boas práticas, diagramas e reflexões pessoais.  

---

## 📂 Estrutura do Repositório
```
aws-ec2-notes/
│
├── instancias-ec2/         # Conceitos, EBS, otimização e segurança
├── armazenamento-s3/       # Conceitos e ciclo de vida
├── referencias/            # Links e glossário
├── notas.md                # Reflexões pessoais
├── setup.sh                # Script de automação de usuários e grupos IAM
└── README.md               # Este arquivo
```

---

## 🚀 Principais Tópicos

### 🔹 Introdução à AWS
- Lançada em **2006**, hoje a AWS oferece mais de **200 serviços de nuvem**.  
- Modelo de negócios: **OPEX, pay-as-you-go** (pague apenas pelo que usar).  
- Infraestrutura distribuída em **Regiões 🌍** e **Zonas de Disponibilidade (AZs)** para **baixa latência ⚡, redundância 🔁 e alta disponibilidade 🔒**.  

---

### 🔹 Amazon EC2
- Máquinas virtuais na nuvem (Linux ou Windows).  
- Modelo **IaaS (Infraestrutura como Serviço)**: cliente gerencia apps, dados e conexões.  
- **Famílias de instâncias**:
  - Compute optimized ⚡
  - Memory optimized 🧠
  - Storage optimized 💾  
- **Escalabilidade**:
  - Auto Scaling 📈  
  - Elastic Load Balancer ⚖️  

---

### 🔹 Amazon EBS (Elastic Block Store)
- Armazenamento em **blocos persistentes**, anexável a EC2.  
- Expansão rápida (como um HD externo).  
- Usos: **bancos de dados**, **logs** e dados de aplicativos.  

---

### 🔹 Amazon S3 (Simple Storage Service)
- Armazenamento de **objetos** 📂.  
- Escalável 🚀, barato 💸 e seguro 🔒.  
- Classes de storage: Standard, Infrequent Access, Glacier.  
- Regras de ciclo de vida para reduzir custos.  

---

### 🔹 IAM (Identity and Access Management)
- Gerenciamento de **usuários, grupos e permissões**.  
- Grupos criados no laboratório:
  - `GPO-AWS-DataBase` 🛢️  
  - `GPO-AWS-Developer` 👨‍💻  
  - `GPO-AWS-Linux` 🐧  
  - `GPO-AWS-Network` 🌐  
  - `GPO-AWS-SuperUsers` 🦸  
  - `GPOAdministradorAccess` 🛡️  
- Usuários adicionados via **script CLI** → [setup.sh](./setup.sh).  

---

### 🔹 Segurança e Rede
- **Security Groups** como firewalls virtuais (protocolos, portas, IPs).  
- Boas práticas:
  - Restringir portas (SSH/RDP).  
  - Usar **Key Pairs** seguras.  
  - Controlar permissões com IAM.  

---

## 🛠️ Atividades Práticas
1. Criação e configuração da conta AWS 📝  
2. Organização de usuários e grupos no IAM 👥  
3. Implementação de instâncias EC2 🖥️  
4. Configuração de volumes EBS 💾 e buckets S3 📦  
5. Testes de políticas de acesso e permissões 🔒  
6. Documentação do processo neste repositório 📑  
7. Criação de **diagrama de arquitetura no Draw.io** 🗂️  

---

## 🖼️ Diagrama da Arquitetura
<img width="991" height="572" alt="desafio drawio" src="https://github.com/user-attachments/assets/73806212-f3b3-4291-8ad4-5c5a08b61195" />

### Explicação
1. **Usuário final 👤** → envia arquivos para a AWS.  
2. **EC2 🖥️** → processa operações, conectado a EBS e RDS.  
3. **EBS 💾** → volumes principais e backups.  
4. **RDS 🛢️** → banco de dados gerenciado.  
5. **Fluxos 🔀** → Usuário → EC2 → EBS/RDS.  

---

## 💭 Reflexões Pessoais
👉 [notas.md](./notas.md)  

---

## 📖 Glossário
- **EC2** → Elastic Compute Cloud.  
- **EBS** → Elastic Block Store.  
- **S3** → Simple Storage Service.  
- **AMI** → Amazon Machine Image.  
- **IAM** → Identity and Access Management.  
- **On-Demand, Reserved, Spot** → modelos de cobrança do EC2.  

---

## 📌 Referências
- [AWS EC2 Documentation](https://docs.aws.amazon.com/ec2/)  
- [AWS S3 Documentation](https://docs.aws.amazon.com/s3/)  
- [AWS Well-Architected Framework](https://aws.amazon.com/architecture/well-architected/)  
- [AWS Global Infrastructure](https://aws.amazon.com/about-aws/global-infrastructure/)  
- Material de apoio DIO – prof. Alexsandro Lechner  

---

✨ **Autora :** Patricia Oliveira  
📌 Desafio do Bootcamp **Santander CodeGirls - DIO**  

<a href="https://www.linkedin.com/in/savarezi"><img src="https://img.shields.io/badge/-LinkedIn-67cb57?style=for-the-badge&logo=linkedin&logoColor=fff"></a>  

---

✍️ *Repositório em constante atualização conforme avanço nos estudos.*
