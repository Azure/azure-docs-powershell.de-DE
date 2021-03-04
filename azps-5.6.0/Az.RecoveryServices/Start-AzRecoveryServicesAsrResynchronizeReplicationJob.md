---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/start-azrecoveryservicesasrresynchronizereplicationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
ms.openlocfilehash: 0675756b21c5af56ff3dc3fdff3b48d3bc9c999c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936632"
---
# <span data-ttu-id="36945-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span><span class="sxs-lookup"><span data-stu-id="36945-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span></span>

## <span data-ttu-id="36945-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36945-102">SYNOPSIS</span></span>
<span data-ttu-id="36945-103">Startet die Erneute Synchronisierung der Replikation.</span><span class="sxs-lookup"><span data-stu-id="36945-103">Starts replication resynchronization.</span></span>

## <span data-ttu-id="36945-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="36945-104">SYNTAX</span></span>

### <span data-ttu-id="36945-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="36945-105">Default (Default)</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36945-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="36945-106">ByResourceId</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36945-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="36945-107">DESCRIPTION</span></span>
<span data-ttu-id="36945-108">Das **Cmdlet Start-AzRecoveryServicesAsrResynchronizeReplicationJob** startet die Neusynchronisierung der Replikation für das angegebene geschützte Element, wenn sich der geschützte Zustand im erforderlichen Zustand der Neusynchronisierung befindet.</span><span class="sxs-lookup"><span data-stu-id="36945-108">The **Start-AzRecoveryServicesAsrResynchronizeReplicationJob** cmdlet start resynchronization of replication for the specified protected item if the protected is in a resynchronization required state.</span></span>

## <span data-ttu-id="36945-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="36945-109">EXAMPLES</span></span>

### <span data-ttu-id="36945-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="36945-110">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem $rpi
```

<span data-ttu-id="36945-111">Startet den Auftrag zum Neusynchronisieren der Replikation für übergebene replikationsgeschützte Elemente.</span><span class="sxs-lookup"><span data-stu-id="36945-111">Starts job to resynchronize replication on passed replication protected item.</span></span>

## <span data-ttu-id="36945-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="36945-112">PARAMETERS</span></span>

### <span data-ttu-id="36945-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36945-113">-DefaultProfile</span></span>
<span data-ttu-id="36945-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="36945-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36945-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="36945-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="36945-116">ASR-Replikationsgeschütztes Element, für das die Replikation neu synchronisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="36945-116">ASR replication protected item to resynchronize replication for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36945-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36945-117">-ResourceId</span></span>
<span data-ttu-id="36945-118">Ressourcen-ID des replikationsgeschützten Elements, das neu synchronisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="36945-118">Resource Id of replication protected item to resynchronize.</span></span>

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

### <span data-ttu-id="36945-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="36945-119">-Confirm</span></span>
<span data-ttu-id="36945-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="36945-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36945-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36945-121">-WhatIf</span></span>
<span data-ttu-id="36945-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="36945-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36945-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="36945-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36945-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36945-124">CommonParameters</span></span>
<span data-ttu-id="36945-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36945-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36945-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36945-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36945-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="36945-127">INPUTS</span></span>

### <span data-ttu-id="36945-128">System.String</span><span class="sxs-lookup"><span data-stu-id="36945-128">System.String</span></span>

### <span data-ttu-id="36945-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="36945-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="36945-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="36945-130">OUTPUTS</span></span>

### <span data-ttu-id="36945-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="36945-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="36945-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="36945-132">NOTES</span></span>

## <span data-ttu-id="36945-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="36945-133">RELATED LINKS</span></span>
