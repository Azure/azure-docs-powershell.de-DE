---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/disable-azurermdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmDataCollection.md
ms.openlocfilehash: 07b541636229d65a092dc9a3067d3a4cef89cac3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502546"
---
# <span data-ttu-id="07818-101">Disable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="07818-101">Disable-AzureRmDataCollection</span></span>

## <span data-ttu-id="07818-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="07818-102">SYNOPSIS</span></span>
<span data-ttu-id="07818-103">Entscheidet sich, Daten zu sammeln, um die AzurePowerShell-Cmdlets zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="07818-103">Opts out of collecting data to improve the AzurePowerShell cmdlets.</span></span> <span data-ttu-id="07818-104">Daten werden nicht erfasst, es sei denn, Sie entscheiden sich ausdrücklich dafür.</span><span class="sxs-lookup"><span data-stu-id="07818-104">Data is not collected unless you explicitly opt in.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07818-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="07818-105">SYNTAX</span></span>

```
Disable-AzureRmDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="07818-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="07818-106">DESCRIPTION</span></span>
<span data-ttu-id="07818-107">Sie können die Nutzung der Microsoft-Cloud und Azure PowerShell verbessern, indem Sie sich für die Datensammlung entscheiden.</span><span class="sxs-lookup"><span data-stu-id="07818-107">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="07818-108">Azure PowerShell sammelt keine Daten ohne Ihre Zustimmung – Sie müssen sich explizit durch Ausführen von enable-AzureRmDataCollection oder durch die Beantwortung von "Ja" anmelden, wenn Azure PowerShell Sie zum ersten Mal beim Ausführen eines Cmdlets auffordert, Daten zu sammeln.</span><span class="sxs-lookup"><span data-stu-id="07818-108">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzureRmDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="07818-109">Microsoft aggregiert gesammelte Daten, um Nutzungsmuster zu identifizieren, häufige Probleme zu erkennen und die Nutzung von Azure PowerShell zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="07818-109">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="07818-110">Microsoft Azure PowerShell sammelt keine privaten Daten oder keine persönlich identifizierbaren Informationen.</span><span class="sxs-lookup"><span data-stu-id="07818-110">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>

<span data-ttu-id="07818-111">Führen Sie das Disable-AzureRMDataCollection-Cmdlet aus, um die Datensammlung für den aktuellen Benutzer zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="07818-111">Run the Disable-AzureRMDataCollection cmdlet to disable data collection for the current user.</span></span>
<span data-ttu-id="07818-112">Dadurch wird verhindert, dass der aktuelle Benutzer zur Datensammlung aufgefordert wird, wenn Cmdlets erstmalig ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="07818-112">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>

<span data-ttu-id="07818-113">Wenn Sie die Datensammlung für den aktuellen Benutzer aktivieren möchten, führen Sie das Enable-AzureRmDataCollection-Cmdlet aus.</span><span class="sxs-lookup"><span data-stu-id="07818-113">To enable data collection for the current user, run the Enable-AzureRmDataCollection cmdlet.</span></span>

## <span data-ttu-id="07818-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="07818-114">EXAMPLES</span></span>

### <span data-ttu-id="07818-115">Beispiel 1: Deaktivieren der Datensammlung für den aktuellen Benutzer</span><span class="sxs-lookup"><span data-stu-id="07818-115">Example 1: Disabling data collection for the current user</span></span>
```
PS C:\> Disable-AzureRmDataCollection
```

<span data-ttu-id="07818-116">In diesem Beispiel wird gezeigt, wie Sie die Datensammlung für den aktuellen Benutzer deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="07818-116">This example shows how to disable data collection for the current user.</span></span> 

## <span data-ttu-id="07818-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="07818-117">PARAMETERS</span></span>

### <span data-ttu-id="07818-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07818-118">-DefaultProfile</span></span>
<span data-ttu-id="07818-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="07818-119">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07818-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="07818-120">-Confirm</span></span>
<span data-ttu-id="07818-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="07818-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07818-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07818-122">-WhatIf</span></span>
<span data-ttu-id="07818-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="07818-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="07818-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="07818-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07818-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07818-125">CommonParameters</span></span>
<span data-ttu-id="07818-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07818-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07818-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07818-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07818-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="07818-128">INPUTS</span></span>

### <span data-ttu-id="07818-129">Keine</span><span class="sxs-lookup"><span data-stu-id="07818-129">None</span></span>
<span data-ttu-id="07818-130">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="07818-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="07818-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="07818-131">OUTPUTS</span></span>

### <span data-ttu-id="07818-132">Keine</span><span class="sxs-lookup"><span data-stu-id="07818-132">None</span></span>

## <span data-ttu-id="07818-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="07818-133">NOTES</span></span>

## <span data-ttu-id="07818-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="07818-134">RELATED LINKS</span></span>

[<span data-ttu-id="07818-135">Enable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="07818-135">Enable-AzureRmDataCollection</span></span>](./Enable-AzureRmDataCollection.md)

