---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 8FF53426-D4AE-455E-A182-D7FBC7262FE1
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: 017c084e98d8983343ae1f8c19464cc254b26e2e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176378"
---
# <span data-ttu-id="f969b-101">New-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="f969b-101">New-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="f969b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f969b-102">SYNOPSIS</span></span>
<span data-ttu-id="f969b-103">Erstellt oder aktualisiert eine Transformation innerhalb eines Auftrags.</span><span class="sxs-lookup"><span data-stu-id="f969b-103">Creates or updates a transformation within a job.</span></span>

## <span data-ttu-id="f969b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f969b-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsTransformation [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f969b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f969b-105">DESCRIPTION</span></span>
<span data-ttu-id="f969b-106">Das Cmdlet **New-AzStreamAnalyticsTransformation** erstellt eine Transformation innerhalb eines Datenstrom Analyse Auftrags oder aktualisiert die vorhandene Transformation.</span><span class="sxs-lookup"><span data-stu-id="f969b-106">The **New-AzStreamAnalyticsTransformation** cmdlet creates a transformation within a Stream Analytics job or updates the existing transformation.</span></span>
<span data-ttu-id="f969b-107">Der Name der Transformation kann in der angegeben werden. JSON-Datei oder in der Befehlszeile.</span><span class="sxs-lookup"><span data-stu-id="f969b-107">The name of the transformation can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="f969b-108">Wenn beide angegeben sind, muss der Name in der Befehlszeile mit dem Namen in der Datei übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="f969b-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="f969b-109">Wenn Sie eine Transformation angeben, die bereits vorhanden ist, und den Parameter Force nicht angeben, fragt das Cmdlet, ob die vorhandene Transformation ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f969b-109">If you specify a transformation that already exists and do not specify the Force parameter, the cmdlet will ask whether or not to replace the existing transformation.</span></span>
<span data-ttu-id="f969b-110">Wenn Sie den Parameter *Force* angeben und einen vorhandenen Umwandlungs Namen angeben, wird die Transformation ohne Bestätigung ersetzt.</span><span class="sxs-lookup"><span data-stu-id="f969b-110">If you specify the *Force* parameter and specify an existing transformation name, the transformation will be replaced without confirmation.</span></span>

## <span data-ttu-id="f969b-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f969b-111">EXAMPLES</span></span>

### <span data-ttu-id="f969b-112">Beispiel 1: Erstellen oder Ersetzen einer Transformation in einem Auftrag</span><span class="sxs-lookup"><span data-stu-id="f969b-112">Example 1: Create or replace a transformation in a job</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform"
```

<span data-ttu-id="f969b-113">Dieser Befehl erstellt eine Transformation namens "StreamingJobTransform" im Auftrag "StreamingJob".</span><span class="sxs-lookup"><span data-stu-id="f969b-113">This command creates a transformation called StreamingJobTransform in the job called StreamingJob.</span></span>
<span data-ttu-id="f969b-114">Wenn bereits eine vorhandene Transformation mit diesem Namen definiert ist, fragt das Cmdlet, ob es ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f969b-114">If an existing transformation is already defined with that name, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="f969b-115">Beispiel 2: Ersetzen einer Transformation in einem Auftrag</span><span class="sxs-lookup"><span data-stu-id="f969b-115">Example 2: Replace a transformation in a job</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform" -Force
```

<span data-ttu-id="f969b-116">Dieser Befehl ersetzt die Definition von StreamingJobTransform im Job-StreamingJob ohne Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="f969b-116">This command replaces the definition of StreamingJobTransform in the job StreamingJob without confirmation.</span></span>

## <span data-ttu-id="f969b-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="f969b-117">PARAMETERS</span></span>

### <span data-ttu-id="f969b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f969b-118">-DefaultProfile</span></span>
<span data-ttu-id="f969b-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f969b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f969b-120">-Datei</span><span class="sxs-lookup"><span data-stu-id="f969b-120">-File</span></span>
<span data-ttu-id="f969b-121">Gibt den Pfad zu einer JSON-Datei an, die die JSON-Darstellung der zu erstellende Azure Stream Analytics-Transformation enthält.</span><span class="sxs-lookup"><span data-stu-id="f969b-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics transformation to create.</span></span>

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

### <span data-ttu-id="f969b-122">-Force</span><span class="sxs-lookup"><span data-stu-id="f969b-122">-Force</span></span>
<span data-ttu-id="f969b-123">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="f969b-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f969b-124">-Jobname</span><span class="sxs-lookup"><span data-stu-id="f969b-124">-JobName</span></span>
<span data-ttu-id="f969b-125">Gibt den Namen des Azure Stream Analytics-Auftrags an, unter dem die Azure Stream Analytics-Transformation erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f969b-125">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="f969b-126">-Name</span><span class="sxs-lookup"><span data-stu-id="f969b-126">-Name</span></span>
<span data-ttu-id="f969b-127">Gibt den Namen der zu erstellende Azure Stream Analytics-Transformation an.</span><span class="sxs-lookup"><span data-stu-id="f969b-127">Specifies the name of the Azure Stream Analytics transformation to create.</span></span>

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

### <span data-ttu-id="f969b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f969b-128">-ResourceGroupName</span></span>
<span data-ttu-id="f969b-129">Gibt den Namen der Ressourcengruppe an, unter der die Azure Stream Analytics-Transformation erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f969b-129">Specifies the name of the resource group under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="f969b-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f969b-130">-Confirm</span></span>
<span data-ttu-id="f969b-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f969b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f969b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f969b-132">-WhatIf</span></span>
<span data-ttu-id="f969b-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f969b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f969b-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f969b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f969b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f969b-135">CommonParameters</span></span>
<span data-ttu-id="f969b-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f969b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f969b-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f969b-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f969b-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f969b-138">INPUTS</span></span>

### <span data-ttu-id="f969b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f969b-139">System.String</span></span>

## <span data-ttu-id="f969b-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f969b-140">OUTPUTS</span></span>

### <span data-ttu-id="f969b-141">Microsoft. Azure. Commands. StreamAnalytics. Models. PSTransformation</span><span class="sxs-lookup"><span data-stu-id="f969b-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="f969b-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="f969b-142">NOTES</span></span>

## <span data-ttu-id="f969b-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f969b-143">RELATED LINKS</span></span>

[<span data-ttu-id="f969b-144">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="f969b-144">Get-AzStreamAnalyticsTransformation</span></span>](./Get-AzStreamAnalyticsTransformation.md)


