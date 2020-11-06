---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 79EB2AD9-BFE1-49BE-870F-7DFC99D6FE17
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: 6b05bb1d379a5d9072cc286505a507d3718aa33e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93483237"
---
# <span data-ttu-id="8fa1d-101">New-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="8fa1d-101">New-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="8fa1d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8fa1d-102">SYNOPSIS</span></span>
<span data-ttu-id="8fa1d-103">Erstellt oder ersetzt eine Funktion in einem Datenstrom Analyse Auftrag.</span><span class="sxs-lookup"><span data-stu-id="8fa1d-103">Creates or replaces a function in a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fa1d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8fa1d-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8fa1d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8fa1d-105">DESCRIPTION</span></span>
<span data-ttu-id="8fa1d-106">Das Cmdlet **New-AzureRmStreamAnalyticsFunction** erstellt eine Funktion in einem Azure Stream-Analyse Auftrag oder ersetzt eine vorhandene Funktion.</span><span class="sxs-lookup"><span data-stu-id="8fa1d-106">The **New-AzureRmStreamAnalyticsFunction** cmdlet creates a function in an Azure Stream Analytics job or replaces an existing function.</span></span>
<span data-ttu-id="8fa1d-107">Definieren Sie die Funktion in einer JSON-Datei (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="8fa1d-107">Define the function in a JavaScript Object Notation (JSON) file.</span></span>

<span data-ttu-id="8fa1d-108">Sie können den Namen der Funktion mithilfe des *Name* -Parameters oder in der JSON-Datei angeben.</span><span class="sxs-lookup"><span data-stu-id="8fa1d-108">You can specify the name of the function by using the *Name* parameter or in the .json file.</span></span>
<span data-ttu-id="8fa1d-109">Wenn Sie den Namen auf beide Arten angeben, müssen die Namen übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="8fa1d-109">If you specify the name in both ways, the names must match.</span></span>

<span data-ttu-id="8fa1d-110">Wenn Sie eine vorhandene Funktion ersetzen möchten, geben Sie den Namen der vorhandenen Funktion an.</span><span class="sxs-lookup"><span data-stu-id="8fa1d-110">To replace an existing function, specify the name of the existing function.</span></span>

## <span data-ttu-id="8fa1d-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8fa1d-111">EXAMPLES</span></span>

### <span data-ttu-id="8fa1d-112">Beispiel 1: Erstellen einer Datenstrom Analysefunktion</span><span class="sxs-lookup"><span data-stu-id="8fa1d-112">Example 1: Create a Stream Analytics function</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob07" -File "C:\Function07.json"
```

<span data-ttu-id="8fa1d-113">Dieser Befehl erstellt eine Funktion aus der Datei Function07.jsauf.</span><span class="sxs-lookup"><span data-stu-id="8fa1d-113">This command creates a function from the file Function07.json.</span></span>
<span data-ttu-id="8fa1d-114">Der Name der Funktion wird in der JSON-Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="8fa1d-114">The name of the function is stored in the .json file.</span></span>

### <span data-ttu-id="8fa1d-115">Beispiel 2: Erstellen einer Datenstrom Analysefunktion mit dem Namen ScoreTweet</span><span class="sxs-lookup"><span data-stu-id="8fa1d-115">Example 2: Create a Stream Analytics function named ScoreTweet</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet"
```

<span data-ttu-id="8fa1d-116">Mit diesem Befehl wird eine Funktion für den Auftrag mit dem Namen "ScoreTweet" erstellt.</span><span class="sxs-lookup"><span data-stu-id="8fa1d-116">This command creates a function on the job named ScoreTweet.</span></span>

### <span data-ttu-id="8fa1d-117">Beispiel 3: Ersetzen einer Datenstrom Analysefunktion</span><span class="sxs-lookup"><span data-stu-id="8fa1d-117">Example 3: Replace a Stream Analytics function</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet" -Force
```

<span data-ttu-id="8fa1d-118">Dieser Befehl ersetzt die Definition der vorhandenen Funktion mit dem Namen ScoreTweet durch die Definition in Function22.jsein.</span><span class="sxs-lookup"><span data-stu-id="8fa1d-118">This command replaces the definition of the existing function named ScoreTweet with the definition in Function22.json.</span></span>

## <span data-ttu-id="8fa1d-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="8fa1d-119">PARAMETERS</span></span>

### <span data-ttu-id="8fa1d-120">-Datei</span><span class="sxs-lookup"><span data-stu-id="8fa1d-120">-File</span></span>
<span data-ttu-id="8fa1d-121">Gibt den Pfad einer JSON-Datei an, die die JSON-Darstellung der Datenstrom Analysefunktion enthält.</span><span class="sxs-lookup"><span data-stu-id="8fa1d-121">Specifies the path of a .json file that contains the JSON representation of the Stream Analytics function.</span></span>

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

### <span data-ttu-id="8fa1d-122">-Force</span><span class="sxs-lookup"><span data-stu-id="8fa1d-122">-Force</span></span>
<span data-ttu-id="8fa1d-123">Gibt an, dass dieses Cmdlet eine vorhandene Datenstrom Analysefunktion ersetzt, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="8fa1d-123">Indicates that this cmdlet replaces an existing Stream Analytics function without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="8fa1d-124">-Jobname</span><span class="sxs-lookup"><span data-stu-id="8fa1d-124">-JobName</span></span>
<span data-ttu-id="8fa1d-125">Gibt den Namen des Datenstrom Analyse Auftrags an, unter dem dieses Cmdlet eine Datenstrom Analysefunktion erstellt.</span><span class="sxs-lookup"><span data-stu-id="8fa1d-125">Specifies the name of the Stream Analytics job under which this cmdlet creates a Stream Analytics function.</span></span>

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

### <span data-ttu-id="8fa1d-126">-Name</span><span class="sxs-lookup"><span data-stu-id="8fa1d-126">-Name</span></span>
<span data-ttu-id="8fa1d-127">Gibt den Namen der Datenstrom Analysefunktion an, die von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="8fa1d-127">Specifies the name of the Stream Analytics function that this cmdlet creates.</span></span>

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

### <span data-ttu-id="8fa1d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fa1d-128">-ResourceGroupName</span></span>
<span data-ttu-id="8fa1d-129">Gibt den Namen der Ressourcengruppe an, unter der dieses Cmdlet eine Datenstrom Analysefunktion erstellt.</span><span class="sxs-lookup"><span data-stu-id="8fa1d-129">Specifies the name of the resource group under which this cmdlet creates a Stream Analytics function.</span></span>

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

### <span data-ttu-id="8fa1d-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8fa1d-130">-Confirm</span></span>
<span data-ttu-id="8fa1d-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8fa1d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fa1d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fa1d-132">-WhatIf</span></span>
<span data-ttu-id="8fa1d-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8fa1d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fa1d-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8fa1d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fa1d-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fa1d-135">-DefaultProfile</span></span>
<span data-ttu-id="8fa1d-136">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8fa1d-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fa1d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fa1d-137">CommonParameters</span></span>
<span data-ttu-id="8fa1d-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fa1d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fa1d-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fa1d-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fa1d-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8fa1d-140">INPUTS</span></span>

## <span data-ttu-id="8fa1d-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8fa1d-141">OUTPUTS</span></span>

### <span data-ttu-id="8fa1d-142">Microsoft. Azure. Commands. StreamAnalytics. Models. PSFunction</span><span class="sxs-lookup"><span data-stu-id="8fa1d-142">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="8fa1d-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="8fa1d-143">NOTES</span></span>

## <span data-ttu-id="8fa1d-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8fa1d-144">RELATED LINKS</span></span>

[<span data-ttu-id="8fa1d-145">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="8fa1d-145">Get-AzureRmStreamAnalyticsFunction</span></span>](./Get-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="8fa1d-146">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="8fa1d-146">Remove-AzureRmStreamAnalyticsFunction</span></span>](./Remove-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="8fa1d-147">Test-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="8fa1d-147">Test-AzureRmStreamAnalyticsFunction</span></span>](./Test-AzureRmStreamAnalyticsFunction.md)


