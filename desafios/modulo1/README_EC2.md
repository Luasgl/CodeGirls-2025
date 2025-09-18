# ☁️ AWS EC2 Notes – Desafio DIO

Repositório com **anotações, resumos e práticas** sobre gerenciamento de instâncias **Amazon EC2 (Elastic Compute Cloud)** e serviços relacionados (**EBS, S3, IAM, otimização de custos e segurança**), desenvolvidos durante o **Bootcamp Santander CodeGirls (DIO)**.  

---

## 🎯 Objetivos
- Consolidar conhecimento prático e teórico sobre EC2 e serviços associados.  
- Documentar os **laboratórios da DIO** com exemplos práticos.  
- Servir como **guia de consulta rápida** para estudos, certificações e projetos.  
- Registrar boas práticas, diagramas e reflexões pessoais.  

---

## 🚀 Principais Tópicos

### 🔹 Introdução à AWS
- Lançada em **2006**, hoje a AWS oferece mais de **200 serviços de nuvem**.  
- Modelo de negócios: **OPEX, pay-as-you-go** (paga apenas pelo que usar).  
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
7. Criação de um diagrama de arquitetura no Draw.io para representar a solução de computação em nuvem AWS.

---

### 🔹 Desafio 1: Diagrama de Arquitetura de vizualização de Interação entre Serviços AWS:
📚 Cenário: Instituição de Ensino com Dados Acadêmicos
Contexto
A instituição precisa armazenar arquivos de alunos e professores (trabalhos, provas digitalizadas, planilhas de notas).
Os alunos enviam seus arquivos via portal acadêmico.
Esses arquivos são processados automaticamente (validação, categorização e backup).
Professores e administradores podem acessar os dados já organizados.

🏗️ Arquitetura Explicada

1. Usuário (Aluno/Professor) 👩‍🎓👨‍🏫
  Faz upload de um trabalho ou relatório no portal acadêmico (aplicação hospedada em EC2).
2. Amazon S3 (Storage) 📦
  Recebe os arquivos enviados e guarda de forma escalável.
  Exemplo: s3://dados-academicos/universidade/alunos/2025/

3. AWS Lambda (Processamento Serverless) ⚡
  Disparada automaticamente quando um arquivo chega no S3.
  Tarefas:
    Validar o formato do arquivo (PDF, DOCX).
    Gerar metadados (aluno, disciplina, semestre).
    Criar uma versão compactada para economizar espaço.

4. Amazon EC2 (Aplicação Acadêmica) 🖥️
  Hospeda o sistema web acadêmico.
  Professores acessam relatórios e notas.
  Pode ser chamado pela Lambda quando o processamento for mais pesado (ex.: análises estatísticas sobre desempenho dos alunos).

5. S3 (Dados organizados) 📦
  Arquivos finais (validados e processados) ficam disponíveis para consulta pelo sistema.

[!(desafios/modulo1/aws_EC2_S3.drawio.png)]

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

✨ **Autora: Luane Gonçalves Silva 

📌 Desafio 1 do Bootcamp **Santander CodeGirls - 2025**  

✍️ *Repositório em constante atualização conforme avanço nos estudos.*
