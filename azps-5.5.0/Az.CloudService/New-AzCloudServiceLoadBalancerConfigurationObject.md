---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.CloudService/new-AzCloudServiceLoadBalancerConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerConfigurationObject.md
ms.openlocfilehash: 6afabb94ae006cec122d7e89997be17c20e85b05
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166660"
---
# <span data-ttu-id="c74e4-101">New-AzCloudServiceLoadBalancerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="c74e4-101">New-AzCloudServiceLoadBalancerConfigurationObject</span></span>

## <span data-ttu-id="c74e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c74e4-102">SYNOPSIS</span></span>
<span data-ttu-id="c74e4-103">Erstellen eines Speicherobjekts für loadBalancerConfiguration</span><span class="sxs-lookup"><span data-stu-id="c74e4-103">Create a in-memory object for LoadBalancerConfiguration</span></span>

## <span data-ttu-id="c74e4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c74e4-104">SYNTAX</span></span>

```
New-AzCloudServiceLoadBalancerConfigurationObject
 [-FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>] [-Name <String>] [<CommonParameters>]
```

## <span data-ttu-id="c74e4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c74e4-105">DESCRIPTION</span></span>
<span data-ttu-id="c74e4-106">Erstellen eines Speicherobjekts für loadBalancerConfiguration</span><span class="sxs-lookup"><span data-stu-id="c74e4-106">Create a in-memory object for LoadBalancerConfiguration</span></span>

## <span data-ttu-id="c74e4-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c74e4-107">EXAMPLES</span></span>

### <span data-ttu-id="c74e4-108">Beispiel 1: Erstellen eines Load Balancer-Konfigurationsobjekts</span><span class="sxs-lookup"><span data-stu-id="c74e4-108">Example 1: Create load balancer configuration object</span></span>
```powershell
PS C:\> $publicIP = Get-AzPublicIpAddress -ResourceGroupName 'ContosoOrg' -Name 'ContosoPublicIP'
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIP.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
```

<span data-ttu-id="c74e4-109">Mit diesem Befehl wird ein Konfigurationsobjekt für den Lastenausgleich erstellt, das zum Erstellen oder Aktualisieren eines Clouddiensts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c74e4-109">This command creates load balancer configuration object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="c74e4-110">Weitere Details finden Sie unter "New-AzCloudService".</span><span class="sxs-lookup"><span data-stu-id="c74e4-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="c74e4-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c74e4-111">PARAMETERS</span></span>

### <span data-ttu-id="c74e4-112">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c74e4-112">-FrontendIPConfiguration</span></span>
<span data-ttu-id="c74e4-113">FrontendIPConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c74e4-113">FrontendIPConfiguration.</span></span>
<span data-ttu-id="c74e4-114">Informationen zum Erstellen finden Sie im Abschnitt "NOTES" zu den FrontENDIPCONFIGURATION-Eigenschaften und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="c74e4-114">To construct, see NOTES section for FRONTENDIPCONFIGURATION properties and create a hash table.</span></span>

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

### <span data-ttu-id="c74e4-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c74e4-115">-Name</span></span>
<span data-ttu-id="c74e4-116">Name der LoadBalancerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c74e4-116">Name of LoadBalancerConfiguration.</span></span>

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

### <span data-ttu-id="c74e4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c74e4-117">CommonParameters</span></span>
<span data-ttu-id="c74e4-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c74e4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c74e4-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c74e4-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c74e4-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c74e4-120">INPUTS</span></span>

## <span data-ttu-id="c74e4-121">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c74e4-121">OUTPUTS</span></span>

### <span data-ttu-id="c74e4-122">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.LoadBalancerConfiguration</span><span class="sxs-lookup"><span data-stu-id="c74e4-122">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.LoadBalancerConfiguration</span></span>

## <span data-ttu-id="c74e4-123">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c74e4-123">NOTES</span></span>

<span data-ttu-id="c74e4-124">ALIASE</span><span class="sxs-lookup"><span data-stu-id="c74e4-124">ALIASES</span></span>

<span data-ttu-id="c74e4-125">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="c74e4-125">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c74e4-126">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c74e4-126">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c74e4-127">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c74e4-127">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c74e4-128">FRONTENDIPCONFIGURATION <ILoadBalancerFrontendIPConfiguration[]>: FrontendIPConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c74e4-128">FRONTENDIPCONFIGURATION <ILoadBalancerFrontendIPConfiguration[]>: FrontendIPConfiguration.</span></span>
  - <span data-ttu-id="c74e4-129">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="c74e4-129">`[Name <String>]`:</span></span> 
  - <span data-ttu-id="c74e4-130">`[PrivateIPAddress <String>]`: Die private IP-Adresse, auf die der Clouddienst verwiesen hat.</span><span class="sxs-lookup"><span data-stu-id="c74e4-130">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
  - <span data-ttu-id="c74e4-131">`[PublicIPAddressId <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="c74e4-131">`[PublicIPAddressId <String>]`: Resource Id</span></span>
  - <span data-ttu-id="c74e4-132">`[SubnetId <String>]`: Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="c74e4-132">`[SubnetId <String>]`: Resource Id</span></span>

## <span data-ttu-id="c74e4-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c74e4-133">RELATED LINKS</span></span>

