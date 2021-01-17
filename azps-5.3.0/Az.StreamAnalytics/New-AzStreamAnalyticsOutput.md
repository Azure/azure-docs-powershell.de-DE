---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 43B2A4FD-DA74-403A-89D0-40FE9A3E5A7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsOutput.md
ms.openlocfilehash: b0e32d58d416fce869995595c3e2a2ff69e8f349
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471673"
---
# <span data-ttu-id="adcdf-101">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="adcdf-101">New-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="adcdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adcdf-102">SYNOPSIS</span></span>
<span data-ttu-id="adcdf-103">Erstellt oder aktualisiert Ausgaben für einen Stream Analytics-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="adcdf-103">Creates or updates outputs for a Stream Analytics job.</span></span>

## <span data-ttu-id="adcdf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="adcdf-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="adcdf-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="adcdf-105">DESCRIPTION</span></span>
<span data-ttu-id="adcdf-106">Das **Cmdlet "New-AzStreamAnalyticsOutput"** erstellt eine Ausgabe in einem Stream Analytics-Auftrag oder aktualisiert eine vorhandene Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="adcdf-106">The **New-AzStreamAnalyticsOutput** cmdlet creates an output within a Stream Analytics job or updates an existing output.</span></span>
<span data-ttu-id="adcdf-107">Der Name der Ausgabe kann im angegeben werden. JSON-Datei oder in der Befehlszeile.</span><span class="sxs-lookup"><span data-stu-id="adcdf-107">The name of the output can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="adcdf-108">Wenn beide Angegeben sind, muss der Name in der Befehlszeile mit dem Namen in der Datei übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="adcdf-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="adcdf-109">Wenn Sie eine Ausgabe angeben, die bereits vorhanden ist, ohne den Parameter *"Force"* anzugeben, fragt das Cmdlet, ob die vorhandene Ausgabe ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="adcdf-109">If you specify an output that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing output.</span></span>
<span data-ttu-id="adcdf-110">Wenn Sie den Parameter *"Force"* und einen vorhandenen Ausgabenamen angeben, wird die Ausgabe ohne Bestätigung ersetzt.</span><span class="sxs-lookup"><span data-stu-id="adcdf-110">If you specify the *Force* parameter and specify an existing output name, the output will be replaced without confirmation.</span></span>

## <span data-ttu-id="adcdf-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="adcdf-111">EXAMPLES</span></span>

### <span data-ttu-id="adcdf-112">Beispiel 1: Hinzufügen einer Ausgabe zu einem Auftrag</span><span class="sxs-lookup"><span data-stu-id="adcdf-112">Example 1: Add an output to a job</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="adcdf-113">Mit diesem Befehl wird eine neue Ausgabe namens "Ausgabe" im Auftrag "StreamingJob" erstellt.</span><span class="sxs-lookup"><span data-stu-id="adcdf-113">This command creates a new output called Output in the job called StreamingJob.</span></span>
<span data-ttu-id="adcdf-114">Wenn bereits eine Ausgabe mit diesem Namen definiert ist, fragt das Cmdlet, ob sie ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="adcdf-114">If an existing output with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="adcdf-115">Beispiel 2: Ersetzen einer Auftragsausgabedefinition</span><span class="sxs-lookup"><span data-stu-id="adcdf-115">Example 2: Replace a job output definition</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output" -Force
```

<span data-ttu-id="adcdf-116">Dieser Befehl ersetzt die Definition für "Output" im Auftrag "StreamingJob" ohne Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="adcdf-116">This command replaces the definition for Output in the job called StreamingJob without confirmation.</span></span>

## <span data-ttu-id="adcdf-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="adcdf-117">PARAMETERS</span></span>

### <span data-ttu-id="adcdf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adcdf-118">-DefaultProfile</span></span>
<span data-ttu-id="adcdf-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="adcdf-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="adcdf-120">-File</span><span class="sxs-lookup"><span data-stu-id="adcdf-120">-File</span></span>
<span data-ttu-id="adcdf-121">Gibt den Pfad zu einer JSON-Datei an, die die JSON-Darstellung der zu erstellenden Azure Stream Analytics-Ausgabe enthält.</span><span class="sxs-lookup"><span data-stu-id="adcdf-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics output to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adcdf-122">-Force</span><span class="sxs-lookup"><span data-stu-id="adcdf-122">-Force</span></span>
<span data-ttu-id="adcdf-123">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="adcdf-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="adcdf-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="adcdf-124">-JobName</span></span>
<span data-ttu-id="adcdf-125">Gibt den Namen des Azure Stream Analytics-Auftrags an, unter dem die Azure Stream Analytics-Ausgabe erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="adcdf-125">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics output.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adcdf-126">-Name</span><span class="sxs-lookup"><span data-stu-id="adcdf-126">-Name</span></span>
<span data-ttu-id="adcdf-127">Gibt den Namen der Azure Stream Analytics-Ausgabe an, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="adcdf-127">Specifies the name of the Azure Stream Analytics output to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adcdf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adcdf-128">-ResourceGroupName</span></span>
<span data-ttu-id="adcdf-129">Gibt den Namen der Ressourcengruppe an, unter der die Azure Stream Analytics-Ausgabe erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="adcdf-129">Specifies the name of the resource group under which to create the Azure Stream Analytics output.</span></span>

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

### <span data-ttu-id="adcdf-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="adcdf-130">-Confirm</span></span>
<span data-ttu-id="adcdf-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="adcdf-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adcdf-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="adcdf-132">-WhatIf</span></span>
<span data-ttu-id="adcdf-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="adcdf-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adcdf-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="adcdf-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adcdf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adcdf-135">CommonParameters</span></span>
<span data-ttu-id="adcdf-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adcdf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adcdf-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adcdf-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adcdf-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="adcdf-138">INPUTS</span></span>

### <span data-ttu-id="adcdf-139">System.String</span><span class="sxs-lookup"><span data-stu-id="adcdf-139">System.String</span></span>

## <span data-ttu-id="adcdf-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="adcdf-140">OUTPUTS</span></span>

### <span data-ttu-id="adcdf-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span><span class="sxs-lookup"><span data-stu-id="adcdf-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="adcdf-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="adcdf-142">NOTES</span></span>

## <span data-ttu-id="adcdf-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="adcdf-143">RELATED LINKS</span></span>

[<span data-ttu-id="adcdf-144">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="adcdf-144">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="adcdf-145">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="adcdf-145">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="adcdf-146">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="adcdf-146">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


