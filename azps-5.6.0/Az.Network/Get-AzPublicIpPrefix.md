---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpPrefix.md
ms.openlocfilehash: 6083c87ddf0bd7b2306fdacc6d109ccebc144faa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919667"
---
# <span data-ttu-id="ec128-101">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="ec128-101">Get-AzPublicIpPrefix</span></span>

## <span data-ttu-id="ec128-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec128-102">SYNOPSIS</span></span>
<span data-ttu-id="ec128-103">Ruft ein öffentliches IP-Präfix ab</span><span class="sxs-lookup"><span data-stu-id="ec128-103">Gets a public IP prefix</span></span>

## <span data-ttu-id="ec128-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ec128-104">SYNTAX</span></span>

### <span data-ttu-id="ec128-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ec128-105">ListParameterSet (Default)</span></span>
```
Get-AzPublicIpPrefix [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ec128-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec128-106">GetByResourceIdParameterSet</span></span>
```
Get-AzPublicIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec128-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ec128-107">DESCRIPTION</span></span>
<span data-ttu-id="ec128-108">Das **Get-AzPublicIpPrefix-Cmdlet** ruft mindestens ein öffentliches IP-Präfix in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="ec128-108">The **Get-AzPublicIpPrefix** cmdlet gets one or more public IP prefixes in a resource group.</span></span>

## <span data-ttu-id="ec128-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ec128-109">EXAMPLES</span></span>

### <span data-ttu-id="ec128-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ec128-110">Example 1</span></span>
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

<span data-ttu-id="ec128-111">Dieser Befehl ruft eine öffentliche IP-Präfixressource mit myPublicIpPrefix1 in der Ressourcengruppe myRg ab.</span><span class="sxs-lookup"><span data-stu-id="ec128-111">This command gets a public IP prefix resource with myPublicIpPrefix1 in resource group myRg</span></span>

### <span data-ttu-id="ec128-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ec128-112">Example 2</span></span>
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

<span data-ttu-id="ec128-113">Dieser Befehl ruft alle öffentlichen IP-Präfixressourcen ab, die mit myPublicIpPrefix beginnen.</span><span class="sxs-lookup"><span data-stu-id="ec128-113">This command gets all public IP prefix resources that start with myPublicIpPrefix.</span></span>

## <span data-ttu-id="ec128-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ec128-114">PARAMETERS</span></span>

### <span data-ttu-id="ec128-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec128-115">-DefaultProfile</span></span>
<span data-ttu-id="ec128-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ec128-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec128-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ec128-117">-Name</span></span>
<span data-ttu-id="ec128-118">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="ec128-118">The resource name.</span></span>

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

### <span data-ttu-id="ec128-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec128-119">-ResourceGroupName</span></span>
<span data-ttu-id="ec128-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ec128-120">The resource group name.</span></span>

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

### <span data-ttu-id="ec128-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec128-121">-ResourceId</span></span>
<span data-ttu-id="ec128-122">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="ec128-122">The resource Id.</span></span>

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

### <span data-ttu-id="ec128-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec128-123">CommonParameters</span></span>
<span data-ttu-id="ec128-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec128-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec128-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec128-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec128-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ec128-126">INPUTS</span></span>

### <span data-ttu-id="ec128-127">System.String</span><span class="sxs-lookup"><span data-stu-id="ec128-127">System.String</span></span>

## <span data-ttu-id="ec128-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ec128-128">OUTPUTS</span></span>

### <span data-ttu-id="ec128-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="ec128-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="ec128-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ec128-130">NOTES</span></span>

## <span data-ttu-id="ec128-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ec128-131">RELATED LINKS</span></span>

[<span data-ttu-id="ec128-132">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="ec128-132">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="ec128-133">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="ec128-133">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="ec128-134">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="ec128-134">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
