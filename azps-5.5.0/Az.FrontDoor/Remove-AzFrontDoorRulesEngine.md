---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorRulesEngine.md
ms.openlocfilehash: e0df270a2cfc409025434a4e9ca64a2234e6e7c1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153156"
---
# <span data-ttu-id="01b9e-101">Remove-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="01b9e-101">Remove-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="01b9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01b9e-102">SYNOPSIS</span></span>
<span data-ttu-id="01b9e-103">"Rules Engine" von Front Door entfernen</span><span class="sxs-lookup"><span data-stu-id="01b9e-103">Remove Rules Engine from Front Door</span></span>

## <span data-ttu-id="01b9e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="01b9e-104">SYNTAX</span></span>

### <span data-ttu-id="01b9e-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="01b9e-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01b9e-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="01b9e-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoorRulesEngine -InputObject <PSRulesEngine> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01b9e-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="01b9e-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoorRulesEngine -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01b9e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="01b9e-108">DESCRIPTION</span></span>
<span data-ttu-id="01b9e-109">"Rules Engine" von Front Door entfernen</span><span class="sxs-lookup"><span data-stu-id="01b9e-109">Remove Rules Engine from Front Door</span></span>

## <span data-ttu-id="01b9e-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="01b9e-110">EXAMPLES</span></span>

### <span data-ttu-id="01b9e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="01b9e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name $rulesEngine.Name -PassThru
True
```

<span data-ttu-id="01b9e-112">Entfernen sie die Konfiguration des Regelmoduls.</span><span class="sxs-lookup"><span data-stu-id="01b9e-112">Remove rules engine configuration.</span></span>

### <span data-ttu-id="01b9e-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="01b9e-113">Example 2</span></span>
```powershell
PS C:> Remove-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name nonexistentRulesEngine
Remove-AzFrontDoorRulesEngine : Rules Engine with name 'nonexistentRulesEngine' in Front Door 'frontDoorName' in the resource group 'resourceGroupName' does not exist.
At line:1 char:1
+ Remove-AzFrontDoorRulesEngine -ResourceGroupName resourceGroupName -Fro ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+ CategoryInfo          : CloseError: (:) [Remove-AzFrontDoorRulesEngine], PSArgumentException
+ FullyQualifiedErrorId : Microsoft.Azure.Commands.FrontDoor.Cmdlets.RemoveFrontDoorRulesEngine
```

<span data-ttu-id="01b9e-114">Erwartetes Ergebnis beim Entfernen einer nicht vorhandenen Konfiguration des Regelmoduls.</span><span class="sxs-lookup"><span data-stu-id="01b9e-114">Expected outcome when removing a nonexistent rules engine configuration.</span></span>

## <span data-ttu-id="01b9e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01b9e-115">PARAMETERS</span></span>

### <span data-ttu-id="01b9e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01b9e-116">-DefaultProfile</span></span>
<span data-ttu-id="01b9e-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="01b9e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01b9e-118">-FrontD ernennenName</span><span class="sxs-lookup"><span data-stu-id="01b9e-118">-FrontDoorName</span></span>
<span data-ttu-id="01b9e-119">Name der Eingangstür.</span><span class="sxs-lookup"><span data-stu-id="01b9e-119">Front Door name.</span></span>

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

### <span data-ttu-id="01b9e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01b9e-120">-InputObject</span></span>
<span data-ttu-id="01b9e-121">Das zu aktualisierende Regelmodulobjekt.</span><span class="sxs-lookup"><span data-stu-id="01b9e-121">The Rules Engine object to update.</span></span>

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

### <span data-ttu-id="01b9e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="01b9e-122">-Name</span></span>
<span data-ttu-id="01b9e-123">Name des Regelmoduls.</span><span class="sxs-lookup"><span data-stu-id="01b9e-123">Rules engine name.</span></span>

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

### <span data-ttu-id="01b9e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01b9e-124">-PassThru</span></span>
<span data-ttu-id="01b9e-125">Rückgabeobjekt (sofern angegeben)</span><span class="sxs-lookup"><span data-stu-id="01b9e-125">Return object (if specified).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01b9e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01b9e-126">-ResourceGroupName</span></span>
<span data-ttu-id="01b9e-127">Der Ressourcengruppenname, in dem die Eingangstür erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="01b9e-127">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="01b9e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01b9e-128">-ResourceId</span></span>
<span data-ttu-id="01b9e-129">Ressourcen-ID des zu aktualisierende RulesEngine</span><span class="sxs-lookup"><span data-stu-id="01b9e-129">Resource Id of the RulesEngine to update</span></span>

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

### <span data-ttu-id="01b9e-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01b9e-130">-Confirm</span></span>
<span data-ttu-id="01b9e-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="01b9e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01b9e-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="01b9e-132">-WhatIf</span></span>
<span data-ttu-id="01b9e-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="01b9e-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="01b9e-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="01b9e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01b9e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01b9e-135">CommonParameters</span></span>
<span data-ttu-id="01b9e-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01b9e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01b9e-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="01b9e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01b9e-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="01b9e-138">INPUTS</span></span>

### <span data-ttu-id="01b9e-139">Microsoft.Azure.Commands.Frontd selbst.Models.PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="01b9e-139">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

### <span data-ttu-id="01b9e-140">System.String</span><span class="sxs-lookup"><span data-stu-id="01b9e-140">System.String</span></span>

## <span data-ttu-id="01b9e-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="01b9e-141">OUTPUTS</span></span>

### <span data-ttu-id="01b9e-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="01b9e-142">System.Boolean</span></span>

## <span data-ttu-id="01b9e-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="01b9e-143">NOTES</span></span>

## <span data-ttu-id="01b9e-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="01b9e-144">RELATED LINKS</span></span>
