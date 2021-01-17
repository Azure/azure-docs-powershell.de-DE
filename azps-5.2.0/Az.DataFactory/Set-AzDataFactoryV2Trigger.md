---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Trigger.md
ms.openlocfilehash: cb0d548e1fcbc7acecf1ae1457eb762d4cf81645
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98307979"
---
# <span data-ttu-id="70413-101">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="70413-101">Set-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="70413-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70413-102">SYNOPSIS</span></span>
<span data-ttu-id="70413-103">Erstellt einen Trigger in einer Daten factory.</span><span class="sxs-lookup"><span data-stu-id="70413-103">Creates a trigger in a data factory.</span></span>

## <span data-ttu-id="70413-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="70413-104">SYNTAX</span></span>

### <span data-ttu-id="70413-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="70413-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Trigger [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="70413-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="70413-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Trigger [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70413-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="70413-107">DESCRIPTION</span></span>
<span data-ttu-id="70413-108">Das **Cmdlet "Set-AzDataFactoryV2Trigger"** erstellt einen Trigger in einer Datenfactory.</span><span class="sxs-lookup"><span data-stu-id="70413-108">The **Set-AzDataFactoryV2Trigger** cmdlet creates a trigger in a data factory.</span></span> <span data-ttu-id="70413-109">Wenn Sie einen Namen für einen Trigger angeben, der bereits vorhanden ist, fordert das Cmdlet vor dem Ersetzen des Triggers eine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="70413-109">If you specify a name for a trigger that already exists, the cmdlet prompts for confirmation before replacing the trigger.</span></span> <span data-ttu-id="70413-110">Wenn Sie den Parameter _"Force"_ angeben, ersetzt das Cmdlet den vorhandenen Trigger ohne Bestätigungsaufforderung.</span><span class="sxs-lookup"><span data-stu-id="70413-110">If you specify the _Force_ parameter, the cmdlet replaces the existing trigger without prompting for confirmation.</span></span> <span data-ttu-id="70413-111">Trigger werden im Zustand "Beendet" erstellt, d. h., sie beginnen nicht sofort mit dem Aufrufen von Pipelines, auf die sie verweisen.</span><span class="sxs-lookup"><span data-stu-id="70413-111">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="70413-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="70413-112">EXAMPLES</span></span>

### <span data-ttu-id="70413-113">Beispiel 1: Erstellen eines Triggers</span><span class="sxs-lookup"><span data-stu-id="70413-113">Example 1: Create a trigger</span></span>
```
PS C:\> Set-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger" -DefinitionFile ".\scheduledTrigger.json"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="70413-114">Erstellen Sie einen neuen Trigger namens "ScheduledTrigger" in der Daten factory "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="70413-114">Create a new trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span> <span data-ttu-id="70413-115">Der Trigger wird im Zustand "Stopped" erstellt, was bedeutet, dass er nicht sofort gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="70413-115">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="70413-116">Ein Trigger kann mit dem `Start-AzDataFactoryV2Trigger` Cmdlet gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="70413-116">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="70413-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70413-117">PARAMETERS</span></span>

### <span data-ttu-id="70413-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="70413-118">-DataFactoryName</span></span>
<span data-ttu-id="70413-119">Der Name der Daten factory.</span><span class="sxs-lookup"><span data-stu-id="70413-119">The data factory name.</span></span>

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

### <span data-ttu-id="70413-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70413-120">-DefaultProfile</span></span>
<span data-ttu-id="70413-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="70413-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70413-122">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="70413-122">-DefinitionFile</span></span>
<span data-ttu-id="70413-123">Der JSON-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="70413-123">The JSON file path.</span></span>

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

### <span data-ttu-id="70413-124">-Force</span><span class="sxs-lookup"><span data-stu-id="70413-124">-Force</span></span>
<span data-ttu-id="70413-125">Führt das Cmdlet ohne Bestätigungsaufforderung aus.</span><span class="sxs-lookup"><span data-stu-id="70413-125">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="70413-126">-Name</span><span class="sxs-lookup"><span data-stu-id="70413-126">-Name</span></span>
<span data-ttu-id="70413-127">Der Auslösername.</span><span class="sxs-lookup"><span data-stu-id="70413-127">The trigger name.</span></span>

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

### <span data-ttu-id="70413-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70413-128">-ResourceGroupName</span></span>
<span data-ttu-id="70413-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="70413-129">The resource group name.</span></span>

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

### <span data-ttu-id="70413-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70413-130">-ResourceId</span></span>
<span data-ttu-id="70413-131">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="70413-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="70413-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="70413-132">-Confirm</span></span>
<span data-ttu-id="70413-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="70413-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70413-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="70413-134">-WhatIf</span></span>
<span data-ttu-id="70413-135">Zeigt, was geschieht, wenn das Cmdlet ausgeführt, aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="70413-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="70413-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70413-136">CommonParameters</span></span>
<span data-ttu-id="70413-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70413-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70413-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70413-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70413-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="70413-139">INPUTS</span></span>

### <span data-ttu-id="70413-140">System.String</span><span class="sxs-lookup"><span data-stu-id="70413-140">System.String</span></span>

## <span data-ttu-id="70413-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="70413-141">OUTPUTS</span></span>

### <span data-ttu-id="70413-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="70413-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="70413-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="70413-143">NOTES</span></span>

## <span data-ttu-id="70413-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="70413-144">RELATED LINKS</span></span>

[<span data-ttu-id="70413-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="70413-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="70413-146">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="70413-146">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="70413-147">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="70413-147">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="70413-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="70413-148">Remove-AzDataFactoryV2Trigger</span></span>]()
