---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.CloudService/new-AzCloudServiceLoadBalancerFrontendIPConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject.md
ms.openlocfilehash: cdd983e2ede5cd06c3b9b00805b337eac5b73a9b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162356"
---
# <span data-ttu-id="4d836-101">New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="4d836-101">New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject</span></span>

## <span data-ttu-id="4d836-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d836-102">SYNOPSIS</span></span>
<span data-ttu-id="4d836-103">Erstellen eines Speicherobjekts für loadBalancerFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d836-103">Create a in-memory object for LoadBalancerFrontendIPConfiguration</span></span>

## <span data-ttu-id="4d836-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4d836-104">SYNTAX</span></span>

```
New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject [-Name <String>] [-PublicIPAddressId <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="4d836-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4d836-105">DESCRIPTION</span></span>
<span data-ttu-id="4d836-106">Erstellen eines Speicherobjekts für loadBalancerFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d836-106">Create a in-memory object for LoadBalancerFrontendIPConfiguration</span></span>

## <span data-ttu-id="4d836-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4d836-107">EXAMPLES</span></span>

### <span data-ttu-id="4d836-108">Beispiel 1: Erstellen eines Frontend-IP-Konfigurationsobjekts für das Lastenausgleichsobjekt</span><span class="sxs-lookup"><span data-stu-id="4d836-108">Example 1: Create load balancer frontend IP configuration object</span></span>
```powershell
PS C:\> $publicIP = Get-AzPublicIpAddress -ResourceGroupName 'ContosoOrg' -Name 'ContosoPublicIP'
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
```

<span data-ttu-id="4d836-109">Dieser Befehl erstellt ein Frontend-IP-Konfigurationsobjekt für den Lastenausgleich, das zum Erstellen oder Aktualisieren eines Clouddiensts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4d836-109">This command creates load balancer frontend IP configuration object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="4d836-110">Weitere Details finden Sie unter "New-AzCloudService".</span><span class="sxs-lookup"><span data-stu-id="4d836-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="4d836-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d836-111">PARAMETERS</span></span>

### <span data-ttu-id="4d836-112">-Name</span><span class="sxs-lookup"><span data-stu-id="4d836-112">-Name</span></span>
<span data-ttu-id="4d836-113">Name der FrontendIpConfigration.</span><span class="sxs-lookup"><span data-stu-id="4d836-113">Name of FrontendIpConfigration.</span></span>

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

### <span data-ttu-id="4d836-114">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="4d836-114">-PublicIPAddressId</span></span>
<span data-ttu-id="4d836-115">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="4d836-115">Resource Id.</span></span>

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

### <span data-ttu-id="4d836-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d836-116">CommonParameters</span></span>
<span data-ttu-id="4d836-117">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d836-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d836-118">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4d836-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d836-119">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4d836-119">INPUTS</span></span>

## <span data-ttu-id="4d836-120">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4d836-120">OUTPUTS</span></span>

### <span data-ttu-id="4d836-121">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.LoadBalancerFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d836-121">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.LoadBalancerFrontendIPConfiguration</span></span>

## <span data-ttu-id="4d836-122">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4d836-122">NOTES</span></span>

<span data-ttu-id="4d836-123">ALIASE</span><span class="sxs-lookup"><span data-stu-id="4d836-123">ALIASES</span></span>

## <span data-ttu-id="4d836-124">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4d836-124">RELATED LINKS</span></span>

