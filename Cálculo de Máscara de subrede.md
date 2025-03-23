### **Cálculo da Máscara de Subrede**  

A máscara de subrede é um conjunto de bits que define a parte de um endereço IP que pertence à rede e a parte que identifica os hosts dentro dessa rede. O cálculo da máscara de subrede é essencial para definir a divisão de uma rede IP em sub-redes menores, otimizando o uso de endereços IP e melhorando a eficiência da comunicação.

---

### **Estrutura da Máscara de Subrede**  

A máscara de subrede é representada em notação decimal com quatro octetos, assim como os endereços IP. Exemplo de uma máscara de subrede comum:  

```
255.255.255.0
```

Ou em notação CIDR:  
```
/24
```
A quantidade de bits "1" na máscara representa a parte de rede, enquanto os bits "0" indicam a parte de hosts.  

---

### **Passos para o Cálculo da Máscara de Subrede**  

1. **Determinar a Classe do Endereço IP**  
   A classe do endereço IP define a máscara de subrede padrão:  
   - Classe A: **Máscara padrão 255.0.0.0 (/8)**  
   - Classe B: **Máscara padrão 255.255.0.0 (/16)**  
   - Classe C: **Máscara padrão 255.255.255.0 (/24)**  

2. **Definir o Número de Sub-redes ou Hosts Desejados**  
   Dependendo da necessidade, podemos criar sub-redes ou definir a quantidade de hosts por sub-rede.  

3. **Converter a Máscara para Binário**  
   Uma máscara de subrede é composta por uma sequência contínua de bits "1" seguidos por "0".  
   Exemplo da máscara `/26` em binário:  
   ```
   11111111.11111111.11111111.11000000  (255.255.255.192)
   ```
   Neste caso, os primeiros 26 bits são "1" (definindo a rede), e os últimos 6 bits são "0" (definindo os hosts).  

4. **Cálculo do Número de Hosts por Sub-rede**  
   O número de endereços disponíveis para hosts é calculado pela fórmula:  
   ```
   2^(Número de bits 0) - 2
   ```
   O "-2" ocorre porque um endereço é reservado para a rede e outro para o broadcast.  
   Exemplo para a máscara `/26`:  
   ```
   2^(32-26) - 2 = 2^6 - 2 = 64 - 2 = 62 hosts por sub-rede.
   ```

5. **Determinar os Intervalos das Sub-redes**  
   O tamanho de cada sub-rede é dado pelo valor do último octeto onde há bits "0". Para uma máscara `/26` (255.255.255.192), o bloco de endereços cresce de 64 em 64:  
   ```
   192.168.1.0  - Rede  
   192.168.1.1  até 192.168.1.62 - Hosts  
   192.168.1.63 - Broadcast  
   192.168.1.64  - Próxima sub-rede  
   ```

---

### **Exemplo Prático**  
Dado o IP **192.168.10.0/27**, calcular a sub-rede.  

1. Máscara em binário:  
   ```
   11111111.11111111.11111111.11100000  (255.255.255.224)
   ```
2. Bits para hosts = 5 → `2^5 - 2 = 30 hosts por sub-rede`  
3. Bloco de endereços: `224` → Os intervalos crescem de 32 em 32  
   ```
   192.168.10.0 - Rede  
   192.168.10.1 até 192.168.10.30 - Hosts  
   192.168.10.31 - Broadcast  
   192.168.10.32 - Próxima sub-rede  
   ```

---

### **Conclusão**  
O cálculo da máscara de subrede é fundamental para segmentação de redes, possibilitando melhor controle do tráfego e uso eficiente dos endereços IP. Ele envolve a conversão binária da máscara, a determinação dos hosts disponíveis e a definição dos intervalos de sub-redes.