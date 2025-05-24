## 📚 Seções
<h4 align="left"><a href="https://github.com/caroolps/QA-AS2-Group">INÍCIO</a></h4>
<h4 align="left"><a href="https://github.com/caroolps/AUTOMATIZADO/blob/main/README.md">TESTES AUTOMATIZADOS</a></h4>


## 📋 Plano de Teste

Este plano de teste descreve os cenários e condições a serem validados no projeto XXX para garantir o correto funcionamento das funcionalidades.


## 1. Introdução
- **Objetivo:**  
  Breve descrição do propósito do plano de testes.
- **Escopo:**  
  O que será testado (funcionalidades, módulos, integrações) e o que está fora do escopo.
- **Referências:**  
  Documentos, requisitos, especificações usadas como base.

## 2. Estratégia de Testes
- **Tipos de Testes:**  
  Exemplos: testes funcionais, testes de regressão, testes de integração, testes de performance, etc.
- **Níveis de Teste:**  
  Teste unitário, teste de sistema, teste de aceitação.
- **Ferramentas:**  
  Ferramentas utilizadas (ex: Selenium, JUnit, Postman, etc).
- **Ambiente de Teste:**  
  Descrição do ambiente (hardware, software, configurações, rede).

## 3. Itens a Testar
- Lista das funcionalidades, módulos, APIs ou componentes que serão testados.

## 4. Itens Fora do Escopo
- Lista do que não será testado e o motivo.

## 5. Critérios de Aceitação e Saída
- **Critérios de Aceitação:**  
  Condições que devem ser atendidas para considerar o teste aprovado.
- **Critérios de Saída:**  
  Quando o ciclo de testes será considerado concluído.

## 6. Plano de Execução dos Testes
- **Cronograma:**  
  Datas e etapas de execução.
- **Responsáveis:**  
  Equipe envolvida e suas funções.

## 7. 🧪 Casos de Teste


### 01 - Caso de Teste: Validação da visualização dos projetos abertos

**Rastreabilidade do requisito**: 1 e 2  
**Objetivo**: O app deve listar apenas os projetos abertos e seus donos

## Passos do Teste

| **Step** | **Action** | **Results** |
|----------|------------|-------------|
| 1 | Acessar o aplicativo com o perfil "Dono do produto" | O app direciona o usuário para a tela inicial com as seguintes características: <br> - Lista de projetos <br> - Approvals <br> - Reporting <br> - Gcraft Master File |
| 2 | Acessar a lista de projetos | O app deve apresentar todos os projetos cadastrados no aplicativo |
| 3 | Acessar a seção de "Filtros" > Status do projeto e selecionar a opção "aberto" | O app deve listar todos os projetos que estão abertos |
| 4 | Clicar no projeto | O app deve mostrar o responsável pelo projeto |



## 8. Riscos e Mitigações
- Possíveis riscos que podem impactar o teste e como planejar para mitigá-los.

## 9. Relatórios e Registro de Defeitos
- Como será feito o registro de bugs (ferramenta, formato).  
- Frequência e formato dos relatórios de status.

## 10. Aprovações
- Quais stakeholders precisam aprovar o plano e a execução dos testes.


---




