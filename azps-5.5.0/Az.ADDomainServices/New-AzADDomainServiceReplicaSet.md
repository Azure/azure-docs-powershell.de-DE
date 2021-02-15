---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.ADDomainServices/new-AzADDomainServiceReplicaSet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceReplicaSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceReplicaSet.md
ms.openlocfilehash: f95c4148afa3f317914dabe968376e0e86913dcb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143825"
---
# <span data-ttu-id="89669-101">New-AzADDomainServiceReplicaSet</span><span class="sxs-lookup"><span data-stu-id="89669-101">New-AzADDomainServiceReplicaSet</span></span>

## <span data-ttu-id="89669-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89669-102">SYNOPSIS</span></span>
<span data-ttu-id="89669-103">Erstellen eines Speicherobjekts für ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="89669-103">Create a in-memory object for ReplicaSet</span></span>

## <span data-ttu-id="89669-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="89669-104">SYNTAX</span></span>

```
New-AzADDomainServiceReplicaSet [-Location <String>] [-SubnetId <String>] [<CommonParameters>]
```

## <span data-ttu-id="89669-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="89669-105">DESCRIPTION</span></span>
<span data-ttu-id="89669-106">Erstellen eines Speicherobjekts für ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="89669-106">Create a in-memory object for ReplicaSet</span></span>

## <span data-ttu-id="89669-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="89669-107">EXAMPLES</span></span>

### <span data-ttu-id="89669-108">Beispiel 1: Create ReplicaSet for AdDomain</span><span class="sxs-lookup"><span data-stu-id="89669-108">Example 1: Create ReplicaSet for AdDomain</span></span>
```powershell
PS C:\> New-AzADDomainServiceReplicaSet -Location eastus -SubnetId /subscriptions/**********-****-****-****-****-**********/resourceGroups/youriADDomain-rg-test/providers/Microsoft.Network/virtualNetworks/yourinttest/subnets/default

DomainControllerIPAddress ExternalAccessIPAddress HealthLastEvaluated Location ServiceStatus SubnetId
------------------------- ----------------------- ------------------- -------- ------------- --------
                                                                      eastus                 /subscriptions/****
                                                                      ****-****-****-****-**********/resourceGroups/youriADDomain-rg-test/providers/M…
```

<span data-ttu-id="89669-109">Create ReplicaSet for AdDomain</span><span class="sxs-lookup"><span data-stu-id="89669-109">Create ReplicaSet for AdDomain</span></span>

## <span data-ttu-id="89669-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89669-110">PARAMETERS</span></span>

### <span data-ttu-id="89669-111">-Location</span><span class="sxs-lookup"><span data-stu-id="89669-111">-Location</span></span>
<span data-ttu-id="89669-112">Virtueller Netzwerkspeicherort.</span><span class="sxs-lookup"><span data-stu-id="89669-112">Virtual network location.</span></span>

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

### <span data-ttu-id="89669-113">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="89669-113">-SubnetId</span></span>
<span data-ttu-id="89669-114">Der Name des virtuellen Netzwerks, in dem Domain Services bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="89669-114">The name of the virtual network that Domain Services will be deployed on.</span></span>
<span data-ttu-id="89669-115">Die ID des Subnetzes, in dem Domänendienste bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="89669-115">The id of the subnet that Domain Services will be deployed on.</span></span>
<span data-ttu-id="89669-116">/virtualNetwork/vnetName/subnets/subnetName.</span><span class="sxs-lookup"><span data-stu-id="89669-116">/virtualNetwork/vnetName/subnets/subnetName.</span></span>

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

### <span data-ttu-id="89669-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89669-117">CommonParameters</span></span>
<span data-ttu-id="89669-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89669-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89669-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89669-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89669-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="89669-120">INPUTS</span></span>

## <span data-ttu-id="89669-121">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="89669-121">OUTPUTS</span></span>

### <span data-ttu-id="89669-122">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="89669-122">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.ReplicaSet</span></span>

## <span data-ttu-id="89669-123">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="89669-123">NOTES</span></span>

<span data-ttu-id="89669-124">ALIASE</span><span class="sxs-lookup"><span data-stu-id="89669-124">ALIASES</span></span>

## <span data-ttu-id="89669-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="89669-125">RELATED LINKS</span></span>

