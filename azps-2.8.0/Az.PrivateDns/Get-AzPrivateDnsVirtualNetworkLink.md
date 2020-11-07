---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/get-azprivatednsvirtualnetworklink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 3aea2414a4b7fdfbc14e65d4d087bb7e31206aa2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824519"
---
# <span data-ttu-id="d568c-101">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="d568c-101">Get-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="d568c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d568c-102">SYNOPSIS</span></span>
<span data-ttu-id="d568c-103">Ruft einen virtuellen Netzwerk Link ab, der der angegebenen privaten DNS-Zone zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d568c-103">Gets a virtual network link associated with the specified Private DNS zone.</span></span>

## <span data-ttu-id="d568c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d568c-104">SYNTAX</span></span>

```
Get-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d568c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d568c-105">DESCRIPTION</span></span>
<span data-ttu-id="d568c-106">Das Cmdlet " **Get-AzPrivateDnsVirtualNetworkLink** " ruft virtuelle Netzwerk links ab, die einer bestimmten privaten DNS-Zone aus der angegebenen Ressourcengruppe zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d568c-106">The **Get-AzPrivateDnsVirtualNetworkLink** cmdlet gets virtual network links associated with a particular Private DNS zone from the specified resource group.</span></span>
<span data-ttu-id="d568c-107">Wenn Sie den Parameter *Name* angeben, wird ein einzelnes **PSPrivateDnsVirtualNetworkLink** -Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d568c-107">If you specify the *Name* parameter, a single **PSPrivateDnsVirtualNetworkLink** object is returned.</span></span>
<span data-ttu-id="d568c-108">Wenn Sie den Parameter *Name* nicht angeben, wird ein Array zurückgegeben, das alle Links enthält, die der Zone in der angegebenen Ressourcengruppe zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d568c-108">If you do not specify the *Name* parameter, an array containing all of the links associated with the zone in the specified resource group is returned.</span></span>
<span data-ttu-id="d568c-109">Sie können das **PSPrivateDnsVirtualNetworkLink** -Objekt verwenden, um die Verknüpfung zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="d568c-109">You can use the **PSPrivateDnsVirtualNetworkLink** object to update the link.</span></span>

## <span data-ttu-id="d568c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d568c-110">EXAMPLES</span></span>

### <span data-ttu-id="d568c-111">Beispiel 1: Abrufen eines virtuellen Netzwerk Links.</span><span class="sxs-lookup"><span data-stu-id="d568c-111">Example 1: Get a virtual network link.</span></span>
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

<span data-ttu-id="d568c-112">Dieses Beispiel ruft den virtuellen Netzwerk Link MyLink ab, der der privaten DNS-Zone namens MyZone.com aus der angegebenen Ressourcengruppe zugeordnet ist, und speichert ihn dann in der $Link-Variablen.</span><span class="sxs-lookup"><span data-stu-id="d568c-112">This example gets the virtual network link mylink associated with the Private DNS zone named myzone.com from the specified resource group, and then stores it in the $Link variable.</span></span>

### <span data-ttu-id="d568c-113">Beispiel 2: Abrufen aller Links, die einer Zone in einer Ressourcengruppe zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d568c-113">Example 2: Get all of the links associated with a zone in a resource group.</span></span>
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

<span data-ttu-id="d568c-114">In diesem Beispiel werden alle virtuellen Netzwerk Links abgerufen, die der privaten DNS-Zone "MyZone.com" in der angegebenen Ressourcengruppe zugeordnet sind, und dann in der $Links-Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d568c-114">This example gets all of the virtual network links associated with the Private DNS zone "myzone.com" in the specified resource group, and then stores it in the $Links variable.</span></span>

## <span data-ttu-id="d568c-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="d568c-115">PARAMETERS</span></span>

### <span data-ttu-id="d568c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d568c-116">-DefaultProfile</span></span>
<span data-ttu-id="d568c-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d568c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d568c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d568c-118">-Name</span></span>
<span data-ttu-id="d568c-119">Gibt den Namen des abzurufenden virtuellen Netzwerk Links an.</span><span class="sxs-lookup"><span data-stu-id="d568c-119">Specifies the name of the virtual network link to get.</span></span>
<span data-ttu-id="d568c-120">Wenn Sie keinen Wert für den Parameter *Name* angeben, ruft dieses Cmdlet alle Verknüpfungen ab, die der angegebenen privaten DNS-Zone in der angegebenen Ressourcengruppe zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d568c-120">If you do not specify a value for the *Name* parameter, this cmdlet gets all links associated with the specified Private DNS zone in the specified resource group.</span></span>

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

### <span data-ttu-id="d568c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d568c-121">-ResourceGroupName</span></span>
<span data-ttu-id="d568c-122">Gibt den Namen der Ressourcengruppe an, die den zu erhaltenden virtuellen Netzwerk Link enthält.</span><span class="sxs-lookup"><span data-stu-id="d568c-122">Specifies the name of the resource group that contains the virtual network link to get.</span></span>

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

### <span data-ttu-id="d568c-123">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="d568c-123">-ZoneName</span></span>
<span data-ttu-id="d568c-124">Gibt den Namen der privaten DNS-Zone an, mit der der Link für das virtuelle Netzwerk verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="d568c-124">Specifies the name of the Private DNS zone that the virtual network link is linked to.</span></span>


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

### <span data-ttu-id="d568c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d568c-125">CommonParameters</span></span>
<span data-ttu-id="d568c-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d568c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d568c-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d568c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d568c-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d568c-128">INPUTS</span></span>

### <span data-ttu-id="d568c-129">Keine</span><span class="sxs-lookup"><span data-stu-id="d568c-129">None</span></span>

## <span data-ttu-id="d568c-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d568c-130">OUTPUTS</span></span>

### <span data-ttu-id="d568c-131">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="d568c-131">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="d568c-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="d568c-132">NOTES</span></span>

## <span data-ttu-id="d568c-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d568c-133">RELATED LINKS</span></span>

[<span data-ttu-id="d568c-134">Neu – AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="d568c-134">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="d568c-135">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="d568c-135">Remove-AzPrivateDnsVirtualNetworkLink</span></span>](./Remove-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="d568c-136">Satz-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="d568c-136">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)
