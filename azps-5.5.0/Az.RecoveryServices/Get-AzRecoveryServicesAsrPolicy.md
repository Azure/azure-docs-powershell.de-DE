---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: a7cd359714be965c232019310ac2f2abfe0fe233
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169289"
---
# <span data-ttu-id="b8992-101">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="b8992-101">Get-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="b8992-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8992-102">SYNOPSIS</span></span>
<span data-ttu-id="b8992-103">Ruft die Richtlinien für die ASR-Replikation ab.</span><span class="sxs-lookup"><span data-stu-id="b8992-103">Gets ASR replication policies.</span></span>

## <span data-ttu-id="b8992-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b8992-104">SYNTAX</span></span>

### <span data-ttu-id="b8992-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="b8992-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8992-106">ByName</span><span class="sxs-lookup"><span data-stu-id="b8992-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8992-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="b8992-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b8992-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b8992-108">DESCRIPTION</span></span>
<span data-ttu-id="b8992-109">Das **Cmdlet "Get-AzRecoveryServicesAsrPolicy"** ruft die Liste der konfigurierten Azure-Websitewiederherstellungsreplikationsrichtlinien oder eine bestimmte Replikationsrichtlinie nach Name ab.</span><span class="sxs-lookup"><span data-stu-id="b8992-109">The **Get-AzRecoveryServicesAsrPolicy** cmdlet gets the list of configured Azure Site Recovery replication policies or a specific replication policy by name.</span></span>

## <span data-ttu-id="b8992-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b8992-110">EXAMPLES</span></span>

### <span data-ttu-id="b8992-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b8992-111">Example 1</span></span>
```
PS C:\> $Policy = Get-AzRecoveryServicesAsrPolicy
```

<span data-ttu-id="b8992-112">Gibt die Liste der Replikationsrichtlinien zurück.</span><span class="sxs-lookup"><span data-stu-id="b8992-112">Returns the list of replication policies</span></span>

### <span data-ttu-id="b8992-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b8992-113">Example 2</span></span>
```
PS C:\>  Get-AzRecoveryServicesAsrPolicy -Name abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="b8992-114">Gibt die Replikationsrichtlinie mit Name zurück.</span><span class="sxs-lookup"><span data-stu-id="b8992-114">Returns replication policy with name.</span></span>

### <span data-ttu-id="b8992-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="b8992-115">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrPolicy -FriendlyName abc

FriendlyName                : abc
Name                        : abc
ID                          : /Subscriptions/xxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationPolicies/abc
Type                        : Microsoft.RecoveryServices/vaults/replicationPolicies
ReplicationProvider         : HyperVReplicaAzure
ReplicationProviderSettings : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRHyperVReplicaAzurePolicyDetails
```

<span data-ttu-id="b8992-116">Gibt die Replikationsrichtlinie mit dem angegebenen Anzeigenamen zurück.</span><span class="sxs-lookup"><span data-stu-id="b8992-116">Returns the replication policy with the specified friendly name.</span></span>

## <span data-ttu-id="b8992-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8992-117">PARAMETERS</span></span>

### <span data-ttu-id="b8992-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8992-118">-DefaultProfile</span></span>
<span data-ttu-id="b8992-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b8992-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="b8992-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="b8992-120">-FriendlyName</span></span>
<span data-ttu-id="b8992-121">Gibt den Anzeigenamen der ASR-Replikationsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="b8992-121">Specifies the friendly name of the ASR replication policy.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8992-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b8992-122">-Name</span></span>
<span data-ttu-id="b8992-123">Gibt den Namen der ASR-Replikationsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="b8992-123">Specifies the name of the ASR replication policy.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8992-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8992-124">CommonParameters</span></span>
<span data-ttu-id="b8992-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8992-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8992-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b8992-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8992-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b8992-127">INPUTS</span></span>

### <span data-ttu-id="b8992-128">Keine</span><span class="sxs-lookup"><span data-stu-id="b8992-128">None</span></span>

## <span data-ttu-id="b8992-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b8992-129">OUTPUTS</span></span>

### <span data-ttu-id="b8992-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="b8992-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="b8992-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b8992-131">NOTES</span></span>

## <span data-ttu-id="b8992-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b8992-132">RELATED LINKS</span></span>

[<span data-ttu-id="b8992-133">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="b8992-133">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="b8992-134">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="b8992-134">Remove-AzRecoveryServicesAsrPolicy</span></span>](./Remove-AzRecoveryServicesAsrPolicy.md)
