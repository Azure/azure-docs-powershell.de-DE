---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 8FF53426-D4AE-455E-A182-D7FBC7262FE1
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: 017c084e98d8983343ae1f8c19464cc254b26e2e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384291"
---
# <span data-ttu-id="fa153-101">New-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="fa153-101">New-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="fa153-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa153-102">SYNOPSIS</span></span>
<span data-ttu-id="fa153-103">Erstellt oder aktualisiert eine Transformation innerhalb eines Auftrags.</span><span class="sxs-lookup"><span data-stu-id="fa153-103">Creates or updates a transformation within a job.</span></span>

## <span data-ttu-id="fa153-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fa153-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsTransformation [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fa153-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fa153-105">DESCRIPTION</span></span>
<span data-ttu-id="fa153-106">Das **Cmdlet "New-AzStreamAnalyticsTransformation"** erstellt eine Transformation in einem Stream Analytics-Auftrag oder aktualisiert die vorhandene Transformation.</span><span class="sxs-lookup"><span data-stu-id="fa153-106">The **New-AzStreamAnalyticsTransformation** cmdlet creates a transformation within a Stream Analytics job or updates the existing transformation.</span></span>
<span data-ttu-id="fa153-107">Der Name der Transformation kann im angegeben werden. JSON-Datei oder in der Befehlszeile.</span><span class="sxs-lookup"><span data-stu-id="fa153-107">The name of the transformation can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="fa153-108">Wenn beide Angegeben werden, muss der Name in der Befehlszeile mit dem Namen in der Datei übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="fa153-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="fa153-109">Wenn Sie eine Transformation angeben, die bereits vorhanden ist, ohne den Parameter "Force" anzugeben, fragt das Cmdlet, ob die vorhandene Transformation ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fa153-109">If you specify a transformation that already exists and do not specify the Force parameter, the cmdlet will ask whether or not to replace the existing transformation.</span></span>
<span data-ttu-id="fa153-110">Wenn Sie den Parameter *"Force"* und einen vorhandenen Transformationsnamen angeben, wird die Transformation ohne Bestätigung ersetzt.</span><span class="sxs-lookup"><span data-stu-id="fa153-110">If you specify the *Force* parameter and specify an existing transformation name, the transformation will be replaced without confirmation.</span></span>

## <span data-ttu-id="fa153-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fa153-111">EXAMPLES</span></span>

### <span data-ttu-id="fa153-112">Beispiel 1: Erstellen oder Ersetzen einer Transformation in einem Auftrag</span><span class="sxs-lookup"><span data-stu-id="fa153-112">Example 1: Create or replace a transformation in a job</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform"
```

<span data-ttu-id="fa153-113">Mit diesem Befehl wird eine Transformation namens "StreamingJobTransform" im Auftrag "StreamingJob" erstellt.</span><span class="sxs-lookup"><span data-stu-id="fa153-113">This command creates a transformation called StreamingJobTransform in the job called StreamingJob.</span></span>
<span data-ttu-id="fa153-114">Wenn eine vorhandene Transformation bereits mit diesem Namen definiert ist, fragt das Cmdlet, ob sie ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fa153-114">If an existing transformation is already defined with that name, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="fa153-115">Beispiel 2: Ersetzen einer Transformation in einem Auftrag</span><span class="sxs-lookup"><span data-stu-id="fa153-115">Example 2: Replace a transformation in a job</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform" -Force
```

<span data-ttu-id="fa153-116">Dieser Befehl ersetzt die Definition von StreamingJobTransform im Auftrag von StreamingJob ohne Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="fa153-116">This command replaces the definition of StreamingJobTransform in the job StreamingJob without confirmation.</span></span>

## <span data-ttu-id="fa153-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa153-117">PARAMETERS</span></span>

### <span data-ttu-id="fa153-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa153-118">-DefaultProfile</span></span>
<span data-ttu-id="fa153-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fa153-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa153-120">-File</span><span class="sxs-lookup"><span data-stu-id="fa153-120">-File</span></span>
<span data-ttu-id="fa153-121">Gibt den Pfad zu einer JSON-Datei an, die die JSON-Darstellung der zu erstellenden Azure Stream Analytics-Transformation enthält.</span><span class="sxs-lookup"><span data-stu-id="fa153-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics transformation to create.</span></span>

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

### <span data-ttu-id="fa153-122">-Force</span><span class="sxs-lookup"><span data-stu-id="fa153-122">-Force</span></span>
<span data-ttu-id="fa153-123">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="fa153-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fa153-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="fa153-124">-JobName</span></span>
<span data-ttu-id="fa153-125">Gibt den Namen des Azure Stream Analytics-Auftrags an, unter dem die Azure Stream Analytics-Transformation erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fa153-125">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="fa153-126">-Name</span><span class="sxs-lookup"><span data-stu-id="fa153-126">-Name</span></span>
<span data-ttu-id="fa153-127">Gibt den Namen der zu erstellenden Azure Stream Analytics-Transformation an.</span><span class="sxs-lookup"><span data-stu-id="fa153-127">Specifies the name of the Azure Stream Analytics transformation to create.</span></span>

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

### <span data-ttu-id="fa153-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa153-128">-ResourceGroupName</span></span>
<span data-ttu-id="fa153-129">Gibt den Namen der Ressourcengruppe an, unter der die Azure Stream Analytics-Transformation erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fa153-129">Specifies the name of the resource group under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="fa153-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa153-130">-Confirm</span></span>
<span data-ttu-id="fa153-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fa153-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa153-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fa153-132">-WhatIf</span></span>
<span data-ttu-id="fa153-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fa153-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa153-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fa153-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa153-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa153-135">CommonParameters</span></span>
<span data-ttu-id="fa153-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa153-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa153-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa153-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa153-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fa153-138">INPUTS</span></span>

### <span data-ttu-id="fa153-139">System.String</span><span class="sxs-lookup"><span data-stu-id="fa153-139">System.String</span></span>

## <span data-ttu-id="fa153-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fa153-140">OUTPUTS</span></span>

### <span data-ttu-id="fa153-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span><span class="sxs-lookup"><span data-stu-id="fa153-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="fa153-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fa153-142">NOTES</span></span>

## <span data-ttu-id="fa153-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fa153-143">RELATED LINKS</span></span>

[<span data-ttu-id="fa153-144">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="fa153-144">Get-AzStreamAnalyticsTransformation</span></span>](./Get-AzStreamAnalyticsTransformation.md)


