---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorRulesEngine.md
ms.openlocfilehash: e0df270a2cfc409025434a4e9ca64a2234e6e7c1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94007956"
---
# <span data-ttu-id="e204c-101">Remove-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="e204c-101">Remove-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="e204c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e204c-102">SYNOPSIS</span></span>
<span data-ttu-id="e204c-103">Entfernen des Regelmoduls von der Haustür</span><span class="sxs-lookup"><span data-stu-id="e204c-103">Remove Rules Engine from Front Door</span></span>

## <span data-ttu-id="e204c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e204c-104">SYNTAX</span></span>

### <span data-ttu-id="e204c-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e204c-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e204c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e204c-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoorRulesEngine -InputObject <PSRulesEngine> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e204c-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e204c-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoorRulesEngine -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e204c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e204c-108">DESCRIPTION</span></span>
<span data-ttu-id="e204c-109">Entfernen des Regelmoduls von der Haustür</span><span class="sxs-lookup"><span data-stu-id="e204c-109">Remove Rules Engine from Front Door</span></span>

## <span data-ttu-id="e204c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e204c-110">EXAMPLES</span></span>

### <span data-ttu-id="e204c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e204c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name $rulesEngine.Name -PassThru
True
```

<span data-ttu-id="e204c-112">Entfernen Sie die Konfiguration des Regelmoduls.</span><span class="sxs-lookup"><span data-stu-id="e204c-112">Remove rules engine configuration.</span></span>

### <span data-ttu-id="e204c-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e204c-113">Example 2</span></span>
```powershell
PS C:> Remove-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name nonexistentRulesEngine
Remove-AzFrontDoorRulesEngine : Rules Engine with name 'nonexistentRulesEngine' in Front Door 'frontDoorName' in the resource group 'resourceGroupName' does not exist.
At line:1 char:1
+ Remove-AzFrontDoorRulesEngine -ResourceGroupName resourceGroupName -Fro ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+ CategoryInfo          : CloseError: (:) [Remove-AzFrontDoorRulesEngine], PSArgumentException
+ FullyQualifiedErrorId : Microsoft.Azure.Commands.FrontDoor.Cmdlets.RemoveFrontDoorRulesEngine
```

<span data-ttu-id="e204c-114">Erwartetes Ergebnis beim Entfernen einer nicht vorhandenen Regelmodul Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="e204c-114">Expected outcome when removing a nonexistent rules engine configuration.</span></span>

## <span data-ttu-id="e204c-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="e204c-115">PARAMETERS</span></span>

### <span data-ttu-id="e204c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e204c-116">-DefaultProfile</span></span>
<span data-ttu-id="e204c-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e204c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e204c-118">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="e204c-118">-FrontDoorName</span></span>
<span data-ttu-id="e204c-119">Name der Haustüre</span><span class="sxs-lookup"><span data-stu-id="e204c-119">Front Door name.</span></span>

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

### <span data-ttu-id="e204c-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e204c-120">-InputObject</span></span>
<span data-ttu-id="e204c-121">Das zu aktualisierende Rules Engine-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e204c-121">The Rules Engine object to update.</span></span>

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

### <span data-ttu-id="e204c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e204c-122">-Name</span></span>
<span data-ttu-id="e204c-123">Name des Regelmoduls</span><span class="sxs-lookup"><span data-stu-id="e204c-123">Rules engine name.</span></span>

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

### <span data-ttu-id="e204c-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e204c-124">-PassThru</span></span>
<span data-ttu-id="e204c-125">Objekt zurückgeben (sofern angegeben).</span><span class="sxs-lookup"><span data-stu-id="e204c-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="e204c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e204c-126">-ResourceGroupName</span></span>
<span data-ttu-id="e204c-127">Der Ressourcengruppenname, in dem die Haustür erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e204c-127">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="e204c-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e204c-128">-ResourceId</span></span>
<span data-ttu-id="e204c-129">Ressourcen-ID des zu Aktualisier RulesEngine</span><span class="sxs-lookup"><span data-stu-id="e204c-129">Resource Id of the RulesEngine to update</span></span>

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

### <span data-ttu-id="e204c-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e204c-130">-Confirm</span></span>
<span data-ttu-id="e204c-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e204c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e204c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e204c-132">-WhatIf</span></span>
<span data-ttu-id="e204c-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e204c-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e204c-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e204c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e204c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e204c-135">CommonParameters</span></span>
<span data-ttu-id="e204c-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e204c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e204c-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e204c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e204c-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e204c-138">INPUTS</span></span>

### <span data-ttu-id="e204c-139">Microsoft. Azure. Commands. Haustür. Models. PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="e204c-139">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

### <span data-ttu-id="e204c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e204c-140">System.String</span></span>

## <span data-ttu-id="e204c-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e204c-141">OUTPUTS</span></span>

### <span data-ttu-id="e204c-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e204c-142">System.Boolean</span></span>

## <span data-ttu-id="e204c-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="e204c-143">NOTES</span></span>

## <span data-ttu-id="e204c-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e204c-144">RELATED LINKS</span></span>
