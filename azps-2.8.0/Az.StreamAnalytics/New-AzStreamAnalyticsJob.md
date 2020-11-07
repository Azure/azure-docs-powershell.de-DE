---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F281B351-F7C7-47D1-9745-FFE4BAA840FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsJob.md
ms.openlocfilehash: b50141c37c55d55f8fd8e823f09fefad49a55543
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826796"
---
# <span data-ttu-id="95640-101">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="95640-101">New-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="95640-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="95640-102">SYNOPSIS</span></span>
<span data-ttu-id="95640-103">Erstellt oder aktualisiert einen Datenstrom Analyse Auftrag.</span><span class="sxs-lookup"><span data-stu-id="95640-103">Creates or updates a Stream Analytics job.</span></span>

## <span data-ttu-id="95640-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="95640-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsJob [[-Name] <String>] [-File] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95640-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="95640-105">DESCRIPTION</span></span>
<span data-ttu-id="95640-106">Das Cmdlet **New-AzStreamAnalyticsJob** erstellt einen neuen Datenstrom Analyse Auftrag in Azure oder aktualisiert die Definition eines vorhandenen angegebenen Auftrags.</span><span class="sxs-lookup"><span data-stu-id="95640-106">The **New-AzStreamAnalyticsJob** cmdlet creates a new Stream Analytics job in Azure or updates the definition of an existing specified job.</span></span>
<span data-ttu-id="95640-107">Der Name des Auftrags kann in der angegeben werden. JSON-Datei oder in der Befehlszeile.</span><span class="sxs-lookup"><span data-stu-id="95640-107">The name of the job can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="95640-108">Wenn beide angegeben sind, muss der Name in der Befehlszeile mit dem Namen in der Datei übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="95640-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="95640-109">Wenn Sie einen Auftragsnamen angeben, der bereits vorhanden ist, und den Parameter *Force* nicht angeben, fragt das Cmdlet, ob der vorhandene Auftrag ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="95640-109">If you specify a job name that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing job.</span></span>
<span data-ttu-id="95640-110">Wenn Sie den Parameter *Force* angeben und einen vorhandenen Auftragsnamen angeben, wird die Auftragsdefinition ohne Bestätigung ersetzt.</span><span class="sxs-lookup"><span data-stu-id="95640-110">If you specify the *Force* parameter and specify an existing job name, the job definition will be replaced without confirmation.</span></span>

## <span data-ttu-id="95640-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="95640-111">EXAMPLES</span></span>

### <span data-ttu-id="95640-112">Beispiel 1: Erstellen eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="95640-112">EXAMPLE 1: Create a job</span></span>
```
PS C:\>New-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json"
```

<span data-ttu-id="95640-113">Mit diesem Befehl wird ein Auftrag aus der Definition in JobDefinition.jsauf erstellt.</span><span class="sxs-lookup"><span data-stu-id="95640-113">This command creates a job from the definition in JobDefinition.json.</span></span>
<span data-ttu-id="95640-114">Wenn ein vorhandener Auftrag mit dem angegebenen Namen in der Auftragsdefinitionsdatei bereits definiert ist, fragt das Cmdlet, ob er ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="95640-114">If an existing job with the specified name in the job definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="95640-115">Beispiel 2: Ersetzen einer Auftragsdefinition</span><span class="sxs-lookup"><span data-stu-id="95640-115">EXAMPLE 2: Replace a job definition</span></span>
```
PS C:\>New-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json" -Name "StreamingJob" -Force
```

<span data-ttu-id="95640-116">Dieser Befehl ersetzt die Auftragsdefinition für StreamingJob ohne Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="95640-116">This command replaces the job definition for StreamingJob without confirmation.</span></span>

## <span data-ttu-id="95640-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="95640-117">PARAMETERS</span></span>

### <span data-ttu-id="95640-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95640-118">-DefaultProfile</span></span>
<span data-ttu-id="95640-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="95640-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95640-120">-Datei</span><span class="sxs-lookup"><span data-stu-id="95640-120">-File</span></span>
<span data-ttu-id="95640-121">Gibt den Pfad zu einer JSON-Datei an, die die JSON-Darstellung des zu erstellende Azure Stream Analytics-Auftrags enthält.</span><span class="sxs-lookup"><span data-stu-id="95640-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics job to create.</span></span>

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

### <span data-ttu-id="95640-122">-Force</span><span class="sxs-lookup"><span data-stu-id="95640-122">-Force</span></span>
<span data-ttu-id="95640-123">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="95640-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="95640-124">-Name</span><span class="sxs-lookup"><span data-stu-id="95640-124">-Name</span></span>
<span data-ttu-id="95640-125">Gibt den Namen des zu erstellende Azure Stream Analytics-Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="95640-125">Specifies the name of the Azure Stream Analytics job to create.</span></span>

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

### <span data-ttu-id="95640-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95640-126">-ResourceGroupName</span></span>
<span data-ttu-id="95640-127">Gibt den Namen der Ressourcengruppe an, zu der der Azure-Stream-Analyse Auftrag gehören soll.</span><span class="sxs-lookup"><span data-stu-id="95640-127">Specifies the name of the resource group to which the Azure Stream Analytics job should belong.</span></span>

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

### <span data-ttu-id="95640-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="95640-128">-Confirm</span></span>
<span data-ttu-id="95640-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="95640-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95640-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95640-130">-WhatIf</span></span>
<span data-ttu-id="95640-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="95640-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95640-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="95640-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95640-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95640-133">CommonParameters</span></span>
<span data-ttu-id="95640-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95640-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95640-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95640-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95640-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="95640-136">INPUTS</span></span>

### <span data-ttu-id="95640-137">System. String</span><span class="sxs-lookup"><span data-stu-id="95640-137">System.String</span></span>

## <span data-ttu-id="95640-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="95640-138">OUTPUTS</span></span>

### <span data-ttu-id="95640-139">Microsoft. Azure. Commands. StreamAnalytics. Models. PSJob</span><span class="sxs-lookup"><span data-stu-id="95640-139">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="95640-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="95640-140">NOTES</span></span>

## <span data-ttu-id="95640-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="95640-141">RELATED LINKS</span></span>

[<span data-ttu-id="95640-142">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="95640-142">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="95640-143">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="95640-143">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="95640-144">Anfang-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="95640-144">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="95640-145">Stopp-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="95640-145">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)

[<span data-ttu-id="95640-146">Stopp-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="95640-146">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


