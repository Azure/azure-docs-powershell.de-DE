---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: AC73119B-BB76-425B-AA44-44502028ECC4
online version: ''
schema: 2.0.0
ms.openlocfilehash: a74a02f219b5bb64957ab919168cb79ccf681869
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006012"
---
# <span data-ttu-id="e9bba-101">Start-AzureSiteRecoveryUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="e9bba-101">Start-AzureSiteRecoveryUnplannedFailoverJob</span></span>

## <span data-ttu-id="e9bba-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e9bba-102">SYNOPSIS</span></span>
<span data-ttu-id="e9bba-103">Startet das ungeplante Failover für eine Standort Wiederherstellungs Schutzeinheit oder einen Wiederherstellungsplan.</span><span class="sxs-lookup"><span data-stu-id="e9bba-103">Starts the unplanned failover for a Site Recovery protection entity or recovery plan.</span></span>

## <span data-ttu-id="e9bba-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9bba-104">SYNTAX</span></span>

### <span data-ttu-id="e9bba-105">ByRPId (Standard)</span><span class="sxs-lookup"><span data-stu-id="e9bba-105">ByRPId (Default)</span></span>
```
Start-AzureSiteRecoveryUnplannedFailoverJob -RPId <String> -Direction <String> [-PrimaryAction <Boolean>]
 [-PerformSourceSideActions] [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e9bba-106">ByPEId</span><span class="sxs-lookup"><span data-stu-id="e9bba-106">ByPEId</span></span>
```
Start-AzureSiteRecoveryUnplannedFailoverJob -ProtectionEntityId <String> -ProtectionContainerId <String>
 -Direction <String> [-PerformSourceSiteOperations <Boolean>] [-PerformSourceSideActions] [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e9bba-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="e9bba-107">ByRPObject</span></span>
```
Start-AzureSiteRecoveryUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PrimaryAction <Boolean>] [-PerformSourceSideActions] [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="e9bba-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="e9bba-108">ByPEObject</span></span>
```
Start-AzureSiteRecoveryUnplannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-PerformSourceSiteOperations <Boolean>] [-PerformSourceSideActions] [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e9bba-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e9bba-109">DESCRIPTION</span></span>
<span data-ttu-id="e9bba-110">Mit dem Cmdlet **Start-AzureSiteRecoveryUnplannedFailoverJob** wird das ungeplante Failover einer Azure Site Recovery Protection-Entität oder eines Wiederherstellungsplans gestartet.</span><span class="sxs-lookup"><span data-stu-id="e9bba-110">The **Start-AzureSiteRecoveryUnplannedFailoverJob** cmdlet starts the unplanned failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="e9bba-111">Mit dem Cmdlet **Get-AzureSiteRecoveryJob** können Sie überprüfen, ob der Auftrag erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="e9bba-111">You can check whether the job succeeds by using the **Get-AzureSiteRecoveryJob** cmdlet.</span></span>

## <span data-ttu-id="e9bba-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e9bba-112">EXAMPLES</span></span>

### <span data-ttu-id="e9bba-113">Beispiel 1: Starten eines ungeplanten Failover-Auftrags</span><span class="sxs-lookup"><span data-stu-id="e9bba-113">Example 1: Start an unplanned failover job</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer
PS C:\> $ProtectionEntity = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $ProtectionContainer 
PS C:\> Start-AzureSiteRecoveryUnplannedFailoverJob -ProtectionEntity $ProtectionEntity -Direction "PrimaryToRecovery"
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

<span data-ttu-id="e9bba-114">Der erste Befehl ruft einen geschützten Container mit dem Cmdlet **Get-AzureSiteRecoveryProtectionContainer** ab und speichert ihn dann in der $ProtectionContainer-Variablen.</span><span class="sxs-lookup"><span data-stu-id="e9bba-114">The first command gets a protected container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="e9bba-115">Der zweite Befehl ruft die geschützten Entitäten ab, die zu dem in $ProtectionContainer gespeicherten geschützten Container gehören, indem Sie das Cmdlet " **Get-AzureSiteRecoveryProtectionEntity** " verwenden.</span><span class="sxs-lookup"><span data-stu-id="e9bba-115">The second command gets the protected entities that belong to the protected container stored in $ProtectionContainer by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="e9bba-116">Der Befehl speichert die Ergebnisse in der $ProtectionEntity-Variablen.</span><span class="sxs-lookup"><span data-stu-id="e9bba-116">The command stores the results in the $ProtectionEntity variable.</span></span>

<span data-ttu-id="e9bba-117">Der letzte Befehl startet das Failover für die geschützten Entitäten, die in $ProtectionEntity gespeichert sind, und gibt die Richtung des Failovers an.</span><span class="sxs-lookup"><span data-stu-id="e9bba-117">The final command starts the failover for the protected entities stored in $ProtectionEntity and specifies the direction of the failover.</span></span>

## <span data-ttu-id="e9bba-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9bba-118">PARAMETERS</span></span>

### <span data-ttu-id="e9bba-119">-Richtung</span><span class="sxs-lookup"><span data-stu-id="e9bba-119">-Direction</span></span>
<span data-ttu-id="e9bba-120">Gibt die Richtung des Failovers an.</span><span class="sxs-lookup"><span data-stu-id="e9bba-120">Specifies the direction of the failover.</span></span>
<span data-ttu-id="e9bba-121">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e9bba-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e9bba-122">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="e9bba-122">PrimaryToRecovery</span></span>
- <span data-ttu-id="e9bba-123">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="e9bba-123">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="e9bba-124">-PerformSourceSideActions</span><span class="sxs-lookup"><span data-stu-id="e9bba-124">-PerformSourceSideActions</span></span>
<span data-ttu-id="e9bba-125">Gibt an, dass die Aktion quellseitige Aktionen ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="e9bba-125">Indicates that the action can perform source side actions.</span></span>

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

### <span data-ttu-id="e9bba-126">-PerformSourceSiteOperations</span><span class="sxs-lookup"><span data-stu-id="e9bba-126">-PerformSourceSiteOperations</span></span>
<span data-ttu-id="e9bba-127">Gibt an, dass Quellwebsite Vorgänge ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="e9bba-127">Indicates that source site operations can be performed.</span></span>

```yaml
Type: Boolean
Parameter Sets: ByPEId, ByPEObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9bba-128">-Primary</span><span class="sxs-lookup"><span data-stu-id="e9bba-128">-PrimaryAction</span></span>
<span data-ttu-id="e9bba-129">Gibt an, dass primäre Websiteaktionen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="e9bba-129">Indicates that  primary site actions are required.</span></span>

```yaml
Type: Boolean
Parameter Sets: ByRPId, ByRPObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9bba-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="e9bba-130">-Profile</span></span>
<span data-ttu-id="e9bba-131">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="e9bba-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e9bba-132">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="e9bba-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e9bba-133">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="e9bba-133">-ProtectionContainerId</span></span>
<span data-ttu-id="e9bba-134">Gibt die ID eines geschützten Containers an.</span><span class="sxs-lookup"><span data-stu-id="e9bba-134">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="e9bba-135">Mit diesem Cmdlet wird der Auftrag für einen geschützten virtuellen Computer gestartet, der zu dem Container gehört, den dieses Cmdlet angibt.</span><span class="sxs-lookup"><span data-stu-id="e9bba-135">This cmdlet starts the job for a protected virtual machine that belongs to the container that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="e9bba-136">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="e9bba-136">-ProtectionEntity</span></span>
<span data-ttu-id="e9bba-137">Gibt das Entitätsobjekt für den Standort Wiederherstellungs Schutz an.</span><span class="sxs-lookup"><span data-stu-id="e9bba-137">Specifies the Site Recovery protection entity object.</span></span>

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

### <span data-ttu-id="e9bba-138">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="e9bba-138">-ProtectionEntityId</span></span>
<span data-ttu-id="e9bba-139">Gibt die ID eines geschützten virtuellen Computers an, für den der Auftrag gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9bba-139">Specifies the ID of a protected virtual machine for which to start the job.</span></span>

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

### <span data-ttu-id="e9bba-140">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e9bba-140">-RecoveryPlan</span></span>
<span data-ttu-id="e9bba-141">Gibt ein Wiederherstellungsplan-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="e9bba-141">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="e9bba-142">-RPId</span><span class="sxs-lookup"><span data-stu-id="e9bba-142">-RPId</span></span>
<span data-ttu-id="e9bba-143">Gibt die ID eines Wiederherstellungsplans an, für den der Auftrag gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9bba-143">Specifies the ID of a recovery plan for which to start the job.</span></span>

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

### <span data-ttu-id="e9bba-144">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="e9bba-144">-WaitForCompletion</span></span>
<span data-ttu-id="e9bba-145">Gibt an, dass das Cmdlet wartet, bis der Vorgang abgeschlossen ist, bevor es die Steuerung an die Windows PowerShell-Konsole zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="e9bba-145">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="e9bba-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9bba-146">CommonParameters</span></span>
<span data-ttu-id="e9bba-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9bba-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9bba-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9bba-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9bba-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e9bba-149">INPUTS</span></span>

## <span data-ttu-id="e9bba-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e9bba-150">OUTPUTS</span></span>

## <span data-ttu-id="e9bba-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="e9bba-151">NOTES</span></span>

## <span data-ttu-id="e9bba-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e9bba-152">RELATED LINKS</span></span>

[<span data-ttu-id="e9bba-153">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="e9bba-153">Get-AzureSiteRecoveryJob</span></span>](./Get-AzureSiteRecoveryJob.md)

[<span data-ttu-id="e9bba-154">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="e9bba-154">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="e9bba-155">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="e9bba-155">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="e9bba-156">Anfang-AzureSiteRecoveryTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="e9bba-156">Start-AzureSiteRecoveryTestFailoverJob</span></span>](./Start-AzureSiteRecoveryTestFailoverJob.md)


