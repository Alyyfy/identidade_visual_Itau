# 🎨 Atividade - Guia de Identidade Visual (Itaú)

Este repositório contém as especificações da **Identidade Visual e Style Guide** baseados no ecossistema de design do **Itaú**. O objetivo deste documento é orientar o desenvolvimento de interfaces (UI), garantindo consistência visual, acessibilidade, padronização de cores, tipografia e hierarquia de elementos.

---

## 📌 Sumário
 [🎨 Cores & Paleta de Cores](#-cores--paleta-de-cores)
  - [Laranja (Primária)](#laranja-primária)
  - [Azul (Secundária)](#azul-secundária)
  - [Dark (Escuros / Neutros)](#dark-escuros--neutros)
  - [Light (Claros / Neutros)](#light-claros--neutros)
  - [Success (Sucesso / Feedback Positivo)](#success-sucesso--feedback-positivo)
  - [Danger (Perigo / Feedback Negativo)](#danger-perigo--feedback-negativo)
- [✍️ Tipografia & Escala de Fontes](#️-tipografia--escala-de-fontes)
  - [Escala Tipográfica (Font Scale)](#escala-tipográfica-font-scale)
- [♿ Contraste & Acessibilidade](#-contraste--acessibilidade)
- [🛠️ Como Utilizar no Projeto](#️-como-utilizar-no-projeto)

---

## 🎨 Cores & Paleta de Cores

A paleta foi construída utilizando variações tom sobre tom (`-1`, principal e `+1`) para suportar diferentes estados de interação (hover, active, focus) e garantir feedback visual claro.

### Laranja (Primária)
| Nome | HEX | Descrição / Uso |
| :--- | :--- | :--- |
| **Primário -1** | `#CC4E00` | Variação mais escura (Hover/Focus) |
| **Primário** | `#FF6200` | **Cor principal da marca Itaú** (Botões primários, CTAs) |
| **Primário +1** | `#FF8133` | Variação mais clara (Active/Highlights) |

### Azul (Secundária)
| Nome | HEX | Descrição / Uso |
| :--- | :--- | :--- |
| **Secundário -1** | `#539AE9` | Variação clara de apoio |
| **Secundário** | `#267FE3` | **Cor secundária principal** (Links, elementos interativos) |
| **Secundário +1** | `#1866BE` | Variação escura (Hover/Active) |

### Dark (Escuros / Neutros)
| Nome | HEX | Descrição / Uso |
| :--- | :--- | :--- |
| **Dark +1** | `#403B3B` | Textos secundários, bordas escuras |
| **Dark** | `#262323` | **Texto principal / Body text** |
| **Dark -1** | `#0B0A0A` | Títulos de alto contraste / Backgrounds escuros |

### Light (Claros / Neutros)
| Nome | HEX | Descrição / Uso |
| :--- | :--- | :--- |
| **Light -1** | `#FFFFFF` | Branco puro (Cards, fundos de modais) |
| **Light** | `#F2F5F7` | **Fundo principal de tela (Background)** |
| **Light +1** | `#D3DDE4` | Bordas, divisores e inputs desabilitados |

### Success (Sucesso / Feedback Positivo)
| Nome | HEX | Descrição / Uso |
| :--- | :--- | :--- |
| **Success +1** | `#7BE085` | Destaques sutis de sucesso |
| **Success** | `#52D65F` | **Status positivo / Sucesso / Confirmação** |
| **Success -1** | `#2FC63E` | Variação intensa de sucesso |

### Danger (Perigo / Feedback Negativo)
| Nome | HEX | Descrição / Uso |
| :--- | :--- | :--- |
| **Danger -1** | `#9E1500` | Variação escura / Erro crítico |
| **Danger** | `#D11C00` | **Status de erro / Alertas / Botões destrutivos** |
| **Danger +1** | `#FF2705` | Variação clara de erro |

---

## ✍️ Tipografia & Escala de Fontes

* **Família Tipográfica:** `Poppins` (Sans-serif)
* **Pesos Utilizados:**
  * Light / Regular
  * Medium / SemiBold
  * Bold / ExtraBold

### Escala Tipográfica (Font Scale)

A hierarquia de tamanhos de fonte é definida da seguinte forma:

| Elemento | Tamanho (px) | Exemplo de Aplicação |
| :--- | :--- | :--- |
| **H1** | `40px` | Títulos principais de páginas e dashboards |
| **H2** | `34px` | Títulos de seções |
| **H3** | `28px` | Subseções e cabeçalhos de cards |
| **H4** | `24px` | Títulos de módulos menores / Modais |
| **H5** | `18px` | Destaques no texto / Rótulos em negrito |
| **Parágrafo** | `16px` | **Texto de corpo padrão (Body text)** |
| **Small** | `14px` | Legendas, helpers, tooltips e textos secundários |

---

## ♿ Contraste & Acessibilidade

O estudo de contraste foi realizado testando o comportamento dos tipos de texto sobre diferentes superfícies/fundos:

1. **Fundo Claro (`#F2F5F7` / `#FFFFFF`):**
   * Textos escuros (`Dark`: `#262323`) apresentam contraste ideal (nível AAA).
   * Textos ou títulos em **Laranja (`#FF6200`)** sobre fundo claro devem ser utilizados em pesos maiores (a partir de 24px) para manter boa legibilidade.
2. **Fundo Laranja (`#FF6200`):**
   * Texto em **Branco (`#FFFFFF`)** oferece alto contraste para botões, banners e chamadas principais.
3. **Fundo Escuro (`#0B0A0A`):**
   * Textos em **Laranja (`#FF6200`)** possuem excelente visibilidade para títulos e destaques.

---

## 🛠️ Como Utilizar no Projeto

### Variáveis CSS (Custom Properties)

```css
:root {
  /* Cores Primárias */
  --color-primary-light: #FF8133;
  --color-primary: #FF6200;
  --color-primary-dark: #CC4E00;

  /* Cores Secundárias */
  --color-secondary-light: #539AE9;
  --color-secondary: #267FE3;
  --color-secondary-dark: #1866BE;

  /* Escuros / Neutros */
  --color-dark-light: #403B3B;
  --color-dark: #262323;
  --color-dark-deep: #0B0A0A;

  /* Claros / Neutros */
  --color-light-pure: #FFFFFF;
  --color-light-bg: #F2F5F7;
  --color-light-border: #D3DDE4;

  /* Feedback: Success */
  --color-success-light: #7BE085;
  --color-success: #52D65F;
  --color-success-dark: #2FC63E;

  /* Feedback: Danger */
  --color-danger-dark: #9E1500;
  --color-danger: #D11C00;
  --color-danger-light: #FF2705;

  /* Tipografia */
  --font-family: 'Poppins', sans-serif;
  --font-size-small: 14px;
  --font-size-body: 16px;
  --font-size-h5: 18px;
  --font-size-h4: 24px;
  --font-size-h3: 28px;
  --font-size-h2: 34px;
  --font-size-h1: 40px;
}
```
