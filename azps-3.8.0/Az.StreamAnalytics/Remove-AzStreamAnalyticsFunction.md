---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 75B0776E-32D5-4EE4-B35C-73E13185A4F1
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsFunction.md
ms.openlocfilehash: d481cf5ba28a87e098691d4b3fa5c179670d881d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846380"
---
# <span data-ttu-id="4a4c5-101">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="4a4c5-101">Remove-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="4a4c5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4a4c5-102">SYNOPSIS</span></span>
<span data-ttu-id="4a4c5-103">Löscht eine Funktion aus einem Datenstrom Analyse Auftrag.</span><span class="sxs-lookup"><span data-stu-id="4a4c5-103">Deletes a function from a Stream Analytics job.</span></span>

## <span data-ttu-id="4a4c5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a4c5-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a4c5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4a4c5-105">DESCRIPTION</span></span>
<span data-ttu-id="4a4c5-106">Das Cmdlet **Remove-AzStreamAnalyticsFunction** löscht eine Funktion asynchron aus einem Azure Stream-Analyse Auftrag.</span><span class="sxs-lookup"><span data-stu-id="4a4c5-106">The **Remove-AzStreamAnalyticsFunction** cmdlet deletes a function asynchronously from an Azure Stream Analytics job.</span></span>

## <span data-ttu-id="4a4c5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4a4c5-107">EXAMPLES</span></span>

### <span data-ttu-id="4a4c5-108">Beispiel 1: Entfernen einer Datenstrom Analysefunktion</span><span class="sxs-lookup"><span data-stu-id="4a4c5-108">Example 1: Remove a Stream Analytics function</span></span>
```
PS C:\>Remove-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="4a4c5-109">Dieser Befehl entfernt die Funktion mit dem Namen ScoreTweet aus dem Auftrag mit dem Namen StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="4a4c5-109">This command removes the function named ScoreTweet from the job named StreamJob22.</span></span>

## <span data-ttu-id="4a4c5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a4c5-110">PARAMETERS</span></span>

### <span data-ttu-id="4a4c5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a4c5-111">-DefaultProfile</span></span>
<span data-ttu-id="4a4c5-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4a4c5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a4c5-113">-Jobname</span><span class="sxs-lookup"><span data-stu-id="4a4c5-113">-JobName</span></span>
<span data-ttu-id="4a4c5-114">Gibt den Namen des Datenstrom Analyse Auftrags an, zu dem eine Funktion gehört.</span><span class="sxs-lookup"><span data-stu-id="4a4c5-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>
<span data-ttu-id="4a4c5-115">Mit diesem Cmdlet wird eine Funktion aus dem Auftrag entfernt, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="4a4c5-115">This cmdlet removes a function from the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="4a4c5-116">-Name</span><span class="sxs-lookup"><span data-stu-id="4a4c5-116">-Name</span></span>
<span data-ttu-id="4a4c5-117">Gibt den Namen der Datenstrom Analysefunktion an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="4a4c5-117">Specifies the name of the Stream Analytics function that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a4c5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a4c5-118">-ResourceGroupName</span></span>
<span data-ttu-id="4a4c5-119">Gibt den Namen der Ressourcengruppe an, zu der eine Datenstrom Analysefunktion gehört.</span><span class="sxs-lookup"><span data-stu-id="4a4c5-119">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="4a4c5-120">Dieses Cmdlet löscht eine Funktion in der Ressourcengruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="4a4c5-120">This cmdlet deletes a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="4a4c5-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4a4c5-121">-Confirm</span></span>
<span data-ttu-id="4a4c5-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4a4c5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a4c5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a4c5-123">-WhatIf</span></span>
<span data-ttu-id="4a4c5-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4a4c5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a4c5-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4a4c5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a4c5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a4c5-126">CommonParameters</span></span>
<span data-ttu-id="4a4c5-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a4c5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a4c5-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a4c5-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a4c5-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4a4c5-129">INPUTS</span></span>

### <span data-ttu-id="4a4c5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4a4c5-130">System.String</span></span>

## <span data-ttu-id="4a4c5-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4a4c5-131">OUTPUTS</span></span>

### <span data-ttu-id="4a4c5-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4a4c5-132">System.Boolean</span></span>

## <span data-ttu-id="4a4c5-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="4a4c5-133">NOTES</span></span>

## <span data-ttu-id="4a4c5-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4a4c5-134">RELATED LINKS</span></span>

[<span data-ttu-id="4a4c5-135">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="4a4c5-135">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="4a4c5-136">Neu – AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="4a4c5-136">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="4a4c5-137">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="4a4c5-137">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)


