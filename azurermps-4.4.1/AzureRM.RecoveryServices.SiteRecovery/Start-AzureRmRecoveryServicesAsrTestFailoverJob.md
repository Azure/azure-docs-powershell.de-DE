---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: d547de0af8d4f7b4f98a572d95dcc023d975fc2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501673"
---
# <span data-ttu-id="68fd0-101">Start-AzureRmRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="68fd0-101">Start-AzureRmRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="68fd0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="68fd0-102">SYNOPSIS</span></span>
<span data-ttu-id="68fd0-103">Startet einen Test-Failover-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="68fd0-103">Starts a test failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68fd0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="68fd0-104">SYNTAX</span></span>

### <span data-ttu-id="68fd0-105">ByRPIObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="68fd0-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68fd0-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="68fd0-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="68fd0-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="68fd0-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68fd0-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="68fd0-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68fd0-109">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="68fd0-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68fd0-110">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="68fd0-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68fd0-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="68fd0-111">DESCRIPTION</span></span>
<span data-ttu-id="68fd0-112">Das Cmdlet **Start-AzureRmRecoveryServicesAsrTestFailoverJob** startet das Test-Failover für ein geschütztes Element oder einen Wiederherstellungsplan der Azure Site Recovery-Replikation.</span><span class="sxs-lookup"><span data-stu-id="68fd0-112">The **Start-AzureRmRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="68fd0-113">Mithilfe des Get-AzureRmRecoveryServicesAsrJob-Cmdlets können Sie überprüfen, ob der Auftrag erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="68fd0-113">You can check whether the job succeeded by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="68fd0-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="68fd0-114">EXAMPLES</span></span>

### <span data-ttu-id="68fd0-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="68fd0-115">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="68fd0-116">Startet den Test-Failover-Vorgang für den Wiederherstellungsplan mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="68fd0-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="68fd0-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="68fd0-117">PARAMETERS</span></span>

### <span data-ttu-id="68fd0-118">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="68fd0-118">-AzureVMNetworkId</span></span>
<span data-ttu-id="68fd0-119">Gibt die Azure Virtual Network-ID an, um die Verbindung zwischen dem Testfehler und dem virtuellen Computer herzustellen.</span><span class="sxs-lookup"><span data-stu-id="68fd0-119">Specifies the Azure virtual network ID to connect the test fail over virtual machine(s) to.</span></span>

```yaml
Type: String
Parameter Sets: ByRPObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68fd0-120">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="68fd0-120">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="68fd0-121">Gibt die primäre Zertifikatsdatei an.</span><span class="sxs-lookup"><span data-stu-id="68fd0-121">Specifies the primary certificate file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68fd0-122">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="68fd0-122">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="68fd0-123">Gibt die sekundäre Zertifikatsdatei an.</span><span class="sxs-lookup"><span data-stu-id="68fd0-123">Specifies the secondary certificate file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68fd0-124">-Richtung</span><span class="sxs-lookup"><span data-stu-id="68fd0-124">-Direction</span></span>
<span data-ttu-id="68fd0-125">Gibt die failoverrichtung an.</span><span class="sxs-lookup"><span data-stu-id="68fd0-125">Specifies the failover direction.</span></span>
<span data-ttu-id="68fd0-126">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="68fd0-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="68fd0-127">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="68fd0-127">PrimaryToRecovery</span></span>
- <span data-ttu-id="68fd0-128">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="68fd0-128">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="68fd0-129">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="68fd0-129">-RecoveryPlan</span></span>
<span data-ttu-id="68fd0-130">Gibt ein ASR-Wiederherstellungsplan-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="68fd0-130">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68fd0-131">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="68fd0-131">-ReplicationProtectedItem</span></span>
<span data-ttu-id="68fd0-132">Gibt ein geschütztes ASR-Replikations Element an.</span><span class="sxs-lookup"><span data-stu-id="68fd0-132">Specifies an ASR replication protected item.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68fd0-133">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="68fd0-133">-VMNetwork</span></span>
<span data-ttu-id="68fd0-134">Gibt das Netzwerk der virtuellen Maschine der Standortwiederherstellung an, mit dem die virtuellen Test-Failover-Computer (s) verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="68fd0-134">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByRPObjectWithVMNetwork, ByRPIObjectWithVMNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68fd0-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="68fd0-135">-Confirm</span></span>
<span data-ttu-id="68fd0-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="68fd0-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68fd0-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68fd0-137">-WhatIf</span></span>
<span data-ttu-id="68fd0-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="68fd0-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="68fd0-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="68fd0-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68fd0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68fd0-140">CommonParameters</span></span>
<span data-ttu-id="68fd0-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68fd0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68fd0-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68fd0-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68fd0-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="68fd0-143">INPUTS</span></span>

### <span data-ttu-id="68fd0-144">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="68fd0-144">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="68fd0-145">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="68fd0-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="68fd0-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="68fd0-146">OUTPUTS</span></span>

### <span data-ttu-id="68fd0-147">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="68fd0-147">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="68fd0-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="68fd0-148">NOTES</span></span>

## <span data-ttu-id="68fd0-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="68fd0-149">RELATED LINKS</span></span>

[<span data-ttu-id="68fd0-150">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="68fd0-150">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)
