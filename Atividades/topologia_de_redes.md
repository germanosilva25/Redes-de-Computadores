
## 🔹 **1. Topologia em Barramento (Bus)**

* **Como funciona:**
  Todos os dispositivos (computadores, impressoras etc.) ficam conectados a um único cabo principal (barramento).
* **Transmissão:**
  Quando um dispositivo envia dados, todos os outros recebem, mas apenas o destinatário correto processa a informação.
* **Vantagens:**

  * Simples e barata de instalar.
  * Usa menos cabo que outras topologias.
* **Desvantagens:**

  * Se o cabo principal falhar, toda a rede para.
  * Difícil identificar falhas.
  * Baixo desempenho quando há muito tráfego.

---

## 🔹 **2. Topologia em Anel (Ring)**

* **Como funciona:**
  Cada dispositivo está ligado ao próximo, formando um círculo fechado. Os dados circulam em uma única direção (ou dupla, no caso do "anel duplo").
* **Transmissão:**
  A informação passa de um para o outro até chegar ao destino.
* **Vantagens:**

  * O tráfego flui em ordem, evitando colisões.
  * Cada dispositivo tem a mesma oportunidade de transmitir.
* **Desvantagens:**

  * Se um equipamento falhar, a rede inteira pode parar (a menos que seja anel duplo).
  * Dificuldade de adicionar ou remover dispositivos.

---

## 🔹 **3. Topologia em Estrela (Star)**

* **Como funciona:**
  Todos os dispositivos estão conectados a um ponto central (switch ou roteador).
* **Transmissão:**
  Cada comunicação passa obrigatoriamente pelo dispositivo central.
* **Vantagens:**

  * Fácil de instalar e gerenciar.
  * Se um cabo ou dispositivo falhar, não afeta o resto da rede.
  * Alta escalabilidade (pode adicionar mais máquinas facilmente).
* **Desvantagens:**

  * Se o ponto central falhar, toda a rede cai.
  * Requer mais cabos que a topologia em barramento.

---

## 🔹 **4. Topologia em Malha (Mesh)**

* **Como funciona:**
  Cada dispositivo está conectado a vários (ou todos) os outros. Pode ser **parcial** (nem todos interligados) ou **total** (todos interconectados).
* **Transmissão:**
  Há vários caminhos possíveis para os dados chegarem ao destino.
* **Vantagens:**

  * Alta confiabilidade: se um cabo ou dispositivo falhar, os dados encontram outro caminho.
  * Muito robusta e segura.
* **Desvantagens:**

  * Muito cara, pois exige muitos cabos e portas de rede.
  * Complexa de instalar e manter.

---

## 🔹 **5. Topologia em Árvore (Tree)**

* **Como funciona:**
  Estrutura hierárquica semelhante a uma árvore: um nó central (raiz) e ramificações (LANs menores ligadas a switches/roteadores).
* **Transmissão:**
  As informações fluem por diferentes níveis hierárquicos.
* **Vantagens:**

  * Permite segmentar a rede em grupos (departamentos, setores etc.).
  * Fácil de expandir.
* **Desvantagens:**

  * Se a raiz falhar, toda a rede para.
  * Quanto mais profunda a árvore, mais difícil de gerenciar.

---

## 🔹 **6. Topologia Híbrida**

* **Como funciona:**
  Combina duas ou mais topologias (ex.: estrela + anel, estrela + malha).
* **Transmissão:**
  Depende das topologias combinadas.
* **Vantagens:**

  * Flexível, aproveita o melhor de cada topologia.
  * Mais adaptável a diferentes necessidades.
* **Desvantagens:**

  * Custo elevado.
  * Administração complexa.

---
