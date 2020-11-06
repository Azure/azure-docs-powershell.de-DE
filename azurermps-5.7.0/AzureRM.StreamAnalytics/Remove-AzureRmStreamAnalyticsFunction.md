---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 75B0776E-32D5-4EE4-B35C-73E13185A4F1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/remove-azurermstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: d76b1139955490189aeb9c2269cc4e9ede8197be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498654"
---
# <span data-ttu-id="aa1be-101">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="aa1be-101">Remove-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="aa1be-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aa1be-102">SYNOPSIS</span></span>
<span data-ttu-id="aa1be-103">Löscht eine Funktion aus einem Datenstrom Analyse Auftrag.</span><span class="sxs-lookup"><span data-stu-id="aa1be-103">Deletes a function from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa1be-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa1be-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa1be-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aa1be-105">DESCRIPTION</span></span>
<span data-ttu-id="aa1be-106">Das Cmdlet **Remove-AzureRmStreamAnalyticsFunction** löscht eine Funktion asynchron aus einem Azure Stream-Analyse Auftrag.</span><span class="sxs-lookup"><span data-stu-id="aa1be-106">The **Remove-AzureRmStreamAnalyticsFunction** cmdlet deletes a function asynchronously from an Azure Stream Analytics job.</span></span>

## <span data-ttu-id="aa1be-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aa1be-107">EXAMPLES</span></span>

### <span data-ttu-id="aa1be-108">Beispiel 1: Entfernen einer Datenstrom Analysefunktion</span><span class="sxs-lookup"><span data-stu-id="aa1be-108">Example 1: Remove a Stream Analytics function</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="aa1be-109">Dieser Befehl entfernt die Funktion mit dem Namen ScoreTweet aus dem Auftrag mit dem Namen StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="aa1be-109">This command removes the function named ScoreTweet from the job named StreamJob22.</span></span>

## <span data-ttu-id="aa1be-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa1be-110">PARAMETERS</span></span>

### <span data-ttu-id="aa1be-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa1be-111">-DefaultProfile</span></span>
<span data-ttu-id="aa1be-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="aa1be-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa1be-113">-Jobname</span><span class="sxs-lookup"><span data-stu-id="aa1be-113">-JobName</span></span>
<span data-ttu-id="aa1be-114">Gibt den Namen des Datenstrom Analyse Auftrags an, zu dem eine Funktion gehört.</span><span class="sxs-lookup"><span data-stu-id="aa1be-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>
<span data-ttu-id="aa1be-115">Mit diesem Cmdlet wird eine Funktion aus dem Auftrag entfernt, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="aa1be-115">This cmdlet removes a function from the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="aa1be-116">-Name</span><span class="sxs-lookup"><span data-stu-id="aa1be-116">-Name</span></span>
<span data-ttu-id="aa1be-117">Gibt den Namen der Datenstrom Analysefunktion an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="aa1be-117">Specifies the name of the Stream Analytics function that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa1be-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa1be-118">-ResourceGroupName</span></span>
<span data-ttu-id="aa1be-119">Gibt den Namen der Ressourcengruppe an, zu der eine Datenstrom Analysefunktion gehört.</span><span class="sxs-lookup"><span data-stu-id="aa1be-119">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="aa1be-120">Dieses Cmdlet löscht eine Funktion in der Ressourcengruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="aa1be-120">This cmdlet deletes a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="aa1be-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="aa1be-121">-Confirm</span></span>
<span data-ttu-id="aa1be-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aa1be-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa1be-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa1be-123">-WhatIf</span></span>
<span data-ttu-id="aa1be-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aa1be-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa1be-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aa1be-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa1be-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa1be-126">CommonParameters</span></span>
<span data-ttu-id="aa1be-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa1be-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa1be-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa1be-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa1be-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aa1be-129">INPUTS</span></span>

### <span data-ttu-id="aa1be-130">Keine</span><span class="sxs-lookup"><span data-stu-id="aa1be-130">None</span></span>
<span data-ttu-id="aa1be-131">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="aa1be-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="aa1be-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aa1be-132">OUTPUTS</span></span>

### <span data-ttu-id="aa1be-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="aa1be-133">System.Object</span></span>

## <span data-ttu-id="aa1be-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="aa1be-134">NOTES</span></span>

## <span data-ttu-id="aa1be-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aa1be-135">RELATED LINKS</span></span>

[<span data-ttu-id="aa1be-136">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="aa1be-136">Get-AzureRmStreamAnalyticsFunction</span></span>](./Get-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="aa1be-137">Neu – AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="aa1be-137">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="aa1be-138">Test-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="aa1be-138">Test-AzureRmStreamAnalyticsFunction</span></span>](./Test-AzureRmStreamAnalyticsFunction.md)


