---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Stop-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Stop-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: e639e6fc42e440b5088a34ee29e21d324ed7d235
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663856"
---
# <span data-ttu-id="f4c4e-101">Stop-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="f4c4e-101">Stop-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="f4c4e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f4c4e-102">SYNOPSIS</span></span>
<span data-ttu-id="f4c4e-103">Beendet einen Azure Site Recovery-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="f4c4e-103">Stops an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4c4e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4c4e-104">SYNTAX</span></span>

### <span data-ttu-id="f4c4e-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="f4c4e-105">ByObject (Default)</span></span>
```
Stop-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4c4e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="f4c4e-106">ByName</span></span>
```
Stop-AzureRmRecoveryServicesAsrJob -Name <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4c4e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f4c4e-107">DESCRIPTION</span></span>
<span data-ttu-id="f4c4e-108">Das Cmdlet **Stop-AzureRmRecoveryServicesAsrJob** beendet den angegebenen Azure Site Recovery-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="f4c4e-108">The **Stop-AzureRmRecoveryServicesAsrJob** cmdlet stops the specified Azure Site Recovery job.</span></span>

## <span data-ttu-id="f4c4e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f4c4e-109">EXAMPLES</span></span>

### <span data-ttu-id="f4c4e-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f4c4e-110">Example 1</span></span>
```
PS C:\> $currentJob = Stop-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="f4c4e-111">Versucht, den angegebenen Auftrag zu beenden und gibt ein aktualisiertes ASR-Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="f4c4e-111">Attempts to stop the specified job and returns an updated ASR job object.</span></span>

## <span data-ttu-id="f4c4e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4c4e-112">PARAMETERS</span></span>

### <span data-ttu-id="f4c4e-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f4c4e-113">-InputObject</span></span>
<span data-ttu-id="f4c4e-114">Eingabeobjekt: Geben Sie das ASR-Auftragsobjekt an, das dem zu beendenden ASR-Auftrag entspricht.</span><span class="sxs-lookup"><span data-stu-id="f4c4e-114">Input Object: Specify the ASR job object corresponding to the ASR job to be stopped</span></span>

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: Job

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4c4e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f4c4e-115">-Name</span></span>
<span data-ttu-id="f4c4e-116">Geben Sie den ASR-Auftrag an, der vom ASR-Auftragsnamen angehalten werden soll.</span><span class="sxs-lookup"><span data-stu-id="f4c4e-116">Specify the ASR Job to be stopped by the ASR job name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4c4e-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f4c4e-117">-Confirm</span></span>
<span data-ttu-id="f4c4e-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f4c4e-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4c4e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4c4e-119">-WhatIf</span></span>
<span data-ttu-id="f4c4e-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f4c4e-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4c4e-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f4c4e-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4c4e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4c4e-122">CommonParameters</span></span>
<span data-ttu-id="f4c4e-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4c4e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4c4e-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4c4e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4c4e-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f4c4e-125">INPUTS</span></span>

### <span data-ttu-id="f4c4e-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f4c4e-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f4c4e-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f4c4e-127">OUTPUTS</span></span>

### <span data-ttu-id="f4c4e-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f4c4e-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f4c4e-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="f4c4e-129">NOTES</span></span>

## <span data-ttu-id="f4c4e-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f4c4e-130">RELATED LINKS</span></span>

[<span data-ttu-id="f4c4e-131">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="f4c4e-131">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="f4c4e-132">Neustart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="f4c4e-132">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="f4c4e-133">Lebenslauf-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="f4c4e-133">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)
