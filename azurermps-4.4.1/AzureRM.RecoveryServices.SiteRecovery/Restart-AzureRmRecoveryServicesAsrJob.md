---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Restart-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Restart-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: 2f219882199010b2765ebd4386691451d74a182d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663860"
---
# <span data-ttu-id="73a6b-101">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="73a6b-101">Restart-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="73a6b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="73a6b-102">SYNOPSIS</span></span>
<span data-ttu-id="73a6b-103">Startet einen Azure Site Recovery-Auftrag neu.</span><span class="sxs-lookup"><span data-stu-id="73a6b-103">Restarts an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73a6b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="73a6b-104">SYNTAX</span></span>

### <span data-ttu-id="73a6b-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="73a6b-105">ByObject (Default)</span></span>
```
Restart-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73a6b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="73a6b-106">ByName</span></span>
```
Restart-AzureRmRecoveryServicesAsrJob -Name <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73a6b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="73a6b-107">DESCRIPTION</span></span>
<span data-ttu-id="73a6b-108">Mit dem Cmdlet " **Restart-AzureRmRecoveryServicesAsrJob** " wird ein Azure Site Recovery-Auftrag neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="73a6b-108">The **Restart-AzureRmRecoveryServicesAsrJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="73a6b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="73a6b-109">EXAMPLES</span></span>

### <span data-ttu-id="73a6b-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="73a6b-110">Example 1</span></span>
```
PS C:\> $currentJob = Restart-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="73a6b-111">Startet den angegebenen ASR-Auftrag neu und gibt das aktualisierte ASR-Auftragsobjekt des ASR-Auftrags zurück.</span><span class="sxs-lookup"><span data-stu-id="73a6b-111">Restarts the specified ASR job and returns the updated ASR job object of the ASR job.</span></span>

## <span data-ttu-id="73a6b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="73a6b-112">PARAMETERS</span></span>

### <span data-ttu-id="73a6b-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="73a6b-113">-InputObject</span></span>
<span data-ttu-id="73a6b-114">Das Eingabeobjekt für das Cmdlet: das ASR-Auftragsobjekt, das dem ASR-Auftrag entspricht, der neu gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="73a6b-114">The input object to the cmdlet: The ASR job object corresponding to the ASR job to be restarted</span></span>
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

### <span data-ttu-id="73a6b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="73a6b-115">-Name</span></span>
<span data-ttu-id="73a6b-116">Geben Sie den Auftrag über den Namen an.</span><span class="sxs-lookup"><span data-stu-id="73a6b-116">Specify the job by name.</span></span>

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

### <span data-ttu-id="73a6b-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="73a6b-117">-Confirm</span></span>
<span data-ttu-id="73a6b-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="73a6b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73a6b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73a6b-119">-WhatIf</span></span>
<span data-ttu-id="73a6b-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="73a6b-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="73a6b-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="73a6b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73a6b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73a6b-122">CommonParameters</span></span>
<span data-ttu-id="73a6b-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73a6b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73a6b-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73a6b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73a6b-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="73a6b-125">INPUTS</span></span>

### <span data-ttu-id="73a6b-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="73a6b-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="73a6b-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="73a6b-127">OUTPUTS</span></span>

### <span data-ttu-id="73a6b-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="73a6b-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="73a6b-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="73a6b-129">NOTES</span></span>

## <span data-ttu-id="73a6b-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="73a6b-130">RELATED LINKS</span></span>

[<span data-ttu-id="73a6b-131">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="73a6b-131">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="73a6b-132">Lebenslauf-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="73a6b-132">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="73a6b-133">Stopp-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="73a6b-133">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
