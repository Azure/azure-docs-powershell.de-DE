---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 35CE5C5F-F8D4-426F-A33A-4F9EA50E9B83
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
ms.openlocfilehash: 74145a6d65fdaa9634d7681133e10b2496b5f903
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150212"
---
# <span data-ttu-id="3f989-101">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="3f989-101">New-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="3f989-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f989-102">SYNOPSIS</span></span>
<span data-ttu-id="3f989-103">Erstellt oder aktualisiert eine Auftragseingabe.</span><span class="sxs-lookup"><span data-stu-id="3f989-103">Creates or updates a job input.</span></span>

## <span data-ttu-id="3f989-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3f989-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3f989-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3f989-105">DESCRIPTION</span></span>
<span data-ttu-id="3f989-106">Das **Cmdlet "New-AzStreamAnalyticsInput"** erstellt eine Eingabe in einem Stream Analytics-Auftrag oder aktualisiert eine vorhandene Eingabe.</span><span class="sxs-lookup"><span data-stu-id="3f989-106">The **New-AzStreamAnalyticsInput** cmdlet creates an input within a Stream Analytics job or updates an existing input.</span></span>
<span data-ttu-id="3f989-107">Der Name der Eingabe kann in der Datei "JSON" oder in der Befehlszeile angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3f989-107">The name of the input can be specified in the JSON file or on the command line.</span></span>
<span data-ttu-id="3f989-108">Wenn beide Angegeben sind, muss der Name in der Befehlszeile mit dem Namen in der Datei übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="3f989-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="3f989-109">Wenn Sie eine Eingabe angeben, die bereits vorhanden ist, ohne den Parameter *"Force"* anzugeben, fragt das Cmdlet, ob die vorhandene Eingabe ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3f989-109">If you specify an input that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing input.</span></span>
<span data-ttu-id="3f989-110">Wenn Sie den Parameter *"Force"* und einen vorhandenen Eingabenamen angeben, wird die Eingabe ohne Bestätigung ersetzt.</span><span class="sxs-lookup"><span data-stu-id="3f989-110">If you specify the *Force* parameter and specify an existing input name, the input will be replaced without confirmation.</span></span>

## <span data-ttu-id="3f989-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3f989-111">EXAMPLES</span></span>

### <span data-ttu-id="3f989-112">Beispiel 1: Erstellen einer Auftragseingabe mit einer Definition aus einer Datei</span><span class="sxs-lookup"><span data-stu-id="3f989-112">Example 1: Create a job input with a definition from a file</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json"
```

<span data-ttu-id="3f989-113">Mit diesem Befehl wird eine Eingabe aus der Datei erstellt, Input.jswird.</span><span class="sxs-lookup"><span data-stu-id="3f989-113">This command creates an input from the file Input.json.</span></span>
<span data-ttu-id="3f989-114">Wenn bereits eine Eingabe mit dem in der Eingabedefinitionsdatei angegebenen Namen definiert ist, fragt das Cmdlet, ob sie ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3f989-114">If an existing input with the name specified in the input definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="3f989-115">Beispiel 2: Erstellen einer Auftragseingabe</span><span class="sxs-lookup"><span data-stu-id="3f989-115">Example 2: Create a job input</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream"
```

<span data-ttu-id="3f989-116">Mit diesem Befehl wird eine neue Eingabe für den Auftrag "EntryStream" erstellt.</span><span class="sxs-lookup"><span data-stu-id="3f989-116">This command creates a new input on the job called EntryStream.</span></span>
<span data-ttu-id="3f989-117">Wenn bereits eine Eingabe mit diesem Namen definiert ist, fragt das Cmdlet, ob sie ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3f989-117">If an existing input with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="3f989-118">Beispiel 3: Ersetzen einer Auftragseingabe durch eine Definition aus einer Datei</span><span class="sxs-lookup"><span data-stu-id="3f989-118">Example 3: Replace a job input with a definition from a file</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream" -Force
```

<span data-ttu-id="3f989-119">Dieser Befehl ersetzt die Definition der vorhandenen Eingabequelle namens EntryStream durch die Definition aus der Datei ohne Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="3f989-119">This command replaces the definition of the existing input source called EntryStream with the definition from file without confirmation.</span></span>

## <span data-ttu-id="3f989-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f989-120">PARAMETERS</span></span>

### <span data-ttu-id="3f989-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f989-121">-DefaultProfile</span></span>
<span data-ttu-id="3f989-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3f989-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f989-123">-File</span><span class="sxs-lookup"><span data-stu-id="3f989-123">-File</span></span>
<span data-ttu-id="3f989-124">Gibt den Pfad zu einer JSON-Datei an, die die JSON-Darstellung der zu erstellenden Azure Stream Analytics-Eingabe enthält.</span><span class="sxs-lookup"><span data-stu-id="3f989-124">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics input to create.</span></span>

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

### <span data-ttu-id="3f989-125">-Force</span><span class="sxs-lookup"><span data-stu-id="3f989-125">-Force</span></span>
<span data-ttu-id="3f989-126">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="3f989-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3f989-127">-JobName</span><span class="sxs-lookup"><span data-stu-id="3f989-127">-JobName</span></span>
<span data-ttu-id="3f989-128">Gibt den Namen des Azure Stream Analytics-Auftrags an, unter dem die Azure Stream Analytics-Eingabe erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3f989-128">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics input.</span></span>

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

### <span data-ttu-id="3f989-129">-Name</span><span class="sxs-lookup"><span data-stu-id="3f989-129">-Name</span></span>
<span data-ttu-id="3f989-130">Gibt den Namen der Azure Stream Analytics-Eingabe an, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3f989-130">Specifies the name of the Azure Stream Analytics input to create.</span></span>

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

### <span data-ttu-id="3f989-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f989-131">-ResourceGroupName</span></span>
<span data-ttu-id="3f989-132">Gibt den Namen der Ressourcengruppe an, unter der die Azure -Streaming-Eingabe erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3f989-132">Specifies the name of the resource group under which to create the Azure Streaming input.</span></span>

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

### <span data-ttu-id="3f989-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f989-133">-Confirm</span></span>
<span data-ttu-id="3f989-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3f989-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f989-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3f989-135">-WhatIf</span></span>
<span data-ttu-id="3f989-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3f989-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f989-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3f989-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f989-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f989-138">CommonParameters</span></span>
<span data-ttu-id="3f989-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f989-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f989-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f989-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f989-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3f989-141">INPUTS</span></span>

### <span data-ttu-id="3f989-142">System.String</span><span class="sxs-lookup"><span data-stu-id="3f989-142">System.String</span></span>

## <span data-ttu-id="3f989-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3f989-143">OUTPUTS</span></span>

### <span data-ttu-id="3f989-144">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span><span class="sxs-lookup"><span data-stu-id="3f989-144">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="3f989-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3f989-145">NOTES</span></span>

## <span data-ttu-id="3f989-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3f989-146">RELATED LINKS</span></span>

[<span data-ttu-id="3f989-147">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="3f989-147">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="3f989-148">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="3f989-148">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)

[<span data-ttu-id="3f989-149">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="3f989-149">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


