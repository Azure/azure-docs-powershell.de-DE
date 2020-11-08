---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 9AE41884-C39F-4AEB-8030-96167F98C8DD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6b46cc27b2e5380f3cb533a4355a94170e941cd8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006234"
---
# <span data-ttu-id="2b8fa-101">Start-AzureSiteRecoveryTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="2b8fa-101">Start-AzureSiteRecoveryTestFailoverJob</span></span>

## <span data-ttu-id="2b8fa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2b8fa-102">SYNOPSIS</span></span>
<span data-ttu-id="2b8fa-103">Startet ein testfailover für eine Website Wiederherstellungs Schutz Entität.</span><span class="sxs-lookup"><span data-stu-id="2b8fa-103">Starts a test failover for a Site Recovery protection entity.</span></span>

## <span data-ttu-id="2b8fa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b8fa-104">SYNTAX</span></span>

### <span data-ttu-id="2b8fa-105">ByPEId (Standard)</span><span class="sxs-lookup"><span data-stu-id="2b8fa-105">ByPEId (Default)</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntityId <String> -ProtectionContainerId <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b8fa-106">ByRPId</span><span class="sxs-lookup"><span data-stu-id="2b8fa-106">ByRPId</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -RpId <String> [-Network <ASRNetwork>] [-NetworkType <String>]
 -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="2b8fa-107">ByRPIdWithLogicalNetworkID</span><span class="sxs-lookup"><span data-stu-id="2b8fa-107">ByRPIdWithLogicalNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -RpId <String> [-Network <ASRNetwork>] [-NetworkType <String>]
 -Direction <String> [-WaitForCompletion] -LogicalNetworkId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b8fa-108">ByRPIdWithVMNetworkID</span><span class="sxs-lookup"><span data-stu-id="2b8fa-108">ByRPIdWithVMNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -RpId <String> [-Network <ASRNetwork>] [-NetworkType <String>]
 -Direction <String> [-WaitForCompletion] -VmNetworkId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b8fa-109">ByRPIdWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="2b8fa-109">ByRPIdWithVMNetwork</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -RpId <String> -Network <ASRNetwork> [-NetworkType <String>]
 -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="2b8fa-110">ByPEObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="2b8fa-110">ByPEObjectWithVMNetwork</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -Network <ASRNetwork> [-NetworkType <String>] -Direction <String>
 -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="2b8fa-111">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="2b8fa-111">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -Network <ASRNetwork> [-NetworkType <String>]
 -RecoveryPlan <ASRRecoveryPlan> -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b8fa-112">ByPEIdWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="2b8fa-112">ByPEIdWithVMNetwork</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -Network <ASRNetwork> [-NetworkType <String>] -Direction <String>
 -ProtectionEntityId <String> -ProtectionContainerId <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b8fa-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="2b8fa-113">ByRPObject</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>]
 -RecoveryPlan <ASRRecoveryPlan> -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b8fa-114">ByRPObjectWithLogicalNetworkID</span><span class="sxs-lookup"><span data-stu-id="2b8fa-114">ByRPObjectWithLogicalNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>]
 -RecoveryPlan <ASRRecoveryPlan> -Direction <String> [-WaitForCompletion] -LogicalNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="2b8fa-115">ByRPObjectWithVMNetworkID</span><span class="sxs-lookup"><span data-stu-id="2b8fa-115">ByRPObjectWithVMNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>]
 -RecoveryPlan <ASRRecoveryPlan> -Direction <String> [-WaitForCompletion] -VmNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="2b8fa-116">ByPEIdWithLogicalNetworkID</span><span class="sxs-lookup"><span data-stu-id="2b8fa-116">ByPEIdWithLogicalNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntityId <String> -ProtectionContainerId <String> [-WaitForCompletion] -LogicalNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="2b8fa-117">ByPEIdWithVMNetworkID</span><span class="sxs-lookup"><span data-stu-id="2b8fa-117">ByPEIdWithVMNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntityId <String> -ProtectionContainerId <String> [-WaitForCompletion] -VmNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="2b8fa-118">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="2b8fa-118">ByPEObject</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="2b8fa-119">ByPEObjectWithLogicalNetworkID</span><span class="sxs-lookup"><span data-stu-id="2b8fa-119">ByPEObjectWithLogicalNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion] -LogicalNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="2b8fa-120">ByPEObjectWithVMNetworkID</span><span class="sxs-lookup"><span data-stu-id="2b8fa-120">ByPEObjectWithVMNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion] -VmNetworkId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="2b8fa-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2b8fa-121">DESCRIPTION</span></span>
<span data-ttu-id="2b8fa-122">Das Cmdlet **Start-AzureSiteRecoveryTestFailoverJob** startet das Test-Failover einer Azure Site Recovery Protection-Entität oder eines Wiederherstellungsplans.</span><span class="sxs-lookup"><span data-stu-id="2b8fa-122">The **Start-AzureSiteRecoveryTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="2b8fa-123">Mit dem Cmdlet **Get-AzureRMSiteRecoveryJob** können Sie überprüfen, ob der Auftrag erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="2b8fa-123">You can check whether the job succeeded by using the **Get-AzureRMSiteRecoveryJob** cmdlet.</span></span>

## <span data-ttu-id="2b8fa-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2b8fa-124">EXAMPLES</span></span>

### <span data-ttu-id="2b8fa-125">Beispiel 1: Starten eines Test Failovers</span><span class="sxs-lookup"><span data-stu-id="2b8fa-125">Example 1: Start a test failover</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer
PS C:\> $ProtectionEntity = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $ProtectionContainer
PS C:\> Start-AzureSiteRecoveryTestFailoverJob -ProtectionEntity $ProtectionEntity -Direction "PrimaryToRecovery"
ID               : c38eecdc-731c-405b-a61c-08db99aae2fe
ClientRequestId  : 32ace403-0916-4967-83a1-529176bd6e88-2014-49-06 15:49:24Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : {}
Name             : 
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="2b8fa-126">Der erste Befehl verwendet das Cmdlet " **Get-AzureSiteRecoveryProtectionContainer** ", um einen geschützten Container abzurufen, und speichert ihn dann in der $ProtectionContainer-Variablen.</span><span class="sxs-lookup"><span data-stu-id="2b8fa-126">The first command uses the **Get-AzureSiteRecoveryProtectionContainer** cmdlet to get a protected container, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="2b8fa-127">Der zweite Befehl ruft die geschützten Entitäten ab, die zu dem in $ProtectionContainer gespeicherten geschützten Container gehören, indem Sie das Cmdlet " **Get-AzureSiteRecoveryProtectionEntity** " verwenden.</span><span class="sxs-lookup"><span data-stu-id="2b8fa-127">The second command gets the protected entities that belong to the protected container stored in $ProtectionContainer by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="2b8fa-128">Der Befehl speichert die Ergebnisse in der $ProtectionEntity-Variablen.</span><span class="sxs-lookup"><span data-stu-id="2b8fa-128">The command stores the results in the $ProtectionEntity variable.</span></span>

<span data-ttu-id="2b8fa-129">Der endgültige Befehl startet den Test-Failover-Vorgang für die in $ProtectionEntity gespeicherten geschützten Entitäten und gibt die Richtung des Failovers an.</span><span class="sxs-lookup"><span data-stu-id="2b8fa-129">The final command starts the test failover operation for the protected entities stored in $ProtectionEntity and specifies the direction of the failover.</span></span>

### <span data-ttu-id="2b8fa-130">Beispiel 2: Starten eines Test Failovers mit einem Wiederherstellungsplan</span><span class="sxs-lookup"><span data-stu-id="2b8fa-130">Example 2: Start a test failover using a recovery plan</span></span>
```
PS C:\> $RecoveryPlan = Get-AzureSiteRecoveryRecoveryPlan -Name "RecoveryPlan01"
Start-AzureSiteRecoveryTestFailoverJob -Direction PrimaryToRecovery -RecoveryPlan $RecoveryPlan
```

<span data-ttu-id="2b8fa-131">Dieser Befehl ruft den Wiederherstellungsplan mit dem Namen RecoveryPlan01 für das aktuelle Azure Site Recovery Vault mit dem Cmdlet **Get-AzureSiteRecoveryRecoveryPlan** ab.</span><span class="sxs-lookup"><span data-stu-id="2b8fa-131">This command gets the recovery plan named RecoveryPlan01 for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet.</span></span>
<span data-ttu-id="2b8fa-132">Der Befehl speichert den Plan in der $RecoveryPlan Variablen.</span><span class="sxs-lookup"><span data-stu-id="2b8fa-132">The command stores the plan in the $RecoveryPlan variable.</span></span>

<span data-ttu-id="2b8fa-133">Der zweite Befehl startet den Test-Failover-Vorgang für den in $RecoveryPlan gespeicherten Wiederherstellungsplan und gibt die Richtung des Failovers an.</span><span class="sxs-lookup"><span data-stu-id="2b8fa-133">The second command starts the test failover operation for the recovery plan stored in $RecoveryPlan and specifies the direction of the failover.</span></span>

## <span data-ttu-id="2b8fa-134">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b8fa-134">PARAMETERS</span></span>

### <span data-ttu-id="2b8fa-135">-Richtung</span><span class="sxs-lookup"><span data-stu-id="2b8fa-135">-Direction</span></span>
<span data-ttu-id="2b8fa-136">Gibt die failoverrichtung an.</span><span class="sxs-lookup"><span data-stu-id="2b8fa-136">Specifies the failover direction.</span></span>
<span data-ttu-id="2b8fa-137">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="2b8fa-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2b8fa-138">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="2b8fa-138">PrimaryToRecovery</span></span>
- <span data-ttu-id="2b8fa-139">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="2b8fa-139">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b8fa-140">-LogicalNetworkId</span><span class="sxs-lookup"><span data-stu-id="2b8fa-140">-LogicalNetworkId</span></span>
<span data-ttu-id="2b8fa-141">Gibt die ID des logischen Netzwerks an.</span><span class="sxs-lookup"><span data-stu-id="2b8fa-141">Specifies the ID of the logical network.</span></span>

```yaml
Type: String
Parameter Sets: ByRPIdWithLogicalNetworkID, ByRPObjectWithLogicalNetworkID, ByPEIdWithLogicalNetworkID, ByPEObjectWithLogicalNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b8fa-142">-Netzwerk</span><span class="sxs-lookup"><span data-stu-id="2b8fa-142">-Network</span></span>
<span data-ttu-id="2b8fa-143">Gibt das Netzwerkobjekt an, das für das testfailover verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2b8fa-143">Specifies the network object to use for test failover.</span></span>
<span data-ttu-id="2b8fa-144">Verwenden Sie das Cmdlet " **Get-AzureSiteRecoveryNetwork** ", um ein Netzwerk zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2b8fa-144">To obtain a network, use the **Get-AzureSiteRecoveryNetwork** cmdlet.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByPEId, ByRPId, ByRPIdWithLogicalNetworkID, ByRPIdWithVMNetworkID, ByRPObject, ByRPObjectWithLogicalNetworkID, ByRPObjectWithVMNetworkID, ByPEIdWithLogicalNetworkID, ByPEIdWithVMNetworkID, ByPEObject, ByPEObjectWithLogicalNetworkID, ByPEObjectWithVMNetworkID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: ASRNetwork
Parameter Sets: ByRPIdWithVMNetwork, ByPEObjectWithVMNetwork, ByRPObjectWithVMNetwork, ByPEIdWithVMNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b8fa-145">-NetworkType</span><span class="sxs-lookup"><span data-stu-id="2b8fa-145">-NetworkType</span></span>
<span data-ttu-id="2b8fa-146">Gibt den für das testfailover zu verwendenden Netzwerktyp an.</span><span class="sxs-lookup"><span data-stu-id="2b8fa-146">Specifies the network type to use for test failover.</span></span>
<span data-ttu-id="2b8fa-147">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="2b8fa-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2b8fa-148">Keine</span><span class="sxs-lookup"><span data-stu-id="2b8fa-148">None</span></span>
- <span data-ttu-id="2b8fa-149">Neu</span><span class="sxs-lookup"><span data-stu-id="2b8fa-149">New</span></span>
- <span data-ttu-id="2b8fa-150">Vorhandenen</span><span class="sxs-lookup"><span data-stu-id="2b8fa-150">Existing</span></span>

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

### <span data-ttu-id="2b8fa-151">-Profil</span><span class="sxs-lookup"><span data-stu-id="2b8fa-151">-Profile</span></span>
<span data-ttu-id="2b8fa-152">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="2b8fa-152">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2b8fa-153">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="2b8fa-153">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b8fa-154">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="2b8fa-154">-ProtectionContainerId</span></span>
<span data-ttu-id="2b8fa-155">Gibt die ID eines geschützten Containers an.</span><span class="sxs-lookup"><span data-stu-id="2b8fa-155">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="2b8fa-156">Mit diesem Cmdlet wird der Auftrag für einen geschützten virtuellen Computer gestartet, der zu dem Container gehört, den dieses Cmdlet angibt.</span><span class="sxs-lookup"><span data-stu-id="2b8fa-156">This cmdlet starts the job for a protected virtual machine that belongs to the container that this cmdlet specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId, ByPEIdWithVMNetwork, ByPEIdWithLogicalNetworkID, ByPEIdWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b8fa-157">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="2b8fa-157">-ProtectionEntity</span></span>
<span data-ttu-id="2b8fa-158">Gibt das Entitätsobjekt für den Standort Wiederherstellungs Schutz an.</span><span class="sxs-lookup"><span data-stu-id="2b8fa-158">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObjectWithVMNetwork, ByPEObjectWithLogicalNetworkID, ByPEObjectWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b8fa-159">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="2b8fa-159">-ProtectionEntityId</span></span>
<span data-ttu-id="2b8fa-160">Gibt die ID eines geschützten virtuellen Computers an, für den der Auftrag gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2b8fa-160">Specifies the ID of a protected virtual machine for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId, ByPEIdWithVMNetwork, ByPEIdWithLogicalNetworkID, ByPEIdWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b8fa-161">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2b8fa-161">-RecoveryPlan</span></span>
<span data-ttu-id="2b8fa-162">Gibt einen Wiederherstellungsplan an, für den der Auftrag gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2b8fa-162">Specifies a recovery plan for which to start the job.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObjectWithVMNetwork, ByRPObjectWithLogicalNetworkID, ByRPObjectWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b8fa-163">-RpId</span><span class="sxs-lookup"><span data-stu-id="2b8fa-163">-RpId</span></span>
<span data-ttu-id="2b8fa-164">Gibt die ID eines Wiederherstellungsplans an, für den der Auftrag gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2b8fa-164">Specifies the ID of a recovery plan for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByRPId, ByRPIdWithLogicalNetworkID, ByRPIdWithVMNetworkID, ByRPIdWithVMNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b8fa-165">-VmNetworkId</span><span class="sxs-lookup"><span data-stu-id="2b8fa-165">-VmNetworkId</span></span>
<span data-ttu-id="2b8fa-166">Gibt die ID des virtuellen Computernetzwerks an.</span><span class="sxs-lookup"><span data-stu-id="2b8fa-166">Specifies the ID of the virtual machine network.</span></span>

```yaml
Type: String
Parameter Sets: ByRPIdWithVMNetworkID, ByRPObjectWithVMNetworkID, ByPEIdWithVMNetworkID, ByPEObjectWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b8fa-167">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="2b8fa-167">-WaitForCompletion</span></span>
<span data-ttu-id="2b8fa-168">Gibt an, dass das Cmdlet wartet, bis der Vorgang abgeschlossen ist, bevor es die Steuerung an die Windows PowerShell-Konsole zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="2b8fa-168">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b8fa-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b8fa-169">CommonParameters</span></span>
<span data-ttu-id="2b8fa-170">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b8fa-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b8fa-171">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b8fa-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b8fa-172">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2b8fa-172">INPUTS</span></span>

## <span data-ttu-id="2b8fa-173">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2b8fa-173">OUTPUTS</span></span>

## <span data-ttu-id="2b8fa-174">Notizen</span><span class="sxs-lookup"><span data-stu-id="2b8fa-174">NOTES</span></span>

## <span data-ttu-id="2b8fa-175">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2b8fa-175">RELATED LINKS</span></span>

[<span data-ttu-id="2b8fa-176">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="2b8fa-176">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="2b8fa-177">Get-AzureSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="2b8fa-177">Get-AzureSiteRecoveryNetwork</span></span>](./Get-AzureSiteRecoveryNetwork.md)

[<span data-ttu-id="2b8fa-178">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="2b8fa-178">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="2b8fa-179">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2b8fa-179">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="2b8fa-180">Anfang-AzureSiteRecoveryUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="2b8fa-180">Start-AzureSiteRecoveryUnplannedFailoverJob</span></span>](./Start-AzureSiteRecoveryUnplannedFailoverJob.md)


