---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/set-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoorRulesEngine.md
ms.openlocfilehash: 7f24d7a7fc027e8d4411b12a3f04d24121af5354
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927184"
---
# <span data-ttu-id="3ab9c-101">Set-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="3ab9c-101">Set-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="3ab9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ab9c-102">SYNOPSIS</span></span>
<span data-ttu-id="3ab9c-103">Aktualisieren eines Regelmoduls</span><span class="sxs-lookup"><span data-stu-id="3ab9c-103">Update a Rules Engine.</span></span>

## <span data-ttu-id="3ab9c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3ab9c-104">SYNTAX</span></span>

### <span data-ttu-id="3ab9c-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3ab9c-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 [-Rule <PSRulesEngineRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3ab9c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ab9c-106">ByObjectParameterSet</span></span>
```
Set-AzFrontDoorRulesEngine -InputObject <PSRulesEngine> [-Rule <PSRulesEngineRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ab9c-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ab9c-107">ByResourceIdParameterSet</span></span>
```
Set-AzFrontDoorRulesEngine -ResourceId <String> [-Rule <PSRulesEngineRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ab9c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3ab9c-108">DESCRIPTION</span></span>
<span data-ttu-id="3ab9c-109">Aktualisieren eines Regelmoduls</span><span class="sxs-lookup"><span data-stu-id="3ab9c-109">Update a Rules Engine.</span></span>

## <span data-ttu-id="3ab9c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3ab9c-110">EXAMPLES</span></span>

### <span data-ttu-id="3ab9c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3ab9c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name myRulesEngine

Name          RulesEngineRules
----          ----------------
myRulesEngine {rules1}

PS C:\> $rulesEngineRule2 = New-AzFrontDoorRulesEngineRuleObject -Name rules2 -Priority 3 -Action $rulesEngineAction
PS C:\AFD\azure-powershell\artifacts\Debug\Az.FrontDoor> Set-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name myRulesEngine -Rule $rulesEngineRule1, $rulesEngineRule2

Name          RulesEngineRules
----          ----------------
myRulesEngine {rules1, rules2}
```

<span data-ttu-id="3ab9c-112">Holen Sie sich eine vorhandene Konfiguration des Regelmoduls, und fügen Sie ihr eine weitere Regel des Regelmoduls hinzu.</span><span class="sxs-lookup"><span data-stu-id="3ab9c-112">Get an existing rules engine configuration and add another rules engine rule to it.</span></span>

## <span data-ttu-id="3ab9c-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3ab9c-113">PARAMETERS</span></span>

### <span data-ttu-id="3ab9c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ab9c-114">-DefaultProfile</span></span>
<span data-ttu-id="3ab9c-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3ab9c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ab9c-116">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="3ab9c-116">-FrontDoorName</span></span>
<span data-ttu-id="3ab9c-117">Name der Eingangstür.</span><span class="sxs-lookup"><span data-stu-id="3ab9c-117">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ab9c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ab9c-118">-InputObject</span></span>
<span data-ttu-id="3ab9c-119">Das zu aktualisierende Regelmodulobjekt.</span><span class="sxs-lookup"><span data-stu-id="3ab9c-119">The Rules Engine object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ab9c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="3ab9c-120">-Name</span></span>
<span data-ttu-id="3ab9c-121">Name des Regelmoduls.</span><span class="sxs-lookup"><span data-stu-id="3ab9c-121">Rules engine name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ab9c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ab9c-122">-ResourceGroupName</span></span>
<span data-ttu-id="3ab9c-123">Der Ressourcengruppenname, in dem die Eingangstür erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="3ab9c-123">The resource group name that the Front Door will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ab9c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ab9c-124">-ResourceId</span></span>
<span data-ttu-id="3ab9c-125">Ressourcen-ID des zu aktualisierende RulesEngine</span><span class="sxs-lookup"><span data-stu-id="3ab9c-125">Resource Id of the RulesEngine to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ab9c-126">-Regel</span><span class="sxs-lookup"><span data-stu-id="3ab9c-126">-Rule</span></span>
<span data-ttu-id="3ab9c-127">Eine Liste von Regeln, die eine bestimmte Konfiguration des Regelmoduls definieren.</span><span class="sxs-lookup"><span data-stu-id="3ab9c-127">A list of rules that define a particular Rules Engine Configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ab9c-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3ab9c-128">-Confirm</span></span>
<span data-ttu-id="3ab9c-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3ab9c-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ab9c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ab9c-130">-WhatIf</span></span>
<span data-ttu-id="3ab9c-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3ab9c-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3ab9c-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3ab9c-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ab9c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ab9c-133">CommonParameters</span></span>
<span data-ttu-id="3ab9c-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ab9c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ab9c-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ab9c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ab9c-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3ab9c-136">INPUTS</span></span>

### <span data-ttu-id="3ab9c-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="3ab9c-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

### <span data-ttu-id="3ab9c-138">System.String</span><span class="sxs-lookup"><span data-stu-id="3ab9c-138">System.String</span></span>

## <span data-ttu-id="3ab9c-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3ab9c-139">OUTPUTS</span></span>

### <span data-ttu-id="3ab9c-140">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="3ab9c-140">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="3ab9c-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3ab9c-141">NOTES</span></span>

## <span data-ttu-id="3ab9c-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3ab9c-142">RELATED LINKS</span></span>
