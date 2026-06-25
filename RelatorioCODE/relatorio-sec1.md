Este projeto apresenta uma auditoria de segurança realizada na aplicação OWASP Juice Shop utilizando técnicas de pentest ofensivo em ambiente local. O objetivo foi identificar vulnerabilidades reais, explorar seus impactos e propor medidas de correção alinhadas às boas práticas de segurança da informação.
Durante a análise, foram identificadas três falhas principais:
SQL Injection (CWE-89 / OWASP A03:2021): permitiu o bypass da autenticação e acesso à conta administrativa sem credenciais válidas.
Reflected XSS (CWE-79 / OWASP A03:2021): possibilitou a execução de código JavaScript arbitrário no navegador do usuário, com potencial para roubo de sessão e ataques de phishing.
Exposição de Dados Sensíveis (OWASP A05:2021): revelou arquivos internos e informações da infraestrutura devido a configurações inadequadas de acesso e exposição de diretórios públicos.
Os testes foram realizados com Docker, Burp Suite e navegador Chromium integrado, seguindo uma metodologia composta por enumeração, exploração e documentação das vulnerabilidades encontradas.
Como resultado, foram propostas medidas de mitigação como uso de Prepared Statements, sanitização de entradas e saídas, implementação de Content Security Policy (CSP), controle de acesso adequado e remoção de informações sensíveis expostas publicamente.
