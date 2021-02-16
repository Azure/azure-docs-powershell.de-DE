---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
ms.openlocfilehash: 567fdda7c4f95a1bcdecab172223608ec78ef1f9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151929"
---
# <span data-ttu-id="8e90d-101">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="8e90d-101">Get-AzPublicIpPrefix</span></span>

## <span data-ttu-id="8e90d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e90d-102">SYNOPSIS</span></span>
<span data-ttu-id="8e90d-103">Ruft ein öffentliches IP-Präfix ab.</span><span class="sxs-lookup"><span data-stu-id="8e90d-103">Gets a public IP prefix</span></span>

## <span data-ttu-id="8e90d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e90d-104">SYNTAX</span></span>

### <span data-ttu-id="8e90d-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8e90d-105">ListParameterSet (Default)</span></span>
```
Get-AzPublicIpPrefix [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8e90d-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e90d-106">GetByResourceIdParameterSet</span></span>
```
Get-AzPublicIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e90d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8e90d-107">DESCRIPTION</span></span>
<span data-ttu-id="8e90d-108">Das **Cmdlet "Get-AzPublicIpPrefix"** ruft mindestens ein öffentliches IP-Präfix in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="8e90d-108">The **Get-AzPublicIpPrefix** cmdlet gets one or more public IP prefixes in a resource group.</span></span>

## <span data-ttu-id="8e90d-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8e90d-109">EXAMPLES</span></span>

### <span data-ttu-id="8e90d-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8e90d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzPublicIpPrefix -ResourceGroupName myRg -Name myPublicIpPrefix1

Name                   : myPublicIpPrefix1
ResourceGroupName      : myRg
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Mic
                         rosoft.Network/publicIPPrefixes/myPublicIpPrefix1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
PublicIpAddressVersion : IPv4
PrefixLength           : 28
IPPrefix               : xx.xx.xx.xx/xx
IdleTimeoutInMinutes   :
Zones                  : {}
Sku                    : {
                           "Name": "Standard",
                           "Tier":"Regional"
                         }
IpTags                 : []
PublicIpAddresses      : []
```

<span data-ttu-id="8e90d-111">Dieser Befehl ruft eine öffentliche IP-Präfixressource mit "myPublicIpPrefix1" in der Ressourcengruppe "myRg" ab.</span><span class="sxs-lookup"><span data-stu-id="8e90d-111">This command gets a public IP prefix resource with myPublicIpPrefix1 in resource group myRg</span></span>

### <span data-ttu-id="8e90d-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8e90d-112">Example 2</span></span>
```powershell
PS C:\> Get-AzPublicIpPrefix -Name myPublicIpPrefix*

Name                   : myPublicIpPrefix1
ResourceGroupName      : myRg
Location               : westus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Mic
                         rosoft.Network/publicIPPrefixes/myPublicIpPrefix1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
PublicIpAddressVersion : IPv4
PrefixLength           : 28
IPPrefix               : xx.xx.xx.xx/xx
IdleTimeoutInMinutes   :
Zones                  : {}
Sku                    : {
                           "Name": "Standard",
                           "Tier": "Regional"
                         }
IpTags                 : []
PublicIpAddresses      : []
```

<span data-ttu-id="8e90d-113">Dieser Befehl ruft alle öffentlichen IP-Präfixressourcen ab, die mit myPublicIpPrefix beginnen.</span><span class="sxs-lookup"><span data-stu-id="8e90d-113">This command gets all public IP prefix resources that start with myPublicIpPrefix.</span></span>

## <span data-ttu-id="8e90d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e90d-114">PARAMETERS</span></span>

### <span data-ttu-id="8e90d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e90d-115">-DefaultProfile</span></span>
<span data-ttu-id="8e90d-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8e90d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e90d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8e90d-117">-Name</span></span>
<span data-ttu-id="8e90d-118">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="8e90d-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="8e90d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e90d-119">-ResourceGroupName</span></span>
<span data-ttu-id="8e90d-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8e90d-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="8e90d-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e90d-121">-ResourceId</span></span>
<span data-ttu-id="8e90d-122">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="8e90d-122">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e90d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e90d-123">CommonParameters</span></span>
<span data-ttu-id="8e90d-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e90d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e90d-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e90d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e90d-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8e90d-126">INPUTS</span></span>

### <span data-ttu-id="8e90d-127">System.String</span><span class="sxs-lookup"><span data-stu-id="8e90d-127">System.String</span></span>

## <span data-ttu-id="8e90d-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8e90d-128">OUTPUTS</span></span>

### <span data-ttu-id="8e90d-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="8e90d-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="8e90d-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8e90d-130">NOTES</span></span>

## <span data-ttu-id="8e90d-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8e90d-131">RELATED LINKS</span></span>

[<span data-ttu-id="8e90d-132">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="8e90d-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="8e90d-133">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="8e90d-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="8e90d-134">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="8e90d-134">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
