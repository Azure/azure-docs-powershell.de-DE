---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 43B2A4FD-DA74-403A-89D0-40FE9A3E5A7E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/new-azurermstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: 7b18513a6a9e7ebbf82892500344d13f9cbc8185
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498665"
---
# <span data-ttu-id="25da2-101">New-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="25da2-101">New-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="25da2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="25da2-102">SYNOPSIS</span></span>
<span data-ttu-id="25da2-103">Erstellt oder aktualisiert Ausgaben für einen Datenstrom Analyse Auftrag.</span><span class="sxs-lookup"><span data-stu-id="25da2-103">Creates or updates outputs for a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25da2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="25da2-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="25da2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="25da2-105">DESCRIPTION</span></span>
<span data-ttu-id="25da2-106">Das Cmdlet **New-AzureRmStreamAnalyticsOutput** erstellt eine Ausgabe innerhalb eines Datenstrom Analyse Auftrags oder aktualisiert eine vorhandene Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="25da2-106">The **New-AzureRmStreamAnalyticsOutput** cmdlet creates an output within a Stream Analytics job or updates an existing output.</span></span>
<span data-ttu-id="25da2-107">Der Name der Ausgabe kann in der angegeben werden. JSON-Datei oder in der Befehlszeile.</span><span class="sxs-lookup"><span data-stu-id="25da2-107">The name of the output can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="25da2-108">Wenn beide angegeben sind, muss der Name in der Befehlszeile mit dem Namen in der Datei übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="25da2-108">If both are specified, the name on command line must match the name in the file.</span></span>

<span data-ttu-id="25da2-109">Wenn Sie eine Ausgabe angeben, die bereits vorhanden ist, und den Parameter *Force* nicht angeben, fragt das Cmdlet, ob die vorhandene Ausgabe ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="25da2-109">If you specify an output that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing output.</span></span>

<span data-ttu-id="25da2-110">Wenn Sie den Parameter *Force* angeben und einen vorhandenen Ausgabe Namen angeben, wird die Ausgabe ohne Bestätigung ersetzt.</span><span class="sxs-lookup"><span data-stu-id="25da2-110">If you specify the *Force* parameter and specify an existing output name, the output will be replaced without confirmation.</span></span>

## <span data-ttu-id="25da2-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="25da2-111">EXAMPLES</span></span>

### <span data-ttu-id="25da2-112">Beispiel 1: Hinzufügen einer Ausgabe zu einem Auftrag</span><span class="sxs-lookup"><span data-stu-id="25da2-112">EXAMPLE 1: Add an output to a job</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="25da2-113">Dieser Befehl erstellt eine neue Ausgabe namens Output im Auftrag namens StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="25da2-113">This command creates a new output called Output in the job called StreamingJob.</span></span>
<span data-ttu-id="25da2-114">Wenn eine vorhandene Ausgabe mit diesem Namen bereits definiert ist, fragt das Cmdlet, ob Sie ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="25da2-114">If an existing output with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="25da2-115">Beispiel 2: Ersetzen einer Auftragsausgabe Definition</span><span class="sxs-lookup"><span data-stu-id="25da2-115">EXAMPLE 2: Replace a job output definition</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output" -Force
```

<span data-ttu-id="25da2-116">Dieser Befehl ersetzt die Definition für die Ausgabe im Job namens StreamingJob ohne Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="25da2-116">This command replaces the definition for Output in the job called StreamingJob without confirmation.</span></span>

## <span data-ttu-id="25da2-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="25da2-117">PARAMETERS</span></span>

### <span data-ttu-id="25da2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25da2-118">-DefaultProfile</span></span>
<span data-ttu-id="25da2-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="25da2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25da2-120">-Datei</span><span class="sxs-lookup"><span data-stu-id="25da2-120">-File</span></span>
<span data-ttu-id="25da2-121">Gibt den Pfad zu einer JSON-Datei an, die die JSON-Darstellung der zu erstellende Azure-Stream-Analyseausgabe enthält.</span><span class="sxs-lookup"><span data-stu-id="25da2-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics output to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25da2-122">-Force</span><span class="sxs-lookup"><span data-stu-id="25da2-122">-Force</span></span>
<span data-ttu-id="25da2-123">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="25da2-123">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25da2-124">-Jobname</span><span class="sxs-lookup"><span data-stu-id="25da2-124">-JobName</span></span>
<span data-ttu-id="25da2-125">Gibt den Namen des Azure Stream Analytics-Auftrags an, unter dem die Azure Stream Analytics-Ausgabe erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="25da2-125">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics output.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25da2-126">-Name</span><span class="sxs-lookup"><span data-stu-id="25da2-126">-Name</span></span>
<span data-ttu-id="25da2-127">Gibt den Namen der zu erstellende Azure-Datenstrom Analyseausgabe an.</span><span class="sxs-lookup"><span data-stu-id="25da2-127">Specifies the name of the Azure Stream Analytics output to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25da2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25da2-128">-ResourceGroupName</span></span>
<span data-ttu-id="25da2-129">Gibt den Namen der Ressourcengruppe an, unter der die Azure Stream Analytics-Ausgabe erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="25da2-129">Specifies the name of the resource group under which to create the Azure Stream Analytics output.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25da2-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="25da2-130">-Confirm</span></span>
<span data-ttu-id="25da2-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="25da2-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25da2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25da2-132">-WhatIf</span></span>
<span data-ttu-id="25da2-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="25da2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25da2-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="25da2-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25da2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25da2-135">CommonParameters</span></span>
<span data-ttu-id="25da2-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25da2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25da2-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25da2-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25da2-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="25da2-138">INPUTS</span></span>

### <span data-ttu-id="25da2-139">Keine</span><span class="sxs-lookup"><span data-stu-id="25da2-139">None</span></span>
<span data-ttu-id="25da2-140">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="25da2-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="25da2-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="25da2-141">OUTPUTS</span></span>

### <span data-ttu-id="25da2-142">Microsoft. Azure. Commands. StreamAnalytics. Models. PSOutput</span><span class="sxs-lookup"><span data-stu-id="25da2-142">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="25da2-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="25da2-143">NOTES</span></span>

## <span data-ttu-id="25da2-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="25da2-144">RELATED LINKS</span></span>

[<span data-ttu-id="25da2-145">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="25da2-145">Get-AzureRmStreamAnalyticsOutput</span></span>](./Get-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="25da2-146">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="25da2-146">Remove-AzureRmStreamAnalyticsOutput</span></span>](./Remove-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="25da2-147">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="25da2-147">Test-AzureRmStreamAnalyticsOutput</span></span>](./Test-AzureRmStreamAnalyticsOutput.md)


