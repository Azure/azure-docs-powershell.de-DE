---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/stop-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Stop-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Stop-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: c573cd8162961660dac57be3d3f5fe18cd055a89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476650"
---
# <span data-ttu-id="c963b-101">Stop-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="c963b-101">Stop-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="c963b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c963b-102">SYNOPSIS</span></span>
<span data-ttu-id="c963b-103">Beendet einen Azure Site Recovery-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="c963b-103">Stops an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c963b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c963b-104">SYNTAX</span></span>

### <span data-ttu-id="c963b-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="c963b-105">ByObject (Default)</span></span>
```
Stop-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c963b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c963b-106">ByName</span></span>
```
Stop-AzureRmRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c963b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c963b-107">DESCRIPTION</span></span>
<span data-ttu-id="c963b-108">Das Cmdlet **Stop-AzureRmRecoveryServicesAsrJob** beendet den angegebenen Azure Site Recovery-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="c963b-108">The **Stop-AzureRmRecoveryServicesAsrJob** cmdlet stops the specified Azure Site Recovery job.</span></span>

## <span data-ttu-id="c963b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c963b-109">EXAMPLES</span></span>

### <span data-ttu-id="c963b-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c963b-110">Example 1</span></span>
```
PS C:\> $currentJob = Stop-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="c963b-111">Versucht, den angegebenen Auftrag zu beenden und gibt ein aktualisiertes ASR-Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="c963b-111">Attempts to stop the specified job and returns an updated ASR job object.</span></span>

## <span data-ttu-id="c963b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c963b-112">PARAMETERS</span></span>

### <span data-ttu-id="c963b-113">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c963b-113">-Confirm</span></span>
<span data-ttu-id="c963b-114">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c963b-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c963b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c963b-115">-DefaultProfile</span></span>
<span data-ttu-id="c963b-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c963b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="c963b-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c963b-117">-InputObject</span></span>
<span data-ttu-id="c963b-118">Eingabeobjekt: Geben Sie das ASR-Auftragsobjekt an, das dem zu beendenden ASR-Auftrag entspricht.</span><span class="sxs-lookup"><span data-stu-id="c963b-118">Input Object: Specify the ASR job object corresponding to the ASR job to be stopped</span></span>

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

### <span data-ttu-id="c963b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c963b-119">-Name</span></span>
<span data-ttu-id="c963b-120">Geben Sie den ASR-Auftrag an, der vom ASR-Auftragsnamen angehalten werden soll.</span><span class="sxs-lookup"><span data-stu-id="c963b-120">Specify the ASR Job to be stopped by the ASR job name.</span></span>

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

### <span data-ttu-id="c963b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c963b-121">-WhatIf</span></span>
<span data-ttu-id="c963b-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c963b-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c963b-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c963b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c963b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c963b-124">CommonParameters</span></span>
<span data-ttu-id="c963b-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c963b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c963b-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c963b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c963b-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c963b-127">INPUTS</span></span>

### <span data-ttu-id="c963b-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c963b-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c963b-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c963b-129">OUTPUTS</span></span>

### <span data-ttu-id="c963b-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c963b-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c963b-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="c963b-131">NOTES</span></span>

## <span data-ttu-id="c963b-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c963b-132">RELATED LINKS</span></span>

[<span data-ttu-id="c963b-133">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="c963b-133">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="c963b-134">Neustart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="c963b-134">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="c963b-135">Lebenslauf-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="c963b-135">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)
