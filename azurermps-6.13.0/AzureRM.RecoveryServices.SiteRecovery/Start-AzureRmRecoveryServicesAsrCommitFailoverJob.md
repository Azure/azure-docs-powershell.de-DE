---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrcommitfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrCommitFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrCommitFailoverJob.md
ms.openlocfilehash: 4543b127af4c0c6ca882daf93c95fb1dce614b73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477781"
---
# <span data-ttu-id="53f7f-101">Start-AzureRmRecoveryServicesAsrCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="53f7f-101">Start-AzureRmRecoveryServicesAsrCommitFailoverJob</span></span>

## <span data-ttu-id="53f7f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="53f7f-102">SYNOPSIS</span></span>
<span data-ttu-id="53f7f-103">Startet die Commit-Failover-Aktion für ein Website Wiederherstellungs Objekt.</span><span class="sxs-lookup"><span data-stu-id="53f7f-103">Starts the commit failover action for a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53f7f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="53f7f-104">SYNTAX</span></span>

### <span data-ttu-id="53f7f-105">ByRPIObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="53f7f-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrCommitFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53f7f-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="53f7f-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53f7f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="53f7f-107">DESCRIPTION</span></span>
<span data-ttu-id="53f7f-108">Mit dem Cmdlet " **Start-AzureRmRecoveryServicesAsrCommitFailoverJob** " wird der Commit-Failoverprozess für ein Azure Site Recovery-Objekt nach einem Failover-Vorgang gestartet.</span><span class="sxs-lookup"><span data-stu-id="53f7f-108">The **Start-AzureRmRecoveryServicesAsrCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="53f7f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="53f7f-109">EXAMPLES</span></span>

### <span data-ttu-id="53f7f-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="53f7f-110">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrCommitFailoverJob -RecoveryPlan $RP
```

<span data-ttu-id="53f7f-111">Startet das Commit-Failover für den angegebenen Wiederherstellungsplan und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="53f7f-111">Starts the commit failover for the specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="53f7f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="53f7f-112">PARAMETERS</span></span>

### <span data-ttu-id="53f7f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53f7f-113">-DefaultProfile</span></span>
<span data-ttu-id="53f7f-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="53f7f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="53f7f-115">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="53f7f-115">-RecoveryPlan</span></span>
<span data-ttu-id="53f7f-116">Gibt ein ASR-Wiederherstellungsplan Objekt entsprechend dem Wiederherstellungsplan für Failover an.</span><span class="sxs-lookup"><span data-stu-id="53f7f-116">Specifies an ASR recovery plan object corresponding to recovery plan to be failovered.</span></span>

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

### <span data-ttu-id="53f7f-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="53f7f-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="53f7f-118">Gibt ein geschütztes ASR-Replikations Element Objekt an, das dem zu failoverden Replikations geschützten Element entspricht.</span><span class="sxs-lookup"><span data-stu-id="53f7f-118">Specifies an ASR replication protected item object corresponding to replication protected item  to be failovered.</span></span>

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

### <span data-ttu-id="53f7f-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="53f7f-119">-Confirm</span></span>
<span data-ttu-id="53f7f-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="53f7f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53f7f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53f7f-121">-WhatIf</span></span>
<span data-ttu-id="53f7f-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="53f7f-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="53f7f-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="53f7f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53f7f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53f7f-124">CommonParameters</span></span>
<span data-ttu-id="53f7f-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53f7f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53f7f-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53f7f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53f7f-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="53f7f-127">INPUTS</span></span>

### <span data-ttu-id="53f7f-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="53f7f-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="53f7f-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="53f7f-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="53f7f-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="53f7f-130">OUTPUTS</span></span>

### <span data-ttu-id="53f7f-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="53f7f-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="53f7f-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="53f7f-132">NOTES</span></span>

## <span data-ttu-id="53f7f-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="53f7f-133">RELATED LINKS</span></span>
