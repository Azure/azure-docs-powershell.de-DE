---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrunplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrUnplannedFailoverJob.md
ms.openlocfilehash: 61bb846067127b8e7d0a4deca0dd9a726d9dd1f0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293159"
---
# <span data-ttu-id="90250-101">Start-AzRecoveryServicesAsrUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="90250-101">Start-AzRecoveryServicesAsrUnplannedFailoverJob</span></span>

## <span data-ttu-id="90250-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90250-102">SYNOPSIS</span></span>
<span data-ttu-id="90250-103">Startet einen nicht geplanten Failovervorgang.</span><span class="sxs-lookup"><span data-stu-id="90250-103">Starts an unplanned failover operation.</span></span>

## <span data-ttu-id="90250-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="90250-104">SYNTAX</span></span>

### <span data-ttu-id="90250-105">ByRPIObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="90250-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90250-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="90250-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90250-107">ByRPIObjectWithRecoveryTag</span><span class="sxs-lookup"><span data-stu-id="90250-107">ByRPIObjectWithRecoveryTag</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] -RecoveryTag <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90250-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="90250-108">DESCRIPTION</span></span>
<span data-ttu-id="90250-109">Das **Cmdlet "Start-AzRecoveryServicesAsrUnplannedFailoverJob"** startet einen nicht geplanten Failover eines geschützten Elements oder Wiederherstellungsplans für die Azure-Websitewiederherstellungsreplikation.</span><span class="sxs-lookup"><span data-stu-id="90250-109">The **Start-AzRecoveryServicesAsrUnplannedFailoverJob** cmdlet starts unplanned failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="90250-110">Sie können mithilfe des Cmdlets "Get-AzRecoveryServicesAsrJob überprüfen, ob der Auftrag erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="90250-110">You can check whether the job succeeded by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="90250-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="90250-111">EXAMPLES</span></span>

### <span data-ttu-id="90250-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="90250-112">Example 1</span></span>
```powershell
PS C:\> $currentJob = Start-AzRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $RecoveryNetwork
```

<span data-ttu-id="90250-113">Startet den nicht geplanten Failovervorgang für den Wiederherstellungsplan mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, der zum Nachverfolgen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="90250-113">Starts the unplanned failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="90250-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="90250-114">Example 2</span></span>

<span data-ttu-id="90250-115">Startet einen nicht geplanten Failovervorgang.</span><span class="sxs-lookup"><span data-stu-id="90250-115">Starts an unplanned failover operation.</span></span> <span data-ttu-id="90250-116">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="90250-116">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Start-AzRecoveryServicesAsrUnplannedFailoverJob -Direction PrimaryToRecovery -RecoveryPoint $rp[0] -ReplicationProtectedItem $ReplicationProtectedItem
```

## <span data-ttu-id="90250-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90250-117">PARAMETERS</span></span>

### <span data-ttu-id="90250-118">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="90250-118">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="90250-119">Gibt den Dateipfad des primären Zertifikats für die Datenverschlüsselung für den Failover des geschützten Elements an.</span><span class="sxs-lookup"><span data-stu-id="90250-119">Specifies the data encryption primary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="90250-120">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="90250-120">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="90250-121">Gibt den Dateipfad des sekundären Zertifikats für die Datenverschlüsselung für den Failover des geschützten Elements an.</span><span class="sxs-lookup"><span data-stu-id="90250-121">Specifies the data encryption secondary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="90250-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90250-122">-DefaultProfile</span></span>
<span data-ttu-id="90250-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="90250-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="90250-124">-Direction</span><span class="sxs-lookup"><span data-stu-id="90250-124">-Direction</span></span>
<span data-ttu-id="90250-125">Gibt die Failoverrichtung an.</span><span class="sxs-lookup"><span data-stu-id="90250-125">Specifies the failover direction.</span></span>
<span data-ttu-id="90250-126">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="90250-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="90250-127">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="90250-127">PrimaryToRecovery</span></span>
- <span data-ttu-id="90250-128">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="90250-128">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="90250-129">-PerformSourceSideAction</span><span class="sxs-lookup"><span data-stu-id="90250-129">-PerformSourceSideAction</span></span>
<span data-ttu-id="90250-130">Führen Sie den Vorgang auf der Quellseite aus, bevor Sie einen ungeplanten Failover starten.</span><span class="sxs-lookup"><span data-stu-id="90250-130">Perform operation in source side before starting unplanned failover.</span></span>

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

### <span data-ttu-id="90250-131">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="90250-131">-RecoveryPlan</span></span>
<span data-ttu-id="90250-132">Gibt ein ASR-Wiederherstellungsplanobjekt an.</span><span class="sxs-lookup"><span data-stu-id="90250-132">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="90250-133">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="90250-133">-RecoveryPoint</span></span>
<span data-ttu-id="90250-134">Gibt einen benutzerdefinierten Wiederherstellungspunkt für den Failover des geschützten Computers an.</span><span class="sxs-lookup"><span data-stu-id="90250-134">Specifies a custom recovery point to failover the protected machine to.</span></span>

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

### <span data-ttu-id="90250-135">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="90250-135">-RecoveryTag</span></span>
<span data-ttu-id="90250-136">Gibt das Wiederherstellungstag für den Failover an.</span><span class="sxs-lookup"><span data-stu-id="90250-136">Specifies the recovery tag to failover to.</span></span>

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

### <span data-ttu-id="90250-137">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="90250-137">-ReplicationProtectedItem</span></span>
<span data-ttu-id="90250-138">Gibt ein geschütztes Element für die Azure-Websitewiederherstellungsreplikation an.</span><span class="sxs-lookup"><span data-stu-id="90250-138">Specifies an azure site recovery replication protected item.</span></span>

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

### <span data-ttu-id="90250-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="90250-139">-Confirm</span></span>
<span data-ttu-id="90250-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="90250-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90250-141">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="90250-141">-WhatIf</span></span>
<span data-ttu-id="90250-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="90250-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90250-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="90250-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90250-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90250-144">CommonParameters</span></span>
<span data-ttu-id="90250-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90250-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90250-146">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="90250-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90250-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="90250-147">INPUTS</span></span>

### <span data-ttu-id="90250-148">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="90250-148">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="90250-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="90250-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="90250-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="90250-150">OUTPUTS</span></span>

### <span data-ttu-id="90250-151">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="90250-151">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="90250-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="90250-152">NOTES</span></span>

## <span data-ttu-id="90250-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="90250-153">RELATED LINKS</span></span>

[<span data-ttu-id="90250-154">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="90250-154">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)
