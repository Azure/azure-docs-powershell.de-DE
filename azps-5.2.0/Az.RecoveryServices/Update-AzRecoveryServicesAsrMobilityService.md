---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrmobilityservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
ms.openlocfilehash: 3374ba9cbc1db05b80da6b0b6dd5c5d89212ad51
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358068"
---
# <span data-ttu-id="38f04-101">Update-AzRecoveryServicesAsrMobilityService</span><span class="sxs-lookup"><span data-stu-id="38f04-101">Update-AzRecoveryServicesAsrMobilityService</span></span>

## <span data-ttu-id="38f04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38f04-102">SYNOPSIS</span></span>
<span data-ttu-id="38f04-103">Aktualisierungen des Agent für Push mobility Service auf geschützte Computer.</span><span class="sxs-lookup"><span data-stu-id="38f04-103">Push mobility service agent updates to protected machines.</span></span>

## <span data-ttu-id="38f04-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="38f04-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrMobilityService [-Account <ASRRunAsAccount>]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38f04-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="38f04-105">DESCRIPTION</span></span>
<span data-ttu-id="38f04-106">Das **Cmdlet "Update-AzRecoveryServicesAsrMobilityService"** versucht, Updates des Mobility Service Agent auf geschützte Computer zu schieben (wenn ein Update verfügbar ist).)</span><span class="sxs-lookup"><span data-stu-id="38f04-106">The **Update-AzRecoveryServicesAsrMobilityService** cmdlet attempts to push mobility service agent updates to protected machines(if an update is available.)</span></span>

## <span data-ttu-id="38f04-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="38f04-107">EXAMPLES</span></span>

### <span data-ttu-id="38f04-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="38f04-108">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrMobilityService -ReplicationProtectedItem $rpi -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="38f04-109">Aufgabe zum Nachverfolgen des Mobility Service Agents für das elementgeschützte Updatereplikation.</span><span class="sxs-lookup"><span data-stu-id="38f04-109">Job to track Update Replication Protected Item's Mobility Service Agent.</span></span>

## <span data-ttu-id="38f04-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38f04-110">PARAMETERS</span></span>

### <span data-ttu-id="38f04-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="38f04-111">-Account</span></span>
<span data-ttu-id="38f04-112">Die als Konto-ID ausführen, die zum Pushen des Updates verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="38f04-112">The run as account ID to be used to push the update.</span></span> <span data-ttu-id="38f04-113">Must be one from the list of run as accounts in the ASR fabric corresponding to machine being updated.</span><span class="sxs-lookup"><span data-stu-id="38f04-113">Must be one from the list of run as accounts in the ASR fabric corresponding to machine being updated.</span></span>

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

### <span data-ttu-id="38f04-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38f04-114">-DefaultProfile</span></span>
<span data-ttu-id="38f04-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="38f04-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38f04-116">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="38f04-116">-ReplicationProtectedItem</span></span>
<span data-ttu-id="38f04-117">Das zu aktualisierende geschützte Element der Azure-Websitewiederherstellungsreplikation.</span><span class="sxs-lookup"><span data-stu-id="38f04-117">Azure Site Recovery replication protected item to be updated.</span></span>

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

### <span data-ttu-id="38f04-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38f04-118">-Confirm</span></span>
<span data-ttu-id="38f04-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="38f04-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38f04-120">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="38f04-120">-WhatIf</span></span>
<span data-ttu-id="38f04-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="38f04-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="38f04-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="38f04-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38f04-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38f04-123">CommonParameters</span></span>
<span data-ttu-id="38f04-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38f04-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38f04-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="38f04-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38f04-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="38f04-126">INPUTS</span></span>

### <span data-ttu-id="38f04-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="38f04-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="38f04-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="38f04-128">OUTPUTS</span></span>

### <span data-ttu-id="38f04-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="38f04-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="38f04-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="38f04-130">NOTES</span></span>

## <span data-ttu-id="38f04-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="38f04-131">RELATED LINKS</span></span>
