---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrtestfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: a05467b19aaf69bccdca64c8e17b894941f3ac6f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659796"
---
# <span data-ttu-id="f17e6-101">Start-AzRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="f17e6-101">Start-AzRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="f17e6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f17e6-102">SYNOPSIS</span></span>
<span data-ttu-id="f17e6-103">Startet einen Test-Failover-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="f17e6-103">Starts a test failover operation.</span></span>

## <span data-ttu-id="f17e6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f17e6-104">SYNTAX</span></span>

### <span data-ttu-id="f17e6-105">ByRPIObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="f17e6-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f17e6-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="f17e6-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f17e6-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="f17e6-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f17e6-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="f17e6-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f17e6-109">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="f17e6-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f17e6-110">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="f17e6-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryPoint <ASRRecoveryPoint>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f17e6-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f17e6-111">DESCRIPTION</span></span>
<span data-ttu-id="f17e6-112">Das Cmdlet **Start-AzRecoveryServicesAsrTestFailoverJob** startet das Test-Failover für ein geschütztes Element oder einen Wiederherstellungsplan der Azure Site Recovery-Replikation.</span><span class="sxs-lookup"><span data-stu-id="f17e6-112">The **Start-AzRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="f17e6-113">Mithilfe des Get-AzRecoveryServicesAsrJob-Cmdlets können Sie überprüfen, ob der Auftrag erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="f17e6-113">You can check whether the job succeeded by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="f17e6-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f17e6-114">EXAMPLES</span></span>

### <span data-ttu-id="f17e6-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f17e6-115">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="f17e6-116">Startet den Test-Failover-Vorgang für den Wiederherstellungsplan mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f17e6-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="f17e6-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="f17e6-117">PARAMETERS</span></span>

### <span data-ttu-id="f17e6-118">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="f17e6-118">-AzureVMNetworkId</span></span>
<span data-ttu-id="f17e6-119">{{Fill AzureVMNetworkId Description}}</span><span class="sxs-lookup"><span data-stu-id="f17e6-119">{{Fill AzureVMNetworkId Description}}</span></span>

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

### <span data-ttu-id="f17e6-120">-CloudServiceCreationOption</span><span class="sxs-lookup"><span data-stu-id="f17e6-120">-CloudServiceCreationOption</span></span>
<span data-ttu-id="f17e6-121">Gibt an, ob ein neuer clouddienst erstellt oder der für den virtuellen Computer konfigurierte Wiederherstellungs clouddienst für das testfailover verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f17e6-121">Specifies whether a new cloud service should be created or the recovery cloud service configured for the VM should be used for the test failover.</span></span>

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

### <span data-ttu-id="f17e6-122">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="f17e6-122">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="f17e6-123">Gibt die primäre Zertifikatsdatei an.</span><span class="sxs-lookup"><span data-stu-id="f17e6-123">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="f17e6-124">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="f17e6-124">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="f17e6-125">Gibt die sekundäre Zertifikatsdatei an.</span><span class="sxs-lookup"><span data-stu-id="f17e6-125">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="f17e6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f17e6-126">-DefaultProfile</span></span>
<span data-ttu-id="f17e6-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f17e6-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f17e6-128">-Richtung</span><span class="sxs-lookup"><span data-stu-id="f17e6-128">-Direction</span></span>
<span data-ttu-id="f17e6-129">Gibt die failoverrichtung an.</span><span class="sxs-lookup"><span data-stu-id="f17e6-129">Specifies the failover direction.</span></span>
<span data-ttu-id="f17e6-130">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f17e6-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f17e6-131">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="f17e6-131">PrimaryToRecovery</span></span>
- <span data-ttu-id="f17e6-132">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="f17e6-132">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="f17e6-133">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f17e6-133">-RecoveryPlan</span></span>
<span data-ttu-id="f17e6-134">Gibt ein ASR-Wiederherstellungsplan-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="f17e6-134">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="f17e6-135">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="f17e6-135">-RecoveryPoint</span></span>
<span data-ttu-id="f17e6-136">Gibt einen benutzerdefinierten Wiederherstellungspunkt an, um das Failover des geschützten Computers zu testen.</span><span class="sxs-lookup"><span data-stu-id="f17e6-136">Specifies a custom recovery point to test failover the protected machine to.</span></span>

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

### <span data-ttu-id="f17e6-137">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="f17e6-137">-RecoveryTag</span></span>
<span data-ttu-id="f17e6-138">Gibt das Wiederherstellungs an, um das Failover zu testen.</span><span class="sxs-lookup"><span data-stu-id="f17e6-138">Specifies the recovery tag to test failover to</span></span>

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

### <span data-ttu-id="f17e6-139">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f17e6-139">-ReplicationProtectedItem</span></span>
<span data-ttu-id="f17e6-140">Gibt ein geschütztes ASR-Replikations Element an.</span><span class="sxs-lookup"><span data-stu-id="f17e6-140">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="f17e6-141">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="f17e6-141">-VMNetwork</span></span>
<span data-ttu-id="f17e6-142">Gibt das Netzwerk der virtuellen Maschine der Standortwiederherstellung an, mit dem die virtuellen Test-Failover-Computer (s) verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="f17e6-142">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

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

### <span data-ttu-id="f17e6-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f17e6-143">-Confirm</span></span>
<span data-ttu-id="f17e6-144">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f17e6-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f17e6-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f17e6-145">-WhatIf</span></span>
<span data-ttu-id="f17e6-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f17e6-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f17e6-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f17e6-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f17e6-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f17e6-148">CommonParameters</span></span>
<span data-ttu-id="f17e6-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f17e6-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f17e6-150">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f17e6-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f17e6-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f17e6-151">INPUTS</span></span>

### <span data-ttu-id="f17e6-152">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f17e6-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="f17e6-153">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f17e6-153">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="f17e6-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f17e6-154">OUTPUTS</span></span>

### <span data-ttu-id="f17e6-155">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f17e6-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f17e6-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="f17e6-156">NOTES</span></span>

## <span data-ttu-id="f17e6-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f17e6-157">RELATED LINKS</span></span>

[<span data-ttu-id="f17e6-158">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="f17e6-158">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)
