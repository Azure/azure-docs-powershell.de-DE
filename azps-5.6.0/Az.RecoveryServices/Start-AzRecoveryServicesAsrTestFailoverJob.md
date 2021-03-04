---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/start-azrecoveryservicesasrtestfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: b5a06683e5254077a63d4c0b1933d51d9c1ad8e3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936624"
---
# <span data-ttu-id="aa5d7-101">Start-AzRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="aa5d7-101">Start-AzRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="aa5d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa5d7-102">SYNOPSIS</span></span>
<span data-ttu-id="aa5d7-103">Startet einen Test failover-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="aa5d7-103">Starts a test failover operation.</span></span>

## <span data-ttu-id="aa5d7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aa5d7-104">SYNTAX</span></span>

### <span data-ttu-id="aa5d7-105">ByRPIObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="aa5d7-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa5d7-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="aa5d7-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa5d7-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="aa5d7-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa5d7-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="aa5d7-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa5d7-109">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="aa5d7-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa5d7-110">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="aa5d7-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryPoint <ASRRecoveryPoint>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aa5d7-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aa5d7-111">DESCRIPTION</span></span>
<span data-ttu-id="aa5d7-112">Das **Cmdlet Start-AzRecoveryServicesAsrTestFailoverJob** startet das Test failover eines geschützten Elements oder Wiederherstellungsplans für azuree Websitewiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="aa5d7-112">The **Start-AzRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="aa5d7-113">Sie können überprüfen, ob der Auftrag erfolgreich war, indem Sie das cmdlet Get-AzRecoveryServicesAsrJob verwenden.</span><span class="sxs-lookup"><span data-stu-id="aa5d7-113">You can check whether the job succeeded by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="aa5d7-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="aa5d7-114">EXAMPLES</span></span>

### <span data-ttu-id="aa5d7-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="aa5d7-115">Example 1</span></span>
```powershell
PS C:\> $currentJob = Start-AzRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="aa5d7-116">Startet den Test failover-Vorgang für den Wiederherstellungsplan mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, der zum Nachverfolgen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="aa5d7-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="aa5d7-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="aa5d7-117">Example 2</span></span>

<span data-ttu-id="aa5d7-118">Startet einen Test failover-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="aa5d7-118">Starts a test failover operation.</span></span> <span data-ttu-id="aa5d7-119">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="aa5d7-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Start-AzRecoveryServicesAsrTestFailoverJob -AzureVMNetworkId <String> -Direction PrimaryToRecovery -RecoveryPlan $RP
```

## <span data-ttu-id="aa5d7-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="aa5d7-120">PARAMETERS</span></span>

### <span data-ttu-id="aa5d7-121">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="aa5d7-121">-AzureVMNetworkId</span></span>
<span data-ttu-id="aa5d7-122">Gibt die Azure VM-Netzwerk-ID für die Wiederherstellungs-VM nach dem Failover an.</span><span class="sxs-lookup"><span data-stu-id="aa5d7-122">Specifies the Azure vm network id for recovery VM after failover.</span></span>

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

### <span data-ttu-id="aa5d7-123">-CloudServiceCreationOption</span><span class="sxs-lookup"><span data-stu-id="aa5d7-123">-CloudServiceCreationOption</span></span>
<span data-ttu-id="aa5d7-124">Gibt an, ob ein neuer Clouddienst erstellt oder der für die VM konfigurierte Wiederherstellungs-Clouddienst für den Test failover verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="aa5d7-124">Specifies whether a new cloud service should be created or the recovery cloud service configured for the VM should be used for the test failover.</span></span>

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

### <span data-ttu-id="aa5d7-125">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="aa5d7-125">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="aa5d7-126">Gibt die primäre Zertifikatdatei an.</span><span class="sxs-lookup"><span data-stu-id="aa5d7-126">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="aa5d7-127">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="aa5d7-127">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="aa5d7-128">Gibt die sekundäre Zertifikatdatei an.</span><span class="sxs-lookup"><span data-stu-id="aa5d7-128">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="aa5d7-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa5d7-129">-DefaultProfile</span></span>
<span data-ttu-id="aa5d7-130">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aa5d7-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="aa5d7-131">-Richtung</span><span class="sxs-lookup"><span data-stu-id="aa5d7-131">-Direction</span></span>
<span data-ttu-id="aa5d7-132">Gibt die Failoverrichtung an.</span><span class="sxs-lookup"><span data-stu-id="aa5d7-132">Specifies the failover direction.</span></span>
<span data-ttu-id="aa5d7-133">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="aa5d7-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aa5d7-134">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="aa5d7-134">PrimaryToRecovery</span></span>
- <span data-ttu-id="aa5d7-135">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="aa5d7-135">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="aa5d7-136">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="aa5d7-136">-RecoveryPlan</span></span>
<span data-ttu-id="aa5d7-137">Gibt ein ASR-Wiederherstellungsplanobjekt an.</span><span class="sxs-lookup"><span data-stu-id="aa5d7-137">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="aa5d7-138">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="aa5d7-138">-RecoveryPoint</span></span>
<span data-ttu-id="aa5d7-139">Gibt einen benutzerdefinierten Wiederherstellungspunkt zum Testen des Failovers für den geschützten Computer an.</span><span class="sxs-lookup"><span data-stu-id="aa5d7-139">Specifies a custom recovery point to test failover the protected machine to.</span></span>

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

### <span data-ttu-id="aa5d7-140">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="aa5d7-140">-RecoveryTag</span></span>
<span data-ttu-id="aa5d7-141">Gibt das Wiederherstellungstag zum Testen des Failovers an.</span><span class="sxs-lookup"><span data-stu-id="aa5d7-141">Specifies the recovery tag to test failover to</span></span>

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

### <span data-ttu-id="aa5d7-142">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="aa5d7-142">-ReplicationProtectedItem</span></span>
<span data-ttu-id="aa5d7-143">Gibt ein geschütztes Element für die ASR-Replikation an.</span><span class="sxs-lookup"><span data-stu-id="aa5d7-143">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="aa5d7-144">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="aa5d7-144">-VMNetwork</span></span>
<span data-ttu-id="aa5d7-145">Gibt das Netzwerk des virtuellen Websitewiederherstellungscomputers an, mit dem die virtuellen Test-Failovercomputer verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="aa5d7-145">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

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

### <span data-ttu-id="aa5d7-146">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="aa5d7-146">-Confirm</span></span>
<span data-ttu-id="aa5d7-147">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aa5d7-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa5d7-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa5d7-148">-WhatIf</span></span>
<span data-ttu-id="aa5d7-149">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aa5d7-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aa5d7-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aa5d7-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa5d7-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa5d7-151">CommonParameters</span></span>
<span data-ttu-id="aa5d7-152">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa5d7-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa5d7-153">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa5d7-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa5d7-154">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="aa5d7-154">INPUTS</span></span>

### <span data-ttu-id="aa5d7-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="aa5d7-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="aa5d7-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="aa5d7-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="aa5d7-157">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="aa5d7-157">OUTPUTS</span></span>

### <span data-ttu-id="aa5d7-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="aa5d7-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="aa5d7-159">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="aa5d7-159">NOTES</span></span>

## <span data-ttu-id="aa5d7-160">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="aa5d7-160">RELATED LINKS</span></span>

[<span data-ttu-id="aa5d7-161">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="aa5d7-161">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)
