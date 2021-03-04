---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
ms.openlocfilehash: 05248a299b907c74f43edddb7caf18697794dc08
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928104"
---
# <span data-ttu-id="e0557-101">New-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="e0557-101">New-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="e0557-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0557-102">SYNOPSIS</span></span>
<span data-ttu-id="e0557-103">Erstellen Sie eine neue Konfiguration des Regelmoduls für eine angegebene Eingangstür.</span><span class="sxs-lookup"><span data-stu-id="e0557-103">Create a new rules engine configuration for a specified front door.</span></span> 

## <span data-ttu-id="e0557-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e0557-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 [-Rule <PSRulesEngineRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e0557-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e0557-105">DESCRIPTION</span></span>
<span data-ttu-id="e0557-106">Erstellen Sie eine neue Konfiguration des Regelmoduls für eine angegebene Eingangstür.</span><span class="sxs-lookup"><span data-stu-id="e0557-106">Create a new rules engine configuration for a specified front door.</span></span> 

<span data-ttu-id="e0557-107">Verwenden Sie das Cmdlet "New-AzFrontDoorRulesEngineRule", um Regeln zu erstellen, die an den Parameter "-Rules" dieses Cmdlets übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="e0557-107">Use cmdlet "New-AzFrontDoorRulesEngineRule" to construct rules engine rules to pass into the "-Rules" parameter of this cmdlet.</span></span>

## <span data-ttu-id="e0557-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e0557-108">EXAMPLES</span></span>

### <span data-ttu-id="e0557-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e0557-109">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name myRulesEngine -Rule $rulesEngineRule1

Name          RulesEngineRules
----          ----------------
myRulesEngine {rules1}
```

<span data-ttu-id="e0557-110">Erstellen Sie eine neue Konfiguration des Regelmoduls für die angegebene Eingangstür.</span><span class="sxs-lookup"><span data-stu-id="e0557-110">Create a new rules engine configuration for specified front door.</span></span>

## <span data-ttu-id="e0557-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e0557-111">PARAMETERS</span></span>

### <span data-ttu-id="e0557-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0557-112">-DefaultProfile</span></span>
<span data-ttu-id="e0557-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e0557-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0557-114">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="e0557-114">-FrontDoorName</span></span>
<span data-ttu-id="e0557-115">Name der Eingangstür.</span><span class="sxs-lookup"><span data-stu-id="e0557-115">Front Door name.</span></span>

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

### <span data-ttu-id="e0557-116">-Name</span><span class="sxs-lookup"><span data-stu-id="e0557-116">-Name</span></span>
<span data-ttu-id="e0557-117">Name des Regelmoduls.</span><span class="sxs-lookup"><span data-stu-id="e0557-117">Rules engine name.</span></span>

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

### <span data-ttu-id="e0557-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0557-118">-ResourceGroupName</span></span>
<span data-ttu-id="e0557-119">Der Ressourcengruppenname, in dem die Eingangstür erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e0557-119">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="e0557-120">-Regel</span><span class="sxs-lookup"><span data-stu-id="e0557-120">-Rule</span></span>
<span data-ttu-id="e0557-121">Eine Liste von Regeln, die eine bestimmte Konfiguration des Regelmoduls definieren.</span><span class="sxs-lookup"><span data-stu-id="e0557-121">A list of rules that define a particular Rules Engine Configuration.</span></span>

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

### <span data-ttu-id="e0557-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e0557-122">-Confirm</span></span>
<span data-ttu-id="e0557-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e0557-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0557-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0557-124">-WhatIf</span></span>
<span data-ttu-id="e0557-125">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e0557-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0557-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e0557-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0557-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0557-127">CommonParameters</span></span>
<span data-ttu-id="e0557-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0557-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0557-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0557-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0557-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e0557-130">INPUTS</span></span>

### <span data-ttu-id="e0557-131">Keine</span><span class="sxs-lookup"><span data-stu-id="e0557-131">None</span></span>

## <span data-ttu-id="e0557-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e0557-132">OUTPUTS</span></span>

### <span data-ttu-id="e0557-133">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="e0557-133">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="e0557-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e0557-134">NOTES</span></span>

## <span data-ttu-id="e0557-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e0557-135">RELATED LINKS</span></span>
