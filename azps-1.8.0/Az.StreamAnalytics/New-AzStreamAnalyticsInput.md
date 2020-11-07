---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 35CE5C5F-F8D4-426F-A33A-4F9EA50E9B83
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
ms.openlocfilehash: 60bc6754fb63d118e2b74e60ab503600a128ba3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658655"
---
# <span data-ttu-id="03754-101">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="03754-101">New-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="03754-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="03754-102">SYNOPSIS</span></span>
<span data-ttu-id="03754-103">Erstellt eine Auftragseingabe oder aktualisiert sie.</span><span class="sxs-lookup"><span data-stu-id="03754-103">Creates or updates a job input.</span></span>

## <span data-ttu-id="03754-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="03754-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="03754-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="03754-105">DESCRIPTION</span></span>
<span data-ttu-id="03754-106">Das Cmdlet **New-AzStreamAnalyticsInput** erstellt eine Eingabe in einem Datenstrom Analyse Auftrag oder aktualisiert eine vorhandene Eingabe.</span><span class="sxs-lookup"><span data-stu-id="03754-106">The **New-AzStreamAnalyticsInput** cmdlet creates an input within a Stream Analytics job or updates an existing input.</span></span>
<span data-ttu-id="03754-107">Der Name der Eingabe kann in der JSON-Datei oder in der Befehlszeile angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="03754-107">The name of the input can be specified in the JSON file or on the command line.</span></span>
<span data-ttu-id="03754-108">Wenn beide angegeben sind, muss der Name in der Befehlszeile mit dem Namen in der Datei übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="03754-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="03754-109">Wenn Sie eine Eingabe angeben, die bereits vorhanden ist, und den Parameter *Force* nicht angeben, fragt das Cmdlet, ob die vorhandene Eingabe ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="03754-109">If you specify an input that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing input.</span></span>
<span data-ttu-id="03754-110">Wenn Sie den Parameter *Force* angeben und einen vorhandenen Eingabenamen angeben, wird die Eingabe ohne Bestätigung ersetzt.</span><span class="sxs-lookup"><span data-stu-id="03754-110">If you specify the *Force* parameter and specify an existing input name, the input will be replaced without confirmation.</span></span>

## <span data-ttu-id="03754-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="03754-111">EXAMPLES</span></span>

### <span data-ttu-id="03754-112">Beispiel 1: Erstellen einer Auftragseingabe mit einer Definition aus einer Datei</span><span class="sxs-lookup"><span data-stu-id="03754-112">EXAMPLE 1: Create a job input with a definition from a file</span></span>
```
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json"
```

<span data-ttu-id="03754-113">Dieser Befehl erstellt eine Eingabe aus der Datei Input.jsauf.</span><span class="sxs-lookup"><span data-stu-id="03754-113">This command creates an input from the file Input.json.</span></span>
<span data-ttu-id="03754-114">Wenn eine vorhandene Eingabe mit dem in der Eingabe Definitionsdatei angegebenen Namen bereits definiert ist, fragt das Cmdlet, ob es ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="03754-114">If an existing input with the name specified in the input definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="03754-115">Beispiel 2: Erstellen einer Auftragseingabe</span><span class="sxs-lookup"><span data-stu-id="03754-115">EXAMPLE 2: Create a job input</span></span>
```
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream"
```

<span data-ttu-id="03754-116">Dieser Befehl erstellt eine neue Eingabe für den Auftrag mit dem Namen EntryStream.</span><span class="sxs-lookup"><span data-stu-id="03754-116">This command creates a new input on the job called EntryStream.</span></span>
<span data-ttu-id="03754-117">Wenn eine vorhandene Eingabe mit diesem Namen bereits definiert ist, fragt das Cmdlet, ob Sie ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="03754-117">If an existing input with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="03754-118">Beispiel 3: Ersetzen einer Auftragseingabe durch eine Definition aus einer Datei</span><span class="sxs-lookup"><span data-stu-id="03754-118">EXAMPLE 3: Replace a job input with a definition from a file</span></span>
```
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream" -Force
```

<span data-ttu-id="03754-119">Dieser Befehl ersetzt die Definition der vorhandenen Eingabequelle namens EntryStream durch die Definition aus Datei ohne Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="03754-119">This command replaces the definition of the existing input source called EntryStream with the definition from file without confirmation.</span></span>

## <span data-ttu-id="03754-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="03754-120">PARAMETERS</span></span>

### <span data-ttu-id="03754-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03754-121">-DefaultProfile</span></span>
<span data-ttu-id="03754-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="03754-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03754-123">-Datei</span><span class="sxs-lookup"><span data-stu-id="03754-123">-File</span></span>
<span data-ttu-id="03754-124">Gibt den Pfad zu einer JSON-Datei an, die die JSON-Darstellung der zu erstellende Azure-Stream-Analyse Eingabe enthält.</span><span class="sxs-lookup"><span data-stu-id="03754-124">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics input to create.</span></span>

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

### <span data-ttu-id="03754-125">-Force</span><span class="sxs-lookup"><span data-stu-id="03754-125">-Force</span></span>
<span data-ttu-id="03754-126">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="03754-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="03754-127">-Jobname</span><span class="sxs-lookup"><span data-stu-id="03754-127">-JobName</span></span>
<span data-ttu-id="03754-128">Gibt den Namen des Azure Stream Analytics-Auftrags an, unter dem die Azure Stream Analytics-Eingabe erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="03754-128">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics input.</span></span>

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

### <span data-ttu-id="03754-129">-Name</span><span class="sxs-lookup"><span data-stu-id="03754-129">-Name</span></span>
<span data-ttu-id="03754-130">Gibt den Namen der zu erstellende Azure-Stream-Analyse Eingabe an.</span><span class="sxs-lookup"><span data-stu-id="03754-130">Specifies the name of the Azure Stream Analytics input to create.</span></span>

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

### <span data-ttu-id="03754-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03754-131">-ResourceGroupName</span></span>
<span data-ttu-id="03754-132">Gibt den Namen der Ressourcengruppe an, unter der die Azure-Streaming-Eingabe erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="03754-132">Specifies the name of the resource group under which to create the Azure Streaming input.</span></span>

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

### <span data-ttu-id="03754-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="03754-133">-Confirm</span></span>
<span data-ttu-id="03754-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="03754-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03754-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03754-135">-WhatIf</span></span>
<span data-ttu-id="03754-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="03754-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03754-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="03754-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03754-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03754-138">CommonParameters</span></span>
<span data-ttu-id="03754-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03754-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03754-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03754-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03754-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="03754-141">INPUTS</span></span>

### <span data-ttu-id="03754-142">System. String</span><span class="sxs-lookup"><span data-stu-id="03754-142">System.String</span></span>

## <span data-ttu-id="03754-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="03754-143">OUTPUTS</span></span>

### <span data-ttu-id="03754-144">Microsoft. Azure. Commands. StreamAnalytics. Models. PSInput</span><span class="sxs-lookup"><span data-stu-id="03754-144">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="03754-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="03754-145">NOTES</span></span>

## <span data-ttu-id="03754-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="03754-146">RELATED LINKS</span></span>

[<span data-ttu-id="03754-147">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="03754-147">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="03754-148">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="03754-148">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)

[<span data-ttu-id="03754-149">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="03754-149">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


