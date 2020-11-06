---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 8FF53426-D4AE-455E-A182-D7FBC7262FE1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsTransformation.md
ms.openlocfilehash: eb9f8b82e8ff8a0f60931953f2a3b4349e7b4a4f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481405"
---
# <span data-ttu-id="2a093-101">New-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="2a093-101">New-AzureRmStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="2a093-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2a093-102">SYNOPSIS</span></span>
<span data-ttu-id="2a093-103">Erstellt oder aktualisiert eine Transformation innerhalb eines Auftrags.</span><span class="sxs-lookup"><span data-stu-id="2a093-103">Creates or updates a transformation within a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a093-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a093-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsTransformation [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2a093-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2a093-105">DESCRIPTION</span></span>
<span data-ttu-id="2a093-106">Das Cmdlet **New-AzureRmStreamAnalyticsTransformation** erstellt eine Transformation innerhalb eines Datenstrom Analyse Auftrags oder aktualisiert die vorhandene Transformation.</span><span class="sxs-lookup"><span data-stu-id="2a093-106">The **New-AzureRmStreamAnalyticsTransformation** cmdlet creates a transformation within a Stream Analytics job or updates the existing transformation.</span></span>
<span data-ttu-id="2a093-107">Der Name der Transformation kann in der angegeben werden. JSON-Datei oder in der Befehlszeile.</span><span class="sxs-lookup"><span data-stu-id="2a093-107">The name of the transformation can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="2a093-108">Wenn beide angegeben sind, muss der Name in der Befehlszeile mit dem Namen in der Datei übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="2a093-108">If both are specified, the name on command line must match the name in the file.</span></span>

<span data-ttu-id="2a093-109">Wenn Sie eine Transformation angeben, die bereits vorhanden ist, und den Parameter Force nicht angeben, fragt das Cmdlet, ob die vorhandene Transformation ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2a093-109">If you specify a transformation that already exists and do not specify the Force parameter, the cmdlet will ask whether or not to replace the existing transformation.</span></span>

<span data-ttu-id="2a093-110">Wenn Sie den Parameter *Force* angeben und einen vorhandenen Umwandlungs Namen angeben, wird die Transformation ohne Bestätigung ersetzt.</span><span class="sxs-lookup"><span data-stu-id="2a093-110">If you specify the *Force* parameter and specify an existing transformation name, the transformation will be replaced without confirmation.</span></span>

## <span data-ttu-id="2a093-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2a093-111">EXAMPLES</span></span>

### <span data-ttu-id="2a093-112">Beispiel 1: Erstellen oder Ersetzen einer Transformation in einem Auftrag</span><span class="sxs-lookup"><span data-stu-id="2a093-112">EXAMPLE 1: Create or replace a transformation in a job</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform"
```

<span data-ttu-id="2a093-113">Dieser Befehl erstellt eine Transformation namens "StreamingJobTransform" im Auftrag "StreamingJob".</span><span class="sxs-lookup"><span data-stu-id="2a093-113">This command creates a transformation called StreamingJobTransform in the job called StreamingJob.</span></span>
<span data-ttu-id="2a093-114">Wenn bereits eine vorhandene Transformation mit diesem Namen definiert ist, fragt das Cmdlet, ob es ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2a093-114">If an existing transformation is already defined with that name, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="2a093-115">Beispiel 2: Ersetzen einer Transformation in einem Auftrag</span><span class="sxs-lookup"><span data-stu-id="2a093-115">EXAMPLE 2: Replace a transformation in a job</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform" -Force
```

<span data-ttu-id="2a093-116">Dieser Befehl ersetzt die Definition von StreamingJobTransform im Job-StreamingJob ohne Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="2a093-116">This command replaces the definition of StreamingJobTransform in the job StreamingJob without confirmation.</span></span>

## <span data-ttu-id="2a093-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="2a093-117">PARAMETERS</span></span>

### <span data-ttu-id="2a093-118">-Datei</span><span class="sxs-lookup"><span data-stu-id="2a093-118">-File</span></span>
<span data-ttu-id="2a093-119">Gibt den Pfad zu einer JSON-Datei an, die die JSON-Darstellung der zu erstellende Azure Stream Analytics-Transformation enthält.</span><span class="sxs-lookup"><span data-stu-id="2a093-119">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics transformation to create.</span></span>

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

### <span data-ttu-id="2a093-120">-Force</span><span class="sxs-lookup"><span data-stu-id="2a093-120">-Force</span></span>
<span data-ttu-id="2a093-121">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="2a093-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2a093-122">-Jobname</span><span class="sxs-lookup"><span data-stu-id="2a093-122">-JobName</span></span>
<span data-ttu-id="2a093-123">Gibt den Namen des Azure Stream Analytics-Auftrags an, unter dem die Azure Stream Analytics-Transformation erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2a093-123">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="2a093-124">-Name</span><span class="sxs-lookup"><span data-stu-id="2a093-124">-Name</span></span>
<span data-ttu-id="2a093-125">Gibt den Namen der zu erstellende Azure Stream Analytics-Transformation an.</span><span class="sxs-lookup"><span data-stu-id="2a093-125">Specifies the name of the Azure Stream Analytics transformation to create.</span></span>

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

### <span data-ttu-id="2a093-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a093-126">-ResourceGroupName</span></span>
<span data-ttu-id="2a093-127">Gibt den Namen der Ressourcengruppe an, unter der die Azure Stream Analytics-Transformation erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2a093-127">Specifies the name of the resource group under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="2a093-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2a093-128">-Confirm</span></span>
<span data-ttu-id="2a093-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2a093-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a093-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a093-130">-WhatIf</span></span>
<span data-ttu-id="2a093-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2a093-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a093-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2a093-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a093-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a093-133">-DefaultProfile</span></span>
<span data-ttu-id="2a093-134">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2a093-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a093-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a093-135">CommonParameters</span></span>
<span data-ttu-id="2a093-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a093-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a093-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a093-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a093-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2a093-138">INPUTS</span></span>

## <span data-ttu-id="2a093-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2a093-139">OUTPUTS</span></span>

### <span data-ttu-id="2a093-140">Microsoft. Azure. Commands. StreamAnalytics. Models. PSTransformation</span><span class="sxs-lookup"><span data-stu-id="2a093-140">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="2a093-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="2a093-141">NOTES</span></span>

## <span data-ttu-id="2a093-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2a093-142">RELATED LINKS</span></span>

[<span data-ttu-id="2a093-143">Get-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="2a093-143">Get-AzureRmStreamAnalyticsTransformation</span></span>](./Get-AzureRmStreamAnalyticsTransformation.md)


