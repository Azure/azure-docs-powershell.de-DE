---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 43B2A4FD-DA74-403A-89D0-40FE9A3E5A7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsOutput.md
ms.openlocfilehash: b0e32d58d416fce869995595c3e2a2ff69e8f349
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010353"
---
# <span data-ttu-id="8779f-101">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="8779f-101">New-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="8779f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8779f-102">SYNOPSIS</span></span>
<span data-ttu-id="8779f-103">Erstellt oder aktualisiert Ausgaben für einen Datenstrom Analyse Auftrag.</span><span class="sxs-lookup"><span data-stu-id="8779f-103">Creates or updates outputs for a Stream Analytics job.</span></span>

## <span data-ttu-id="8779f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8779f-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8779f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8779f-105">DESCRIPTION</span></span>
<span data-ttu-id="8779f-106">Das Cmdlet **New-AzStreamAnalyticsOutput** erstellt eine Ausgabe innerhalb eines Datenstrom Analyse Auftrags oder aktualisiert eine vorhandene Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="8779f-106">The **New-AzStreamAnalyticsOutput** cmdlet creates an output within a Stream Analytics job or updates an existing output.</span></span>
<span data-ttu-id="8779f-107">Der Name der Ausgabe kann in der angegeben werden. JSON-Datei oder in der Befehlszeile.</span><span class="sxs-lookup"><span data-stu-id="8779f-107">The name of the output can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="8779f-108">Wenn beide angegeben sind, muss der Name in der Befehlszeile mit dem Namen in der Datei übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="8779f-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="8779f-109">Wenn Sie eine Ausgabe angeben, die bereits vorhanden ist, und den Parameter *Force* nicht angeben, fragt das Cmdlet, ob die vorhandene Ausgabe ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8779f-109">If you specify an output that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing output.</span></span>
<span data-ttu-id="8779f-110">Wenn Sie den Parameter *Force* angeben und einen vorhandenen Ausgabe Namen angeben, wird die Ausgabe ohne Bestätigung ersetzt.</span><span class="sxs-lookup"><span data-stu-id="8779f-110">If you specify the *Force* parameter and specify an existing output name, the output will be replaced without confirmation.</span></span>

## <span data-ttu-id="8779f-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8779f-111">EXAMPLES</span></span>

### <span data-ttu-id="8779f-112">Beispiel 1: Hinzufügen einer Ausgabe zu einem Auftrag</span><span class="sxs-lookup"><span data-stu-id="8779f-112">Example 1: Add an output to a job</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="8779f-113">Dieser Befehl erstellt eine neue Ausgabe namens Output im Auftrag namens StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="8779f-113">This command creates a new output called Output in the job called StreamingJob.</span></span>
<span data-ttu-id="8779f-114">Wenn eine vorhandene Ausgabe mit diesem Namen bereits definiert ist, fragt das Cmdlet, ob Sie ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8779f-114">If an existing output with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="8779f-115">Beispiel 2: Ersetzen einer Auftragsausgabe Definition</span><span class="sxs-lookup"><span data-stu-id="8779f-115">Example 2: Replace a job output definition</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output" -Force
```

<span data-ttu-id="8779f-116">Dieser Befehl ersetzt die Definition für die Ausgabe im Job namens StreamingJob ohne Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="8779f-116">This command replaces the definition for Output in the job called StreamingJob without confirmation.</span></span>

## <span data-ttu-id="8779f-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="8779f-117">PARAMETERS</span></span>

### <span data-ttu-id="8779f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8779f-118">-DefaultProfile</span></span>
<span data-ttu-id="8779f-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8779f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8779f-120">-Datei</span><span class="sxs-lookup"><span data-stu-id="8779f-120">-File</span></span>
<span data-ttu-id="8779f-121">Gibt den Pfad zu einer JSON-Datei an, die die JSON-Darstellung der zu erstellende Azure-Stream-Analyseausgabe enthält.</span><span class="sxs-lookup"><span data-stu-id="8779f-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics output to create.</span></span>

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

### <span data-ttu-id="8779f-122">-Force</span><span class="sxs-lookup"><span data-stu-id="8779f-122">-Force</span></span>
<span data-ttu-id="8779f-123">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="8779f-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8779f-124">-Jobname</span><span class="sxs-lookup"><span data-stu-id="8779f-124">-JobName</span></span>
<span data-ttu-id="8779f-125">Gibt den Namen des Azure Stream Analytics-Auftrags an, unter dem die Azure Stream Analytics-Ausgabe erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8779f-125">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics output.</span></span>

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

### <span data-ttu-id="8779f-126">-Name</span><span class="sxs-lookup"><span data-stu-id="8779f-126">-Name</span></span>
<span data-ttu-id="8779f-127">Gibt den Namen der zu erstellende Azure-Datenstrom Analyseausgabe an.</span><span class="sxs-lookup"><span data-stu-id="8779f-127">Specifies the name of the Azure Stream Analytics output to create.</span></span>

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

### <span data-ttu-id="8779f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8779f-128">-ResourceGroupName</span></span>
<span data-ttu-id="8779f-129">Gibt den Namen der Ressourcengruppe an, unter der die Azure Stream Analytics-Ausgabe erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8779f-129">Specifies the name of the resource group under which to create the Azure Stream Analytics output.</span></span>

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

### <span data-ttu-id="8779f-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8779f-130">-Confirm</span></span>
<span data-ttu-id="8779f-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8779f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8779f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8779f-132">-WhatIf</span></span>
<span data-ttu-id="8779f-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8779f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8779f-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8779f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8779f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8779f-135">CommonParameters</span></span>
<span data-ttu-id="8779f-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8779f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8779f-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8779f-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8779f-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8779f-138">INPUTS</span></span>

### <span data-ttu-id="8779f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8779f-139">System.String</span></span>

## <span data-ttu-id="8779f-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8779f-140">OUTPUTS</span></span>

### <span data-ttu-id="8779f-141">Microsoft. Azure. Commands. StreamAnalytics. Models. PSOutput</span><span class="sxs-lookup"><span data-stu-id="8779f-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="8779f-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="8779f-142">NOTES</span></span>

## <span data-ttu-id="8779f-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8779f-143">RELATED LINKS</span></span>

[<span data-ttu-id="8779f-144">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="8779f-144">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="8779f-145">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="8779f-145">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="8779f-146">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="8779f-146">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


