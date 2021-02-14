---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F281B351-F7C7-47D1-9745-FFE4BAA840FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsJob.md
ms.openlocfilehash: ed5b11684fdb8701343c9390962e95942f4075e9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150209"
---
# <span data-ttu-id="a4e0a-101">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a4e0a-101">New-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="a4e0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4e0a-102">SYNOPSIS</span></span>
<span data-ttu-id="a4e0a-103">Erstellt oder aktualisiert einen Stream Analytics-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-103">Creates or updates a Stream Analytics job.</span></span>

## <span data-ttu-id="a4e0a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a4e0a-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsJob [[-Name] <String>] [-File] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4e0a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a4e0a-105">DESCRIPTION</span></span>
<span data-ttu-id="a4e0a-106">Das **Cmdlet "New-AzStreamAnalyticsJob"** erstellt einen neuen Stream Analytics-Auftrag in Azure oder aktualisiert die Definition eines vorhandenen angegebenen Auftrags.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-106">The **New-AzStreamAnalyticsJob** cmdlet creates a new Stream Analytics job in Azure or updates the definition of an existing specified job.</span></span>
<span data-ttu-id="a4e0a-107">Der Name des Auftrags kann in der angegeben werden. JSON-Datei oder in der Befehlszeile.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-107">The name of the job can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="a4e0a-108">Wenn beide Angegeben sind, muss der Name in der Befehlszeile mit dem Namen in der Datei übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="a4e0a-109">Wenn Sie einen Auftragsnamen angeben, der bereits vorhanden ist, ohne den Parameter *"Force"* anzugeben, fragt das Cmdlet, ob der vorhandene Auftrag ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-109">If you specify a job name that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing job.</span></span>
<span data-ttu-id="a4e0a-110">Wenn Sie den Parameter *"Force"* und einen vorhandenen Auftragsnamen angeben, wird die Auftragsdefinition ohne Bestätigung ersetzt.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-110">If you specify the *Force* parameter and specify an existing job name, the job definition will be replaced without confirmation.</span></span>

## <span data-ttu-id="a4e0a-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a4e0a-111">EXAMPLES</span></span>

### <span data-ttu-id="a4e0a-112">BEISPIEL 1: Erstellen eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="a4e0a-112">EXAMPLE 1: Create a job</span></span>
```
PS C:\>New-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json"
```

<span data-ttu-id="a4e0a-113">Mit diesem Befehl wird ein Auftrag aus der Definition in JobDefinition.jserstellt.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-113">This command creates a job from the definition in JobDefinition.json.</span></span>
<span data-ttu-id="a4e0a-114">Wenn ein vorhandener Auftrag mit dem angegebenen Namen in der Auftragsdefinitionsdatei bereits definiert ist, fragt das Cmdlet, ob er ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-114">If an existing job with the specified name in the job definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="a4e0a-115">BEISPIEL 2: Ersetzen einer Auftragsdefinition</span><span class="sxs-lookup"><span data-stu-id="a4e0a-115">EXAMPLE 2: Replace a job definition</span></span>
```
PS C:\>New-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json" -Name "StreamingJob" -Force
```

<span data-ttu-id="a4e0a-116">Dieser Befehl ersetzt die Auftragsdefinition für StreamingJob ohne Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-116">This command replaces the job definition for StreamingJob without confirmation.</span></span>

## <span data-ttu-id="a4e0a-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4e0a-117">PARAMETERS</span></span>

### <span data-ttu-id="a4e0a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4e0a-118">-DefaultProfile</span></span>
<span data-ttu-id="a4e0a-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4e0a-120">-File</span><span class="sxs-lookup"><span data-stu-id="a4e0a-120">-File</span></span>
<span data-ttu-id="a4e0a-121">Gibt den Pfad zu einer JSON-Datei an, die die JSON-Darstellung des zu erstellenden Azure Stream Analytics-Auftrags enthält.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics job to create.</span></span>

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

### <span data-ttu-id="a4e0a-122">-Force</span><span class="sxs-lookup"><span data-stu-id="a4e0a-122">-Force</span></span>
<span data-ttu-id="a4e0a-123">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a4e0a-124">-Name</span><span class="sxs-lookup"><span data-stu-id="a4e0a-124">-Name</span></span>
<span data-ttu-id="a4e0a-125">Gibt den Namen des zu erstellenden Azure Stream Analytics-Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-125">Specifies the name of the Azure Stream Analytics job to create.</span></span>

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

### <span data-ttu-id="a4e0a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4e0a-126">-ResourceGroupName</span></span>
<span data-ttu-id="a4e0a-127">Gibt den Namen der Ressourcengruppe an, zu der der Azure Stream Analytics-Auftrag gehören soll.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-127">Specifies the name of the resource group to which the Azure Stream Analytics job should belong.</span></span>

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

### <span data-ttu-id="a4e0a-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4e0a-128">-Confirm</span></span>
<span data-ttu-id="a4e0a-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4e0a-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a4e0a-130">-WhatIf</span></span>
<span data-ttu-id="a4e0a-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4e0a-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4e0a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4e0a-133">CommonParameters</span></span>
<span data-ttu-id="a4e0a-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4e0a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4e0a-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4e0a-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4e0a-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a4e0a-136">INPUTS</span></span>

### <span data-ttu-id="a4e0a-137">System.String</span><span class="sxs-lookup"><span data-stu-id="a4e0a-137">System.String</span></span>

## <span data-ttu-id="a4e0a-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a4e0a-138">OUTPUTS</span></span>

### <span data-ttu-id="a4e0a-139">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span><span class="sxs-lookup"><span data-stu-id="a4e0a-139">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="a4e0a-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a4e0a-140">NOTES</span></span>

## <span data-ttu-id="a4e0a-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a4e0a-141">RELATED LINKS</span></span>

[<span data-ttu-id="a4e0a-142">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a4e0a-142">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="a4e0a-143">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a4e0a-143">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="a4e0a-144">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a4e0a-144">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="a4e0a-145">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a4e0a-145">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)

[<span data-ttu-id="a4e0a-146">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a4e0a-146">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


