---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: B7FED447-C398-47D7-AF1B-A3E4FDAD0B41
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicappupgradeddefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppUpgradedDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppUpgradedDefinition.md
ms.openlocfilehash: 2c0eb437aaa8a280b970e9c2a210b37b8fbce2d8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180358"
---
# <span data-ttu-id="07f0a-101">Get-AzLogicAppUpgradedDefinition</span><span class="sxs-lookup"><span data-stu-id="07f0a-101">Get-AzLogicAppUpgradedDefinition</span></span>

## <span data-ttu-id="07f0a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="07f0a-102">SYNOPSIS</span></span>
<span data-ttu-id="07f0a-103">Ruft die aktualisierte Definition für eine Logik-App ab.</span><span class="sxs-lookup"><span data-stu-id="07f0a-103">Gets the upgraded definition for a logic app.</span></span>

## <span data-ttu-id="07f0a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="07f0a-104">SYNTAX</span></span>

```
Get-AzLogicAppUpgradedDefinition -ResourceGroupName <String> -Name <String> -TargetSchemaVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07f0a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="07f0a-105">DESCRIPTION</span></span>
<span data-ttu-id="07f0a-106">Das Cmdlet " **Get-AzLogicAppUpgradedDefinition** " Ruft die aktualisierte Definition für die Schemaversion und die Logik-App aus einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="07f0a-106">The **Get-AzLogicAppUpgradedDefinition** cmdlet gets the upgraded definition for the schema version and logic app from a resource group.</span></span>
<span data-ttu-id="07f0a-107">Dieses Cmdlet gibt ein Objekt zurück, das die Definition der aktualisierten Logik-APP darstellt.</span><span class="sxs-lookup"><span data-stu-id="07f0a-107">This cmdlet returns an object that represents the definition of the upgraded logic app.</span></span>
<span data-ttu-id="07f0a-108">Geben Sie den Namen der Ressourcengruppe, den Logik-APP-Namen und die Zielschema Version an.</span><span class="sxs-lookup"><span data-stu-id="07f0a-108">Specify the resource group name, logic app name, and target schema version.</span></span>
<span data-ttu-id="07f0a-109">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="07f0a-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="07f0a-110">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="07f0a-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="07f0a-111">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="07f0a-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="07f0a-112">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="07f0a-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="07f0a-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="07f0a-113">EXAMPLES</span></span>

### <span data-ttu-id="07f0a-114">Beispiel 1: Abrufen einer aktualisierten Definition für eine Logik-App</span><span class="sxs-lookup"><span data-stu-id="07f0a-114">Example 1: Get a logic app upgraded definition</span></span>
```
PS C:\>$UpgradedDefinition = Get-AzLogicAppUpgradedDefinition -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -TargetSchemaVersion "2016-06-01"
$UpgradedDefinition.ToString()
{

  "$schema": "http://schema.management.azure.com/providers/Microsoft.Logic/schemas/2016-06-01/workflowdefinition.json#",

  "contentVersion": "1.0.0.0",

  "parameters": {},

  "triggers": {

    "httpTrigger": {

      "recurrence": {

        "frequency": "Hour",

        "interval": 1

      },

      "type": "Http",

      "inputs": {

        "method": "GET",

        "uri": "http://www.bing.com"

      },

      "conditions": [

        {

          "expression": "@bool('true')" 

        }

      ] 

    },

    "manualTrigger": {

      "type": "Request",

      "kind": "Http"

    }

  },

  "actions": {

    "httpScope": {

      "actions": {

        "http": {

          "runAfter": {},

          "type": "Http",

          "inputs": {

            "method": "GET",

            "uri": "http://www.bing.com"

          }

        }

      },

      "runAfter": {},

      "else": {

        "actions": {}

      },

      "expression": "@bool('true')", 

      "type": "If"

    },

    "http1Scope": {

      "actions": {

        "http1": {

          "runAfter": {},

          "type": "Http",

          "inputs": {

            "method": "GET",

            "uri": "http://www.bing.com"

          }

        }

      },

      "runAfter": {},

      "else": {

        "actions": {}

      },

      "expression": "@bool('true')", 

      "type": "If"

    }

  },

  "outputs": {

    "output1": {

      "type": "String",

      "value": "true"

    }

  }

}
```

<span data-ttu-id="07f0a-115">Der erste Befehl ruft die Definition für die Logik-App ab, die auf die angegebene Zielschema Version aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="07f0a-115">The first command gets the definition for the logic app upgraded to the specified target schema version.</span></span>
<span data-ttu-id="07f0a-116">Der Befehl speichert die Definition in der $UpgradedDefinition-Variablen.</span><span class="sxs-lookup"><span data-stu-id="07f0a-116">The command stores the definition in the $UpgradedDefinition variable.</span></span>
<span data-ttu-id="07f0a-117">Der zweite Befehl zeigt den Inhalt von $UpgradedDefinition als Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="07f0a-117">The second command displays the contents of $UpgradedDefinition as a string.</span></span>

## <span data-ttu-id="07f0a-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="07f0a-118">PARAMETERS</span></span>

### <span data-ttu-id="07f0a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07f0a-119">-DefaultProfile</span></span>
<span data-ttu-id="07f0a-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="07f0a-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07f0a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="07f0a-121">-Name</span></span>
<span data-ttu-id="07f0a-122">Gibt den Namen einer Logik-APP an.</span><span class="sxs-lookup"><span data-stu-id="07f0a-122">Specifies the name of a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07f0a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07f0a-123">-ResourceGroupName</span></span>
<span data-ttu-id="07f0a-124">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="07f0a-124">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07f0a-125">-TargetSchemaVersion</span><span class="sxs-lookup"><span data-stu-id="07f0a-125">-TargetSchemaVersion</span></span>
<span data-ttu-id="07f0a-126">Gibt die Zielschema Version der Definition an.</span><span class="sxs-lookup"><span data-stu-id="07f0a-126">Specifies the target schema version of the definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07f0a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07f0a-127">CommonParameters</span></span>
<span data-ttu-id="07f0a-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07f0a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07f0a-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07f0a-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07f0a-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="07f0a-130">INPUTS</span></span>

### <span data-ttu-id="07f0a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="07f0a-131">System.String</span></span>

## <span data-ttu-id="07f0a-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="07f0a-132">OUTPUTS</span></span>

### <span data-ttu-id="07f0a-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="07f0a-133">System.Object</span></span>

## <span data-ttu-id="07f0a-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="07f0a-134">NOTES</span></span>

## <span data-ttu-id="07f0a-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="07f0a-135">RELATED LINKS</span></span>

[<span data-ttu-id="07f0a-136">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="07f0a-136">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)


