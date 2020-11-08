---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 44A22B6C-5FD4-43B0-9726-71E28AE53E9D
online version: ''
schema: 2.0.0
ms.openlocfilehash: de1b7a24c1af362297319d0297ce356b00ef9d49
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005984"
---
# <span data-ttu-id="f2d9b-101">Start-AzureSiteRecoveryCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="f2d9b-101">Start-AzureSiteRecoveryCommitFailoverJob</span></span>

## <span data-ttu-id="f2d9b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f2d9b-102">SYNOPSIS</span></span>
<span data-ttu-id="f2d9b-103">Startet die Commit-Failover-Aktion für ein Website Wiederherstellungs Objekt.</span><span class="sxs-lookup"><span data-stu-id="f2d9b-103">Starts the commit failover action for a Site Recovery object.</span></span>

## <span data-ttu-id="f2d9b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2d9b-104">SYNTAX</span></span>

### <span data-ttu-id="f2d9b-105">ByRPId (Standard)</span><span class="sxs-lookup"><span data-stu-id="f2d9b-105">ByRPId (Default)</span></span>
```
Start-AzureSiteRecoveryCommitFailoverJob -RPId <String> [-Direction <String>] [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f2d9b-106">ByPEId</span><span class="sxs-lookup"><span data-stu-id="f2d9b-106">ByPEId</span></span>
```
Start-AzureSiteRecoveryCommitFailoverJob -ProtectionEntityId <String> -ProtectionContainerId <String>
 [-Direction <String>] [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f2d9b-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="f2d9b-107">ByRPObject</span></span>
```
Start-AzureSiteRecoveryCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan> [-Direction <String>]
 [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f2d9b-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="f2d9b-108">ByPEObject</span></span>
```
Start-AzureSiteRecoveryCommitFailoverJob -ProtectionEntity <ASRProtectionEntity> [-Direction <String>]
 [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f2d9b-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f2d9b-109">DESCRIPTION</span></span>
<span data-ttu-id="f2d9b-110">Mit dem Cmdlet " **Start-AzureSiteRecoveryCommitFailoverJob** " wird der Commit-Failoverprozess für ein Azure Site Recovery-Objekt nach einem Failover-Vorgang gestartet.</span><span class="sxs-lookup"><span data-stu-id="f2d9b-110">The **Start-AzureSiteRecoveryCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="f2d9b-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f2d9b-111">EXAMPLES</span></span>

### <span data-ttu-id="f2d9b-112">Beispiel 1: Starten eines Commit-Failover-Auftrags</span><span class="sxs-lookup"><span data-stu-id="f2d9b-112">Example 1: Start a commit failover job</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer 
PS C:\> $Protected = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container 
PS C:\> Start-AzureSiteRecoveryCommitFailoverJob -ProtectionEntity $Protected
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

<span data-ttu-id="f2d9b-113">Der erste Befehl ruft alle geschützten Container für das aktuelle Azure Site Recovery Vault mit dem Cmdlet **Get-AzureSiteRecoveryProtectionContainer** ab und speichert die Ergebnisse dann in der $Container Variablen.</span><span class="sxs-lookup"><span data-stu-id="f2d9b-113">The first command gets all protected containers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores the results in the $Container variable.</span></span>

<span data-ttu-id="f2d9b-114">Der zweite Befehl ruft die geschützten virtuellen Computer ab, die zu dem in $Container gespeicherten Container gehören, indem Sie das Cmdlet " **Get-AzureSiteRecoveryProtectionEntity** " verwenden.</span><span class="sxs-lookup"><span data-stu-id="f2d9b-114">The second command gets the protected virtual machines that belong to the container stored in $Container by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="f2d9b-115">Der Befehl speichert die Ergebnisse in der $protected-Variablen.</span><span class="sxs-lookup"><span data-stu-id="f2d9b-115">The command stores the results in the $Protected variable.</span></span>

<span data-ttu-id="f2d9b-116">Mit dem letzten Befehl wird der Failover-Auftrag für die in $Protected gespeicherten geschützten Objekte gestartet.</span><span class="sxs-lookup"><span data-stu-id="f2d9b-116">The final command starts the failover job for the protected objects stored in $Protected.</span></span>

## <span data-ttu-id="f2d9b-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2d9b-117">PARAMETERS</span></span>

### <span data-ttu-id="f2d9b-118">-Richtung</span><span class="sxs-lookup"><span data-stu-id="f2d9b-118">-Direction</span></span>
<span data-ttu-id="f2d9b-119">Gibt die Richtung des Failovers an.</span><span class="sxs-lookup"><span data-stu-id="f2d9b-119">Specifies the direction of the failover.</span></span>
<span data-ttu-id="f2d9b-120">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f2d9b-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f2d9b-121">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="f2d9b-121">PrimaryToRecovery</span></span>
- <span data-ttu-id="f2d9b-122">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="f2d9b-122">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="f2d9b-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="f2d9b-123">-Profile</span></span>
<span data-ttu-id="f2d9b-124">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="f2d9b-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f2d9b-125">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="f2d9b-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f2d9b-126">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="f2d9b-126">-ProtectionContainerId</span></span>
<span data-ttu-id="f2d9b-127">Gibt die ID eines geschützten Containers an.</span><span class="sxs-lookup"><span data-stu-id="f2d9b-127">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="f2d9b-128">Mit diesem Cmdlet wird der Auftrag für einen geschützten virtuellen Computer gestartet, der zu dem Container gehört, den dieses Cmdlet angibt.</span><span class="sxs-lookup"><span data-stu-id="f2d9b-128">This cmdlet starts the job for a protected virtual machine that belongs to the container that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="f2d9b-129">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="f2d9b-129">-ProtectionEntity</span></span>
<span data-ttu-id="f2d9b-130">Gibt ein **ASRProtectionEntity** -Objekt an, für das der Auftrag gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f2d9b-130">Specifies an **ASRProtectionEntity** object for which to start the job.</span></span>
<span data-ttu-id="f2d9b-131">Verwenden Sie das Cmdlet **Get-AzureSiteRecoveryProtectionEntity** , um ein **ASRProtectionEntity** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f2d9b-131">To obtain an **ASRProtectionEntity** object, use the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>

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

### <span data-ttu-id="f2d9b-132">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="f2d9b-132">-ProtectionEntityId</span></span>
<span data-ttu-id="f2d9b-133">Gibt die ID eines geschützten virtuellen Computers an, für den der Auftrag gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f2d9b-133">Specifies the ID of a protected virtual machine for which to start the job.</span></span>

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

### <span data-ttu-id="f2d9b-134">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f2d9b-134">-RecoveryPlan</span></span>
<span data-ttu-id="f2d9b-135">Gibt ein Wiederherstellungsplan-Objekt an, für das der Auftrag gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f2d9b-135">Specifies a recovery plan object for which to start the job.</span></span>
<span data-ttu-id="f2d9b-136">Verwenden Sie das Cmdlet **Get-AzureSiteRecoveryRecoveryPlan** , um ein **ASRRecoveryPlan** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f2d9b-136">To obtain an **ASRRecoveryPlan** object, use the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet.</span></span>

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

### <span data-ttu-id="f2d9b-137">-RPId</span><span class="sxs-lookup"><span data-stu-id="f2d9b-137">-RPId</span></span>
<span data-ttu-id="f2d9b-138">Gibt die ID eines Wiederherstellungsplans an, für den der Auftrag gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f2d9b-138">Specifies the ID of a recovery plan for which to start the job.</span></span>

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

### <span data-ttu-id="f2d9b-139">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="f2d9b-139">-WaitForCompletion</span></span>
<span data-ttu-id="f2d9b-140">Gibt an, dass das Cmdlet wartet, bis der Vorgang abgeschlossen ist, bevor es die Steuerung an die Windows PowerShell-Konsole zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="f2d9b-140">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="f2d9b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2d9b-141">CommonParameters</span></span>
<span data-ttu-id="f2d9b-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2d9b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2d9b-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2d9b-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2d9b-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f2d9b-144">INPUTS</span></span>

## <span data-ttu-id="f2d9b-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f2d9b-145">OUTPUTS</span></span>

## <span data-ttu-id="f2d9b-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="f2d9b-146">NOTES</span></span>

## <span data-ttu-id="f2d9b-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f2d9b-147">RELATED LINKS</span></span>

[<span data-ttu-id="f2d9b-148">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f2d9b-148">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="f2d9b-149">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="f2d9b-149">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="f2d9b-150">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="f2d9b-150">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)


