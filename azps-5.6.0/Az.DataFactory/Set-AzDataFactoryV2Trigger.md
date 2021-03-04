---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/set-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Trigger.md
ms.openlocfilehash: b0058f21f472f14e97898ea81636fa000034bed5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946186"
---
# <span data-ttu-id="eec91-101">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="eec91-101">Set-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="eec91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eec91-102">SYNOPSIS</span></span>
<span data-ttu-id="eec91-103">Erstellt einen Trigger in einer Daten factory.</span><span class="sxs-lookup"><span data-stu-id="eec91-103">Creates a trigger in a data factory.</span></span>

## <span data-ttu-id="eec91-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eec91-104">SYNTAX</span></span>

### <span data-ttu-id="eec91-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="eec91-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Trigger [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eec91-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="eec91-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Trigger [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eec91-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eec91-107">DESCRIPTION</span></span>
<span data-ttu-id="eec91-108">Das **Cmdlet Set-AzDataFactoryV2Trigger** erstellt einen Trigger in einer Datenfactory.</span><span class="sxs-lookup"><span data-stu-id="eec91-108">The **Set-AzDataFactoryV2Trigger** cmdlet creates a trigger in a data factory.</span></span> <span data-ttu-id="eec91-109">Wenn Sie einen Namen für einen bereits vorhandenen Trigger angeben, fordert das Cmdlet zur Bestätigung auf, bevor der Trigger ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="eec91-109">If you specify a name for a trigger that already exists, the cmdlet prompts for confirmation before replacing the trigger.</span></span> <span data-ttu-id="eec91-110">Wenn Sie den Parameter _Erzwingen_ angeben, ersetzt das Cmdlet den vorhandenen Trigger, ohne zur Bestätigung aufgefordert zu werden.</span><span class="sxs-lookup"><span data-stu-id="eec91-110">If you specify the _Force_ parameter, the cmdlet replaces the existing trigger without prompting for confirmation.</span></span> <span data-ttu-id="eec91-111">Trigger werden im Zustand "Beendet" erstellt, d. h., sie beginnen nicht sofort mit dem Aufrufen von Pipelines, auf die sie verweisen.</span><span class="sxs-lookup"><span data-stu-id="eec91-111">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="eec91-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="eec91-112">EXAMPLES</span></span>

### <span data-ttu-id="eec91-113">Beispiel 1: Erstellen eines Triggers</span><span class="sxs-lookup"><span data-stu-id="eec91-113">Example 1: Create a trigger</span></span>
```
PS C:\> Set-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger" -DefinitionFile ".\scheduledTrigger.json"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="eec91-114">Erstellen Sie einen neuen Trigger namens "ScheduledTrigger" in der Daten factory "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="eec91-114">Create a new trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span> <span data-ttu-id="eec91-115">Der Trigger wird im Zustand "Beendet" erstellt, was bedeutet, dass er nicht sofort gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="eec91-115">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="eec91-116">Ein Trigger kann mit dem `Start-AzDataFactoryV2Trigger` Cmdlet gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="eec91-116">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="eec91-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="eec91-117">PARAMETERS</span></span>

### <span data-ttu-id="eec91-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="eec91-118">-DataFactoryName</span></span>
<span data-ttu-id="eec91-119">Der Name der Datenfabrik.</span><span class="sxs-lookup"><span data-stu-id="eec91-119">The data factory name.</span></span>

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

### <span data-ttu-id="eec91-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eec91-120">-DefaultProfile</span></span>
<span data-ttu-id="eec91-121">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eec91-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eec91-122">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="eec91-122">-DefinitionFile</span></span>
<span data-ttu-id="eec91-123">Der JSON-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="eec91-123">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eec91-124">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="eec91-124">-Force</span></span>
<span data-ttu-id="eec91-125">Führt das Cmdlet aus, ohne zur Bestätigung aufgefordert zu werden.</span><span class="sxs-lookup"><span data-stu-id="eec91-125">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="eec91-126">-Name</span><span class="sxs-lookup"><span data-stu-id="eec91-126">-Name</span></span>
<span data-ttu-id="eec91-127">Der Triggername.</span><span class="sxs-lookup"><span data-stu-id="eec91-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eec91-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eec91-128">-ResourceGroupName</span></span>
<span data-ttu-id="eec91-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="eec91-129">The resource group name.</span></span>

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

### <span data-ttu-id="eec91-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eec91-130">-ResourceId</span></span>
<span data-ttu-id="eec91-131">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="eec91-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="eec91-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="eec91-132">-Confirm</span></span>
<span data-ttu-id="eec91-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="eec91-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eec91-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eec91-134">-WhatIf</span></span>
<span data-ttu-id="eec91-135">Zeigt, was geschieht, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eec91-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="eec91-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eec91-136">CommonParameters</span></span>
<span data-ttu-id="eec91-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eec91-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eec91-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eec91-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eec91-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="eec91-139">INPUTS</span></span>

### <span data-ttu-id="eec91-140">System.String</span><span class="sxs-lookup"><span data-stu-id="eec91-140">System.String</span></span>

## <span data-ttu-id="eec91-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="eec91-141">OUTPUTS</span></span>

### <span data-ttu-id="eec91-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="eec91-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="eec91-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="eec91-143">NOTES</span></span>

## <span data-ttu-id="eec91-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="eec91-144">RELATED LINKS</span></span>

[<span data-ttu-id="eec91-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="eec91-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="eec91-146">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="eec91-146">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="eec91-147">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="eec91-147">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="eec91-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="eec91-148">Remove-AzDataFactoryV2Trigger</span></span>]()
