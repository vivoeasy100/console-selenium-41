# Automação Web com Selenium - Exercício Prático

## 📋 Informações do Aluno
- **Nome:** Fernando Almeida
- **RA:** 326132695

## 📚 Informações da Matéria
- **Disciplina:** Tecnologia .NET / Automação de Testes
- **Professor:** Daniel Henrique Matos de Paiva
- **Data:** Novembro 2026

## 🛠️ Tecnologias Utilizadas
| Tecnologia | Versão |
|------------|--------|
| .NET SDK | 10.0 |
| Selenium.WebDriver | 4.52.0 |
| MSTest | 4.0.2 |
| C# | 13 (latest) |
| ChromeDriver | Compatível com Chrome instalado |

## 🏗️ Estrutura do Projeto
```
ConsoleSelenium41/
├── ConsoleSelenium/           # Projeto Console (aplicação principal)
│   ├── ConsoleSelenium.csproj
│   └── Program.cs
├── ConsoleSelenium.Tests/     # Projeto de Testes (MSTest)
│   ├── ConsoleSelenium.Tests.csproj
│   ├── MSTestSettings.cs
│   └── Test1.cs
├── ConsoleSelenium41.slnx     # Solution file
└── README.md
```

## 🎯 Objetivo do Exercício
Automatizar o preenchimento e envio de um formulário web utilizando Selenium WebDriver com C#.

## 🌐 URL de Teste
```
https://www.selenium.dev/selenium/web/web-form.html
```

## 📝 Valores do Teste
| Campo | Seletor | Valor |
|-------|---------|-------|
| Caixa de texto | `By.Name("my-text")` | `"Daniel o melhor professor da minha vida"` |
| Botão Submit | `By.TagName("button")` | Click |
| Mensagem de sucesso | `By.Id("message")` | Validação: contém `"Received"` |

## ⚙️ Como Executar

### Pré-requisitos
- [.NET 10 SDK](https://dotnet.microsoft.com/download/dotnet/10.0)
- Google Chrome instalado
- ChromeDriver compatível (gerenciado automaticamente pelo Selenium 4+)

### Restaurar dependências
```bash
dotnet restore
```

### Compilar
```bash
dotnet build
```

### Executar aplicação console
```bash
dotnet run --project ConsoleSelenium/ConsoleSelenium.csproj
```

### Executar testes
```bash
dotnet test ConsoleSelenium.Tests/ConsoleSelenium.Tests.csproj
```

## 📦 Pacotes NuGet Instalados

### ConsoleSelenium
```xml
<PackageReference Include="Selenium.WebDriver" Version="4.52.0" />
```

### ConsoleSelenium.Tests
```xml
<PackageReference Include="MSTest" Version="4.0.2" />
```

## 🧪 Cenário de Teste Implementado

### `Automatizar_Envio_Texto_ComSucesso()`
1. Inicializa ChromeDriver
2. Navega para `https://www.selenium.dev/selenium/web/web-form.html`
3. Captura e exibe o título da página
4. Configura `ImplicitWait` de 2 segundos
5. Localiza campo de texto por `Name="my-text"`
6. Envia texto: `"Daniel o melhor professor da minha vida"`
7. Localiza botão submit por `TagName="button"`
8. Clica no botão
9. Localiza mensagem de resultado por `Id="message"`
10. Valida se mensagem contém `"Received"` (Assert.Contains)
11. Finaliza driver (Quit)

## 📚 Referências
- [Selenium WebDriver Documentation](https://www.selenium.dev/documentation/webdriver/)
- [Selenium Web Form Demo](https://www.selenium.dev/selenium/web/web-form.html)
- [MSTest Documentation](https://learn.microsoft.com/dotnet/core/testing/unit-testing-with-mstest)

---

**Desenvolvido por:** Fernando Almeida (RA: 326132695)  
**Orientação:** Prof. Daniel Henrique Matos de Paiva