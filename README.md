# README — Estrutura em Flexbox

Este documento apresenta uma explicação clara e profissional sobre o uso de **Flexbox** aplicado no código fornecido. Ele destaca as principais classes, propriedades e conceitos que estruturam o layout.

---

## 📌 Objetivo do Código

O projeto constrói uma página de postagens organizada em **cards principais** e uma **barra lateral de posts menores**, utilizando **Flexbox** como base de alinhamento, distribuição e organização visual.

A página é dividida em:

* Cabeçalho com título e botão.
* Conteúdo principal composto por dois cards e um bloco lateral.

---

## 📁 Estrutura Geral do HTML

A estrutura principal da página utiliza as seguintes tags relevantes:

### **1. `<header>`**

Contém o título "Últimas Postagens" e o botão "Todas as Postagens". Essa seção usa Flexbox para alinhamento horizontal.

### **2. `<main>`**

Agrupa todo o conteúdo principal da página.

### **3. `<article>`**

Utilizado para cada card principal. Semântico e apropriado para conteúdo independente.

### **4. `<aside>`**

Usado corretamente para o bloco lateral de posts menores.

---

## 🎨 Organização do Layout com Flexbox

O Flexbox foi aplicado nos seguintes elementos principais:

### **1. `.topo`** — Cabeçalho

```css
display: flex;
justify-content: space-between;
align-items: center;
gap: 10px;
```

**Função:**

* Alinha título e botão na mesma linha;
* Cria espaçamento uniforme entre os elementos.

### **2. `.container`** — Container Geral dos Cards

```css
display: flex;
gap: 30px;
flex-wrap: nowrap;
```

**Função:**

* Posiciona os dois artigos principais e a barra lateral na horizontal;
* Mantém distância constante entre os elementos.

### **3. `.lateral-lista`** — Posts Laterais

```css
display: flex;
flex-direction: column;
gap: 28px;
```

**Função:**

* Organiza cada post lateral verticalmente;
* Garante espaçamento consistente.

### **4. `.post-lateral`** — Estrutura de Cada Item Lateral

```css
display: flex;
gap: 15px;
align-items: flex-start;
```

**Função:**

* Coloca a imagem e o texto lado a lado;
* Mantém desalinhamento natural para leitura.

---

## 🖼️ Estilização de Imagens e Textos

### **Imagens dos artigos principais**

```css
.img1, .img2 {
    width: 378px;
    height: 270px;
    border-radius: 16px;
}
```

### **Imagens dos posts laterais**

```css
.post-lateral img {
    width: 110px;
    height: 80px;
    border-radius: 12px;
    object-fit: cover;
}
```

O uso de **object-fit: cover** garante que a imagem seja exibida sem distorção.

---

## ✒️ Tipografia e Layout Geral

### Reset global

```css
* {
    padding: 0;
    border: 0;
    margin: 0;
    box-sizing: border-box;
    font-family: "manrope";
}
```

Este reset assegura consistência em todo o layout.

### Espaçamentos laterais

A classe `.alinhamento` cria margens internas para centralizar todo o conteúdo:

```css
.alinhamento {
    padding-left: 122px;
    padding-right: 122px;
}
```

---

## 🧩 Componentes Importantes

### Linha separadora lateral

```css
.linha {
    border-top: 1px solid #e0e0e0;
    width: 100%;
}
```

Fornece organização visual na coluna lateral.

### Botão

```css
button.allpost {
    background-color: black;
    color: white;
    border-radius: 16px;
    width: 195px;
    height: 60px;
    cursor: pointer;
}
```

Botão estilizado com design simples e funcional.

---

## 📌 Conclusão

O código utiliza Flexbox de maneira eficiente para criar uma **estrutura limpa, responsiva e organizada**, mesclando:

* alinhamento horizontal e vertical;
* distribuição de espaço adequada;
* uso correto de tags semânticas;
* imagens e textos bem estruturados;
* separadores e espaçamentos consistentes.

Este README serve como documentação técnica clara para manutenção e evolução do projeto.
