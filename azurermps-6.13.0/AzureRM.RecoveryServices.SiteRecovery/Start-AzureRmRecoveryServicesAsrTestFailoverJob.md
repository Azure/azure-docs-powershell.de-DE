---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrtestfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: f0350cfa9facfe8fc21e6c039c2fa5838bba8875
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495746"
---
# <span data-ttu-id="599c5-101">Start-AzureRmRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="599c5-101">Start-AzureRmRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="599c5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="599c5-102">SYNOPSIS</span></span>
<span data-ttu-id="599c5-103">Startet einen Test-Failover-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="599c5-103">Starts a test failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="599c5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="599c5-104">SYNTAX</span></span>

### <span data-ttu-id="599c5-105">ByRPIObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="599c5-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="599c5-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="599c5-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="599c5-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="599c5-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="599c5-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="599c5-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="599c5-109">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="599c5-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="599c5-110">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="599c5-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryPoint <ASRRecoveryPoint>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="599c5-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="599c5-111">DESCRIPTION</span></span>
<span data-ttu-id="599c5-112">Das Cmdlet **Start-AzureRmRecoveryServicesAsrTestFailoverJob** startet das Test-Failover für ein geschütztes Element oder einen Wiederherstellungsplan der Azure Site Recovery-Replikation.</span><span class="sxs-lookup"><span data-stu-id="599c5-112">The **Start-AzureRmRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="599c5-113">Mithilfe des Get-AzureRmRecoveryServicesAsrJob-Cmdlets können Sie überprüfen, ob der Auftrag erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="599c5-113">You can check whether the job succeeded by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="599c5-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="599c5-114">EXAMPLES</span></span>

### <span data-ttu-id="599c5-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="599c5-115">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="599c5-116">Startet den Test-Failover-Vorgang für den Wiederherstellungsplan mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="599c5-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="599c5-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="599c5-117">PARAMETERS</span></span>

### <span data-ttu-id="599c5-118">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="599c5-118">-AzureVMNetworkId</span></span>
<span data-ttu-id="599c5-119">Gibt die Azure Virtual Network-ID an, um die Verbindung zwischen dem Testfehler und dem virtuellen Computer herzustellen.</span><span class="sxs-lookup"><span data-stu-id="599c5-119">Specifies the Azure virtual network ID to connect the test fail over virtual machine(s) to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="599c5-120">-CloudServiceCreationOption</span><span class="sxs-lookup"><span data-stu-id="599c5-120">-CloudServiceCreationOption</span></span>
<span data-ttu-id="599c5-121">Gibt an, ob ein neuer clouddienst erstellt oder der für den virtuellen Computer konfigurierte Wiederherstellungs clouddienst für das testfailover verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="599c5-121">Specifies whether a new cloud service should be created or the recovery cloud service configured for the VM should be used for the test failover.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPIObject, ByRPObject, ByRPObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases:
Accepted values: UseRecoveryCloudService, AutoCreateCloudService

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="599c5-122">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="599c5-122">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="599c5-123">Gibt die primäre Zertifikatsdatei an.</span><span class="sxs-lookup"><span data-stu-id="599c5-123">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="599c5-124">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="599c5-124">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="599c5-125">Gibt die sekundäre Zertifikatsdatei an.</span><span class="sxs-lookup"><span data-stu-id="599c5-125">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="599c5-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="599c5-126">-DefaultProfile</span></span>
<span data-ttu-id="599c5-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="599c5-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="599c5-128">-Richtung</span><span class="sxs-lookup"><span data-stu-id="599c5-128">-Direction</span></span>
<span data-ttu-id="599c5-129">Gibt die failoverrichtung an.</span><span class="sxs-lookup"><span data-stu-id="599c5-129">Specifies the failover direction.</span></span>
<span data-ttu-id="599c5-130">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="599c5-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="599c5-131">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="599c5-131">PrimaryToRecovery</span></span>
- <span data-ttu-id="599c5-132">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="599c5-132">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="599c5-133">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="599c5-133">-RecoveryPlan</span></span>
<span data-ttu-id="599c5-134">Gibt ein ASR-Wiederherstellungsplan-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="599c5-134">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="599c5-135">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="599c5-135">-RecoveryPoint</span></span>
<span data-ttu-id="599c5-136">Gibt einen benutzerdefinierten Wiederherstellungspunkt an, um das Failover des geschützten Computers zu testen.</span><span class="sxs-lookup"><span data-stu-id="599c5-136">Specifies a custom recovery point to test failover the protected machine to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="599c5-137">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="599c5-137">-RecoveryTag</span></span>
<span data-ttu-id="599c5-138">Gibt das Wiederherstellungs an, um das Failover zu testen.</span><span class="sxs-lookup"><span data-stu-id="599c5-138">Specifies the recovery tag to test failover to</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="599c5-139">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="599c5-139">-ReplicationProtectedItem</span></span>
<span data-ttu-id="599c5-140">Gibt ein geschütztes ASR-Replikations Element an.</span><span class="sxs-lookup"><span data-stu-id="599c5-140">Specifies an ASR replication protected item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="599c5-141">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="599c5-141">-VMNetwork</span></span>
<span data-ttu-id="599c5-142">Gibt das Netzwerk der virtuellen Maschine der Standortwiederherstellung an, mit dem die virtuellen Test-Failover-Computer (s) verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="599c5-142">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: ByRPObjectWithVMNetwork, ByRPIObjectWithVMNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="599c5-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="599c5-143">-Confirm</span></span>
<span data-ttu-id="599c5-144">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="599c5-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="599c5-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="599c5-145">-WhatIf</span></span>
<span data-ttu-id="599c5-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="599c5-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="599c5-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="599c5-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="599c5-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="599c5-148">CommonParameters</span></span>
<span data-ttu-id="599c5-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="599c5-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="599c5-150">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="599c5-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="599c5-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="599c5-151">INPUTS</span></span>

### <span data-ttu-id="599c5-152">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="599c5-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="599c5-153">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="599c5-153">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="599c5-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="599c5-154">OUTPUTS</span></span>

### <span data-ttu-id="599c5-155">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="599c5-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="599c5-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="599c5-156">NOTES</span></span>

## <span data-ttu-id="599c5-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="599c5-157">RELATED LINKS</span></span>

[<span data-ttu-id="599c5-158">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="599c5-158">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)
