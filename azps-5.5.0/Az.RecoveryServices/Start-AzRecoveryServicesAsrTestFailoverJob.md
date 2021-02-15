---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrtestfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: 11d254fbf43a05e4e58f0d51f5226a6a7065dd50
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160057"
---
# <span data-ttu-id="dbe73-101">Start-AzRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="dbe73-101">Start-AzRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="dbe73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbe73-102">SYNOPSIS</span></span>
<span data-ttu-id="dbe73-103">Startet einen Test failover-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="dbe73-103">Starts a test failover operation.</span></span>

## <span data-ttu-id="dbe73-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dbe73-104">SYNTAX</span></span>

### <span data-ttu-id="dbe73-105">ByRPIObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="dbe73-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbe73-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="dbe73-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbe73-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="dbe73-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbe73-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="dbe73-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbe73-109">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="dbe73-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbe73-110">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="dbe73-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryPoint <ASRRecoveryPoint>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dbe73-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dbe73-111">DESCRIPTION</span></span>
<span data-ttu-id="dbe73-112">Das **Cmdlet "Start-AzRecoveryServicesAsrTestFailoverJob"** startet den Test failover eines geschützten Elements oder Wiederherstellungsplans für die Azure-Websitewiederherstellungsreplikation.</span><span class="sxs-lookup"><span data-stu-id="dbe73-112">The **Start-AzRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="dbe73-113">Sie können mithilfe des Cmdlets "Get-AzRecoveryServicesAsrJob überprüfen, ob der Auftrag erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="dbe73-113">You can check whether the job succeeded by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="dbe73-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dbe73-114">EXAMPLES</span></span>

### <span data-ttu-id="dbe73-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dbe73-115">Example 1</span></span>
```powershell
PS C:\> $currentJob = Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="dbe73-116">Startet den Test failovervorgang für den Wiederherstellungsplan mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, mit dem der Vorgang nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="dbe73-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="dbe73-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="dbe73-117">Example 2</span></span>

<span data-ttu-id="dbe73-118">Startet einen Test failover-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="dbe73-118">Starts a test failover operation.</span></span> <span data-ttu-id="dbe73-119">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="dbe73-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Start-AzRecoveryServicesAsrTestFailoverJob -AzureVMNetworkId <String> -Direction PrimaryToRecovery -RecoveryPlan $RP
```

## <span data-ttu-id="dbe73-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dbe73-120">PARAMETERS</span></span>

### <span data-ttu-id="dbe73-121">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="dbe73-121">-AzureVMNetworkId</span></span>
<span data-ttu-id="dbe73-122">Gibt die Azure VM-Netzwerk-ID für die Wiederherstellungs-VM nach dem Failover an.</span><span class="sxs-lookup"><span data-stu-id="dbe73-122">Specifies the Azure vm network id for recovery VM after failover.</span></span>

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

### <span data-ttu-id="dbe73-123">-CloudServiceCreationOption</span><span class="sxs-lookup"><span data-stu-id="dbe73-123">-CloudServiceCreationOption</span></span>
<span data-ttu-id="dbe73-124">Gibt an, ob ein neuer Clouddienst erstellt oder der für die VM konfigurierte Wiederherstellungs-Clouddienst für den Test failover verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="dbe73-124">Specifies whether a new cloud service should be created or the recovery cloud service configured for the VM should be used for the test failover.</span></span>

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

### <span data-ttu-id="dbe73-125">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="dbe73-125">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="dbe73-126">Gibt die primäre Zertifikatdatei an.</span><span class="sxs-lookup"><span data-stu-id="dbe73-126">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="dbe73-127">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="dbe73-127">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="dbe73-128">Gibt die sekundäre Zertifikatdatei an.</span><span class="sxs-lookup"><span data-stu-id="dbe73-128">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="dbe73-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbe73-129">-DefaultProfile</span></span>
<span data-ttu-id="dbe73-130">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dbe73-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="dbe73-131">-Direction</span><span class="sxs-lookup"><span data-stu-id="dbe73-131">-Direction</span></span>
<span data-ttu-id="dbe73-132">Gibt die Failoverrichtung an.</span><span class="sxs-lookup"><span data-stu-id="dbe73-132">Specifies the failover direction.</span></span>
<span data-ttu-id="dbe73-133">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="dbe73-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dbe73-134">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="dbe73-134">PrimaryToRecovery</span></span>
- <span data-ttu-id="dbe73-135">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="dbe73-135">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="dbe73-136">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="dbe73-136">-RecoveryPlan</span></span>
<span data-ttu-id="dbe73-137">Gibt ein ASR-Wiederherstellungsplanobjekt an.</span><span class="sxs-lookup"><span data-stu-id="dbe73-137">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="dbe73-138">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="dbe73-138">-RecoveryPoint</span></span>
<span data-ttu-id="dbe73-139">Gibt einen benutzerdefinierten Wiederherstellungspunkt an, um den Failover des geschützten Computers zu testen.</span><span class="sxs-lookup"><span data-stu-id="dbe73-139">Specifies a custom recovery point to test failover the protected machine to.</span></span>

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

### <span data-ttu-id="dbe73-140">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="dbe73-140">-RecoveryTag</span></span>
<span data-ttu-id="dbe73-141">Gibt das Wiederherstellungstag an, zu dem der Failover zu testen ist.</span><span class="sxs-lookup"><span data-stu-id="dbe73-141">Specifies the recovery tag to test failover to</span></span>

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

### <span data-ttu-id="dbe73-142">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="dbe73-142">-ReplicationProtectedItem</span></span>
<span data-ttu-id="dbe73-143">Gibt ein asR-replikationsgeschütztes Element an.</span><span class="sxs-lookup"><span data-stu-id="dbe73-143">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="dbe73-144">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="dbe73-144">-VMNetwork</span></span>
<span data-ttu-id="dbe73-145">Gibt das Netzwerk des virtuellen Site Recovery-Computers an, mit dem die virtuellen Test failovercomputer verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="dbe73-145">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

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

### <span data-ttu-id="dbe73-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dbe73-146">-Confirm</span></span>
<span data-ttu-id="dbe73-147">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dbe73-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbe73-148">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="dbe73-148">-WhatIf</span></span>
<span data-ttu-id="dbe73-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dbe73-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dbe73-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dbe73-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbe73-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbe73-151">CommonParameters</span></span>
<span data-ttu-id="dbe73-152">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbe73-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbe73-153">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dbe73-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbe73-154">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dbe73-154">INPUTS</span></span>

### <span data-ttu-id="dbe73-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="dbe73-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="dbe73-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="dbe73-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="dbe73-157">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dbe73-157">OUTPUTS</span></span>

### <span data-ttu-id="dbe73-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="dbe73-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="dbe73-159">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="dbe73-159">NOTES</span></span>

## <span data-ttu-id="dbe73-160">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="dbe73-160">RELATED LINKS</span></span>

[<span data-ttu-id="dbe73-161">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="dbe73-161">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)
