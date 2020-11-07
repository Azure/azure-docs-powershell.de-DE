---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrtestfailovercleanupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverCleanupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrTestFailoverCleanupJob.md
ms.openlocfilehash: 24fbbd3d0d9d2e165a2edfbf289b434c886b0b0c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846959"
---
# <span data-ttu-id="7c399-101">Start-AzRecoveryServicesAsrTestFailoverCleanupJob</span><span class="sxs-lookup"><span data-stu-id="7c399-101">Start-AzRecoveryServicesAsrTestFailoverCleanupJob</span></span>

## <span data-ttu-id="7c399-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7c399-102">SYNOPSIS</span></span>
<span data-ttu-id="7c399-103">Startet den testfailover-Bereinigungsvorgang.</span><span class="sxs-lookup"><span data-stu-id="7c399-103">Starts the test failover cleanup operation.</span></span>

## <span data-ttu-id="7c399-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c399-104">SYNTAX</span></span>

### <span data-ttu-id="7c399-105">ByRPIObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="7c399-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-Comment <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c399-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7c399-106">ByResourceId</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverCleanupJob -ResourceId <String> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c399-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="7c399-107">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrTestFailoverCleanupJob -RecoveryPlan <ASRRecoveryPlan> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c399-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7c399-108">DESCRIPTION</span></span>
<span data-ttu-id="7c399-109">Das Cmdlet **Start-AzRecoveryServicesAsrTestFailoverCleanupJob** startet den Test-Failover-Bereinigungsvorgang für ein geschütztes Replikations Element oder einen Wiederherstellungsplan, auf dem ein testfailover durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="7c399-109">The **Start-AzRecoveryServicesAsrTestFailoverCleanupJob** cmdlet starts the test failover cleanup operation on a replication protected item or recovery plan on which a test failover has been performed.</span></span>

## <span data-ttu-id="7c399-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7c399-110">EXAMPLES</span></span>

### <span data-ttu-id="7c399-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7c399-111">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem $rpi -Comments "testing done"
```

<span data-ttu-id="7c399-112">Auftrag zum Nachvollziehen der Bereinigung des Test Failovers für ein geschütztes Element der Azure Site Recovery-Replikation.</span><span class="sxs-lookup"><span data-stu-id="7c399-112">Job to track test failover Cleanup of an Azure Site Recovery replication protected item.</span></span>

### <span data-ttu-id="7c399-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7c399-113">Example 2</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrTestFailoverCleanupJob -RecoveryPlan $recoveryPlan -Comment "testing done"
```

<span data-ttu-id="7c399-114">Auftrag zum Nachvollziehen der Bereinigung des Test Failovers eines Azure Site Recovery-recoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7c399-114">Job to track test failover Cleanup of an Azure Site Recovery recoveryPlan.</span></span>

## <span data-ttu-id="7c399-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c399-115">PARAMETERS</span></span>

### <span data-ttu-id="7c399-116">-Kommentar</span><span class="sxs-lookup"><span data-stu-id="7c399-116">-Comment</span></span>
<span data-ttu-id="7c399-117">Benutzerkommentar für Test-Failover</span><span class="sxs-lookup"><span data-stu-id="7c399-117">User Comment for Test Failover.</span></span>

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

### <span data-ttu-id="7c399-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c399-118">-DefaultProfile</span></span>
<span data-ttu-id="7c399-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7c399-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c399-120">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7c399-120">-RecoveryPlan</span></span>
<span data-ttu-id="7c399-121">Wiederherstellungs Plan zum Durchführen der Test-Failover-Bereinigung.</span><span class="sxs-lookup"><span data-stu-id="7c399-121">Recovery Plan to perform the test failover cleanup on.</span></span>

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

### <span data-ttu-id="7c399-122">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7c399-122">-ReplicationProtectedItem</span></span>
<span data-ttu-id="7c399-123">Geschütztes Replikations Element, um die Bereinigung des Test Failovers durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="7c399-123">Replication Protected Item to perform the test failover cleanup on.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c399-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="7c399-124">-ResourceId</span></span>
<span data-ttu-id="7c399-125">Ressourcen-ID des Replikat geschützten Elements/Wiederherstellungsplans für das CleaningUp-testfailover.</span><span class="sxs-lookup"><span data-stu-id="7c399-125">Resource Id of replication protected item / recovery plan for cleaningup test failover.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c399-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7c399-126">-Confirm</span></span>
<span data-ttu-id="7c399-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7c399-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c399-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c399-128">-WhatIf</span></span>
<span data-ttu-id="7c399-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7c399-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c399-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7c399-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c399-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c399-131">CommonParameters</span></span>
<span data-ttu-id="7c399-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c399-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c399-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c399-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c399-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7c399-134">INPUTS</span></span>

### <span data-ttu-id="7c399-135">System. String</span><span class="sxs-lookup"><span data-stu-id="7c399-135">System.String</span></span>

### <span data-ttu-id="7c399-136">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7c399-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="7c399-137">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="7c399-137">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="7c399-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7c399-138">OUTPUTS</span></span>

### <span data-ttu-id="7c399-139">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7c399-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7c399-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="7c399-140">NOTES</span></span>

## <span data-ttu-id="7c399-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7c399-141">RELATED LINKS</span></span>
