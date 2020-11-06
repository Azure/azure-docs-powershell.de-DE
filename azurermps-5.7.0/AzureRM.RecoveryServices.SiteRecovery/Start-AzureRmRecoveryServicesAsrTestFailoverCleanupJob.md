---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrtestfailovercleanupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob.md
ms.openlocfilehash: 423ec89745b21176c714c1c2e956d4320c28b034
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476657"
---
# <span data-ttu-id="bf200-101">Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob</span><span class="sxs-lookup"><span data-stu-id="bf200-101">Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob</span></span>

## <span data-ttu-id="bf200-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bf200-102">SYNOPSIS</span></span>
<span data-ttu-id="bf200-103">Startet den testfailover-Bereinigungsvorgang.</span><span class="sxs-lookup"><span data-stu-id="bf200-103">Starts the test failover cleanup operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf200-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf200-104">SYNTAX</span></span>

### <span data-ttu-id="bf200-105">ByRPIObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="bf200-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-Comment <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf200-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bf200-106">ByResourceId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -ResourceId <String> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf200-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="bf200-107">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -RecoveryPlan <ASRRecoveryPlan> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf200-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf200-108">DESCRIPTION</span></span>
<span data-ttu-id="bf200-109">Das Cmdlet **Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob** startet den Test-Failover-Bereinigungsvorgang für ein geschütztes Replikations Element oder einen Wiederherstellungsplan, auf dem ein testfailover durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="bf200-109">The **Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob** cmdlet starts the test failover cleanup operation on a replication protected item or recovery plan on which a test failover has been performed.</span></span>

## <span data-ttu-id="bf200-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bf200-110">EXAMPLES</span></span>

### <span data-ttu-id="bf200-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bf200-111">Example 1</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem $rpi -Comments "testing done"
```

<span data-ttu-id="bf200-112">Auftrag zum Nachvollziehen der Bereinigung des Test Failovers für ein geschütztes Element der Azure Site Recovery-Replikation.</span><span class="sxs-lookup"><span data-stu-id="bf200-112">Job to track test failover Cleanup of an Azure Site Recovery replication protected item.</span></span>

### <span data-ttu-id="bf200-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="bf200-113">Example 2</span></span>
```
PS C:\> Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem $recoveryPlan -Comments "testing done"
```

<span data-ttu-id="bf200-114">Auftrag zum Nachvollziehen der Bereinigung des Test Failovers eines Azure Site Recovery-recoveryPlan</span><span class="sxs-lookup"><span data-stu-id="bf200-114">Job to track test failover Cleanup of an Azure Site Recovery recoveryPlan.</span></span>

## <span data-ttu-id="bf200-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf200-115">PARAMETERS</span></span>

### <span data-ttu-id="bf200-116">-Kommentar</span><span class="sxs-lookup"><span data-stu-id="bf200-116">-Comment</span></span>
<span data-ttu-id="bf200-117">Benutzerkommentar für Test-Failover</span><span class="sxs-lookup"><span data-stu-id="bf200-117">User Comment for Test Failover.</span></span>

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

### <span data-ttu-id="bf200-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bf200-118">-Confirm</span></span>
<span data-ttu-id="bf200-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bf200-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf200-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf200-120">-DefaultProfile</span></span>
<span data-ttu-id="bf200-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bf200-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf200-122">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="bf200-122">-RecoveryPlan</span></span>
<span data-ttu-id="bf200-123">Wiederherstellungs Plan zum Durchführen der Test-Failover-Bereinigung.</span><span class="sxs-lookup"><span data-stu-id="bf200-123">Recovery Plan to perform the test failover cleanup on.</span></span>

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

### <span data-ttu-id="bf200-124">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="bf200-124">-ReplicationProtectedItem</span></span>
<span data-ttu-id="bf200-125">Geschütztes Replikations Element, um die Bereinigung des Test Failovers durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="bf200-125">Replication Protected Item to perform the test failover cleanup on.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf200-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="bf200-126">-ResourceId</span></span>
<span data-ttu-id="bf200-127">Ressourcen-ID des Replikat geschützten Elements/Wiederherstellungsplans für das CleaningUp-testfailover.</span><span class="sxs-lookup"><span data-stu-id="bf200-127">Resource Id of replication protected item / recovery plan for cleaningup test failover.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf200-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf200-128">-WhatIf</span></span>
<span data-ttu-id="bf200-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bf200-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf200-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bf200-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf200-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf200-131">CommonParameters</span></span>
<span data-ttu-id="bf200-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf200-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf200-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf200-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf200-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bf200-134">INPUTS</span></span>

### <span data-ttu-id="bf200-135">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="bf200-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="bf200-136">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="bf200-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="bf200-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bf200-137">OUTPUTS</span></span>

### <span data-ttu-id="bf200-138">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="bf200-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="bf200-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="bf200-139">NOTES</span></span>

## <span data-ttu-id="bf200-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bf200-140">RELATED LINKS</span></span>
