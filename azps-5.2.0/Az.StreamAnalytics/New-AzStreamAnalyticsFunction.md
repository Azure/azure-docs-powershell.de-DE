---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 79EB2AD9-BFE1-49BE-870F-7DFC99D6FE17
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsFunction.md
ms.openlocfilehash: 71a6267b06ce47ee36f220033ec598af3680deeb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366385"
---
# <span data-ttu-id="62bfe-101">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="62bfe-101">New-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="62bfe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62bfe-102">SYNOPSIS</span></span>
<span data-ttu-id="62bfe-103">Erstellt oder ersetzt eine Funktion in einem Stream Analytics-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="62bfe-103">Creates or replaces a function in a Stream Analytics job.</span></span>

## <span data-ttu-id="62bfe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="62bfe-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="62bfe-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="62bfe-105">DESCRIPTION</span></span>
<span data-ttu-id="62bfe-106">Das **Cmdlet "New-AzStreamAnalyticsFunction"** erstellt eine Funktion in einem Azure Stream Analytics-Auftrag oder ersetzt eine vorhandene Funktion.</span><span class="sxs-lookup"><span data-stu-id="62bfe-106">The **New-AzStreamAnalyticsFunction** cmdlet creates a function in an Azure Stream Analytics job or replaces an existing function.</span></span>
<span data-ttu-id="62bfe-107">Definieren Sie die Funktion in einer JavaScript Object Notation (JSON)-Datei.</span><span class="sxs-lookup"><span data-stu-id="62bfe-107">Define the function in a JavaScript Object Notation (JSON) file.</span></span>
<span data-ttu-id="62bfe-108">Sie können den Namen der Funktion  mithilfe des Namensparameters oder in der JSON-Datei angeben.</span><span class="sxs-lookup"><span data-stu-id="62bfe-108">You can specify the name of the function by using the *Name* parameter or in the .json file.</span></span>
<span data-ttu-id="62bfe-109">Wenn Sie den Namen in beiden Weisen angeben, müssen die Namen übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="62bfe-109">If you specify the name in both ways, the names must match.</span></span>
<span data-ttu-id="62bfe-110">Um eine vorhandene Funktion zu ersetzen, geben Sie den Namen der vorhandenen Funktion an.</span><span class="sxs-lookup"><span data-stu-id="62bfe-110">To replace an existing function, specify the name of the existing function.</span></span>

## <span data-ttu-id="62bfe-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="62bfe-111">EXAMPLES</span></span>

### <span data-ttu-id="62bfe-112">Beispiel 1: Erstellen einer Streamanalysefunktion</span><span class="sxs-lookup"><span data-stu-id="62bfe-112">Example 1: Create a Stream Analytics function</span></span>
```
PS C:\>New-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob07" -File "C:\Function07.json"
```

<span data-ttu-id="62bfe-113">Mit diesem Befehl wird eine Funktion aus der Datei erstellt, Function07.jsist.</span><span class="sxs-lookup"><span data-stu-id="62bfe-113">This command creates a function from the file Function07.json.</span></span>
<span data-ttu-id="62bfe-114">Der Name der Funktion wird in der Datei ".json" gespeichert.</span><span class="sxs-lookup"><span data-stu-id="62bfe-114">The name of the function is stored in the .json file.</span></span>

### <span data-ttu-id="62bfe-115">Beispiel 2: Erstellen einer Datenstromanalysefunktion mit dem Namen ScoreTweet</span><span class="sxs-lookup"><span data-stu-id="62bfe-115">Example 2: Create a Stream Analytics function named ScoreTweet</span></span>
```
PS C:\>New-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet"
```

<span data-ttu-id="62bfe-116">Mit diesem Befehl wird eine Funktion für den Auftrag "ScoreTweet" erstellt.</span><span class="sxs-lookup"><span data-stu-id="62bfe-116">This command creates a function on the job named ScoreTweet.</span></span>

### <span data-ttu-id="62bfe-117">Beispiel 3: Ersetzen einer Datenstromanalysefunktion</span><span class="sxs-lookup"><span data-stu-id="62bfe-117">Example 3: Replace a Stream Analytics function</span></span>
```
PS C:\>New-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet" -Force
```

<span data-ttu-id="62bfe-118">Dieser Befehl ersetzt die Definition der vorhandenen Funktion "ScoreTweet" durch die Definition in Function22.json.</span><span class="sxs-lookup"><span data-stu-id="62bfe-118">This command replaces the definition of the existing function named ScoreTweet with the definition in Function22.json.</span></span>

## <span data-ttu-id="62bfe-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62bfe-119">PARAMETERS</span></span>

### <span data-ttu-id="62bfe-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62bfe-120">-DefaultProfile</span></span>
<span data-ttu-id="62bfe-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="62bfe-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62bfe-122">-File</span><span class="sxs-lookup"><span data-stu-id="62bfe-122">-File</span></span>
<span data-ttu-id="62bfe-123">Gibt den Pfad einer JSON-Datei an, die die JSON-Darstellung der Stream Analytics-Funktion enthält.</span><span class="sxs-lookup"><span data-stu-id="62bfe-123">Specifies the path of a .json file that contains the JSON representation of the Stream Analytics function.</span></span>

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

### <span data-ttu-id="62bfe-124">-Force</span><span class="sxs-lookup"><span data-stu-id="62bfe-124">-Force</span></span>
<span data-ttu-id="62bfe-125">Gibt an, dass dieses Cmdlet eine vorhandene Stream Analytics-Funktion ersetzt, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="62bfe-125">Indicates that this cmdlet replaces an existing Stream Analytics function without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="62bfe-126">-JobName</span><span class="sxs-lookup"><span data-stu-id="62bfe-126">-JobName</span></span>
<span data-ttu-id="62bfe-127">Gibt den Namen des Stream analytics-Auftrags an, unter dem dieses Cmdlet eine Stream Analytics-Funktion erstellt.</span><span class="sxs-lookup"><span data-stu-id="62bfe-127">Specifies the name of the Stream Analytics job under which this cmdlet creates a Stream Analytics function.</span></span>

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

### <span data-ttu-id="62bfe-128">-Name</span><span class="sxs-lookup"><span data-stu-id="62bfe-128">-Name</span></span>
<span data-ttu-id="62bfe-129">Gibt den Namen der Stream Analytics-Funktion an, die von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="62bfe-129">Specifies the name of the Stream Analytics function that this cmdlet creates.</span></span>

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

### <span data-ttu-id="62bfe-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62bfe-130">-ResourceGroupName</span></span>
<span data-ttu-id="62bfe-131">Gibt den Namen der Ressourcengruppe an, unter der dieses Cmdlet eine Stream analytics-Funktion erstellt.</span><span class="sxs-lookup"><span data-stu-id="62bfe-131">Specifies the name of the resource group under which this cmdlet creates a Stream Analytics function.</span></span>

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

### <span data-ttu-id="62bfe-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62bfe-132">-Confirm</span></span>
<span data-ttu-id="62bfe-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="62bfe-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62bfe-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="62bfe-134">-WhatIf</span></span>
<span data-ttu-id="62bfe-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="62bfe-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62bfe-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="62bfe-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62bfe-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62bfe-137">CommonParameters</span></span>
<span data-ttu-id="62bfe-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62bfe-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62bfe-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62bfe-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62bfe-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="62bfe-140">INPUTS</span></span>

### <span data-ttu-id="62bfe-141">System.String</span><span class="sxs-lookup"><span data-stu-id="62bfe-141">System.String</span></span>

## <span data-ttu-id="62bfe-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="62bfe-142">OUTPUTS</span></span>

### <span data-ttu-id="62bfe-143">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span><span class="sxs-lookup"><span data-stu-id="62bfe-143">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="62bfe-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="62bfe-144">NOTES</span></span>

## <span data-ttu-id="62bfe-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="62bfe-145">RELATED LINKS</span></span>

[<span data-ttu-id="62bfe-146">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="62bfe-146">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="62bfe-147">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="62bfe-147">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="62bfe-148">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="62bfe-148">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)


