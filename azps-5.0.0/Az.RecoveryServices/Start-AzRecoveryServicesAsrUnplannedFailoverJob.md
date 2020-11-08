---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrunplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrUnplannedFailoverJob.md
ms.openlocfilehash: 61bb846067127b8e7d0a4deca0dd9a726d9dd1f0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176125"
---
# <span data-ttu-id="d2f28-101">Start-AzRecoveryServicesAsrUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="d2f28-101">Start-AzRecoveryServicesAsrUnplannedFailoverJob</span></span>

## <span data-ttu-id="d2f28-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d2f28-102">SYNOPSIS</span></span>
<span data-ttu-id="d2f28-103">Startet einen ungeplanten Failover-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="d2f28-103">Starts an unplanned failover operation.</span></span>

## <span data-ttu-id="d2f28-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2f28-104">SYNTAX</span></span>

### <span data-ttu-id="d2f28-105">ByRPIObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="d2f28-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2f28-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="d2f28-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2f28-107">ByRPIObjectWithRecoveryTag</span><span class="sxs-lookup"><span data-stu-id="d2f28-107">ByRPIObjectWithRecoveryTag</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] -RecoveryTag <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2f28-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d2f28-108">DESCRIPTION</span></span>
<span data-ttu-id="d2f28-109">Das Cmdlet **Start-AzRecoveryServicesAsrUnplannedFailoverJob** startet ein ungeplantes Failover für ein geschütztes Element oder einen Wiederherstellungsplan der Azure Site Recovery-Replikation.</span><span class="sxs-lookup"><span data-stu-id="d2f28-109">The **Start-AzRecoveryServicesAsrUnplannedFailoverJob** cmdlet starts unplanned failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="d2f28-110">Mithilfe des Get-AzRecoveryServicesAsrJob-Cmdlets können Sie überprüfen, ob der Auftrag erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="d2f28-110">You can check whether the job succeeded by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="d2f28-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d2f28-111">EXAMPLES</span></span>

### <span data-ttu-id="d2f28-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d2f28-112">Example 1</span></span>
```powershell
PS C:\> $currentJob = Start-AzRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $RecoveryNetwork
```

<span data-ttu-id="d2f28-113">Startet den ungeplanten Failover-Vorgang für den Wiederherstellungsplan mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d2f28-113">Starts the unplanned failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="d2f28-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d2f28-114">Example 2</span></span>

<span data-ttu-id="d2f28-115">Startet einen ungeplanten Failover-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="d2f28-115">Starts an unplanned failover operation.</span></span> <span data-ttu-id="d2f28-116">automatisch</span><span class="sxs-lookup"><span data-stu-id="d2f28-116">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Start-AzRecoveryServicesAsrUnplannedFailoverJob -Direction PrimaryToRecovery -RecoveryPoint $rp[0] -ReplicationProtectedItem $ReplicationProtectedItem
```

## <span data-ttu-id="d2f28-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2f28-117">PARAMETERS</span></span>

### <span data-ttu-id="d2f28-118">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="d2f28-118">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="d2f28-119">Gibt den Datei Pfad für das primäre Daten Verschlüsselungszertifikat für das Failover eines geschützten Elements an.</span><span class="sxs-lookup"><span data-stu-id="d2f28-119">Specifies the data encryption primary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="d2f28-120">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="d2f28-120">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="d2f28-121">Gibt den Pfad der Daten Verschlüsselungs sekundären Zertifikatsdatei für das Failover des geschützten Elements an.</span><span class="sxs-lookup"><span data-stu-id="d2f28-121">Specifies the data encryption secondary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="d2f28-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2f28-122">-DefaultProfile</span></span>
<span data-ttu-id="d2f28-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d2f28-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d2f28-124">-Richtung</span><span class="sxs-lookup"><span data-stu-id="d2f28-124">-Direction</span></span>
<span data-ttu-id="d2f28-125">Gibt die failoverrichtung an.</span><span class="sxs-lookup"><span data-stu-id="d2f28-125">Specifies the failover direction.</span></span>
<span data-ttu-id="d2f28-126">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d2f28-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d2f28-127">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="d2f28-127">PrimaryToRecovery</span></span>
- <span data-ttu-id="d2f28-128">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="d2f28-128">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="d2f28-129">-PerformSourceSideAction</span><span class="sxs-lookup"><span data-stu-id="d2f28-129">-PerformSourceSideAction</span></span>
<span data-ttu-id="d2f28-130">Führen Sie den Vorgang auf der Quellseite aus, bevor Sie das ungeplante Failover starten.</span><span class="sxs-lookup"><span data-stu-id="d2f28-130">Perform operation in source side before starting unplanned failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: PerformSourceSideActions

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2f28-131">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d2f28-131">-RecoveryPlan</span></span>
<span data-ttu-id="d2f28-132">Gibt ein ASR-Wiederherstellungsplan-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="d2f28-132">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2f28-133">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="d2f28-133">-RecoveryPoint</span></span>
<span data-ttu-id="d2f28-134">Gibt einen benutzerdefinierten Wiederherstellungspunkt für das Failover des geschützten Computers an.</span><span class="sxs-lookup"><span data-stu-id="d2f28-134">Specifies a custom recovery point to failover the protected machine to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint
Parameter Sets: ByRPIObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2f28-135">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="d2f28-135">-RecoveryTag</span></span>
<span data-ttu-id="d2f28-136">Gibt das Wiederherstellungs für Failover an an.</span><span class="sxs-lookup"><span data-stu-id="d2f28-136">Specifies the recovery tag to failover to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPObject
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByRPIObjectWithRecoveryTag
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2f28-137">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d2f28-137">-ReplicationProtectedItem</span></span>
<span data-ttu-id="d2f28-138">Gibt ein geschütztes Element der Azure Site Recovery-Replikation an.</span><span class="sxs-lookup"><span data-stu-id="d2f28-138">Specifies an azure site recovery replication protected item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithRecoveryTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2f28-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d2f28-139">-Confirm</span></span>
<span data-ttu-id="d2f28-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d2f28-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2f28-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2f28-141">-WhatIf</span></span>
<span data-ttu-id="d2f28-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d2f28-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d2f28-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d2f28-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2f28-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2f28-144">CommonParameters</span></span>
<span data-ttu-id="d2f28-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2f28-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2f28-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2f28-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2f28-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d2f28-147">INPUTS</span></span>

### <span data-ttu-id="d2f28-148">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d2f28-148">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="d2f28-149">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d2f28-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="d2f28-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d2f28-150">OUTPUTS</span></span>

### <span data-ttu-id="d2f28-151">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d2f28-151">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d2f28-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="d2f28-152">NOTES</span></span>

## <span data-ttu-id="d2f28-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d2f28-153">RELATED LINKS</span></span>

[<span data-ttu-id="d2f28-154">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="d2f28-154">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)
