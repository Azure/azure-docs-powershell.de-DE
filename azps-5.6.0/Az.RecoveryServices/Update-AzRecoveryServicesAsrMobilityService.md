---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesasrmobilityservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
ms.openlocfilehash: 5c5c9509c7ae242f98c8474a2ab87635f94dd62d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927800"
---
# <span data-ttu-id="e8057-101">Update-AzRecoveryServicesAsrMobilityService</span><span class="sxs-lookup"><span data-stu-id="e8057-101">Update-AzRecoveryServicesAsrMobilityService</span></span>

## <span data-ttu-id="e8057-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8057-102">SYNOPSIS</span></span>
<span data-ttu-id="e8057-103">Push mobility service agent updates to protected machines.</span><span class="sxs-lookup"><span data-stu-id="e8057-103">Push mobility service agent updates to protected machines.</span></span>

## <span data-ttu-id="e8057-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e8057-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrMobilityService [-Account <ASRRunAsAccount>]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8057-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e8057-105">DESCRIPTION</span></span>
<span data-ttu-id="e8057-106">Das **Cmdlet Update-AzRecoveryServicesAsrMobilityService** versucht, Updates des Mobility Service Agent auf geschützte Computer zu schieben(wenn ein Update verfügbar ist).)</span><span class="sxs-lookup"><span data-stu-id="e8057-106">The **Update-AzRecoveryServicesAsrMobilityService** cmdlet attempts to push mobility service agent updates to protected machines(if an update is available.)</span></span>

## <span data-ttu-id="e8057-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e8057-107">EXAMPLES</span></span>

### <span data-ttu-id="e8057-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e8057-108">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrMobilityService -ReplicationProtectedItem $rpi -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="e8057-109">Aufgabe zum Nachverfolgen des Mobility Service Agents des geschützten Elements für die Aktualisierungsreplikation.</span><span class="sxs-lookup"><span data-stu-id="e8057-109">Job to track Update Replication Protected Item's Mobility Service Agent.</span></span>

## <span data-ttu-id="e8057-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e8057-110">PARAMETERS</span></span>

### <span data-ttu-id="e8057-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="e8057-111">-Account</span></span>
<span data-ttu-id="e8057-112">Die als Konto-ID ausführen, um das Update zu pushen.</span><span class="sxs-lookup"><span data-stu-id="e8057-112">The run as account ID to be used to push the update.</span></span> <span data-ttu-id="e8057-113">Muss eins aus der Liste der konten im ASR-Fabric sein, die dem aktualisierten Computer entspricht.</span><span class="sxs-lookup"><span data-stu-id="e8057-113">Must be one from the list of run as accounts in the ASR fabric corresponding to machine being updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8057-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8057-114">-DefaultProfile</span></span>
<span data-ttu-id="e8057-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e8057-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8057-116">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e8057-116">-ReplicationProtectedItem</span></span>
<span data-ttu-id="e8057-117">Geschütztes Element für die Azure-Websitewiederherstellungsreplikation, das aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e8057-117">Azure Site Recovery replication protected item to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8057-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e8057-118">-Confirm</span></span>
<span data-ttu-id="e8057-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e8057-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8057-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8057-120">-WhatIf</span></span>
<span data-ttu-id="e8057-121">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e8057-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e8057-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e8057-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8057-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8057-123">CommonParameters</span></span>
<span data-ttu-id="e8057-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8057-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8057-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8057-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8057-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e8057-126">INPUTS</span></span>

### <span data-ttu-id="e8057-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e8057-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="e8057-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e8057-128">OUTPUTS</span></span>

### <span data-ttu-id="e8057-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="e8057-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e8057-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e8057-130">NOTES</span></span>

## <span data-ttu-id="e8057-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e8057-131">RELATED LINKS</span></span>
