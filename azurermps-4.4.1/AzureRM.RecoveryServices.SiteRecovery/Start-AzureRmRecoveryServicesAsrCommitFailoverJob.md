---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrCommitFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrCommitFailoverJob.md
ms.openlocfilehash: 590512c822bd55b992c8cc58eab4091863792e21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500778"
---
# <span data-ttu-id="b6d94-101">Start-AzureRmRecoveryServicesAsrCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="b6d94-101">Start-AzureRmRecoveryServicesAsrCommitFailoverJob</span></span>

## <span data-ttu-id="b6d94-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b6d94-102">SYNOPSIS</span></span>
<span data-ttu-id="b6d94-103">Startet die Commit-Failover-Aktion für ein Website Wiederherstellungs Objekt.</span><span class="sxs-lookup"><span data-stu-id="b6d94-103">Starts the commit failover action for a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6d94-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6d94-104">SYNTAX</span></span>

### <span data-ttu-id="b6d94-105">ByRPIObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="b6d94-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrCommitFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6d94-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="b6d94-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b6d94-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b6d94-107">DESCRIPTION</span></span>
<span data-ttu-id="b6d94-108">Mit dem Cmdlet " **Start-AzureRmRecoveryServicesAsrCommitFailoverJob** " wird der Commit-Failoverprozess für ein Azure Site Recovery-Objekt nach einem Failover-Vorgang gestartet.</span><span class="sxs-lookup"><span data-stu-id="b6d94-108">The **Start-AzureRmRecoveryServicesAsrCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="b6d94-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b6d94-109">EXAMPLES</span></span>

### <span data-ttu-id="b6d94-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b6d94-110">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrCommitFailoverJob -RecoveryPlan $RP
```

<span data-ttu-id="b6d94-111">Startet das Commit-Failover für den angegebenen Wiederherstellungsplan und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b6d94-111">Starts the commit failover for the specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="b6d94-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6d94-112">PARAMETERS</span></span>

### <span data-ttu-id="b6d94-113">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b6d94-113">-RecoveryPlan</span></span>
<span data-ttu-id="b6d94-114">Gibt ein ASR-Wiederherstellungsplan-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="b6d94-114">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6d94-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b6d94-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="b6d94-116">Gibt ein geschütztes ASR-Replikations Element Objekt an.</span><span class="sxs-lookup"><span data-stu-id="b6d94-116">Specifies an ASR replication protected item object.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6d94-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b6d94-117">-Confirm</span></span>
<span data-ttu-id="b6d94-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b6d94-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6d94-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6d94-119">-WhatIf</span></span>
<span data-ttu-id="b6d94-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b6d94-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b6d94-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b6d94-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6d94-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6d94-122">CommonParameters</span></span>
<span data-ttu-id="b6d94-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6d94-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6d94-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6d94-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6d94-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b6d94-125">INPUTS</span></span>

### <span data-ttu-id="b6d94-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b6d94-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="b6d94-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b6d94-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="b6d94-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b6d94-128">OUTPUTS</span></span>

### <span data-ttu-id="b6d94-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="b6d94-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b6d94-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="b6d94-130">NOTES</span></span>

## <span data-ttu-id="b6d94-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b6d94-131">RELATED LINKS</span></span>

