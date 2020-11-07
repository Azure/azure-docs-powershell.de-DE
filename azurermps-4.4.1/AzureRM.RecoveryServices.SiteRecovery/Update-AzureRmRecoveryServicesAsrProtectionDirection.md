---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: afa5da5a34954c1e1a610ce9153172934069c2a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663852"
---
# <span data-ttu-id="4c580-101">Update-AzureRmRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="4c580-101">Update-AzureRmRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="4c580-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4c580-102">SYNOPSIS</span></span>
<span data-ttu-id="4c580-103">Aktualisiert die Replikationsrichtung für das angegebene Replikations geschützte Element oder den Wiederherstellungsplan.</span><span class="sxs-lookup"><span data-stu-id="4c580-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="4c580-104">Wird verwendet, um einen fehlerhaften über replizierten Artikel oder Wiederherstellungsplan wieder zu replizieren/zurück zu replizieren.</span><span class="sxs-lookup"><span data-stu-id="4c580-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c580-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c580-105">SYNTAX</span></span>

### <span data-ttu-id="4c580-106">ByRPIObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="4c580-106">ByRPIObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c580-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="4c580-107">ByRPObject</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c580-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="4c580-108">ByPEObject</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -Direction <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4c580-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4c580-109">DESCRIPTION</span></span>
<span data-ttu-id="4c580-110">Das Cmdlet **Update-AzureRmRecoveryServicesAsrProtectionDirection** aktualisiert die Replikationsrichtung für das angegebene Azure Site Recovery-Objekt nach Abschluss eines Commit-Failover-Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="4c580-110">The **Update-AzureRmRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="4c580-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4c580-111">EXAMPLES</span></span>

### <span data-ttu-id="4c580-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4c580-112">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="4c580-113">Starten Sie den Vorgang "Richtung aktualisieren" für den angegebenen Recover-Plan, und geben Sie das ASR-Auftragsobjekt zurück, das zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4c580-113">Start the update direction operation for the specified recoveyr plan and returns the ASR job object used to track the operation.</span></span>

## <span data-ttu-id="4c580-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="4c580-114">PARAMETERS</span></span>

### <span data-ttu-id="4c580-115">-Richtung</span><span class="sxs-lookup"><span data-stu-id="4c580-115">-Direction</span></span>
<span data-ttu-id="4c580-116">Gibt die Richtung an, die für den Aktualisierungsvorgang verwendet werden soll, um einen Failover zu senden.</span><span class="sxs-lookup"><span data-stu-id="4c580-116">Specifies the direction to be used for the update operation post a failover.</span></span>  
<span data-ttu-id="4c580-117">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4c580-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4c580-118">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="4c580-118">PrimaryToRecovery</span></span>
- <span data-ttu-id="4c580-119">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="4c580-119">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c580-120">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4c580-120">-RecoveryPlan</span></span>
<span data-ttu-id="4c580-121">Gibt ein ASR-Wiederherstellungsplan-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="4c580-121">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="4c580-122">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4c580-122">-ReplicationProtectedItem</span></span>
<span data-ttu-id="4c580-123">Gibt ein geschütztes ASR-Replikations Element an.</span><span class="sxs-lookup"><span data-stu-id="4c580-123">Specifies an ASR replication protected item</span></span>

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

### <span data-ttu-id="4c580-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4c580-124">-Confirm</span></span>
<span data-ttu-id="4c580-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4c580-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c580-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c580-126">-WhatIf</span></span>
<span data-ttu-id="4c580-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4c580-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4c580-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4c580-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c580-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c580-129">CommonParameters</span></span>
<span data-ttu-id="4c580-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c580-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c580-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c580-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c580-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4c580-132">INPUTS</span></span>

### <span data-ttu-id="4c580-133">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4c580-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="4c580-134">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4c580-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="4c580-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4c580-135">OUTPUTS</span></span>

### <span data-ttu-id="4c580-136">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="4c580-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="4c580-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="4c580-137">NOTES</span></span>

## <span data-ttu-id="4c580-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4c580-138">RELATED LINKS</span></span>

