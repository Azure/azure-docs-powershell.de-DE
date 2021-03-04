---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F281B351-F7C7-47D1-9745-FFE4BAA840FD
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/new-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsJob.md
ms.openlocfilehash: 8a9da4d68456b612cbd1bd4db3997cc67e724975
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923216"
---
# <span data-ttu-id="db6aa-101">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="db6aa-101">New-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="db6aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db6aa-102">SYNOPSIS</span></span>
<span data-ttu-id="db6aa-103">Erstellt oder aktualisiert einen Stream Analytics-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="db6aa-103">Creates or updates a Stream Analytics job.</span></span>

## <span data-ttu-id="db6aa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="db6aa-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsJob [[-Name] <String>] [-File] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db6aa-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="db6aa-105">DESCRIPTION</span></span>
<span data-ttu-id="db6aa-106">Das **Cmdlet New-AzStreamAnalyticsJob** erstellt einen neuen Stream Analytics-Auftrag in Azure oder aktualisiert die Definition eines vorhandenen angegebenen Auftrags.</span><span class="sxs-lookup"><span data-stu-id="db6aa-106">The **New-AzStreamAnalyticsJob** cmdlet creates a new Stream Analytics job in Azure or updates the definition of an existing specified job.</span></span>
<span data-ttu-id="db6aa-107">Der Name des Auftrags kann im angegeben werden. JSON-Datei oder in der Befehlszeile.</span><span class="sxs-lookup"><span data-stu-id="db6aa-107">The name of the job can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="db6aa-108">Wenn beide angegeben sind, muss der Name in der Befehlszeile mit dem Namen in der Datei übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="db6aa-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="db6aa-109">Wenn Sie einen bereits vorhandenen Auftragsnamen  angeben und nicht den Parameter Erzwingen angeben, fragt das Cmdlet, ob der vorhandene Auftrag ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="db6aa-109">If you specify a job name that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing job.</span></span>
<span data-ttu-id="db6aa-110">Wenn Sie den Parameter *Erzwingen* angeben und einen vorhandenen Auftragsnamen angeben, wird die Auftragsdefinition ohne Bestätigung ersetzt.</span><span class="sxs-lookup"><span data-stu-id="db6aa-110">If you specify the *Force* parameter and specify an existing job name, the job definition will be replaced without confirmation.</span></span>

## <span data-ttu-id="db6aa-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="db6aa-111">EXAMPLES</span></span>

### <span data-ttu-id="db6aa-112">BEISPIEL 1: Erstellen eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="db6aa-112">EXAMPLE 1: Create a job</span></span>
```
PS C:\>New-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json"
```

<span data-ttu-id="db6aa-113">Mit diesem Befehl wird ein Auftrag aus der Definition in JobDefinition.jserstellt.</span><span class="sxs-lookup"><span data-stu-id="db6aa-113">This command creates a job from the definition in JobDefinition.json.</span></span>
<span data-ttu-id="db6aa-114">Wenn ein vorhandener Auftrag mit dem angegebenen Namen in der Auftragsdefinitionsdatei bereits definiert ist, fragt das Cmdlet, ob er ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="db6aa-114">If an existing job with the specified name in the job definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="db6aa-115">BEISPIEL 2: Ersetzen einer Auftragsdefinition</span><span class="sxs-lookup"><span data-stu-id="db6aa-115">EXAMPLE 2: Replace a job definition</span></span>
```
PS C:\>New-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json" -Name "StreamingJob" -Force
```

<span data-ttu-id="db6aa-116">Dieser Befehl ersetzt die Auftragsdefinition für StreamingJob ohne Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="db6aa-116">This command replaces the job definition for StreamingJob without confirmation.</span></span>

## <span data-ttu-id="db6aa-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="db6aa-117">PARAMETERS</span></span>

### <span data-ttu-id="db6aa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db6aa-118">-DefaultProfile</span></span>
<span data-ttu-id="db6aa-119">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="db6aa-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db6aa-120">-Datei</span><span class="sxs-lookup"><span data-stu-id="db6aa-120">-File</span></span>
<span data-ttu-id="db6aa-121">Gibt den Pfad zu einer JSON-Datei an, der die JSON-Darstellung des zu erstellenden Azure Stream Analytics-Auftrags enthält.</span><span class="sxs-lookup"><span data-stu-id="db6aa-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics job to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db6aa-122">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="db6aa-122">-Force</span></span>
<span data-ttu-id="db6aa-123">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="db6aa-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="db6aa-124">-Name</span><span class="sxs-lookup"><span data-stu-id="db6aa-124">-Name</span></span>
<span data-ttu-id="db6aa-125">Gibt den Namen des zu erstellenden Azure Stream Analytics-Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="db6aa-125">Specifies the name of the Azure Stream Analytics job to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db6aa-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db6aa-126">-ResourceGroupName</span></span>
<span data-ttu-id="db6aa-127">Gibt den Namen der Ressourcengruppe an, zu der der Azure Stream Analytics-Auftrag gehören soll.</span><span class="sxs-lookup"><span data-stu-id="db6aa-127">Specifies the name of the resource group to which the Azure Stream Analytics job should belong.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db6aa-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="db6aa-128">-Confirm</span></span>
<span data-ttu-id="db6aa-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="db6aa-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db6aa-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db6aa-130">-WhatIf</span></span>
<span data-ttu-id="db6aa-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="db6aa-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db6aa-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="db6aa-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db6aa-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db6aa-133">CommonParameters</span></span>
<span data-ttu-id="db6aa-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db6aa-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db6aa-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db6aa-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db6aa-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="db6aa-136">INPUTS</span></span>

### <span data-ttu-id="db6aa-137">System.String</span><span class="sxs-lookup"><span data-stu-id="db6aa-137">System.String</span></span>

## <span data-ttu-id="db6aa-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="db6aa-138">OUTPUTS</span></span>

### <span data-ttu-id="db6aa-139">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span><span class="sxs-lookup"><span data-stu-id="db6aa-139">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="db6aa-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="db6aa-140">NOTES</span></span>

## <span data-ttu-id="db6aa-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="db6aa-141">RELATED LINKS</span></span>

[<span data-ttu-id="db6aa-142">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="db6aa-142">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="db6aa-143">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="db6aa-143">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="db6aa-144">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="db6aa-144">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="db6aa-145">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="db6aa-145">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)

[<span data-ttu-id="db6aa-146">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="db6aa-146">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


