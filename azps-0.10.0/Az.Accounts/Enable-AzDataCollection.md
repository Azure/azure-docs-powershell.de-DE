---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: c9cfd91ecc094ad5df98d3c8478d197fbfa98a15
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841083"
---
# <span data-ttu-id="c0e28-101">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="c0e28-101">Enable-AzDataCollection</span></span>

## <span data-ttu-id="c0e28-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c0e28-102">SYNOPSIS</span></span>
<span data-ttu-id="c0e28-103">Ermöglicht Azure PowerShell das Sammeln von Daten, um die Benutzerfreundlichkeit mit AzurePowerShell-Cmdlets zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="c0e28-103">Enables Azure PowerShell to collect data to improve the user experience with AzurePowerShell cmdlets.</span></span>
<span data-ttu-id="c0e28-104">Das Ausführen dieses Cmdlets entscheidet sich für die Datensammlung für den aktuellen Benutzer auf dem aktuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="c0e28-104">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span>
<span data-ttu-id="c0e28-105">Es werden keine Daten erfasst, es sei denn, Sie entscheiden sich ausdrücklich dafür.</span><span class="sxs-lookup"><span data-stu-id="c0e28-105">No data is collected unless you explicitly opt in.</span></span>

## <span data-ttu-id="c0e28-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0e28-106">SYNTAX</span></span>

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0e28-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c0e28-107">DESCRIPTION</span></span>
<span data-ttu-id="c0e28-108">Sie können die Nutzung der Microsoft-Cloud und Azure PowerShell verbessern, indem Sie sich für die Datensammlung entscheiden.</span><span class="sxs-lookup"><span data-stu-id="c0e28-108">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="c0e28-109">Azure PowerShell sammelt keine Daten ohne Ihre Zustimmung – Sie müssen sich explizit durch Ausführen von enable-AzDataCollection oder durch die Beantwortung von "Ja" anmelden, wenn Azure PowerShell Sie zum ersten Mal beim Ausführen eines Cmdlets auffordert, Daten zu sammeln.</span><span class="sxs-lookup"><span data-stu-id="c0e28-109">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="c0e28-110">Microsoft aggregiert gesammelte Daten, um Nutzungsmuster zu identifizieren, häufige Probleme zu erkennen und die Nutzung von Azure PowerShell zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="c0e28-110">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="c0e28-111">Microsoft Azure PowerShell sammelt keine privaten Daten oder keine persönlich identifizierbaren Informationen.</span><span class="sxs-lookup"><span data-stu-id="c0e28-111">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>
<span data-ttu-id="c0e28-112">Führen Sie das Enable-AzDataCollection-Cmdlet aus, um die Datensammlung für den aktuellen Benutzer auf dem aktuellen Computer zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c0e28-112">Run the Enable-AzDataCollection cmdlet to enable data collection for the current user on the current machine.</span></span>
<span data-ttu-id="c0e28-113">Dadurch wird verhindert, dass der aktuelle Benutzer zur Datensammlung aufgefordert wird, wenn Cmdlets erstmalig ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c0e28-113">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>
<span data-ttu-id="c0e28-114">Wenn Sie die Datensammlung für den aktuellen Benutzer deaktivieren möchten, führen Sie das Disable-AzDataCollection-Cmdlet aus.</span><span class="sxs-lookup"><span data-stu-id="c0e28-114">To disable data collection for the current user, run the Disable-AzDataCollection cmdlet.</span></span>

## <span data-ttu-id="c0e28-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c0e28-115">EXAMPLES</span></span>

### <span data-ttu-id="c0e28-116">Beispiel 1: Aktivieren der Datensammlung für den aktuellen Benutzer</span><span class="sxs-lookup"><span data-stu-id="c0e28-116">Example 1: Enabling data collection for the current user</span></span>
```
PS C:\> Enable-AzDataCollection
```

<span data-ttu-id="c0e28-117">In diesem Beispiel wird gezeigt, wie Sie die Datensammlung für den aktuellen Benutzer aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c0e28-117">This example shows how to enable data collection for the current user.</span></span>

## <span data-ttu-id="c0e28-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0e28-118">PARAMETERS</span></span>

### <span data-ttu-id="c0e28-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0e28-119">-DefaultProfile</span></span>
<span data-ttu-id="c0e28-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c0e28-120">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0e28-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c0e28-121">-Confirm</span></span>
<span data-ttu-id="c0e28-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c0e28-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0e28-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0e28-123">-WhatIf</span></span>
<span data-ttu-id="c0e28-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c0e28-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c0e28-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c0e28-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0e28-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0e28-126">CommonParameters</span></span>
<span data-ttu-id="c0e28-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0e28-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0e28-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c0e28-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0e28-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c0e28-129">INPUTS</span></span>

### <span data-ttu-id="c0e28-130">Keine</span><span class="sxs-lookup"><span data-stu-id="c0e28-130">None</span></span>

## <span data-ttu-id="c0e28-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c0e28-131">OUTPUTS</span></span>

### <span data-ttu-id="c0e28-132">System. void</span><span class="sxs-lookup"><span data-stu-id="c0e28-132">System.Void</span></span>

## <span data-ttu-id="c0e28-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="c0e28-133">NOTES</span></span>

## <span data-ttu-id="c0e28-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c0e28-134">RELATED LINKS</span></span>

[<span data-ttu-id="c0e28-135">Deaktivieren-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="c0e28-135">Disable-AzDataCollection</span></span>](./Disable-AzDataCollection.md)

