---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: DBB0E08F-63F4-4D61-A69E-3C16A35301EC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPlannedFailoverJob.md
ms.openlocfilehash: e723aacbfbd1b782a91fdc6aa589bfe15df42cff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496830"
---
# <span data-ttu-id="a84ed-101">Start-AzureRmSiteRecoveryPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="a84ed-101">Start-AzureRmSiteRecoveryPlannedFailoverJob</span></span>

## <span data-ttu-id="a84ed-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a84ed-102">SYNOPSIS</span></span>
<span data-ttu-id="a84ed-103">Startet einen geplanten Failover-Vorgang für eine Websitewiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="a84ed-103">Starts a Site Recovery planned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a84ed-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a84ed-104">SYNTAX</span></span>

### <span data-ttu-id="a84ed-105">ByPEObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="a84ed-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-Server <ASRServer>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a84ed-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="a84ed-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a84ed-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="a84ed-107">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a84ed-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a84ed-108">DESCRIPTION</span></span>
<span data-ttu-id="a84ed-109">Das Cmdlet **Start-AzureRmSiteRecoveryPlannedFailoverJob** startet ein Geplantes Failover für eine Azure Site Recovery Protection-Entität oder einen Wiederherstellungsplan.</span><span class="sxs-lookup"><span data-stu-id="a84ed-109">The **Start-AzureRmSiteRecoveryPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="a84ed-110">Mithilfe des Get-AzureRmSiteRecoveryJob-Cmdlets können Sie überprüfen, ob der Auftrag erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="a84ed-110">You can check whether the job succeeds by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="a84ed-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a84ed-111">EXAMPLES</span></span>

## <span data-ttu-id="a84ed-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a84ed-112">PARAMETERS</span></span>

### <span data-ttu-id="a84ed-113">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="a84ed-113">-CreateVmIfNotFound</span></span>
<span data-ttu-id="a84ed-114">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a84ed-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a84ed-115">Ja</span><span class="sxs-lookup"><span data-stu-id="a84ed-115">Yes</span></span>
- <span data-ttu-id="a84ed-116">Nein</span><span class="sxs-lookup"><span data-stu-id="a84ed-116">No</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Yes, No

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a84ed-117">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="a84ed-117">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="a84ed-118">Gibt die primäre Zertifikatsdatei an.</span><span class="sxs-lookup"><span data-stu-id="a84ed-118">Specifies the primary certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a84ed-119">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="a84ed-119">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="a84ed-120">Gibt die sekundäre Zertifikatsdatei an.</span><span class="sxs-lookup"><span data-stu-id="a84ed-120">Specifies the secondary certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a84ed-121">-Richtung</span><span class="sxs-lookup"><span data-stu-id="a84ed-121">-Direction</span></span>
<span data-ttu-id="a84ed-122">Gibt die Richtung des Failovers an.</span><span class="sxs-lookup"><span data-stu-id="a84ed-122">Specifies the direction of the failover.</span></span>
<span data-ttu-id="a84ed-123">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a84ed-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a84ed-124">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="a84ed-124">PrimaryToRecovery</span></span>
- <span data-ttu-id="a84ed-125">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="a84ed-125">RecoveryToPrimary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a84ed-126">-Optimieren</span><span class="sxs-lookup"><span data-stu-id="a84ed-126">-Optimize</span></span>
<span data-ttu-id="a84ed-127">Gibt an, was optimiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a84ed-127">Specifies what to optimize for.</span></span>
<span data-ttu-id="a84ed-128">Dieser Parameter gilt, wenn ein Failover von einer Azure-Website zu einer lokalen Website durchgeführt wird, für die eine beträchtliche Datensynchronisierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a84ed-128">This parameter applies when failover is done from an Azure site to an on-premise site which requires a substantial data synchronization.</span></span>
<span data-ttu-id="a84ed-129">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="a84ed-129">Valid values are:</span></span>

- <span data-ttu-id="a84ed-130">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="a84ed-130">ForDowntime</span></span>
- <span data-ttu-id="a84ed-131">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="a84ed-131">ForSynchronization</span></span>

<span data-ttu-id="a84ed-132">Wenn **ForDowntime** angegeben wird, bedeutet dies, dass Daten vor dem Failover synchronisiert werden, um die Ausfallzeit zu minimieren.</span><span class="sxs-lookup"><span data-stu-id="a84ed-132">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="a84ed-133">Die Synchronisierung wird ausgeführt, ohne den virtuellen Computer herunterzufahren.</span><span class="sxs-lookup"><span data-stu-id="a84ed-133">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="a84ed-134">Nach Abschluss der Synchronisierung wird der Auftrag angehalten.</span><span class="sxs-lookup"><span data-stu-id="a84ed-134">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="a84ed-135">Setzen Sie den Auftrag fort, um einen zusätzlichen Synchronisierungsvorgang auszuführen, der den virtuellen Computer herunterfährt.</span><span class="sxs-lookup"><span data-stu-id="a84ed-135">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="a84ed-136">Wenn **ForSynchronization** angegeben wird, bedeutet dies, dass Daten während des Failovers nur synchronisiert werden, damit die Datensynchronisierung minimiert wird.</span><span class="sxs-lookup"><span data-stu-id="a84ed-136">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="a84ed-137">Wenn diese Einstellung aktiviert ist, wird der virtuelle Computer sofort heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="a84ed-137">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="a84ed-138">Die Synchronisierung beginnt nach dem Herunterfahren, um den Failovervorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="a84ed-138">Synchronization starts after shutdown to complete the failover operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: ForDownTime, ForSynchronization

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a84ed-139">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="a84ed-139">-ProtectionEntity</span></span>
<span data-ttu-id="a84ed-140">Gibt das Entitätsobjekt für den Standort Wiederherstellungs Schutz an.</span><span class="sxs-lookup"><span data-stu-id="a84ed-140">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a84ed-141">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a84ed-141">-RecoveryPlan</span></span>
<span data-ttu-id="a84ed-142">Gibt ein Wiederherstellungsplan-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="a84ed-142">Specifies a recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a84ed-143">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a84ed-143">-ReplicationProtectedItem</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a84ed-144">-Server</span><span class="sxs-lookup"><span data-stu-id="a84ed-144">-Server</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: ByPEObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a84ed-145">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="a84ed-145">-ServicesProvider</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: ByRPIObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a84ed-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a84ed-146">-DefaultProfile</span></span>
<span data-ttu-id="a84ed-147">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a84ed-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a84ed-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a84ed-148">CommonParameters</span></span>
<span data-ttu-id="a84ed-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a84ed-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a84ed-150">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a84ed-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a84ed-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a84ed-151">INPUTS</span></span>

### <span data-ttu-id="a84ed-152">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="a84ed-152">ASRProtectionEntity</span></span>
<span data-ttu-id="a84ed-153">Der Parameter "ProtectionEntity" akzeptiert den Wert vom Typ "ASRProtectionEntity" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="a84ed-153">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="a84ed-154">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a84ed-154">ASRRecoveryPlan</span></span>
<span data-ttu-id="a84ed-155">Der Parameter "RecoveryPlan" akzeptiert den Wert vom Typ "ASRRecoveryPlan" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="a84ed-155">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="a84ed-156">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a84ed-156">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="a84ed-157">Der Parameter "ReplicationProtectedItem" akzeptiert den Wert vom Typ "ASRReplicationProtectedItem" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="a84ed-157">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="a84ed-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a84ed-158">OUTPUTS</span></span>

### <span data-ttu-id="a84ed-159">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="a84ed-159">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a84ed-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="a84ed-160">NOTES</span></span>

## <span data-ttu-id="a84ed-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a84ed-161">RELATED LINKS</span></span>

