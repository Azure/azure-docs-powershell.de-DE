---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/enable-azurermdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmDataCollection.md
ms.openlocfilehash: 9a6e87fb28fde1af024460a0b09d0339222d1ee8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663459"
---
# <span data-ttu-id="c536c-101">Enable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="c536c-101">Enable-AzureRmDataCollection</span></span>

## <span data-ttu-id="c536c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c536c-102">SYNOPSIS</span></span>
<span data-ttu-id="c536c-103">Ermöglicht Azure PowerShell das Sammeln von Daten, um die Benutzerfreundlichkeit mit AzurePowerShell-Cmdlets zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="c536c-103">Enables Azure PowerShell to collect data to improve the user experience with AzurePowerShell cmdlets.</span></span>
<span data-ttu-id="c536c-104">Das Ausführen dieses Cmdlets entscheidet sich für die Datensammlung für den aktuellen Benutzer auf dem aktuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="c536c-104">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span>
<span data-ttu-id="c536c-105">Es werden keine Daten erfasst, es sei denn, Sie entscheiden sich ausdrücklich dafür.</span><span class="sxs-lookup"><span data-stu-id="c536c-105">No data is collected unless you explicitly opt in.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c536c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c536c-106">SYNTAX</span></span>

```
Enable-AzureRmDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c536c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c536c-107">DESCRIPTION</span></span>
<span data-ttu-id="c536c-108">Sie können die Nutzung der Microsoft-Cloud und Azure PowerShell verbessern, indem Sie sich für die Datensammlung entscheiden.</span><span class="sxs-lookup"><span data-stu-id="c536c-108">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="c536c-109">Azure PowerShell sammelt keine Daten ohne Ihre Zustimmung – Sie müssen sich explizit durch Ausführen von enable-AzureRmDataCollection oder durch die Beantwortung von "Ja" anmelden, wenn Azure PowerShell Sie zum ersten Mal beim Ausführen eines Cmdlets auffordert, Daten zu sammeln.</span><span class="sxs-lookup"><span data-stu-id="c536c-109">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzureRmDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="c536c-110">Microsoft aggregiert gesammelte Daten, um Nutzungsmuster zu identifizieren, häufige Probleme zu erkennen und die Nutzung von Azure PowerShell zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="c536c-110">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="c536c-111">Microsoft Azure PowerShell sammelt keine privaten Daten oder keine persönlich identifizierbaren Informationen.</span><span class="sxs-lookup"><span data-stu-id="c536c-111">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>

<span data-ttu-id="c536c-112">Führen Sie das Enable-AzureRMDataCollection-Cmdlet aus, um die Datensammlung für den aktuellen Benutzer auf dem aktuellen Computer zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c536c-112">Run the Enable-AzureRMDataCollection cmdlet to enable data collection for the current user on the current machine.</span></span>
<span data-ttu-id="c536c-113">Dadurch wird verhindert, dass der aktuelle Benutzer zur Datensammlung aufgefordert wird, wenn Cmdlets erstmalig ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c536c-113">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>

<span data-ttu-id="c536c-114">Wenn Sie die Datensammlung für den aktuellen Benutzer deaktivieren möchten, führen Sie das Disable-AzureRmDataCollection-Cmdlet aus.</span><span class="sxs-lookup"><span data-stu-id="c536c-114">To disable data collection for the current user, run the Disable-AzureRmDataCollection cmdlet.</span></span>

## <span data-ttu-id="c536c-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c536c-115">EXAMPLES</span></span>

### <span data-ttu-id="c536c-116">Beispiel 1: Aktivieren der Datensammlung für den aktuellen Benutzer</span><span class="sxs-lookup"><span data-stu-id="c536c-116">Example 1: Enabling data collection for the current user</span></span>
```
PS C:\> Enable-AzureRmDataCollection
```

<span data-ttu-id="c536c-117">In diesem Beispiel wird gezeigt, wie Sie die Datensammlung für den aktuellen Benutzer aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c536c-117">This example shows how to enable data collection for the current user.</span></span>

## <span data-ttu-id="c536c-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="c536c-118">PARAMETERS</span></span>

### <span data-ttu-id="c536c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c536c-119">-DefaultProfile</span></span>
<span data-ttu-id="c536c-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c536c-120">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c536c-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c536c-121">-Confirm</span></span>
<span data-ttu-id="c536c-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c536c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c536c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c536c-123">-WhatIf</span></span>
<span data-ttu-id="c536c-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c536c-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c536c-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c536c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c536c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c536c-126">CommonParameters</span></span>
<span data-ttu-id="c536c-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c536c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c536c-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c536c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c536c-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c536c-129">INPUTS</span></span>

### <span data-ttu-id="c536c-130">Keine</span><span class="sxs-lookup"><span data-stu-id="c536c-130">None</span></span>
<span data-ttu-id="c536c-131">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="c536c-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c536c-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c536c-132">OUTPUTS</span></span>

### <span data-ttu-id="c536c-133">Keine</span><span class="sxs-lookup"><span data-stu-id="c536c-133">None</span></span>

## <span data-ttu-id="c536c-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="c536c-134">NOTES</span></span>

## <span data-ttu-id="c536c-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c536c-135">RELATED LINKS</span></span>

[<span data-ttu-id="c536c-136">Deaktivieren-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="c536c-136">Disable-AzureRmDataCollection</span></span>](./Disable-AzureRmDataCollection.md)

