---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
ms.openlocfilehash: d5426decba60df0e18e331c01481ae4f99d5c27c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166065"
---
# <span data-ttu-id="d9f42-101">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="d9f42-101">Remove-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="d9f42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9f42-102">SYNOPSIS</span></span>
<span data-ttu-id="d9f42-103">Entfernt einen Trigger aus einer Daten factory.</span><span class="sxs-lookup"><span data-stu-id="d9f42-103">Removes a trigger from a data factory.</span></span>

## <span data-ttu-id="d9f42-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d9f42-104">SYNTAX</span></span>

### <span data-ttu-id="d9f42-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d9f42-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9f42-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d9f42-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9f42-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d9f42-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9f42-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d9f42-108">DESCRIPTION</span></span>
<span data-ttu-id="d9f42-109">Das **Cmdlet "Remove-AzDataFactoryV2Trigger"** entfernt einen Trigger aus einer Datenfactory.</span><span class="sxs-lookup"><span data-stu-id="d9f42-109">The **Remove-AzDataFactoryV2Trigger** cmdlet removes a trigger from a data factory.</span></span> <span data-ttu-id="d9f42-110">Wenn der _Parameter "Force"_ angegeben ist, fordert das Cmdlet vor dem Entfernen des Triggers keine Eingabeaufforderung an.</span><span class="sxs-lookup"><span data-stu-id="d9f42-110">If the _Force_ parameter is specified, the cmdlet doesn't prompt before removing the trigger.</span></span>

## <span data-ttu-id="d9f42-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d9f42-111">EXAMPLES</span></span>

### <span data-ttu-id="d9f42-112">Beispiel 1: Entfernen eines Triggers</span><span class="sxs-lookup"><span data-stu-id="d9f42-112">Example 1: Remove a trigger</span></span>
```
Remove-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger"

Confirm
Are you sure you want to remove trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="d9f42-113">Entfernen Sie einen Trigger namens "ScheduledTrigger" aus der Daten factory "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="d9f42-113">Remove a trigger called "ScheduledTrigger" from the data factory "WikiADF".</span></span>

## <span data-ttu-id="d9f42-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9f42-114">PARAMETERS</span></span>

### <span data-ttu-id="d9f42-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d9f42-115">-DataFactoryName</span></span>
<span data-ttu-id="d9f42-116">Der Name der Daten factory.</span><span class="sxs-lookup"><span data-stu-id="d9f42-116">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9f42-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9f42-117">-DefaultProfile</span></span>
<span data-ttu-id="d9f42-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d9f42-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9f42-119">-Force</span><span class="sxs-lookup"><span data-stu-id="d9f42-119">-Force</span></span>
<span data-ttu-id="d9f42-120">Führt das Cmdlet ohne Bestätigungsaufforderung aus.</span><span class="sxs-lookup"><span data-stu-id="d9f42-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="d9f42-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9f42-121">-InputObject</span></span>
<span data-ttu-id="d9f42-122">Das zu entfernende Triggerobjekt.</span><span class="sxs-lookup"><span data-stu-id="d9f42-122">The Trigger object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9f42-123">-Name</span><span class="sxs-lookup"><span data-stu-id="d9f42-123">-Name</span></span>
<span data-ttu-id="d9f42-124">Der Auslösername.</span><span class="sxs-lookup"><span data-stu-id="d9f42-124">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9f42-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9f42-125">-ResourceGroupName</span></span>
<span data-ttu-id="d9f42-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d9f42-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9f42-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9f42-127">-ResourceId</span></span>
<span data-ttu-id="d9f42-128">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="d9f42-128">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9f42-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9f42-129">-Confirm</span></span>
<span data-ttu-id="d9f42-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d9f42-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9f42-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d9f42-131">-WhatIf</span></span>
<span data-ttu-id="d9f42-132">Zeigt, was geschieht, wenn das Cmdlet ausgeführt, aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d9f42-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="d9f42-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9f42-133">CommonParameters</span></span>
<span data-ttu-id="d9f42-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9f42-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9f42-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9f42-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9f42-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d9f42-136">INPUTS</span></span>

### <span data-ttu-id="d9f42-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="d9f42-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

### <span data-ttu-id="d9f42-138">System.String</span><span class="sxs-lookup"><span data-stu-id="d9f42-138">System.String</span></span>

## <span data-ttu-id="d9f42-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d9f42-139">OUTPUTS</span></span>

### <span data-ttu-id="d9f42-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d9f42-140">System.Boolean</span></span>

## <span data-ttu-id="d9f42-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d9f42-141">NOTES</span></span>

## <span data-ttu-id="d9f42-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d9f42-142">RELATED LINKS</span></span>

[<span data-ttu-id="d9f42-143">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="d9f42-143">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="d9f42-144">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="d9f42-144">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="d9f42-145">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="d9f42-145">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="d9f42-146">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="d9f42-146">Stop-AzDataFactoryV2Trigger</span></span>]()

