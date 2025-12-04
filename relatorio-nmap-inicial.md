 Relatório Técnico – Varredura Inicial com Nmap

**Autor:** Pedro Tahan  
**Ambiente:** Kali Linux em máquina virtual (VirtualBox – NAT)  
**Ferramenta:** Nmap  

---

## 1. Objetivo

Realizar a primeira varredura de portas utilizando o Nmap, analisando a própria máquina atacante (Kali Linux) para validar conectividade, comportamento da rede e estado padrão das portas TCP em uma instalação limpa.

---

## 2. Procedimentos Executados

### 2.1 Identificação do IP

Usei o comando:

```bash
ip a
Saída registrada em:


2.2 Execução da Varredura
Com o IP identificado, executei:

bash
Copiar código
sudo nmap 10.0.2.15
A saída completa registrada foi:

yaml
Copiar código
Host is up (0.0000050s latency).
All 1000 scanned ports on 10.0.2.15 are in ignored states.
Not shown: 1000 closed tcp ports (reset)
Nmap done: 1 IP address (1 host up) scanned in 0.09 seconds
Evidência:


3. Análise dos Resultados
O host respondeu imediatamente, indicando que a rede NAT está funcional.

As 1000 portas TCP escaneadas estavam fechadas (reset).

Não havia serviços ativos em escuta, comportamento esperado para uma instalação limpa.

O estado ignored/reset demonstra uma superfície mínima de ataque.

Isso confirma que o Kali está totalmente controlado e enxuto.

4. Considerações Técnicas
Em ambientes mínimos, portas fechadas representam segurança inicial.

Nenhum serviço opcional (como SSH) estava ativo por padrão.

A comunicação da VM e o retorno ICMP confirmam integridade do ambiente.

5. Aprendizados da Etapa
Compreendi melhor o funcionamento do Nmap.

Entendi a diferença entre portas abertas, fechadas e filtradas.

Aprendi a interpretar estados como reset.

Fortaleci a noção de “superfície de ataque” e exposição mínima.

Passei a organizar evidências com prints de forma profissional.

Entendi o papel da rede NAT como forma segura de comunicação.

Aprendi a documentar um pequeno laboratório real como um projeto técnico.

6. Conclusão
A varredura inicial demonstrou que a máquina atacante está configurada de forma correta, segura e operacional. A partir desta etapa, o ambiente está pronto para evoluir com novos testes, novas máquinas e análises mais profundas.
