---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrtestfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: bab9cb87f347b198b430c1dadc65a002dfa94141
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476654"
---
# <span data-ttu-id="6c869-101">Start-AzureRmRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="6c869-101">Start-AzureRmRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="6c869-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6c869-102">SYNOPSIS</span></span>
<span data-ttu-id="6c869-103">Startet einen Test-Failover-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="6c869-103">Starts a test failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c869-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c869-104">SYNTAX</span></span>

### <span data-ttu-id="6c869-105">ByRPIObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="6c869-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c869-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="6c869-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c869-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="6c869-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c869-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="6c869-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c869-109">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="6c869-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c869-110">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="6c869-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryPoint <ASRRecoveryPoint>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6c869-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6c869-111">DESCRIPTION</span></span>
<span data-ttu-id="6c869-112">Das Cmdlet **Start-AzureRmRecoveryServicesAsrTestFailoverJob** startet das Test-Failover für ein geschütztes Element oder einen Wiederherstellungsplan der Azure Site Recovery-Replikation.</span><span class="sxs-lookup"><span data-stu-id="6c869-112">The **Start-AzureRmRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="6c869-113">Mithilfe des Get-AzureRmRecoveryServicesAsrJob-Cmdlets können Sie überprüfen, ob der Auftrag erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="6c869-113">You can check whether the job succeeded by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="6c869-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6c869-114">EXAMPLES</span></span>

### <span data-ttu-id="6c869-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6c869-115">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="6c869-116">Startet den Test-Failover-Vorgang für den Wiederherstellungsplan mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6c869-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="6c869-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c869-117">PARAMETERS</span></span>

### <span data-ttu-id="6c869-118">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="6c869-118">-AzureVMNetworkId</span></span>
<span data-ttu-id="6c869-119">Gibt die Azure Virtual Network-ID an, um die Verbindung zwischen dem Testfehler und dem virtuellen Computer herzustellen.</span><span class="sxs-lookup"><span data-stu-id="6c869-119">Specifies the Azure virtual network ID to connect the test fail over virtual machine(s) to.</span></span>

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

### <span data-ttu-id="6c869-120">-CloudServiceCreationOption</span><span class="sxs-lookup"><span data-stu-id="6c869-120">-CloudServiceCreationOption</span></span>
<span data-ttu-id="6c869-121">Gibt an, ob ein neuer clouddienst erstellt oder der für den virtuellen Computer konfigurierte Wiederherstellungs clouddienst für das testfailover verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6c869-121">Specifies whether a new cloud service should be created or the recovery cloud service configured for the VM should be used for the test failover.</span></span>

```yaml
Type: String
Parameter Sets: ByRPIObject, ByRPObject, ByRPObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases:
Accepted values: UseRecoveryCloudService, AutoCreateCloudService

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c869-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6c869-122">-Confirm</span></span>
<span data-ttu-id="6c869-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6c869-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c869-124">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="6c869-124">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="6c869-125">Gibt die primäre Zertifikatsdatei an.</span><span class="sxs-lookup"><span data-stu-id="6c869-125">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="6c869-126">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="6c869-126">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="6c869-127">Gibt die sekundäre Zertifikatsdatei an.</span><span class="sxs-lookup"><span data-stu-id="6c869-127">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="6c869-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c869-128">-DefaultProfile</span></span>
<span data-ttu-id="6c869-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6c869-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="6c869-130">-Richtung</span><span class="sxs-lookup"><span data-stu-id="6c869-130">-Direction</span></span>
<span data-ttu-id="6c869-131">Gibt die failoverrichtung an.</span><span class="sxs-lookup"><span data-stu-id="6c869-131">Specifies the failover direction.</span></span>
<span data-ttu-id="6c869-132">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="6c869-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6c869-133">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="6c869-133">PrimaryToRecovery</span></span>
- <span data-ttu-id="6c869-134">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="6c869-134">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="6c869-135">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6c869-135">-RecoveryPlan</span></span>
<span data-ttu-id="6c869-136">Gibt ein ASR-Wiederherstellungsplan-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="6c869-136">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="6c869-137">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="6c869-137">-RecoveryPoint</span></span>
<span data-ttu-id="6c869-138">Gibt einen benutzerdefinierten Wiederherstellungspunkt an, um das Failover des geschützten Computers zu testen.</span><span class="sxs-lookup"><span data-stu-id="6c869-138">Specifies a custom recovery point to test failover the protected machine to.</span></span>

```yaml
Type: ASRRecoveryPoint
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c869-139">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="6c869-139">-RecoveryTag</span></span>
<span data-ttu-id="6c869-140">Gibt das Wiederherstellungs an, um das Failover zu testen.</span><span class="sxs-lookup"><span data-stu-id="6c869-140">Specifies the recovery tag to test failover to</span></span>

```yaml
Type: String
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c869-141">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6c869-141">-ReplicationProtectedItem</span></span>
<span data-ttu-id="6c869-142">Gibt ein geschütztes ASR-Replikations Element an.</span><span class="sxs-lookup"><span data-stu-id="6c869-142">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="6c869-143">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="6c869-143">-VMNetwork</span></span>
<span data-ttu-id="6c869-144">Gibt das Netzwerk der virtuellen Maschine der Standortwiederherstellung an, mit dem die virtuellen Test-Failover-Computer (s) verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="6c869-144">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

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

### <span data-ttu-id="6c869-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c869-145">-WhatIf</span></span>
<span data-ttu-id="6c869-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6c869-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6c869-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6c869-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c869-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c869-148">CommonParameters</span></span>
<span data-ttu-id="6c869-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c869-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c869-150">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c869-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c869-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6c869-151">INPUTS</span></span>

### <span data-ttu-id="6c869-152">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6c869-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="6c869-153">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="6c869-153">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="6c869-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6c869-154">OUTPUTS</span></span>

### <span data-ttu-id="6c869-155">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="6c869-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6c869-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="6c869-156">NOTES</span></span>

## <span data-ttu-id="6c869-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6c869-157">RELATED LINKS</span></span>

[<span data-ttu-id="6c869-158">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="6c869-158">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)
