---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2575F5C4-A276-49CE-AB0C-726F359DA6F9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7f71138e47c851097fe36ca294784fc571b6369f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005957"
---
# <span data-ttu-id="c7c97-101">Start-AzureSiteRecoveryPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="c7c97-101">Start-AzureSiteRecoveryPlannedFailoverJob</span></span>

## <span data-ttu-id="c7c97-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c7c97-102">SYNOPSIS</span></span>
<span data-ttu-id="c7c97-103">Startet einen geplanten Failover-Vorgang für eine Websitewiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="c7c97-103">Starts a Site Recovery planned failover operation.</span></span>

## <span data-ttu-id="c7c97-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7c97-104">SYNTAX</span></span>

### <span data-ttu-id="c7c97-105">ByRPId (Standard)</span><span class="sxs-lookup"><span data-stu-id="c7c97-105">ByRPId (Default)</span></span>
```
Start-AzureSiteRecoveryPlannedFailoverJob -RPId <String> -Direction <String> [-WaitForCompletion]
 [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c7c97-106">ByPEId</span><span class="sxs-lookup"><span data-stu-id="c7c97-106">ByPEId</span></span>
```
Start-AzureSiteRecoveryPlannedFailoverJob -ProtectionEntityId <String> -ProtectionContainerId <String>
 -Direction <String> [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c7c97-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="c7c97-107">ByRPObject</span></span>
```
Start-AzureSiteRecoveryPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c7c97-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="c7c97-108">ByPEObject</span></span>
```
Start-AzureSiteRecoveryPlannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c7c97-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c7c97-109">DESCRIPTION</span></span>
<span data-ttu-id="c7c97-110">Das Cmdlet **Start-AzureSiteRecoveryPlannedFailoverJob** startet ein Geplantes Failover für eine Azure Site Recovery Protection-Entität oder einen Wiederherstellungsplan.</span><span class="sxs-lookup"><span data-stu-id="c7c97-110">The **Start-AzureSiteRecoveryPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="c7c97-111">Mit dem Cmdlet **Get-AzureSiteRecoveryJob** können Sie überprüfen, ob der Auftrag erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="c7c97-111">You can check whether the job succeeds by using the **Get-AzureSiteRecoveryJob** cmdlet.</span></span>

## <span data-ttu-id="c7c97-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c7c97-112">EXAMPLES</span></span>

### <span data-ttu-id="c7c97-113">Beispiel 1: Starten eines geplanten Failover-Auftrags</span><span class="sxs-lookup"><span data-stu-id="c7c97-113">Example 1: Start a planned failover job</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer 
PS C:\> $Protected = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container 
PS C:\> Start-AzureSiteRecoveryPlannedFailoverJob -Direction PrimaryToRecovery -ProtectionEntity $Protected -Optimize ForDowntime
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

<span data-ttu-id="c7c97-114">Der erste Befehl ruft alle geschützten Container im aktuellen Azure Site Recovery Vault mit dem Cmdlet **Get-AzureSiteRecoveryProtectionContainer** ab und speichert die Ergebnisse dann in der $Container Variablen.</span><span class="sxs-lookup"><span data-stu-id="c7c97-114">The first command gets all protected containers in the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores the results in the $Container variable.</span></span>
<span data-ttu-id="c7c97-115">In diesem Beispiel ist ein einzelner Container vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c7c97-115">In this example, there is a single container.</span></span>

<span data-ttu-id="c7c97-116">Der zweite Befehl ruft die geschützten virtuellen Computer ab, die zu dem in $Container gespeicherten Container gehören, indem Sie das Cmdlet " **Get-AzureSiteRecoveryProtectionEntity** " verwenden.</span><span class="sxs-lookup"><span data-stu-id="c7c97-116">The second command gets the protected virtual machines that belong to the container stored in $Container by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="c7c97-117">Der Befehl speichert die Ergebnisse in der $protected-Variablen.</span><span class="sxs-lookup"><span data-stu-id="c7c97-117">The command stores the results in the $Protected variable.</span></span>

<span data-ttu-id="c7c97-118">Der endgültige Befehl startet den Failover-Auftrag in Richtung PrimaryToRecovery für die geschützten virtuellen Computer, die in $Protected gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="c7c97-118">The final command starts the failover job in the direction PrimaryToRecovery for the protected virtual machines stored in $Protected.</span></span>

## <span data-ttu-id="c7c97-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7c97-119">PARAMETERS</span></span>

### <span data-ttu-id="c7c97-120">-Richtung</span><span class="sxs-lookup"><span data-stu-id="c7c97-120">-Direction</span></span>
<span data-ttu-id="c7c97-121">Gibt die Richtung des Failovers an.</span><span class="sxs-lookup"><span data-stu-id="c7c97-121">Specifies the direction of the failover.</span></span>
<span data-ttu-id="c7c97-122">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c7c97-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c7c97-123">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="c7c97-123">PrimaryToRecovery</span></span>
- <span data-ttu-id="c7c97-124">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="c7c97-124">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="c7c97-125">-Optimieren</span><span class="sxs-lookup"><span data-stu-id="c7c97-125">-Optimize</span></span>
<span data-ttu-id="c7c97-126">Gibt an, was optimiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c7c97-126">Specifies what to optimize for.</span></span>
<span data-ttu-id="c7c97-127">Dieser Parameter gilt für Failover von einer Azure-Website zu einer lokalen Website, für die eine signifikante Datensynchronisierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c7c97-127">This parameter applies for failover from an Azure site to an on-premise site which requires a significant data synchronization.</span></span>
<span data-ttu-id="c7c97-128">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c7c97-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c7c97-129">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="c7c97-129">ForDowntime</span></span>
- <span data-ttu-id="c7c97-130">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="c7c97-130">ForSynchronization</span></span>

<span data-ttu-id="c7c97-131">Wenn **ForDowntime** angegeben wird, bedeutet dies, dass Daten vor dem Failover synchronisiert werden, um die Ausfallzeit zu minimieren.</span><span class="sxs-lookup"><span data-stu-id="c7c97-131">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="c7c97-132">Die Synchronisierung wird ausgeführt, ohne den virtuellen Computer herunterzufahren.</span><span class="sxs-lookup"><span data-stu-id="c7c97-132">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="c7c97-133">Nach Abschluss der Synchronisierung wird der Auftrag angehalten.</span><span class="sxs-lookup"><span data-stu-id="c7c97-133">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="c7c97-134">Setzen Sie den Auftrag fort, um einen zusätzlichen Synchronisierungsvorgang auszuführen, der den virtuellen Computer herunterfährt.</span><span class="sxs-lookup"><span data-stu-id="c7c97-134">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="c7c97-135">Wenn **ForSynchronization** angegeben wird, bedeutet dies, dass Daten während des Failovers nur synchronisiert werden, damit die Datensynchronisierung minimiert wird.</span><span class="sxs-lookup"><span data-stu-id="c7c97-135">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="c7c97-136">Da diese Einstellung aktiviert ist, wird der virtuelle Computer sofort heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="c7c97-136">Because this setting is enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="c7c97-137">Die Synchronisierung beginnt nach dem Herunterfahren, um den Failovervorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="c7c97-137">Synchronization starts after shutdown to complete the failover operation.</span></span>

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

### <span data-ttu-id="c7c97-138">-Profil</span><span class="sxs-lookup"><span data-stu-id="c7c97-138">-Profile</span></span>
<span data-ttu-id="c7c97-139">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="c7c97-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c7c97-140">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="c7c97-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c7c97-141">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="c7c97-141">-ProtectionContainerId</span></span>
<span data-ttu-id="c7c97-142">Gibt die ID des geschützten Containers an, für den der Auftrag gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c7c97-142">Specifies the ID of the protected container for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7c97-143">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="c7c97-143">-ProtectionEntity</span></span>
<span data-ttu-id="c7c97-144">Gibt das Entitätsobjekt für den Standort Wiederherstellungs Schutz an.</span><span class="sxs-lookup"><span data-stu-id="c7c97-144">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7c97-145">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="c7c97-145">-ProtectionEntityId</span></span>
<span data-ttu-id="c7c97-146">Gibt ein **ASRProtectionEntity** -Objekt an, für das der Auftrag gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c7c97-146">Specifies an **ASRProtectionEntity** object for which to start the job.</span></span>
<span data-ttu-id="c7c97-147">Verwenden Sie das Cmdlet **Get-AzureSiteRecoveryProtectionEntity** , um ein **ASRProtectionEntity** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c7c97-147">To obtain an **ASRProtectionEntity** object, use the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7c97-148">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c7c97-148">-RecoveryPlan</span></span>
<span data-ttu-id="c7c97-149">Gibt ein Wiederherstellungsplan-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="c7c97-149">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="c7c97-150">-RPId</span><span class="sxs-lookup"><span data-stu-id="c7c97-150">-RPId</span></span>
<span data-ttu-id="c7c97-151">Gibt die ID eines Wiederherstellungsplans an, für den der Auftrag gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c7c97-151">Specifies the ID of a recovery plan for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByRPId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7c97-152">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="c7c97-152">-WaitForCompletion</span></span>
<span data-ttu-id="c7c97-153">Gibt an, dass das Cmdlet wartet, bis der Vorgang abgeschlossen ist, bevor es die Steuerung an die Windows PowerShell-Konsole zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="c7c97-153">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="c7c97-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7c97-154">CommonParameters</span></span>
<span data-ttu-id="c7c97-155">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7c97-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7c97-156">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7c97-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7c97-157">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c7c97-157">INPUTS</span></span>

## <span data-ttu-id="c7c97-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c7c97-158">OUTPUTS</span></span>

## <span data-ttu-id="c7c97-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="c7c97-159">NOTES</span></span>

## <span data-ttu-id="c7c97-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c7c97-160">RELATED LINKS</span></span>

[<span data-ttu-id="c7c97-161">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="c7c97-161">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="c7c97-162">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="c7c97-162">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)


