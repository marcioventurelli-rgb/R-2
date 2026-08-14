# R-2 Android App

Um projeto Android básico em Kotlin com Jetpack Compose.

## 📱 Sobre

Este é um projeto Android moderno que usa:
- **Kotlin** como linguagem de programação
- **Jetpack Compose** para UI
- **Material Design 3** para componentes

## 🚀 Download do APK

O APK é gerado automaticamente via **GitHub Actions**. Você pode baixar os builds nos seguintes locais:

### 📥 Baixar APK

1. Vá para a aba **Actions** no repositório
2. Selecione o workflow **Build APK**
3. Procure o run mais recente (com status ✅)
4. Na seção **Artifacts** você encontrará:
   - **app-debug** - Para testes em desenvolvimento
   - **app-release** - Para publicação (versão release)

Ou simplesmente acesse: https://github.com/marcioventurelli-rgb/R-2/actions

## 🛠️ Como funciona o Build Automático

O workflow `.github/workflows/build.yml` faz o seguinte:

- ✅ Detecta qualquer push na branch `main`
- ✅ Configura JDK 11
- ✅ Compila o projeto
- ✅ Gera o APK Debug
- ✅ Gera o APK Release (não assinado)
- ✅ Disponibiliza para download

## 📂 Estrutura do Projeto

```
R-2/
├── .github/
│   └── workflows/
│       └── build.yml          # Workflow de build automático
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── kotlin/com/example/r2/
│   │   │   │   ├── MainActivity.kt
│   │   │   │   └── ui/theme/
│   │   │   ├── res/
│   │   │   │   ├── values/
│   │   │   │   │   ├── strings.xml
│   │   │   │   │   └── themes.xml
│   │   │   └── AndroidManifest.xml
│   ├── build.gradle.kts
│   └── proguard-rules.pro
├── build.gradle.kts
├── settings.gradle.kts
├── gradle.properties
└── README.md
```

## 💻 Instalação do APK em um Dispositivo

### Via ADB (Android Debug Bridge)
```bash
adb install app-debug.apk
```

### Via Gerenciador de Arquivos
1. Transfira o APK para seu dispositivo Android
2. Abra o gerenciador de arquivos
3. Toque no arquivo `.apk`
4. Clique em "Instalar"

## 🔧 Desenvolvimento Local

Se quiser clonar e compilar localmente:

```bash
git clone https://github.com/marcioventurelli-rgb/R-2.git
cd R-2
chmod +x gradlew
./gradlew assembleDebug
```

O APK estará em: `app/build/outputs/apk/debug/app-debug.apk`

## 📝 Licença

Este projeto é de código aberto.

---

**Criado com ❤️ usando Kotlin e Compose**
