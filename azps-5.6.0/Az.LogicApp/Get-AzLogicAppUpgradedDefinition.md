---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: B7FED447-C398-47D7-AF1B-A3E4FDAD0B41
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azlogicappupgradeddefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppUpgradedDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppUpgradedDefinition.md
ms.openlocfilehash: 1be662b88b487fbf79092c30f8bd7277adc9e3cc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947051"
---
# <span data-ttu-id="aca12-101">Get-AzLogicAppUpgradedDefinition</span><span class="sxs-lookup"><span data-stu-id="aca12-101">Get-AzLogicAppUpgradedDefinition</span></span>

## <span data-ttu-id="aca12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aca12-102">SYNOPSIS</span></span>
<span data-ttu-id="aca12-103">Ruft die aktualisierte Definition für eine Logik-App ab.</span><span class="sxs-lookup"><span data-stu-id="aca12-103">Gets the upgraded definition for a logic app.</span></span>

## <span data-ttu-id="aca12-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aca12-104">SYNTAX</span></span>

```
Get-AzLogicAppUpgradedDefinition -ResourceGroupName <String> -Name <String> -TargetSchemaVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aca12-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aca12-105">DESCRIPTION</span></span>
<span data-ttu-id="aca12-106">Das **Cmdlet Get-AzLogicAppUpgradedDefinition** ruft die aktualisierte Definition für die Schemaversion und Logik-App aus einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="aca12-106">The **Get-AzLogicAppUpgradedDefinition** cmdlet gets the upgraded definition for the schema version and logic app from a resource group.</span></span>
<span data-ttu-id="aca12-107">Dieses Cmdlet gibt ein -Objekt zurück, das die Definition der aktualisierten Logik-App darstellt.</span><span class="sxs-lookup"><span data-stu-id="aca12-107">This cmdlet returns an object that represents the definition of the upgraded logic app.</span></span>
<span data-ttu-id="aca12-108">Geben Sie den Namen der Ressourcengruppe, den Namen der Logik-App und die Zielschemaversion an.</span><span class="sxs-lookup"><span data-stu-id="aca12-108">Specify the resource group name, logic app name, and target schema version.</span></span>
<span data-ttu-id="aca12-109">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="aca12-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="aca12-110">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="aca12-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="aca12-111">Um die Namen dynamischer Parameter zu ermitteln, geben Sie nach dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchkreisen.</span><span class="sxs-lookup"><span data-stu-id="aca12-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="aca12-112">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="aca12-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="aca12-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="aca12-113">EXAMPLES</span></span>

### <span data-ttu-id="aca12-114">Beispiel 1: Herunterladen einer aktualisierten Definition einer Logik-App</span><span class="sxs-lookup"><span data-stu-id="aca12-114">Example 1: Get a logic app upgraded definition</span></span>
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

<span data-ttu-id="aca12-115">Der erste Befehl ruft die Definition für die Logik-App ab, die auf die angegebene Zielschemaversion aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="aca12-115">The first command gets the definition for the logic app upgraded to the specified target schema version.</span></span>
<span data-ttu-id="aca12-116">Der Befehl speichert die Definition in der $UpgradedDefinition-Variable.</span><span class="sxs-lookup"><span data-stu-id="aca12-116">The command stores the definition in the $UpgradedDefinition variable.</span></span>
<span data-ttu-id="aca12-117">Der zweite Befehl zeigt den Inhalt der $UpgradedDefinition als Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="aca12-117">The second command displays the contents of $UpgradedDefinition as a string.</span></span>

## <span data-ttu-id="aca12-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="aca12-118">PARAMETERS</span></span>

### <span data-ttu-id="aca12-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aca12-119">-DefaultProfile</span></span>
<span data-ttu-id="aca12-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="aca12-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aca12-121">-Name</span><span class="sxs-lookup"><span data-stu-id="aca12-121">-Name</span></span>
<span data-ttu-id="aca12-122">Gibt den Namen einer Logik-App an.</span><span class="sxs-lookup"><span data-stu-id="aca12-122">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="aca12-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aca12-123">-ResourceGroupName</span></span>
<span data-ttu-id="aca12-124">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="aca12-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="aca12-125">-TargetSchemaVersion</span><span class="sxs-lookup"><span data-stu-id="aca12-125">-TargetSchemaVersion</span></span>
<span data-ttu-id="aca12-126">Gibt die Zielschemaversion der Definition an.</span><span class="sxs-lookup"><span data-stu-id="aca12-126">Specifies the target schema version of the definition.</span></span>

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

### <span data-ttu-id="aca12-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aca12-127">CommonParameters</span></span>
<span data-ttu-id="aca12-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aca12-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aca12-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aca12-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aca12-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="aca12-130">INPUTS</span></span>

### <span data-ttu-id="aca12-131">System.String</span><span class="sxs-lookup"><span data-stu-id="aca12-131">System.String</span></span>

## <span data-ttu-id="aca12-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="aca12-132">OUTPUTS</span></span>

### <span data-ttu-id="aca12-133">System.Object</span><span class="sxs-lookup"><span data-stu-id="aca12-133">System.Object</span></span>

## <span data-ttu-id="aca12-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="aca12-134">NOTES</span></span>

## <span data-ttu-id="aca12-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="aca12-135">RELATED LINKS</span></span>

[<span data-ttu-id="aca12-136">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="aca12-136">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)


