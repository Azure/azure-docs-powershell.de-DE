---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 35CE5C5F-F8D4-426F-A33A-4F9EA50E9B83
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: 84df5d0ed28b2d11b3e03e298242da4938a47eba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504689"
---
# <span data-ttu-id="1da9a-101">New-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="1da9a-101">New-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="1da9a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1da9a-102">SYNOPSIS</span></span>
<span data-ttu-id="1da9a-103">Erstellt eine Auftragseingabe oder aktualisiert sie.</span><span class="sxs-lookup"><span data-stu-id="1da9a-103">Creates or updates a job input.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1da9a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1da9a-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1da9a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1da9a-105">DESCRIPTION</span></span>
<span data-ttu-id="1da9a-106">Das Cmdlet **New-AzureRmStreamAnalyticsInput** erstellt eine Eingabe in einem Datenstrom Analyse Auftrag oder aktualisiert eine vorhandene Eingabe.</span><span class="sxs-lookup"><span data-stu-id="1da9a-106">The **New-AzureRmStreamAnalyticsInput** cmdlet creates an input within a Stream Analytics job or updates an existing input.</span></span>
<span data-ttu-id="1da9a-107">Der Name der Eingabe kann in der JSON-Datei oder in der Befehlszeile angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1da9a-107">The name of the input can be specified in the JSON file or on the command line.</span></span>
<span data-ttu-id="1da9a-108">Wenn beide angegeben sind, muss der Name in der Befehlszeile mit dem Namen in der Datei übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="1da9a-108">If both are specified, the name on command line must match the name in the file.</span></span>

<span data-ttu-id="1da9a-109">Wenn Sie eine Eingabe angeben, die bereits vorhanden ist, und den Parameter *Force* nicht angeben, fragt das Cmdlet, ob die vorhandene Eingabe ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1da9a-109">If you specify an input that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing input.</span></span>

<span data-ttu-id="1da9a-110">Wenn Sie den Parameter *Force* angeben und einen vorhandenen Eingabenamen angeben, wird die Eingabe ohne Bestätigung ersetzt.</span><span class="sxs-lookup"><span data-stu-id="1da9a-110">If you specify the *Force* parameter and specify an existing input name, the input will be replaced without confirmation.</span></span>

## <span data-ttu-id="1da9a-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1da9a-111">EXAMPLES</span></span>

### <span data-ttu-id="1da9a-112">Beispiel 1: Erstellen einer Auftragseingabe mit einer Definition aus einer Datei</span><span class="sxs-lookup"><span data-stu-id="1da9a-112">EXAMPLE 1: Create a job input with a definition from a file</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json"
```

<span data-ttu-id="1da9a-113">Dieser Befehl erstellt eine Eingabe aus der Datei Input.jsauf.</span><span class="sxs-lookup"><span data-stu-id="1da9a-113">This command creates an input from the file Input.json.</span></span>
<span data-ttu-id="1da9a-114">Wenn eine vorhandene Eingabe mit dem in der Eingabe Definitionsdatei angegebenen Namen bereits definiert ist, fragt das Cmdlet, ob es ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1da9a-114">If an existing input with the name specified in the input definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="1da9a-115">Beispiel 2: Erstellen einer Auftragseingabe</span><span class="sxs-lookup"><span data-stu-id="1da9a-115">EXAMPLE 2: Create a job input</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream"
```

<span data-ttu-id="1da9a-116">Dieser Befehl erstellt eine neue Eingabe für den Auftrag mit dem Namen EntryStream.</span><span class="sxs-lookup"><span data-stu-id="1da9a-116">This command creates a new input on the job called EntryStream.</span></span>
<span data-ttu-id="1da9a-117">Wenn eine vorhandene Eingabe mit diesem Namen bereits definiert ist, fragt das Cmdlet, ob Sie ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1da9a-117">If an existing input with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="1da9a-118">Beispiel 3: Ersetzen einer Auftragseingabe durch eine Definition aus einer Datei</span><span class="sxs-lookup"><span data-stu-id="1da9a-118">EXAMPLE 3: Replace a job input with a definition from a file</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream" -Force
```

<span data-ttu-id="1da9a-119">Dieser Befehl ersetzt die Definition der vorhandenen Eingabequelle namens EntryStream durch die Definition aus Datei ohne Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="1da9a-119">This command replaces the definition of the existing input source called EntryStream with the definition from file without confirmation.</span></span>

## <span data-ttu-id="1da9a-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="1da9a-120">PARAMETERS</span></span>

### <span data-ttu-id="1da9a-121">-Datei</span><span class="sxs-lookup"><span data-stu-id="1da9a-121">-File</span></span>
<span data-ttu-id="1da9a-122">Gibt den Pfad zu einer JSON-Datei an, die die JSON-Darstellung der zu erstellende Azure-Stream-Analyse Eingabe enthält.</span><span class="sxs-lookup"><span data-stu-id="1da9a-122">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics input to create.</span></span>

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

### <span data-ttu-id="1da9a-123">-Force</span><span class="sxs-lookup"><span data-stu-id="1da9a-123">-Force</span></span>
<span data-ttu-id="1da9a-124">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="1da9a-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1da9a-125">-Jobname</span><span class="sxs-lookup"><span data-stu-id="1da9a-125">-JobName</span></span>
<span data-ttu-id="1da9a-126">Gibt den Namen des Azure Stream Analytics-Auftrags an, unter dem die Azure Stream Analytics-Eingabe erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1da9a-126">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics input.</span></span>

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

### <span data-ttu-id="1da9a-127">-Name</span><span class="sxs-lookup"><span data-stu-id="1da9a-127">-Name</span></span>
<span data-ttu-id="1da9a-128">Gibt den Namen der zu erstellende Azure-Stream-Analyse Eingabe an.</span><span class="sxs-lookup"><span data-stu-id="1da9a-128">Specifies the name of the Azure Stream Analytics input to create.</span></span>

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

### <span data-ttu-id="1da9a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1da9a-129">-ResourceGroupName</span></span>
<span data-ttu-id="1da9a-130">Gibt den Namen der Ressourcengruppe an, unter der die Azure-Streaming-Eingabe erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1da9a-130">Specifies the name of the resource group under which to create the Azure Streaming input.</span></span>

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

### <span data-ttu-id="1da9a-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1da9a-131">-Confirm</span></span>
<span data-ttu-id="1da9a-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1da9a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1da9a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1da9a-133">-WhatIf</span></span>
<span data-ttu-id="1da9a-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1da9a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1da9a-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1da9a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1da9a-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1da9a-136">-DefaultProfile</span></span>
<span data-ttu-id="1da9a-137">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1da9a-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1da9a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1da9a-138">CommonParameters</span></span>
<span data-ttu-id="1da9a-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1da9a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1da9a-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1da9a-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1da9a-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1da9a-141">INPUTS</span></span>

## <span data-ttu-id="1da9a-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1da9a-142">OUTPUTS</span></span>

### <span data-ttu-id="1da9a-143">Microsoft. Azure. Commands. StreamAnalytics. Models. PSInput</span><span class="sxs-lookup"><span data-stu-id="1da9a-143">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="1da9a-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="1da9a-144">NOTES</span></span>

## <span data-ttu-id="1da9a-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1da9a-145">RELATED LINKS</span></span>

[<span data-ttu-id="1da9a-146">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="1da9a-146">Get-AzureRmStreamAnalyticsInput</span></span>](./Get-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="1da9a-147">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="1da9a-147">Remove-AzureRmStreamAnalyticsInput</span></span>](./Remove-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="1da9a-148">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="1da9a-148">Test-AzureRmStreamAnalyticsInput</span></span>](./Test-AzureRmStreamAnalyticsInput.md)


