---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrmobilityservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
ms.openlocfilehash: 3374ba9cbc1db05b80da6b0b6dd5c5d89212ad51
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460871"
---
# <span data-ttu-id="4f1c1-101">Update-AzRecoveryServicesAsrMobilityService</span><span class="sxs-lookup"><span data-stu-id="4f1c1-101">Update-AzRecoveryServicesAsrMobilityService</span></span>

## <span data-ttu-id="4f1c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f1c1-102">SYNOPSIS</span></span>
<span data-ttu-id="4f1c1-103">Aktualisierungen des Agent für Push mobility Service auf geschützte Computer.</span><span class="sxs-lookup"><span data-stu-id="4f1c1-103">Push mobility service agent updates to protected machines.</span></span>

## <span data-ttu-id="4f1c1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4f1c1-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrMobilityService [-Account <ASRRunAsAccount>]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f1c1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4f1c1-105">DESCRIPTION</span></span>
<span data-ttu-id="4f1c1-106">Das **Cmdlet "Update-AzRecoveryServicesAsrMobilityService"** versucht, Updates des Mobility Service Agent auf geschützte Computer zu schieben (wenn ein Update verfügbar ist).)</span><span class="sxs-lookup"><span data-stu-id="4f1c1-106">The **Update-AzRecoveryServicesAsrMobilityService** cmdlet attempts to push mobility service agent updates to protected machines(if an update is available.)</span></span>

## <span data-ttu-id="4f1c1-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4f1c1-107">EXAMPLES</span></span>

### <span data-ttu-id="4f1c1-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4f1c1-108">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrMobilityService -ReplicationProtectedItem $rpi -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="4f1c1-109">Aufgabe zum Nachverfolgen des Mobility Service-Agents für aktualisierungsgeschützte Elemente.</span><span class="sxs-lookup"><span data-stu-id="4f1c1-109">Job to track Update Replication Protected Item's Mobility Service Agent.</span></span>

## <span data-ttu-id="4f1c1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f1c1-110">PARAMETERS</span></span>

### <span data-ttu-id="4f1c1-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="4f1c1-111">-Account</span></span>
<span data-ttu-id="4f1c1-112">Die als Konto-ID ausführen, die zum Pushen des Updates verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4f1c1-112">The run as account ID to be used to push the update.</span></span> <span data-ttu-id="4f1c1-113">Must be one from the list of run as accounts in the ASR fabric corresponding to machine being updated.</span><span class="sxs-lookup"><span data-stu-id="4f1c1-113">Must be one from the list of run as accounts in the ASR fabric corresponding to machine being updated.</span></span>

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

### <span data-ttu-id="4f1c1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f1c1-114">-DefaultProfile</span></span>
<span data-ttu-id="4f1c1-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4f1c1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f1c1-116">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4f1c1-116">-ReplicationProtectedItem</span></span>
<span data-ttu-id="4f1c1-117">Geschütztes Element für die Azure-Websitewiederherstellungsreplikation, das aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="4f1c1-117">Azure Site Recovery replication protected item to be updated.</span></span>

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

### <span data-ttu-id="4f1c1-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4f1c1-118">-Confirm</span></span>
<span data-ttu-id="4f1c1-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4f1c1-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f1c1-120">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4f1c1-120">-WhatIf</span></span>
<span data-ttu-id="4f1c1-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4f1c1-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4f1c1-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4f1c1-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f1c1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f1c1-123">CommonParameters</span></span>
<span data-ttu-id="4f1c1-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f1c1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f1c1-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4f1c1-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f1c1-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4f1c1-126">INPUTS</span></span>

### <span data-ttu-id="4f1c1-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4f1c1-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="4f1c1-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4f1c1-128">OUTPUTS</span></span>

### <span data-ttu-id="4f1c1-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="4f1c1-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="4f1c1-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4f1c1-130">NOTES</span></span>

## <span data-ttu-id="4f1c1-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4f1c1-131">RELATED LINKS</span></span>
