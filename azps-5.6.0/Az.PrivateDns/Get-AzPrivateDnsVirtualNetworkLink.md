---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/powershell/module/az.privatedns/get-azprivatednsvirtualnetworklink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 81f71e455e28403d4d54e5ddca80e2d02b0699f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941464"
---
# <span data-ttu-id="c689a-101">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="c689a-101">Get-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="c689a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c689a-102">SYNOPSIS</span></span>
<span data-ttu-id="c689a-103">Ruft einen virtuellen Netzwerklink ab, der der angegebenen privaten DNS-Zone zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c689a-103">Gets a virtual network link associated with the specified Private DNS zone.</span></span>

## <span data-ttu-id="c689a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c689a-104">SYNTAX</span></span>

```
Get-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c689a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c689a-105">DESCRIPTION</span></span>
<span data-ttu-id="c689a-106">Das **Get-AzPrivateDnsVirtualNetworkLink-Cmdlet** ruft virtuelle Netzwerkverbindungen ab, die mit einer bestimmten privaten DNS-Zone verknüpft sind, aus der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c689a-106">The **Get-AzPrivateDnsVirtualNetworkLink** cmdlet gets virtual network links associated with a particular Private DNS zone from the specified resource group.</span></span>
<span data-ttu-id="c689a-107">Wenn Sie den *Parameter Name* angeben, wird ein **einzelnes PSPrivateDnsVirtualNetworkLink-Objekt** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c689a-107">If you specify the *Name* parameter, a single **PSPrivateDnsVirtualNetworkLink** object is returned.</span></span>
<span data-ttu-id="c689a-108">Wenn Sie den  Parameter Name nicht angeben, wird ein Array zurückgegeben, das alle Links enthält, die der Zone in der angegebenen Ressourcengruppe zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c689a-108">If you do not specify the *Name* parameter, an array containing all of the links associated with the zone in the specified resource group is returned.</span></span>
<span data-ttu-id="c689a-109">Sie können das **PSPrivateDnsVirtualNetworkLink-Objekt** verwenden, um den Link zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c689a-109">You can use the **PSPrivateDnsVirtualNetworkLink** object to update the link.</span></span>

## <span data-ttu-id="c689a-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c689a-110">EXAMPLES</span></span>

### <span data-ttu-id="c689a-111">Beispiel 1: Erstellen eines virtuellen Netzwerklinks</span><span class="sxs-lookup"><span data-stu-id="c689a-111">Example 1: Get a virtual network link.</span></span>
```
PS C:\> $Link = Get-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "mylink"

The link object returned looks like the following:

Name                    : mylink
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {tag1}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded
```

<span data-ttu-id="c689a-112">In diesem Beispiel wird der mylink des virtuellen Netzwerks, der der Privaten DNS-Zone mit dem Namen myzone.com aus der angegebenen Ressourcengruppe zugeordnet ist, und speichert sie dann in der $Link-Variable.</span><span class="sxs-lookup"><span data-stu-id="c689a-112">This example gets the virtual network link mylink associated with the Private DNS zone named myzone.com from the specified resource group, and then stores it in the $Link variable.</span></span>

### <span data-ttu-id="c689a-113">Beispiel 2: Alle Verknüpfungen, die einer Zone in einer Ressourcengruppe zugeordnet sind, erhalten.</span><span class="sxs-lookup"><span data-stu-id="c689a-113">Example 2: Get all of the links associated with a zone in a resource group.</span></span>
```
PS C:\> $Links = Get-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"

Name                    : mylink1
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink1
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {tag1}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded

Name                    : mylink2
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink2
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {tag1}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded
```

<span data-ttu-id="c689a-114">In diesem Beispiel werden alle virtuellen Netzwerkverbindungen, die der Privaten DNS-Zone "myzone.com" in der angegebenen Ressourcengruppe zugeordnet sind, und dann in der Variablen $Links gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c689a-114">This example gets all of the virtual network links associated with the Private DNS zone "myzone.com" in the specified resource group, and then stores it in the $Links variable.</span></span>

## <span data-ttu-id="c689a-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c689a-115">PARAMETERS</span></span>

### <span data-ttu-id="c689a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c689a-116">-DefaultProfile</span></span>
<span data-ttu-id="c689a-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="c689a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c689a-118">-Name</span><span class="sxs-lookup"><span data-stu-id="c689a-118">-Name</span></span>
<span data-ttu-id="c689a-119">Gibt den Namen der zu erhaltenden virtuellen Netzwerkverknüpfung an.</span><span class="sxs-lookup"><span data-stu-id="c689a-119">Specifies the name of the virtual network link to get.</span></span>
<span data-ttu-id="c689a-120">Wenn Sie keinen Wert für den Parameter *Name* angeben, ruft dieses Cmdlet alle Links ab, die der angegebenen privaten DNS-Zone in der angegebenen Ressourcengruppe zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c689a-120">If you do not specify a value for the *Name* parameter, this cmdlet gets all links associated with the specified Private DNS zone in the specified resource group.</span></span>

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

### <span data-ttu-id="c689a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c689a-121">-ResourceGroupName</span></span>
<span data-ttu-id="c689a-122">Gibt den Namen der Ressourcengruppe an, die den zu erhaltenden virtuellen Netzwerklink enthält.</span><span class="sxs-lookup"><span data-stu-id="c689a-122">Specifies the name of the resource group that contains the virtual network link to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c689a-123">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="c689a-123">-ZoneName</span></span>
<span data-ttu-id="c689a-124">Gibt den Namen der privaten DNS-Zone an, mit der die Virtuelle Netzwerkverknüpfung verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="c689a-124">Specifies the name of the Private DNS zone that the virtual network link is linked to.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c689a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c689a-125">CommonParameters</span></span>
<span data-ttu-id="c689a-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c689a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c689a-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c689a-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c689a-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c689a-128">INPUTS</span></span>

### <span data-ttu-id="c689a-129">Keine</span><span class="sxs-lookup"><span data-stu-id="c689a-129">None</span></span>

## <span data-ttu-id="c689a-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c689a-130">OUTPUTS</span></span>

### <span data-ttu-id="c689a-131">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="c689a-131">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="c689a-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c689a-132">NOTES</span></span>

## <span data-ttu-id="c689a-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c689a-133">RELATED LINKS</span></span>

[<span data-ttu-id="c689a-134">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="c689a-134">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="c689a-135">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="c689a-135">Remove-AzPrivateDnsVirtualNetworkLink</span></span>](./Remove-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="c689a-136">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="c689a-136">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)
