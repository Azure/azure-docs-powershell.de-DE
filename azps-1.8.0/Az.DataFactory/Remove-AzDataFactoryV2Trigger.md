---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 5b3052682785a694b3fb0999bb5df761eb3b96be
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820351"
---
# <span data-ttu-id="edf03-101">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="edf03-101">Remove-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="edf03-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="edf03-102">SYNOPSIS</span></span>
<span data-ttu-id="edf03-103">Entfernt einen Trigger aus einer Data Factory.</span><span class="sxs-lookup"><span data-stu-id="edf03-103">Removes a trigger from a data factory.</span></span>

## <span data-ttu-id="edf03-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="edf03-104">SYNTAX</span></span>

### <span data-ttu-id="edf03-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="edf03-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edf03-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="edf03-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edf03-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="edf03-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edf03-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="edf03-108">DESCRIPTION</span></span>
<span data-ttu-id="edf03-109">Das Cmdlet **Remove-AzDataFactoryV2Trigger** entfernt einen Trigger aus einer Data Factory.</span><span class="sxs-lookup"><span data-stu-id="edf03-109">The **Remove-AzDataFactoryV2Trigger** cmdlet removes a trigger from a data factory.</span></span> <span data-ttu-id="edf03-110">Wenn der Parameter _Force_ angegeben wird, wird das Cmdlet vor dem Entfernen des Triggers nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="edf03-110">If the _Force_ parameter is specified, the cmdlet doesn't prompt before removing the trigger.</span></span>

## <span data-ttu-id="edf03-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="edf03-111">EXAMPLES</span></span>

### <span data-ttu-id="edf03-112">Beispiel 1: Entfernen eines Triggers</span><span class="sxs-lookup"><span data-stu-id="edf03-112">Example 1: Remove a trigger</span></span>
```
Remove-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger"

Confirm
Are you sure you want to remove trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="edf03-113">Entfernen Sie einen Trigger mit dem Namen "ScheduledTrigger" aus der Data Factory "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="edf03-113">Remove a trigger called "ScheduledTrigger" from the data factory "WikiADF".</span></span>

## <span data-ttu-id="edf03-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="edf03-114">PARAMETERS</span></span>

### <span data-ttu-id="edf03-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="edf03-115">-DataFactoryName</span></span>
<span data-ttu-id="edf03-116">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="edf03-116">The data factory name.</span></span>

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

### <span data-ttu-id="edf03-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edf03-117">-DefaultProfile</span></span>
<span data-ttu-id="edf03-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="edf03-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="edf03-119">-Force</span><span class="sxs-lookup"><span data-stu-id="edf03-119">-Force</span></span>
<span data-ttu-id="edf03-120">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="edf03-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="edf03-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="edf03-121">-InputObject</span></span>
<span data-ttu-id="edf03-122">Das zu entfernende Trigger-Objekt.</span><span class="sxs-lookup"><span data-stu-id="edf03-122">The Trigger object to remove.</span></span>

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

### <span data-ttu-id="edf03-123">-Name</span><span class="sxs-lookup"><span data-stu-id="edf03-123">-Name</span></span>
<span data-ttu-id="edf03-124">Der Name des Triggers.</span><span class="sxs-lookup"><span data-stu-id="edf03-124">The trigger name.</span></span>

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

### <span data-ttu-id="edf03-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edf03-125">-ResourceGroupName</span></span>
<span data-ttu-id="edf03-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="edf03-126">The resource group name.</span></span>

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

### <span data-ttu-id="edf03-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="edf03-127">-ResourceId</span></span>
<span data-ttu-id="edf03-128">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="edf03-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="edf03-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="edf03-129">-Confirm</span></span>
<span data-ttu-id="edf03-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="edf03-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edf03-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edf03-131">-WhatIf</span></span>
<span data-ttu-id="edf03-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="edf03-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="edf03-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edf03-133">CommonParameters</span></span>
<span data-ttu-id="edf03-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edf03-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edf03-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edf03-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edf03-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="edf03-136">INPUTS</span></span>

### <span data-ttu-id="edf03-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="edf03-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

### <span data-ttu-id="edf03-138">System. String</span><span class="sxs-lookup"><span data-stu-id="edf03-138">System.String</span></span>

## <span data-ttu-id="edf03-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="edf03-139">OUTPUTS</span></span>

### <span data-ttu-id="edf03-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="edf03-140">System.Boolean</span></span>

## <span data-ttu-id="edf03-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="edf03-141">NOTES</span></span>

## <span data-ttu-id="edf03-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="edf03-142">RELATED LINKS</span></span>

[<span data-ttu-id="edf03-143">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="edf03-143">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="edf03-144">Satz-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="edf03-144">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="edf03-145">Anfang-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="edf03-145">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="edf03-146">Stopp-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="edf03-146">Stop-AzDataFactoryV2Trigger</span></span>]()

