---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: 771097c11aceabb9bd2011c6024e469a37a39f4e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477182"
---
# <span data-ttu-id="67e7c-101">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="67e7c-101">Remove-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="67e7c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="67e7c-102">SYNOPSIS</span></span>
<span data-ttu-id="67e7c-103">Entfernt einen Trigger aus einer Data Factory.</span><span class="sxs-lookup"><span data-stu-id="67e7c-103">Removes a trigger from a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67e7c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="67e7c-104">SYNTAX</span></span>

### <span data-ttu-id="67e7c-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="67e7c-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67e7c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="67e7c-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67e7c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="67e7c-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67e7c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="67e7c-108">DESCRIPTION</span></span>
<span data-ttu-id="67e7c-109">Das Cmdlet **Remove-AzureRmDataFactoryV2Trigger** entfernt einen Trigger aus einer Data Factory.</span><span class="sxs-lookup"><span data-stu-id="67e7c-109">The **Remove-AzureRmDataFactoryV2Trigger** cmdlet removes a trigger from a data factory.</span></span> <span data-ttu-id="67e7c-110">Wenn der Parameter _Force_ angegeben wird, wird das Cmdlet vor dem Entfernen des Triggers nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="67e7c-110">If the _Force_ parameter is specified, the cmdlet doesn't prompt before removing the trigger.</span></span>

## <span data-ttu-id="67e7c-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="67e7c-111">EXAMPLES</span></span>

### <span data-ttu-id="67e7c-112">Beispiel 1: Entfernen eines Triggers</span><span class="sxs-lookup"><span data-stu-id="67e7c-112">Example 1: Remove a trigger</span></span>
```
Remove-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger"

Confirm
Are you sure you want to remove trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="67e7c-113">Entfernen Sie einen Trigger mit dem Namen "ScheduledTrigger" aus der Data Factory "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="67e7c-113">Remove a trigger called "ScheduledTrigger" from the data factory "WikiADF".</span></span>

## <span data-ttu-id="67e7c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="67e7c-114">PARAMETERS</span></span>

### <span data-ttu-id="67e7c-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="67e7c-115">-Confirm</span></span>
<span data-ttu-id="67e7c-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="67e7c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67e7c-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="67e7c-117">-DataFactoryName</span></span>
<span data-ttu-id="67e7c-118">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="67e7c-118">The data factory name.</span></span>

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

### <span data-ttu-id="67e7c-119">-Force</span><span class="sxs-lookup"><span data-stu-id="67e7c-119">-Force</span></span>
<span data-ttu-id="67e7c-120">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="67e7c-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="67e7c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="67e7c-121">-Name</span></span>
<span data-ttu-id="67e7c-122">Der Name des Triggers.</span><span class="sxs-lookup"><span data-stu-id="67e7c-122">The trigger name.</span></span>

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

### <span data-ttu-id="67e7c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67e7c-123">-ResourceGroupName</span></span>
<span data-ttu-id="67e7c-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="67e7c-124">The resource group name.</span></span>

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

### <span data-ttu-id="67e7c-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="67e7c-125">-ResourceId</span></span>
<span data-ttu-id="67e7c-126">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="67e7c-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="67e7c-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="67e7c-127">-InputObject</span></span>
<span data-ttu-id="67e7c-128">Das zu entfernende Trigger-Objekt.</span><span class="sxs-lookup"><span data-stu-id="67e7c-128">The Trigger object to remove.</span></span>

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

### <span data-ttu-id="67e7c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67e7c-129">-WhatIf</span></span>
<span data-ttu-id="67e7c-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="67e7c-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="67e7c-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67e7c-131">-DefaultProfile</span></span>
<span data-ttu-id="67e7c-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="67e7c-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67e7c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67e7c-133">CommonParameters</span></span>
<span data-ttu-id="67e7c-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67e7c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67e7c-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67e7c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67e7c-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="67e7c-136">INPUTS</span></span>

### <span data-ttu-id="67e7c-137">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="67e7c-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>
<span data-ttu-id="67e7c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="67e7c-138">System.String</span></span>

## <span data-ttu-id="67e7c-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="67e7c-139">OUTPUTS</span></span>

### <span data-ttu-id="67e7c-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="67e7c-140">System.Object</span></span>

## <span data-ttu-id="67e7c-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="67e7c-141">NOTES</span></span>

## <span data-ttu-id="67e7c-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="67e7c-142">RELATED LINKS</span></span>

[<span data-ttu-id="67e7c-143">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="67e7c-143">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="67e7c-144">Satz-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="67e7c-144">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="67e7c-145">Anfang-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="67e7c-145">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="67e7c-146">Stopp-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="67e7c-146">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

