---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 75B0776E-32D5-4EE4-B35C-73E13185A4F1
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsFunction.md
ms.openlocfilehash: bf5c869e8831fd37a10f9923d415a91f88fd0960
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658650"
---
# <span data-ttu-id="91759-101">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="91759-101">Remove-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="91759-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="91759-102">SYNOPSIS</span></span>
<span data-ttu-id="91759-103">Löscht eine Funktion aus einem Datenstrom Analyse Auftrag.</span><span class="sxs-lookup"><span data-stu-id="91759-103">Deletes a function from a Stream Analytics job.</span></span>

## <span data-ttu-id="91759-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="91759-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91759-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="91759-105">DESCRIPTION</span></span>
<span data-ttu-id="91759-106">Das Cmdlet **Remove-AzStreamAnalyticsFunction** löscht eine Funktion asynchron aus einem Azure Stream-Analyse Auftrag.</span><span class="sxs-lookup"><span data-stu-id="91759-106">The **Remove-AzStreamAnalyticsFunction** cmdlet deletes a function asynchronously from an Azure Stream Analytics job.</span></span>

## <span data-ttu-id="91759-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="91759-107">EXAMPLES</span></span>

### <span data-ttu-id="91759-108">Beispiel 1: Entfernen einer Datenstrom Analysefunktion</span><span class="sxs-lookup"><span data-stu-id="91759-108">Example 1: Remove a Stream Analytics function</span></span>
```
PS C:\>Remove-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="91759-109">Dieser Befehl entfernt die Funktion mit dem Namen ScoreTweet aus dem Auftrag mit dem Namen StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="91759-109">This command removes the function named ScoreTweet from the job named StreamJob22.</span></span>

## <span data-ttu-id="91759-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="91759-110">PARAMETERS</span></span>

### <span data-ttu-id="91759-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91759-111">-DefaultProfile</span></span>
<span data-ttu-id="91759-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="91759-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91759-113">-Jobname</span><span class="sxs-lookup"><span data-stu-id="91759-113">-JobName</span></span>
<span data-ttu-id="91759-114">Gibt den Namen des Datenstrom Analyse Auftrags an, zu dem eine Funktion gehört.</span><span class="sxs-lookup"><span data-stu-id="91759-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>
<span data-ttu-id="91759-115">Mit diesem Cmdlet wird eine Funktion aus dem Auftrag entfernt, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="91759-115">This cmdlet removes a function from the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="91759-116">-Name</span><span class="sxs-lookup"><span data-stu-id="91759-116">-Name</span></span>
<span data-ttu-id="91759-117">Gibt den Namen der Datenstrom Analysefunktion an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="91759-117">Specifies the name of the Stream Analytics function that this cmdlet removes.</span></span>

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

### <span data-ttu-id="91759-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91759-118">-ResourceGroupName</span></span>
<span data-ttu-id="91759-119">Gibt den Namen der Ressourcengruppe an, zu der eine Datenstrom Analysefunktion gehört.</span><span class="sxs-lookup"><span data-stu-id="91759-119">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="91759-120">Dieses Cmdlet löscht eine Funktion in der Ressourcengruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="91759-120">This cmdlet deletes a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="91759-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="91759-121">-Confirm</span></span>
<span data-ttu-id="91759-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="91759-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91759-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91759-123">-WhatIf</span></span>
<span data-ttu-id="91759-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="91759-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91759-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="91759-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91759-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91759-126">CommonParameters</span></span>
<span data-ttu-id="91759-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91759-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91759-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91759-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91759-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="91759-129">INPUTS</span></span>

### <span data-ttu-id="91759-130">System. String</span><span class="sxs-lookup"><span data-stu-id="91759-130">System.String</span></span>

## <span data-ttu-id="91759-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="91759-131">OUTPUTS</span></span>

### <span data-ttu-id="91759-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="91759-132">System.Boolean</span></span>

## <span data-ttu-id="91759-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="91759-133">NOTES</span></span>

## <span data-ttu-id="91759-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="91759-134">RELATED LINKS</span></span>

[<span data-ttu-id="91759-135">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="91759-135">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="91759-136">Neu – AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="91759-136">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="91759-137">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="91759-137">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)


