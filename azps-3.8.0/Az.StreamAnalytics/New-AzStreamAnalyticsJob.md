---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F281B351-F7C7-47D1-9745-FFE4BAA840FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsJob.md
ms.openlocfilehash: ed5b11684fdb8701343c9390962e95942f4075e9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845780"
---
# <span data-ttu-id="d43bc-101">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d43bc-101">New-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="d43bc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d43bc-102">SYNOPSIS</span></span>
<span data-ttu-id="d43bc-103">Erstellt oder aktualisiert einen Datenstrom Analyse Auftrag.</span><span class="sxs-lookup"><span data-stu-id="d43bc-103">Creates or updates a Stream Analytics job.</span></span>

## <span data-ttu-id="d43bc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d43bc-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsJob [[-Name] <String>] [-File] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d43bc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d43bc-105">DESCRIPTION</span></span>
<span data-ttu-id="d43bc-106">Das Cmdlet **New-AzStreamAnalyticsJob** erstellt einen neuen Datenstrom Analyse Auftrag in Azure oder aktualisiert die Definition eines vorhandenen angegebenen Auftrags.</span><span class="sxs-lookup"><span data-stu-id="d43bc-106">The **New-AzStreamAnalyticsJob** cmdlet creates a new Stream Analytics job in Azure or updates the definition of an existing specified job.</span></span>
<span data-ttu-id="d43bc-107">Der Name des Auftrags kann in der angegeben werden. JSON-Datei oder in der Befehlszeile.</span><span class="sxs-lookup"><span data-stu-id="d43bc-107">The name of the job can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="d43bc-108">Wenn beide angegeben sind, muss der Name in der Befehlszeile mit dem Namen in der Datei übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="d43bc-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="d43bc-109">Wenn Sie einen Auftragsnamen angeben, der bereits vorhanden ist, und den Parameter *Force* nicht angeben, fragt das Cmdlet, ob der vorhandene Auftrag ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d43bc-109">If you specify a job name that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing job.</span></span>
<span data-ttu-id="d43bc-110">Wenn Sie den Parameter *Force* angeben und einen vorhandenen Auftragsnamen angeben, wird die Auftragsdefinition ohne Bestätigung ersetzt.</span><span class="sxs-lookup"><span data-stu-id="d43bc-110">If you specify the *Force* parameter and specify an existing job name, the job definition will be replaced without confirmation.</span></span>

## <span data-ttu-id="d43bc-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d43bc-111">EXAMPLES</span></span>

### <span data-ttu-id="d43bc-112">Beispiel 1: Erstellen eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="d43bc-112">EXAMPLE 1: Create a job</span></span>
```
PS C:\>New-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json"
```

<span data-ttu-id="d43bc-113">Mit diesem Befehl wird ein Auftrag aus der Definition in JobDefinition.jsauf erstellt.</span><span class="sxs-lookup"><span data-stu-id="d43bc-113">This command creates a job from the definition in JobDefinition.json.</span></span>
<span data-ttu-id="d43bc-114">Wenn ein vorhandener Auftrag mit dem angegebenen Namen in der Auftragsdefinitionsdatei bereits definiert ist, fragt das Cmdlet, ob er ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d43bc-114">If an existing job with the specified name in the job definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="d43bc-115">Beispiel 2: Ersetzen einer Auftragsdefinition</span><span class="sxs-lookup"><span data-stu-id="d43bc-115">EXAMPLE 2: Replace a job definition</span></span>
```
PS C:\>New-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json" -Name "StreamingJob" -Force
```

<span data-ttu-id="d43bc-116">Dieser Befehl ersetzt die Auftragsdefinition für StreamingJob ohne Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="d43bc-116">This command replaces the job definition for StreamingJob without confirmation.</span></span>

## <span data-ttu-id="d43bc-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="d43bc-117">PARAMETERS</span></span>

### <span data-ttu-id="d43bc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d43bc-118">-DefaultProfile</span></span>
<span data-ttu-id="d43bc-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d43bc-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d43bc-120">-Datei</span><span class="sxs-lookup"><span data-stu-id="d43bc-120">-File</span></span>
<span data-ttu-id="d43bc-121">Gibt den Pfad zu einer JSON-Datei an, die die JSON-Darstellung des zu erstellende Azure Stream Analytics-Auftrags enthält.</span><span class="sxs-lookup"><span data-stu-id="d43bc-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics job to create.</span></span>

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

### <span data-ttu-id="d43bc-122">-Force</span><span class="sxs-lookup"><span data-stu-id="d43bc-122">-Force</span></span>
<span data-ttu-id="d43bc-123">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="d43bc-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d43bc-124">-Name</span><span class="sxs-lookup"><span data-stu-id="d43bc-124">-Name</span></span>
<span data-ttu-id="d43bc-125">Gibt den Namen des zu erstellende Azure Stream Analytics-Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="d43bc-125">Specifies the name of the Azure Stream Analytics job to create.</span></span>

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

### <span data-ttu-id="d43bc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d43bc-126">-ResourceGroupName</span></span>
<span data-ttu-id="d43bc-127">Gibt den Namen der Ressourcengruppe an, zu der der Azure-Stream-Analyse Auftrag gehören soll.</span><span class="sxs-lookup"><span data-stu-id="d43bc-127">Specifies the name of the resource group to which the Azure Stream Analytics job should belong.</span></span>

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

### <span data-ttu-id="d43bc-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d43bc-128">-Confirm</span></span>
<span data-ttu-id="d43bc-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d43bc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d43bc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d43bc-130">-WhatIf</span></span>
<span data-ttu-id="d43bc-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d43bc-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d43bc-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d43bc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d43bc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d43bc-133">CommonParameters</span></span>
<span data-ttu-id="d43bc-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d43bc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d43bc-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d43bc-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d43bc-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d43bc-136">INPUTS</span></span>

### <span data-ttu-id="d43bc-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d43bc-137">System.String</span></span>

## <span data-ttu-id="d43bc-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d43bc-138">OUTPUTS</span></span>

### <span data-ttu-id="d43bc-139">Microsoft. Azure. Commands. StreamAnalytics. Models. PSJob</span><span class="sxs-lookup"><span data-stu-id="d43bc-139">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="d43bc-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="d43bc-140">NOTES</span></span>

## <span data-ttu-id="d43bc-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d43bc-141">RELATED LINKS</span></span>

[<span data-ttu-id="d43bc-142">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d43bc-142">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="d43bc-143">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d43bc-143">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="d43bc-144">Anfang-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d43bc-144">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="d43bc-145">Stopp-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d43bc-145">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)

[<span data-ttu-id="d43bc-146">Stopp-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d43bc-146">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


