# Bibliotecas Expo - Guia de Uso

## 1. expo-image-picker

### Instalação

```bash
npx expo install expo-image-picker
```

### O que é?

`expo-image-picker` é uma biblioteca do Expo que permite ao aplicativo acessar imagens do dispositivo.

Com ela podemos:

* Escolher imagens da galeria;
* Tirar fotos usando a câmera;
* Criar upload de imagens;
* Adicionar foto de perfil;
* Enviar imagens em publicações.

### Por que usar `npx expo install`?

O comando:

```bash
npx expo install
```

instala a versão da biblioteca compatível com a versão do Expo que o projeto está usando.

Isso evita problemas de incompatibilidade.

---

## Exemplo de uso

### Importar a biblioteca

```javascript
import * as ImagePicker from 'expo-image-picker';
```

### Abrir a galeria e escolher uma imagem

```javascript
async function escolherImagem() {
  const resultado = await ImagePicker.launchImageLibraryAsync({
    mediaTypes: ['images'],
    allowsEditing: true,
    quality: 1,
  });

  if (!resultado.canceled) {
    const imagemSelecionada = resultado.assets[0].uri;

    console.log(imagemSelecionada);
  }
}
```

### Mostrar a imagem escolhida

```javascript
import { Image } from 'react-native';

<Image
  source={{ uri: imagemSelecionada }}
  style={{
    width: 200,
    height: 200
  }}
/>
```

### Exemplo de aplicação real

* Foto de perfil de usuário;
* Cadastro de produtos;
* Rede social;
* Aplicativo de denúncias;
* Envio de documentos.

---

# 2. react-native-paper

### Instalação

```bash
npx expo install react-native-paper
```

### O que é?

`react-native-paper` é uma biblioteca de componentes visuais prontos para React Native.

Ela ajuda a criar interfaces modernas sem precisar criar todos os componentes do zero.

Ela possui:

* Botões;
* Campos de texto;
* Cards;
* Menus;
* Diálogos;
* Switches;
* Barras de progresso.

---

## Exemplo de uso

### Importar um botão

```javascript
import { Button } from 'react-native-paper';
```

### Criar um botão

```jsx
<Button mode="contained">
  Entrar
</Button>
```

Resultado:

Um botão estilizado pronto para usar.

---

## Exemplo usando campo de texto

```javascript
import { TextInput } from 'react-native-paper';
```

```jsx
<TextInput
  label="Email"
  mode="outlined"
/>
```

Resultado:

Um campo de entrada com borda e estilo profissional.

---

# Diferença entre as duas bibliotecas

## expo-image-picker

Serve para:

* Trabalhar com imagens;
* Acessar galeria;
* Usar câmera.

Exemplo:

"Quero deixar o usuário escolher uma foto."

---

## react-native-paper

Serve para:

* Criar componentes de interface;
* Melhorar o design;
* Ter elementos prontos.

Exemplo:

"Quero criar um botão bonito sem programar tudo."

---

# Observação

Se o projeto usar apenas ícones, não é necessário instalar `react-native-paper`.

Para ícones pode usar:

```bash
npx expo install @expo/vector-icons
```

Exemplo:

```javascript
import { Ionicons } from '@expo/vector-icons';

<Ionicons 
  name="home"
  size={30}
  color="blue"
/>
```

---

# Resumo rápido

| Biblioteca         | Função                           |
| ------------------ | -------------------------------- |
| expo-image-picker  | Escolher fotos e usar câmera     |
| react-native-paper | Componentes de interface prontos |
| @expo/vector-icons | Ícones para aplicativos          |

# Comandos guardados

```bash
npx expo install expo-image-picker

npx expo install react-native-paper

npx expo install @expo/vector-icon

```
