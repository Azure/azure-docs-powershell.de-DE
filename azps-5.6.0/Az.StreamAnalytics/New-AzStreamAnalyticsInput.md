---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 35CE5C5F-F8D4-426F-A33A-4F9EA50E9B83
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/new-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
ms.openlocfilehash: 6dfb659987178b4bfe65855552e1018d085de360
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929528"
---
# <span data-ttu-id="1dfc1-101">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="1dfc1-101">New-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="1dfc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dfc1-102">SYNOPSIS</span></span>
<span data-ttu-id="1dfc1-103">Erstellt oder aktualisiert eine Auftragseingabe.</span><span class="sxs-lookup"><span data-stu-id="1dfc1-103">Creates or updates a job input.</span></span>

## <span data-ttu-id="1dfc1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1dfc1-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1dfc1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1dfc1-105">DESCRIPTION</span></span>
<span data-ttu-id="1dfc1-106">Das **Cmdlet New-AzStreamAnalyticsInput** erstellt eine Eingabe in einem Stream Analytics-Auftrag oder aktualisiert eine vorhandene Eingabe.</span><span class="sxs-lookup"><span data-stu-id="1dfc1-106">The **New-AzStreamAnalyticsInput** cmdlet creates an input within a Stream Analytics job or updates an existing input.</span></span>
<span data-ttu-id="1dfc1-107">Der Name der Eingabe kann in der JSON-Datei oder in der Befehlszeile angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1dfc1-107">The name of the input can be specified in the JSON file or on the command line.</span></span>
<span data-ttu-id="1dfc1-108">Wenn beide angegeben sind, muss der Name in der Befehlszeile mit dem Namen in der Datei übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="1dfc1-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="1dfc1-109">Wenn Sie eine bereits vorhandene Eingabe angeben  und nicht den Parameter Erzwingen angeben, fragt das Cmdlet, ob die vorhandene Eingabe ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1dfc1-109">If you specify an input that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing input.</span></span>
<span data-ttu-id="1dfc1-110">Wenn Sie den Parameter *Erzwingen* angeben und einen vorhandenen Eingabenamen angeben, wird die Eingabe ohne Bestätigung ersetzt.</span><span class="sxs-lookup"><span data-stu-id="1dfc1-110">If you specify the *Force* parameter and specify an existing input name, the input will be replaced without confirmation.</span></span>

## <span data-ttu-id="1dfc1-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1dfc1-111">EXAMPLES</span></span>

### <span data-ttu-id="1dfc1-112">Beispiel 1: Erstellen einer Auftragseingabe mit einer Definition aus einer Datei</span><span class="sxs-lookup"><span data-stu-id="1dfc1-112">Example 1: Create a job input with a definition from a file</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json"
```

<span data-ttu-id="1dfc1-113">Mit diesem Befehl wird eine Eingabe aus der Datei erstellt, Input.jswird.</span><span class="sxs-lookup"><span data-stu-id="1dfc1-113">This command creates an input from the file Input.json.</span></span>
<span data-ttu-id="1dfc1-114">Wenn eine vorhandene Eingabe mit dem in der Eingabedefinitionsdatei angegebenen Namen bereits definiert ist, fragt das Cmdlet, ob es ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1dfc1-114">If an existing input with the name specified in the input definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="1dfc1-115">Beispiel 2: Erstellen einer Auftragseingabe</span><span class="sxs-lookup"><span data-stu-id="1dfc1-115">Example 2: Create a job input</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream"
```

<span data-ttu-id="1dfc1-116">Mit diesem Befehl wird eine neue Eingabe für den Auftrag namens EntryStream erstellt.</span><span class="sxs-lookup"><span data-stu-id="1dfc1-116">This command creates a new input on the job called EntryStream.</span></span>
<span data-ttu-id="1dfc1-117">Wenn eine vorhandene Eingabe mit diesem Namen bereits definiert ist, fragt das Cmdlet, ob es ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1dfc1-117">If an existing input with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="1dfc1-118">Beispiel 3: Ersetzen einer Auftragseingabe durch eine Definition aus einer Datei</span><span class="sxs-lookup"><span data-stu-id="1dfc1-118">Example 3: Replace a job input with a definition from a file</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream" -Force
```

<span data-ttu-id="1dfc1-119">Dieser Befehl ersetzt die Definition der vorhandenen Eingabequelle namens EntryStream durch die Definition aus der Datei ohne Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="1dfc1-119">This command replaces the definition of the existing input source called EntryStream with the definition from file without confirmation.</span></span>

## <span data-ttu-id="1dfc1-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1dfc1-120">PARAMETERS</span></span>

### <span data-ttu-id="1dfc1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dfc1-121">-DefaultProfile</span></span>
<span data-ttu-id="1dfc1-122">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1dfc1-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1dfc1-123">-Datei</span><span class="sxs-lookup"><span data-stu-id="1dfc1-123">-File</span></span>
<span data-ttu-id="1dfc1-124">Gibt den Pfad zu einer JSON-Datei an, der die JSON-Darstellung der zu erstellenden Azure Stream Analytics-Eingabe enthält.</span><span class="sxs-lookup"><span data-stu-id="1dfc1-124">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics input to create.</span></span>

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

### <span data-ttu-id="1dfc1-125">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="1dfc1-125">-Force</span></span>
<span data-ttu-id="1dfc1-126">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="1dfc1-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1dfc1-127">-JobName</span><span class="sxs-lookup"><span data-stu-id="1dfc1-127">-JobName</span></span>
<span data-ttu-id="1dfc1-128">Gibt den Namen des Azure Stream Analytics-Auftrags an, unter dem die Azure Stream Analytics-Eingabe erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1dfc1-128">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics input.</span></span>

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

### <span data-ttu-id="1dfc1-129">-Name</span><span class="sxs-lookup"><span data-stu-id="1dfc1-129">-Name</span></span>
<span data-ttu-id="1dfc1-130">Gibt den Namen der zu erstellenden Azure Stream Analytics-Eingabe an.</span><span class="sxs-lookup"><span data-stu-id="1dfc1-130">Specifies the name of the Azure Stream Analytics input to create.</span></span>

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

### <span data-ttu-id="1dfc1-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dfc1-131">-ResourceGroupName</span></span>
<span data-ttu-id="1dfc1-132">Gibt den Namen der Ressourcengruppe an, unter der die Azure Streaming-Eingabe erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1dfc1-132">Specifies the name of the resource group under which to create the Azure Streaming input.</span></span>

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

### <span data-ttu-id="1dfc1-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1dfc1-133">-Confirm</span></span>
<span data-ttu-id="1dfc1-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1dfc1-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dfc1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dfc1-135">-WhatIf</span></span>
<span data-ttu-id="1dfc1-136">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1dfc1-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dfc1-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1dfc1-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dfc1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dfc1-138">CommonParameters</span></span>
<span data-ttu-id="1dfc1-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dfc1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dfc1-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dfc1-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dfc1-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1dfc1-141">INPUTS</span></span>

### <span data-ttu-id="1dfc1-142">System.String</span><span class="sxs-lookup"><span data-stu-id="1dfc1-142">System.String</span></span>

## <span data-ttu-id="1dfc1-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1dfc1-143">OUTPUTS</span></span>

### <span data-ttu-id="1dfc1-144">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span><span class="sxs-lookup"><span data-stu-id="1dfc1-144">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="1dfc1-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1dfc1-145">NOTES</span></span>

## <span data-ttu-id="1dfc1-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1dfc1-146">RELATED LINKS</span></span>

[<span data-ttu-id="1dfc1-147">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="1dfc1-147">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="1dfc1-148">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="1dfc1-148">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)

[<span data-ttu-id="1dfc1-149">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="1dfc1-149">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


