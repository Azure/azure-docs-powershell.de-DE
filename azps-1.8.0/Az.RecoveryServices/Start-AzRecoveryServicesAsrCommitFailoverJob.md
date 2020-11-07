---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrcommitfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrCommitFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrCommitFailoverJob.md
ms.openlocfilehash: 1e453f8b11929b96e6e0f2dbe96164c2bf351ae7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659808"
---
# <span data-ttu-id="d49ea-101">Start-AzRecoveryServicesAsrCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="d49ea-101">Start-AzRecoveryServicesAsrCommitFailoverJob</span></span>

## <span data-ttu-id="d49ea-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d49ea-102">SYNOPSIS</span></span>
<span data-ttu-id="d49ea-103">Startet die Commit-Failover-Aktion für ein Website Wiederherstellungs Objekt.</span><span class="sxs-lookup"><span data-stu-id="d49ea-103">Starts the commit failover action for a Site Recovery object.</span></span>

## <span data-ttu-id="d49ea-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d49ea-104">SYNTAX</span></span>

### <span data-ttu-id="d49ea-105">ByRPIObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="d49ea-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrCommitFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d49ea-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="d49ea-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d49ea-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d49ea-107">DESCRIPTION</span></span>
<span data-ttu-id="d49ea-108">Mit dem Cmdlet " **Start-AzRecoveryServicesAsrCommitFailoverJob** " wird der Commit-Failoverprozess für ein Azure Site Recovery-Objekt nach einem Failover-Vorgang gestartet.</span><span class="sxs-lookup"><span data-stu-id="d49ea-108">The **Start-AzRecoveryServicesAsrCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="d49ea-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d49ea-109">EXAMPLES</span></span>

### <span data-ttu-id="d49ea-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d49ea-110">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrCommitFailoverJob -RecoveryPlan $RP
```

<span data-ttu-id="d49ea-111">Startet das Commit-Failover für den angegebenen Wiederherstellungsplan und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d49ea-111">Starts the commit failover for the specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="d49ea-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d49ea-112">PARAMETERS</span></span>

### <span data-ttu-id="d49ea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d49ea-113">-DefaultProfile</span></span>
<span data-ttu-id="d49ea-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d49ea-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d49ea-115">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d49ea-115">-RecoveryPlan</span></span>
<span data-ttu-id="d49ea-116">Gibt ein ASR-Wiederherstellungsplan Objekt entsprechend dem Wiederherstellungsplan für Failover an.</span><span class="sxs-lookup"><span data-stu-id="d49ea-116">Specifies an ASR recovery plan object corresponding to recovery plan to be failovered.</span></span>

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

### <span data-ttu-id="d49ea-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d49ea-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="d49ea-118">Gibt ein geschütztes ASR-Replikations Element Objekt an, das dem zu failoverden Replikations geschützten Element entspricht.</span><span class="sxs-lookup"><span data-stu-id="d49ea-118">Specifies an ASR replication protected item object corresponding to replication protected item  to be failovered.</span></span>

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

### <span data-ttu-id="d49ea-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d49ea-119">-Confirm</span></span>
<span data-ttu-id="d49ea-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d49ea-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d49ea-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d49ea-121">-WhatIf</span></span>
<span data-ttu-id="d49ea-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d49ea-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d49ea-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d49ea-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d49ea-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d49ea-124">CommonParameters</span></span>
<span data-ttu-id="d49ea-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d49ea-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d49ea-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d49ea-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d49ea-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d49ea-127">INPUTS</span></span>

### <span data-ttu-id="d49ea-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="d49ea-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="d49ea-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d49ea-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="d49ea-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d49ea-130">OUTPUTS</span></span>

### <span data-ttu-id="d49ea-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d49ea-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d49ea-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="d49ea-132">NOTES</span></span>

## <span data-ttu-id="d49ea-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d49ea-133">RELATED LINKS</span></span>
