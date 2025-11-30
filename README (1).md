# 📘 ZeusLib --- Documentação Oficial Completa

## 🌩️ Sobre

ZeusLib é uma biblioteca para criação de interfaces gráficas no Roblox.\
Ela oferece ferramentas simples e poderosas para criar janelas, abas,
botões, toggles, sliders, dropdowns, textbox, seções, labels e
notificações, além de suportar salvamento automático de configurações.

## 📦 Instalação

``` lua
local ZeusLib = loadstring(game:HttpGet("https://pastefy.app/TfCN9JhU/raw"))()
```

## 🪟 Criando a Janela Principal

``` lua
local Window = ZeusLib:MakeWindow({
    Name = "Zeus Library",
    HidePremium = false,
    SaveConfig = true,
    ConfigFolder = "ZeusLib"
})
```

## 📑 Criando Abas

``` lua
local Tab = Window:MakeTab({
    Name = "Geral",
    Icon = "rbxassetid://3926305904"
})
```

## 🧩 Componentes

### 🔘 Botão

``` lua
Tab:AddButton({
    Name = "Executar Ação",
    Callback = function()
        print("Clicado")
    end
})
```

### 🎚️ Toggle

``` lua
Tab:AddToggle({
    Name = "Ativar Sistema",
    Default = false,
    Save = true,
    Flag = "SistemaAtivo",
    Callback = function(v)
        print(v)
    end
})
```

### 📏 Slider

``` lua
Tab:AddSlider({
    Name = "Velocidade",
    Min = 1,
    Max = 100,
    Default = 16,
    Increment = 1,
    Color = Color3.fromRGB(0, 170, 255),
    Save = true,
    Flag = "Speed",
    Callback = function(v)
        print(v)
    end
})
```

### 📝 TextBox

``` lua
Tab:AddTextbox({
    Name = "Digite algo",
    Placeholder = "Texto...",
    Save = true,
    Flag = "UserText",
    Callback = function(text)
        print(text)
    end
})
```

### 📥 Dropdown

``` lua
Tab:AddDropdown({
    Name = "Escolha uma opção",
    Options = {"A", "B", "C"},
    Default = "A",
    Save = true,
    Flag = "Dropdown1",
    Callback = function(option)
        print(option)
    end
})
```

### 🏷️ Label

``` lua
local label = Tab:AddLabel("Carregando...")
label:Set("Pronto!")
```

### 📦 Section

``` lua
Tab:AddSection("Configurações Avançadas")
```

### 🔔 Notificações

``` lua
ZeusLib:MakeNotification({
    Title = "Aviso",
    Content = "Operação concluída.",
    Time = 4
})
```

## ⚙️ Funções do Window

``` lua
Window:ToggleUI()
Window:Destroy()
```

## 📌 Exemplo Completo

``` lua
local ZeusLib = loadstring(game:HttpGet("https://pastefy.app/TfCN9JhU/raw"))()

local Window = ZeusLib:MakeWindow({
    Name = "Zeus Library",
    HidePremium = false,
    SaveConfig = true,
    ConfigFolder = "ZeusLib"
})

local Tab = Window:MakeTab({
    Name = "Menu",
    Icon = "rbxassetid://3926305904"
})

Tab:AddSection("Funções")

Tab:AddButton({
    Name = "Executar",
    Callback = function()
        print("Executado")
    end
})

Tab:AddToggle({
    Name = "Ativar X",
    Default = false,
    Save = true,
    Flag = "T1",
    Callback = function(v)
        print(v)
    end
})
```

## 📣 Créditos

Desenvolvido por VITOR HUGO.
