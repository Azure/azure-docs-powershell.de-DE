---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrunplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
ms.openlocfilehash: b7a9dffe443ca7603b8b5a3bdd100560d83a498e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477773"
---
# <span data-ttu-id="b919e-101">Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="b919e-101">Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob</span></span>

## <span data-ttu-id="b919e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b919e-102">SYNOPSIS</span></span>
<span data-ttu-id="b919e-103">Startet einen ungeplanten Failover-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="b919e-103">Starts a unplanned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b919e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b919e-104">SYNTAX</span></span>

### <span data-ttu-id="b919e-105">ByRPIObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="b919e-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b919e-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="b919e-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b919e-107">ByRPIObjectWithRecoveryTag</span><span class="sxs-lookup"><span data-stu-id="b919e-107">ByRPIObjectWithRecoveryTag</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] -RecoveryTag <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b919e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b919e-108">DESCRIPTION</span></span>
<span data-ttu-id="b919e-109">Das Cmdlet **Start-AzureRmRecoveryServicesAsrTestFailoverJob** startet das Test-Failover für ein geschütztes Element oder einen Wiederherstellungsplan der Azure Site Recovery-Replikation.</span><span class="sxs-lookup"><span data-stu-id="b919e-109">The **Start-AzureRmRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="b919e-110">Mithilfe des Get-AzureRmRecoveryServicesAsrJob-Cmdlets können Sie überprüfen, ob der Auftrag erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="b919e-110">You can check whether the job succeeded by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="b919e-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b919e-111">EXAMPLES</span></span>

### <span data-ttu-id="b919e-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b919e-112">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="b919e-113">Startet den Test-Failover-Vorgang für den Wiederherstellungsplan mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b919e-113">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="b919e-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="b919e-114">PARAMETERS</span></span>

### <span data-ttu-id="b919e-115">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="b919e-115">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="b919e-116">Gibt den Datei Pfad für das primäre Daten Verschlüsselungszertifikat für das Failover eines geschützten Elements an.</span><span class="sxs-lookup"><span data-stu-id="b919e-116">Specifies the data encryption primary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="b919e-117">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="b919e-117">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="b919e-118">Gibt den Pfad der Daten Verschlüsselungs sekundären Zertifikatsdatei für das Failover des geschützten Elements an.</span><span class="sxs-lookup"><span data-stu-id="b919e-118">Specifies the data encryption secondary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="b919e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b919e-119">-DefaultProfile</span></span>
<span data-ttu-id="b919e-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b919e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="b919e-121">-Richtung</span><span class="sxs-lookup"><span data-stu-id="b919e-121">-Direction</span></span>
<span data-ttu-id="b919e-122">Gibt die failoverrichtung an.</span><span class="sxs-lookup"><span data-stu-id="b919e-122">Specifies the failover direction.</span></span>
<span data-ttu-id="b919e-123">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b919e-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b919e-124">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="b919e-124">PrimaryToRecovery</span></span>
- <span data-ttu-id="b919e-125">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="b919e-125">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="b919e-126">-PerformSourceSideAction</span><span class="sxs-lookup"><span data-stu-id="b919e-126">-PerformSourceSideAction</span></span>
<span data-ttu-id="b919e-127">Führen Sie den Vorgang auf der Quellseite aus, bevor Sie das ungeplante Failover starten.</span><span class="sxs-lookup"><span data-stu-id="b919e-127">Perform operation in source side before starting unplanned failover.</span></span>

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

### <span data-ttu-id="b919e-128">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b919e-128">-RecoveryPlan</span></span>
<span data-ttu-id="b919e-129">Gibt ein ASR-Wiederherstellungsplan-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="b919e-129">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="b919e-130">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="b919e-130">-RecoveryPoint</span></span>
<span data-ttu-id="b919e-131">Gibt einen benutzerdefinierten Wiederherstellungspunkt für das Failover des geschützten Computers an.</span><span class="sxs-lookup"><span data-stu-id="b919e-131">Specifies a custom recovery point to failover the protected machine to.</span></span>

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

### <span data-ttu-id="b919e-132">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="b919e-132">-RecoveryTag</span></span>
<span data-ttu-id="b919e-133">Gibt das Wiederherstellungs für Failover an an.</span><span class="sxs-lookup"><span data-stu-id="b919e-133">Specifies the recovery tag to failover to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPObject
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent, Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent

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
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent, Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b919e-134">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b919e-134">-ReplicationProtectedItem</span></span>
<span data-ttu-id="b919e-135">Gibt ein geschütztes Element der Azure Site Recovery-Replikation an.</span><span class="sxs-lookup"><span data-stu-id="b919e-135">Specifies an azure site recovery replication protected item.</span></span>

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

### <span data-ttu-id="b919e-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b919e-136">-Confirm</span></span>
<span data-ttu-id="b919e-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b919e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b919e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b919e-138">-WhatIf</span></span>
<span data-ttu-id="b919e-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b919e-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b919e-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b919e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b919e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b919e-141">CommonParameters</span></span>
<span data-ttu-id="b919e-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b919e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b919e-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b919e-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b919e-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b919e-144">INPUTS</span></span>

### <span data-ttu-id="b919e-145">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b919e-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="b919e-146">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b919e-146">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="b919e-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b919e-147">OUTPUTS</span></span>

### <span data-ttu-id="b919e-148">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="b919e-148">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b919e-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="b919e-149">NOTES</span></span>

## <span data-ttu-id="b919e-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b919e-150">RELATED LINKS</span></span>

[<span data-ttu-id="b919e-151">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="b919e-151">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)
