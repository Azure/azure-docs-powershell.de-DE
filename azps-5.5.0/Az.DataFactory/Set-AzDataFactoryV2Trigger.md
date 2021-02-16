---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Trigger.md
ms.openlocfilehash: cb0d548e1fcbc7acecf1ae1457eb762d4cf81645
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153476"
---
# <span data-ttu-id="6eef3-101">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="6eef3-101">Set-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="6eef3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6eef3-102">SYNOPSIS</span></span>
<span data-ttu-id="6eef3-103">Erstellt einen Trigger in einer Daten factory.</span><span class="sxs-lookup"><span data-stu-id="6eef3-103">Creates a trigger in a data factory.</span></span>

## <span data-ttu-id="6eef3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6eef3-104">SYNTAX</span></span>

### <span data-ttu-id="6eef3-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="6eef3-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Trigger [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6eef3-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6eef3-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Trigger [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6eef3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6eef3-107">DESCRIPTION</span></span>
<span data-ttu-id="6eef3-108">Das **Cmdlet "Set-AzDataFactoryV2Trigger"** erstellt einen Trigger in einer Datenfactory.</span><span class="sxs-lookup"><span data-stu-id="6eef3-108">The **Set-AzDataFactoryV2Trigger** cmdlet creates a trigger in a data factory.</span></span> <span data-ttu-id="6eef3-109">Wenn Sie einen Namen für einen Trigger angeben, der bereits vorhanden ist, fordert das Cmdlet vor dem Ersetzen des Triggers eine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="6eef3-109">If you specify a name for a trigger that already exists, the cmdlet prompts for confirmation before replacing the trigger.</span></span> <span data-ttu-id="6eef3-110">Wenn Sie den Parameter _"Force"_ angeben, ersetzt das Cmdlet den vorhandenen Trigger ohne Bestätigungsaufforderung.</span><span class="sxs-lookup"><span data-stu-id="6eef3-110">If you specify the _Force_ parameter, the cmdlet replaces the existing trigger without prompting for confirmation.</span></span> <span data-ttu-id="6eef3-111">Trigger werden im Zustand "Beendet" erstellt, d. h., sie beginnen nicht sofort mit dem Aufrufen von Pipelines, auf die sie verweisen.</span><span class="sxs-lookup"><span data-stu-id="6eef3-111">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="6eef3-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6eef3-112">EXAMPLES</span></span>

### <span data-ttu-id="6eef3-113">Beispiel 1: Erstellen eines Triggers</span><span class="sxs-lookup"><span data-stu-id="6eef3-113">Example 1: Create a trigger</span></span>
```
PS C:\> Set-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger" -DefinitionFile ".\scheduledTrigger.json"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="6eef3-114">Erstellen Sie einen neuen Trigger namens "ScheduledTrigger" in der Daten factory "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="6eef3-114">Create a new trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span> <span data-ttu-id="6eef3-115">Der Trigger wird im Zustand "Stopped" erstellt, was bedeutet, dass er nicht sofort gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="6eef3-115">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="6eef3-116">Ein Trigger kann mit dem `Start-AzDataFactoryV2Trigger` Cmdlet gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="6eef3-116">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="6eef3-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6eef3-117">PARAMETERS</span></span>

### <span data-ttu-id="6eef3-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="6eef3-118">-DataFactoryName</span></span>
<span data-ttu-id="6eef3-119">Der Name der Daten factory.</span><span class="sxs-lookup"><span data-stu-id="6eef3-119">The data factory name.</span></span>

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

### <span data-ttu-id="6eef3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eef3-120">-DefaultProfile</span></span>
<span data-ttu-id="6eef3-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6eef3-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6eef3-122">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="6eef3-122">-DefinitionFile</span></span>
<span data-ttu-id="6eef3-123">Der JSON-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="6eef3-123">The JSON file path.</span></span>

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

### <span data-ttu-id="6eef3-124">-Force</span><span class="sxs-lookup"><span data-stu-id="6eef3-124">-Force</span></span>
<span data-ttu-id="6eef3-125">Führt das Cmdlet ohne Bestätigungsaufforderung aus.</span><span class="sxs-lookup"><span data-stu-id="6eef3-125">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="6eef3-126">-Name</span><span class="sxs-lookup"><span data-stu-id="6eef3-126">-Name</span></span>
<span data-ttu-id="6eef3-127">Der Auslösername.</span><span class="sxs-lookup"><span data-stu-id="6eef3-127">The trigger name.</span></span>

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

### <span data-ttu-id="6eef3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6eef3-128">-ResourceGroupName</span></span>
<span data-ttu-id="6eef3-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6eef3-129">The resource group name.</span></span>

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

### <span data-ttu-id="6eef3-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6eef3-130">-ResourceId</span></span>
<span data-ttu-id="6eef3-131">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="6eef3-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="6eef3-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6eef3-132">-Confirm</span></span>
<span data-ttu-id="6eef3-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6eef3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6eef3-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6eef3-134">-WhatIf</span></span>
<span data-ttu-id="6eef3-135">Zeigt, was geschieht, wenn das Cmdlet ausgeführt, aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6eef3-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="6eef3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eef3-136">CommonParameters</span></span>
<span data-ttu-id="6eef3-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6eef3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eef3-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6eef3-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eef3-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6eef3-139">INPUTS</span></span>

### <span data-ttu-id="6eef3-140">System.String</span><span class="sxs-lookup"><span data-stu-id="6eef3-140">System.String</span></span>

## <span data-ttu-id="6eef3-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6eef3-141">OUTPUTS</span></span>

### <span data-ttu-id="6eef3-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="6eef3-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="6eef3-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6eef3-143">NOTES</span></span>

## <span data-ttu-id="6eef3-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6eef3-144">RELATED LINKS</span></span>

[<span data-ttu-id="6eef3-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="6eef3-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="6eef3-146">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="6eef3-146">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="6eef3-147">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="6eef3-147">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="6eef3-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="6eef3-148">Remove-AzDataFactoryV2Trigger</span></span>]()
