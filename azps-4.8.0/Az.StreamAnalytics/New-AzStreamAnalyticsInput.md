---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 35CE5C5F-F8D4-426F-A33A-4F9EA50E9B83
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
ms.openlocfilehash: 74145a6d65fdaa9634d7681133e10b2496b5f903
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94007691"
---
# <span data-ttu-id="d9ac5-101">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="d9ac5-101">New-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="d9ac5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d9ac5-102">SYNOPSIS</span></span>
<span data-ttu-id="d9ac5-103">Erstellt eine Auftragseingabe oder aktualisiert sie.</span><span class="sxs-lookup"><span data-stu-id="d9ac5-103">Creates or updates a job input.</span></span>

## <span data-ttu-id="d9ac5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9ac5-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d9ac5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9ac5-105">DESCRIPTION</span></span>
<span data-ttu-id="d9ac5-106">Das Cmdlet **New-AzStreamAnalyticsInput** erstellt eine Eingabe in einem Datenstrom Analyse Auftrag oder aktualisiert eine vorhandene Eingabe.</span><span class="sxs-lookup"><span data-stu-id="d9ac5-106">The **New-AzStreamAnalyticsInput** cmdlet creates an input within a Stream Analytics job or updates an existing input.</span></span>
<span data-ttu-id="d9ac5-107">Der Name der Eingabe kann in der JSON-Datei oder in der Befehlszeile angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d9ac5-107">The name of the input can be specified in the JSON file or on the command line.</span></span>
<span data-ttu-id="d9ac5-108">Wenn beide angegeben sind, muss der Name in der Befehlszeile mit dem Namen in der Datei übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="d9ac5-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="d9ac5-109">Wenn Sie eine Eingabe angeben, die bereits vorhanden ist, und den Parameter *Force* nicht angeben, fragt das Cmdlet, ob die vorhandene Eingabe ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9ac5-109">If you specify an input that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing input.</span></span>
<span data-ttu-id="d9ac5-110">Wenn Sie den Parameter *Force* angeben und einen vorhandenen Eingabenamen angeben, wird die Eingabe ohne Bestätigung ersetzt.</span><span class="sxs-lookup"><span data-stu-id="d9ac5-110">If you specify the *Force* parameter and specify an existing input name, the input will be replaced without confirmation.</span></span>

## <span data-ttu-id="d9ac5-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d9ac5-111">EXAMPLES</span></span>

### <span data-ttu-id="d9ac5-112">Beispiel 1: Erstellen einer Auftragseingabe mit einer Definition aus einer Datei</span><span class="sxs-lookup"><span data-stu-id="d9ac5-112">Example 1: Create a job input with a definition from a file</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json"
```

<span data-ttu-id="d9ac5-113">Dieser Befehl erstellt eine Eingabe aus der Datei Input.jsauf.</span><span class="sxs-lookup"><span data-stu-id="d9ac5-113">This command creates an input from the file Input.json.</span></span>
<span data-ttu-id="d9ac5-114">Wenn eine vorhandene Eingabe mit dem in der Eingabe Definitionsdatei angegebenen Namen bereits definiert ist, fragt das Cmdlet, ob es ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9ac5-114">If an existing input with the name specified in the input definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="d9ac5-115">Beispiel 2: Erstellen einer Auftragseingabe</span><span class="sxs-lookup"><span data-stu-id="d9ac5-115">Example 2: Create a job input</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream"
```

<span data-ttu-id="d9ac5-116">Dieser Befehl erstellt eine neue Eingabe für den Auftrag mit dem Namen EntryStream.</span><span class="sxs-lookup"><span data-stu-id="d9ac5-116">This command creates a new input on the job called EntryStream.</span></span>
<span data-ttu-id="d9ac5-117">Wenn eine vorhandene Eingabe mit diesem Namen bereits definiert ist, fragt das Cmdlet, ob Sie ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9ac5-117">If an existing input with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="d9ac5-118">Beispiel 3: Ersetzen einer Auftragseingabe durch eine Definition aus einer Datei</span><span class="sxs-lookup"><span data-stu-id="d9ac5-118">Example 3: Replace a job input with a definition from a file</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream" -Force
```

<span data-ttu-id="d9ac5-119">Dieser Befehl ersetzt die Definition der vorhandenen Eingabequelle namens EntryStream durch die Definition aus Datei ohne Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="d9ac5-119">This command replaces the definition of the existing input source called EntryStream with the definition from file without confirmation.</span></span>

## <span data-ttu-id="d9ac5-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9ac5-120">PARAMETERS</span></span>

### <span data-ttu-id="d9ac5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9ac5-121">-DefaultProfile</span></span>
<span data-ttu-id="d9ac5-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d9ac5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9ac5-123">-Datei</span><span class="sxs-lookup"><span data-stu-id="d9ac5-123">-File</span></span>
<span data-ttu-id="d9ac5-124">Gibt den Pfad zu einer JSON-Datei an, die die JSON-Darstellung der zu erstellende Azure-Stream-Analyse Eingabe enthält.</span><span class="sxs-lookup"><span data-stu-id="d9ac5-124">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics input to create.</span></span>

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

### <span data-ttu-id="d9ac5-125">-Force</span><span class="sxs-lookup"><span data-stu-id="d9ac5-125">-Force</span></span>
<span data-ttu-id="d9ac5-126">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="d9ac5-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d9ac5-127">-Jobname</span><span class="sxs-lookup"><span data-stu-id="d9ac5-127">-JobName</span></span>
<span data-ttu-id="d9ac5-128">Gibt den Namen des Azure Stream Analytics-Auftrags an, unter dem die Azure Stream Analytics-Eingabe erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9ac5-128">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics input.</span></span>

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

### <span data-ttu-id="d9ac5-129">-Name</span><span class="sxs-lookup"><span data-stu-id="d9ac5-129">-Name</span></span>
<span data-ttu-id="d9ac5-130">Gibt den Namen der zu erstellende Azure-Stream-Analyse Eingabe an.</span><span class="sxs-lookup"><span data-stu-id="d9ac5-130">Specifies the name of the Azure Stream Analytics input to create.</span></span>

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

### <span data-ttu-id="d9ac5-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9ac5-131">-ResourceGroupName</span></span>
<span data-ttu-id="d9ac5-132">Gibt den Namen der Ressourcengruppe an, unter der die Azure-Streaming-Eingabe erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9ac5-132">Specifies the name of the resource group under which to create the Azure Streaming input.</span></span>

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

### <span data-ttu-id="d9ac5-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d9ac5-133">-Confirm</span></span>
<span data-ttu-id="d9ac5-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d9ac5-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9ac5-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9ac5-135">-WhatIf</span></span>
<span data-ttu-id="d9ac5-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d9ac5-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9ac5-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d9ac5-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9ac5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9ac5-138">CommonParameters</span></span>
<span data-ttu-id="d9ac5-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9ac5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9ac5-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9ac5-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9ac5-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d9ac5-141">INPUTS</span></span>

### <span data-ttu-id="d9ac5-142">System. String</span><span class="sxs-lookup"><span data-stu-id="d9ac5-142">System.String</span></span>

## <span data-ttu-id="d9ac5-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d9ac5-143">OUTPUTS</span></span>

### <span data-ttu-id="d9ac5-144">Microsoft. Azure. Commands. StreamAnalytics. Models. PSInput</span><span class="sxs-lookup"><span data-stu-id="d9ac5-144">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="d9ac5-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="d9ac5-145">NOTES</span></span>

## <span data-ttu-id="d9ac5-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d9ac5-146">RELATED LINKS</span></span>

[<span data-ttu-id="d9ac5-147">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="d9ac5-147">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="d9ac5-148">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="d9ac5-148">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)

[<span data-ttu-id="d9ac5-149">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="d9ac5-149">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


