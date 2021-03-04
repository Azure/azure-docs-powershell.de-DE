---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.CloudService/new-AzCloudServiceLoadBalancerFrontendIPConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject.md
ms.openlocfilehash: 5628b7819789ba97ee56a0c69f65e371f9b35e7e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935832"
---
# <span data-ttu-id="66bfe-101">New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="66bfe-101">New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject</span></span>

## <span data-ttu-id="66bfe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66bfe-102">SYNOPSIS</span></span>
<span data-ttu-id="66bfe-103">Erstellen eines Speicherobjekts für LoadBalancerFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="66bfe-103">Create a in-memory object for LoadBalancerFrontendIPConfiguration</span></span>

## <span data-ttu-id="66bfe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="66bfe-104">SYNTAX</span></span>

```
New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject [-Name <String>] [-PublicIPAddressId <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="66bfe-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="66bfe-105">DESCRIPTION</span></span>
<span data-ttu-id="66bfe-106">Erstellen eines Speicherobjekts für LoadBalancerFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="66bfe-106">Create a in-memory object for LoadBalancerFrontendIPConfiguration</span></span>

## <span data-ttu-id="66bfe-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="66bfe-107">EXAMPLES</span></span>

### <span data-ttu-id="66bfe-108">Beispiel 1: Erstellen eines Frontend-IP-Konfigurationsobjekts für load balancer</span><span class="sxs-lookup"><span data-stu-id="66bfe-108">Example 1: Create load balancer frontend IP configuration object</span></span>
```powershell
PS C:\> $publicIP = Get-AzPublicIpAddress -ResourceGroupName 'ContosoOrg' -Name 'ContosoPublicIP'
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
```

<span data-ttu-id="66bfe-109">Mit diesem Befehl wird das Frontend-IP-Konfigurationsobjekt des Load Balancers erstellt, das zum Erstellen oder Aktualisieren eines Clouddiensts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="66bfe-109">This command creates load balancer frontend IP configuration object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="66bfe-110">Weitere Informationen finden Sie unter New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="66bfe-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="66bfe-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="66bfe-111">PARAMETERS</span></span>

### <span data-ttu-id="66bfe-112">-Name</span><span class="sxs-lookup"><span data-stu-id="66bfe-112">-Name</span></span>
<span data-ttu-id="66bfe-113">Name von FrontendIpConfigration.</span><span class="sxs-lookup"><span data-stu-id="66bfe-113">Name of FrontendIpConfigration.</span></span>

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

### <span data-ttu-id="66bfe-114">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="66bfe-114">-PublicIPAddressId</span></span>
<span data-ttu-id="66bfe-115">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="66bfe-115">Resource Id.</span></span>

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

### <span data-ttu-id="66bfe-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66bfe-116">CommonParameters</span></span>
<span data-ttu-id="66bfe-117">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66bfe-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66bfe-118">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="66bfe-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66bfe-119">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="66bfe-119">INPUTS</span></span>

## <span data-ttu-id="66bfe-120">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="66bfe-120">OUTPUTS</span></span>

### <span data-ttu-id="66bfe-121">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.LoadBalancerFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="66bfe-121">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.LoadBalancerFrontendIPConfiguration</span></span>

## <span data-ttu-id="66bfe-122">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="66bfe-122">NOTES</span></span>

<span data-ttu-id="66bfe-123">ALIASE</span><span class="sxs-lookup"><span data-stu-id="66bfe-123">ALIASES</span></span>

## <span data-ttu-id="66bfe-124">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="66bfe-124">RELATED LINKS</span></span>

