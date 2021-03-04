---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.CloudService/new-AzCloudServiceLoadBalancerConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerConfigurationObject.md
ms.openlocfilehash: 5d3acb8c03ceae44024ed8c6c52a8ee962c9861c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935835"
---
# <span data-ttu-id="2756b-101">New-AzCloudServiceLoadBalancerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="2756b-101">New-AzCloudServiceLoadBalancerConfigurationObject</span></span>

## <span data-ttu-id="2756b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2756b-102">SYNOPSIS</span></span>
<span data-ttu-id="2756b-103">Erstellen eines Speicherobjekts für LoadBalancerConfiguration</span><span class="sxs-lookup"><span data-stu-id="2756b-103">Create a in-memory object for LoadBalancerConfiguration</span></span>

## <span data-ttu-id="2756b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2756b-104">SYNTAX</span></span>

```
New-AzCloudServiceLoadBalancerConfigurationObject
 [-FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>] [-Name <String>] [<CommonParameters>]
```

## <span data-ttu-id="2756b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2756b-105">DESCRIPTION</span></span>
<span data-ttu-id="2756b-106">Erstellen eines Speicherobjekts für LoadBalancerConfiguration</span><span class="sxs-lookup"><span data-stu-id="2756b-106">Create a in-memory object for LoadBalancerConfiguration</span></span>

## <span data-ttu-id="2756b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2756b-107">EXAMPLES</span></span>

### <span data-ttu-id="2756b-108">Beispiel 1: Erstellen eines Load Balancer-Konfigurationsobjekts</span><span class="sxs-lookup"><span data-stu-id="2756b-108">Example 1: Create load balancer configuration object</span></span>
```powershell
PS C:\> $publicIP = Get-AzPublicIpAddress -ResourceGroupName 'ContosoOrg' -Name 'ContosoPublicIP'
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIP.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
```

<span data-ttu-id="2756b-109">Mit diesem Befehl wird ein Load Balancer-Konfigurationsobjekt erstellt, das zum Erstellen oder Aktualisieren eines Clouddiensts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2756b-109">This command creates load balancer configuration object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="2756b-110">Weitere Informationen finden Sie unter New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="2756b-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="2756b-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2756b-111">PARAMETERS</span></span>

### <span data-ttu-id="2756b-112">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2756b-112">-FrontendIPConfiguration</span></span>
<span data-ttu-id="2756b-113">FrontendIPConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2756b-113">FrontendIPConfiguration.</span></span>
<span data-ttu-id="2756b-114">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN für FrontENDIPCONFIGURATION-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="2756b-114">To construct, see NOTES section for FRONTENDIPCONFIGURATION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ILoadBalancerFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2756b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="2756b-115">-Name</span></span>
<span data-ttu-id="2756b-116">Name der LoadBalancerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2756b-116">Name of LoadBalancerConfiguration.</span></span>

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

### <span data-ttu-id="2756b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2756b-117">CommonParameters</span></span>
<span data-ttu-id="2756b-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2756b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2756b-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2756b-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2756b-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2756b-120">INPUTS</span></span>

## <span data-ttu-id="2756b-121">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2756b-121">OUTPUTS</span></span>

### <span data-ttu-id="2756b-122">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.LoadBalancerConfiguration</span><span class="sxs-lookup"><span data-stu-id="2756b-122">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.LoadBalancerConfiguration</span></span>

## <span data-ttu-id="2756b-123">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2756b-123">NOTES</span></span>

<span data-ttu-id="2756b-124">ALIASE</span><span class="sxs-lookup"><span data-stu-id="2756b-124">ALIASES</span></span>

<span data-ttu-id="2756b-125">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="2756b-125">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2756b-126">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="2756b-126">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2756b-127">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2756b-127">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2756b-128">FRONTENDIPCONFIGURATION <ILoadBalancerFrontendIPConfiguration[]>: FrontendIPConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2756b-128">FRONTENDIPCONFIGURATION <ILoadBalancerFrontendIPConfiguration[]>: FrontendIPConfiguration.</span></span>
  - <span data-ttu-id="2756b-129">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="2756b-129">`[Name <String>]`:</span></span> 
  - <span data-ttu-id="2756b-130">`[PrivateIPAddress <String>]`: Die private IP-Adresse, auf die vom Clouddienst verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="2756b-130">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
  - <span data-ttu-id="2756b-131">`[PublicIPAddressId <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="2756b-131">`[PublicIPAddressId <String>]`: Resource Id</span></span>
  - <span data-ttu-id="2756b-132">`[SubnetId <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="2756b-132">`[SubnetId <String>]`: Resource Id</span></span>

## <span data-ttu-id="2756b-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2756b-133">RELATED LINKS</span></span>

