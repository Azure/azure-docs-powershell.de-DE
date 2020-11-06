---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 678e08df94d7ea828b04d55892cb66e1c0a62349
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475061"
---
# <span data-ttu-id="7d017-101">Enable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="7d017-101">Enable-AzureRmDataCollection</span></span>

## <span data-ttu-id="7d017-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7d017-102">SYNOPSIS</span></span>
<span data-ttu-id="7d017-103">Ermöglicht Azure PowerShell das Sammeln von Daten, um die Benutzerfreundlichkeit mit AzurePowerShell-Cmdlets zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="7d017-103">Enables Azure PowerShell to collect data to improve the user experience with AzurePowerShell cmdlets.</span></span>
<span data-ttu-id="7d017-104">Das Ausführen dieses Cmdlets entscheidet sich für die Datensammlung für den aktuellen Benutzer auf dem aktuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="7d017-104">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span>
<span data-ttu-id="7d017-105">Es werden keine Daten erfasst, es sei denn, Sie entscheiden sich ausdrücklich dafür.</span><span class="sxs-lookup"><span data-stu-id="7d017-105">No data is collected unless you explicitly opt in.</span></span>

## <span data-ttu-id="7d017-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d017-106">SYNTAX</span></span>

```
Enable-AzureRmDataCollection [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d017-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7d017-107">DESCRIPTION</span></span>
<span data-ttu-id="7d017-108">Sie können die Nutzung der Microsoft-Cloud und Azure PowerShell verbessern, indem Sie sich für die Datensammlung entscheiden.</span><span class="sxs-lookup"><span data-stu-id="7d017-108">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="7d017-109">Azure PowerShell sammelt keine Daten ohne Ihre Zustimmung – Sie müssen sich explizit durch Ausführen von enable-AzureRmDataCollection oder durch die Beantwortung von "Ja" anmelden, wenn Azure PowerShell Sie zum ersten Mal beim Ausführen eines Cmdlets auffordert, Daten zu sammeln.</span><span class="sxs-lookup"><span data-stu-id="7d017-109">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzureRmDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="7d017-110">Microsoft aggregiert gesammelte Daten, um Nutzungsmuster zu identifizieren, häufige Probleme zu erkennen und die Nutzung von Azure PowerShell zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="7d017-110">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="7d017-111">Microsoft Azure PowerShell sammelt keine privaten Daten oder keine persönlich identifizierbaren Informationen.</span><span class="sxs-lookup"><span data-stu-id="7d017-111">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>

<span data-ttu-id="7d017-112">Führen Sie das Enable-AzureRMDataCollection-Cmdlet aus, um die Datensammlung für den aktuellen Benutzer auf dem aktuellen Computer zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="7d017-112">Run the Enable-AzureRMDataCollection cmdlet to enable data collection for the current user on the current machine.</span></span>
<span data-ttu-id="7d017-113">Dadurch wird verhindert, dass der aktuelle Benutzer zur Datensammlung aufgefordert wird, wenn Cmdlets erstmalig ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7d017-113">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>

<span data-ttu-id="7d017-114">Wenn Sie die Datensammlung für den aktuellen Benutzer deaktivieren möchten, führen Sie das Disable-AzureRmDataCollection-Cmdlet aus.</span><span class="sxs-lookup"><span data-stu-id="7d017-114">To disable data collection for the current user, run the Disable-AzureRmDataCollection cmdlet.</span></span>

## <span data-ttu-id="7d017-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7d017-115">EXAMPLES</span></span>

### <span data-ttu-id="7d017-116">Beispiel 1: Aktivieren der Datensammlung für den aktuellen Benutzer</span><span class="sxs-lookup"><span data-stu-id="7d017-116">Example 1: Enabling data collection for the current user</span></span>
```
PS C:\> Enable-AzureRmDataCollection
```

<span data-ttu-id="7d017-117">In diesem Beispiel wird gezeigt, wie Sie die Datensammlung für den aktuellen Benutzer aktivieren.</span><span class="sxs-lookup"><span data-stu-id="7d017-117">This example shows how to enable data collection for the current user.</span></span>

## <span data-ttu-id="7d017-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d017-118">PARAMETERS</span></span>

### <span data-ttu-id="7d017-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7d017-119">-Confirm</span></span>
<span data-ttu-id="7d017-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7d017-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d017-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d017-121">-WhatIf</span></span>
<span data-ttu-id="7d017-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7d017-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7d017-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7d017-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d017-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d017-124">CommonParameters</span></span>
<span data-ttu-id="7d017-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d017-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d017-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d017-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d017-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7d017-127">INPUTS</span></span>

## <span data-ttu-id="7d017-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7d017-128">OUTPUTS</span></span>

### <span data-ttu-id="7d017-129">Keine</span><span class="sxs-lookup"><span data-stu-id="7d017-129">None</span></span>

## <span data-ttu-id="7d017-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="7d017-130">NOTES</span></span>

## <span data-ttu-id="7d017-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7d017-131">RELATED LINKS</span></span>

[<span data-ttu-id="7d017-132">Deaktivieren-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="7d017-132">Disable-AzureRmDataCollection</span></span>]()

