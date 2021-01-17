---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzCustomIpPrefix.md
ms.openlocfilehash: ce9d10726cee7aa5a7416048e2e3582c8a42fd74
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473483"
---
# <span data-ttu-id="20754-101">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="20754-101">Get-AzCustomIpPrefix</span></span>

## <span data-ttu-id="20754-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20754-102">SYNOPSIS</span></span>
<span data-ttu-id="20754-103">Ruft eine CustomIpPrefix-Ressource ab</span><span class="sxs-lookup"><span data-stu-id="20754-103">Gets a CustomIpPrefix resource</span></span>

## <span data-ttu-id="20754-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="20754-104">SYNTAX</span></span>

### <span data-ttu-id="20754-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="20754-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzCustomIpPrefix [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="20754-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="20754-106">GetByResourceIdParameterSet</span></span>
```
Get-AzCustomIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20754-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="20754-107">DESCRIPTION</span></span>
<span data-ttu-id="20754-108">Das **Cmdlet "Get-AzCustomIpPrefix"** erhält eine oder mehrere CustomIpPrefixes, wenn der Satz von Eingabeparametern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="20754-108">The **Get-AzCustomIpPrefix** cmdlet gets one or more CustomIpPrefixes given the set of input parameters</span></span>

## <span data-ttu-id="20754-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="20754-109">EXAMPLES</span></span>

### <span data-ttu-id="20754-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="20754-110">Example 1</span></span>
```powershell
PS C:\> Get-AzPublicIpPrefix -ResourceGroupName myRg -Name myCustomIpPrefix

Name                 : myCustomIpPrefix
ResourceGroupName    : myRg
Location             : westus
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/byoip-test-rg/providers/Micro
                       soft.Network/customIPPrefixes/testCustomIpPrefix
Etag                 : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid         : 00000000-0000-0000-0000-000000000000
ProvisioningState    : Succeeded
Tags                 :
Cidr                 : 111.111.111.111/24
CommissionedState    : Provisioning
PublicIpPrefixes     : []
Zones                : {}
```

<span data-ttu-id="20754-111">Dieser Befehl ruft eine CustomIpPrefix-Ressource mit dem Namen "myCustomIpPrefix" in der Ressourcengruppe "myRg" ab.</span><span class="sxs-lookup"><span data-stu-id="20754-111">This command gets a CustomIpPrefix resource named myCustomIpPrefix in resource group myRg</span></span>

## <span data-ttu-id="20754-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20754-112">PARAMETERS</span></span>

### <span data-ttu-id="20754-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20754-113">-DefaultProfile</span></span>
<span data-ttu-id="20754-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="20754-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20754-115">-Name</span><span class="sxs-lookup"><span data-stu-id="20754-115">-Name</span></span>
<span data-ttu-id="20754-116">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="20754-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20754-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20754-117">-ResourceGroupName</span></span>
<span data-ttu-id="20754-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="20754-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20754-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="20754-119">-ResourceId</span></span>
<span data-ttu-id="20754-120">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="20754-120">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20754-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20754-121">CommonParameters</span></span>
<span data-ttu-id="20754-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20754-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20754-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="20754-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20754-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="20754-124">INPUTS</span></span>

### <span data-ttu-id="20754-125">System.String</span><span class="sxs-lookup"><span data-stu-id="20754-125">System.String</span></span>

## <span data-ttu-id="20754-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="20754-126">OUTPUTS</span></span>

### <span data-ttu-id="20754-127">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="20754-127">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="20754-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="20754-128">NOTES</span></span>

## <span data-ttu-id="20754-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="20754-129">RELATED LINKS</span></span>

[<span data-ttu-id="20754-130">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="20754-130">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="20754-131">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="20754-131">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)

[<span data-ttu-id="20754-132">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="20754-132">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)