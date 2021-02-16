---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 91D58F60-F22A-454A-B04C-E5AEF33E9D06
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewall.md
ms.openlocfilehash: 71fff2d475c5cf3045be8aa4c628776b0dd42dc7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161113"
---
# <span data-ttu-id="a20e3-101">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="a20e3-101">Get-AzFirewall</span></span>

## <span data-ttu-id="a20e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a20e3-102">SYNOPSIS</span></span>
<span data-ttu-id="a20e3-103">Ruft eine Azure Firewall ab.</span><span class="sxs-lookup"><span data-stu-id="a20e3-103">Gets a Azure Firewall.</span></span>

## <span data-ttu-id="a20e3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a20e3-104">SYNTAX</span></span>

```
Get-AzFirewall [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a20e3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a20e3-105">DESCRIPTION</span></span>
<span data-ttu-id="a20e3-106">Das **Cmdlet "Get-AzFirewall"** ruft eine oder mehrere Firewalls in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="a20e3-106">The **Get-AzFirewall** cmdlet gets one or more Firewalls in a resource group.</span></span>

## <span data-ttu-id="a20e3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a20e3-107">EXAMPLES</span></span>

### <span data-ttu-id="a20e3-108">1: Abrufen aller Firewalls in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="a20e3-108">1:  Retrieve all Firewalls in a resource group</span></span>
```
Get-AzFirewall -ResourceGroupName rgName

Name                       : azFw
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}

Name                       : azFw1
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw1
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw1/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}
```

<span data-ttu-id="a20e3-109">In diesem Beispiel werden alle Firewalls in der Ressourcengruppe "rgName" abgerufen.</span><span class="sxs-lookup"><span data-stu-id="a20e3-109">This example retrieves all Firewalls in resource group "rgName".</span></span>

### <span data-ttu-id="a20e3-110">2: Abrufen einer Firewall nach Name</span><span class="sxs-lookup"><span data-stu-id="a20e3-110">2:  Retrieve a Firewall by name</span></span>
```
Get-AzFirewall -ResourceGroupName rgName -Name azFw

Name                       : azFw
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}
```

<span data-ttu-id="a20e3-111">In diesem Beispiel wird die Firewall mit dem Namen "azFw" in der Ressourcengruppe "rgName" abgerufen.</span><span class="sxs-lookup"><span data-stu-id="a20e3-111">This example retrieves Firewall named "azFw" in resource group "rgName".</span></span>

### <span data-ttu-id="a20e3-112">3: Abrufen aller Firewalls durch Filtern</span><span class="sxs-lookup"><span data-stu-id="a20e3-112">3:  Retrieve all Firewalls with filtering</span></span>
```
Get-AzFirewall -Name azFw*

Name                       : azFw
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}

Name                       : azFw1
ResourceGroupName          : rgName
Location                   : westcentralus
Id                         : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/providers/Micros
                             oft.Network/azureFirewalls/azFw1
Etag                       : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid               :
ProvisioningState          : Succeeded
Tags                       :
IpConfigurations           : [
                               {
                                 "Name": "AzureFirewallIpConfiguration",
                                 "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                 "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/provi
                             ders/Microsoft.Network/azureFirewalls/azFw1/azureFirewallIpConfigurations/AzureFirewallIp
                             Configuration",
                                 "PrivateIPAddress": "x.x.x.x",
                                 "Subnet": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/virtualNetworks/vnetname/subnets/AzureFirewallSubnet"
                                 },
                                 "PublicIpAddress": {
                                   "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rgName/pro
                             viders/Microsoft.Network/publicIPAddresses/publicipname"
                                 }
                               }
                             ]
ApplicationRuleCollections : []
NatRuleCollections         : []
NetworkRuleCollections     : []
Zones                      : {}
```

<span data-ttu-id="a20e3-113">In diesem Beispiel werden alle Firewalls abgerufen, die mit "azFw" beginnen.</span><span class="sxs-lookup"><span data-stu-id="a20e3-113">This example retrieves all Firewalls that start with "azFw"</span></span>

### <span data-ttu-id="a20e3-114">4: Abrufen einer Firewall und anschließendes Hinzufügen einer Anwendungsregelsammlung zur Firewall</span><span class="sxs-lookup"><span data-stu-id="a20e3-114">4:  Retrieve a firewall and then add a application rule collection to the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$appRule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$appRuleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $appRule -ActionType "Allow"
$azFw.AddApplicationRuleCollection($appRuleCollection)
```

<span data-ttu-id="a20e3-115">In diesem Beispiel wird eine Firewall abgerufen und dann durch Aufrufen der Methode "AddApplicationRuleCollection" eine Anwendungsregelsammlung zur Firewall hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a20e3-115">This example retrieves a firewall, then adds a application rule collection to the firewall by calling method AddApplicationRuleCollection.</span></span>

### <span data-ttu-id="a20e3-116">5: Abrufen einer Firewall und anschließendes Hinzufügen einer Netzwerkregelsammlung zur Firewall</span><span class="sxs-lookup"><span data-stu-id="a20e3-116">5:  Retrieve a firewall and then add a network rule collection to the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$netRule = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol "UDP" -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$netRuleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $netRule -ActionType "Allow"
$azFw.AddNetworkRuleCollection($netRuleCollection)
```

<span data-ttu-id="a20e3-117">In diesem Beispiel wird eine Firewall abgerufen und der Firewall dann eine Netzwerkregelsammlung hinzugefügt, indem die Methode "AddNetworkRuleCollection" aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a20e3-117">This example retrieves a firewall, then adds a network rule collection to the firewall by calling method AddNetworkRuleCollection.</span></span>

### <span data-ttu-id="a20e3-118">6: Abrufen einer Firewall und anschließendes Abrufen einer Anwendungsregelsammlung nach Namen aus der Firewall</span><span class="sxs-lookup"><span data-stu-id="a20e3-118">6:  Retrieve a firewall and then retrieve a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$getAppRc=$azFw.GetApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="a20e3-119">In diesem Beispiel wird eine Firewall abgerufen, und anschließend wird eine Regelsammlung nach Name und Aufrufmethode "GetApplicationRuleCollectionByName" für das Firewallobjekt abgerufen.</span><span class="sxs-lookup"><span data-stu-id="a20e3-119">This example retrieves a firewall and then gets a rule collection by name, calling method GetApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="a20e3-120">Beim Regelsammlungsnamen für die Methode "GetApplicationRuleCollectionByName" wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="a20e3-120">The rule collection name for method GetApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="a20e3-121">7: Abrufen einer Firewall und anschließendes Abrufen einer Netzwerkregelsammlung nach Namen aus der Firewall</span><span class="sxs-lookup"><span data-stu-id="a20e3-121">7:  Retrieve a firewall and then retrieve a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$getNetRc=$azFw.GetNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="a20e3-122">In diesem Beispiel wird eine Firewall abgerufen, und anschließend wird eine Regelsammlung nach Name und Aufrufmethode "GetNetworkRuleCollectionByName" für das Firewallobjekt abgerufen.</span><span class="sxs-lookup"><span data-stu-id="a20e3-122">This example retrieves a firewall and then gets a rule collection by name, calling method GetNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="a20e3-123">Beim Regelsammlungsnamen für die Methode "GetNetworkRuleCollectionByName" wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="a20e3-123">The rule collection name for method GetNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="a20e3-124">8: Abrufen einer Firewall und anschließendes Entfernen einer Anwendungsregelsammlung nach Namen aus der Firewall</span><span class="sxs-lookup"><span data-stu-id="a20e3-124">8:  Retrieve a firewall and then remove a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="a20e3-125">In diesem Beispiel wird eine Firewall abgerufen und dann eine Regelsammlung nach Name und Aufrufmethode "RemoveApplicationRuleCollectionByName" für das Firewallobjekt entfernt.</span><span class="sxs-lookup"><span data-stu-id="a20e3-125">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="a20e3-126">Beim Regelsammlungsnamen für die Methode "RemoveApplicationRuleCollectionByName" wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="a20e3-126">The rule collection name for method RemoveApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="a20e3-127">9: Abrufen einer Firewall und anschließendes Entfernen einer Netzwerkregelsammlung nach Namen aus der Firewall</span><span class="sxs-lookup"><span data-stu-id="a20e3-127">9:  Retrieve a firewall and then remove a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="a20e3-128">In diesem Beispiel wird eine Firewall abgerufen und dann eine Regelsammlung nach Name und Aufrufmethode "RemoveNetworkRuleCollectionByName" für das Firewallobjekt entfernt.</span><span class="sxs-lookup"><span data-stu-id="a20e3-128">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="a20e3-129">Beim Regelsammlungsnamen für die Methode "RemoveNetworkRuleCollectionByName" wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="a20e3-129">The rule collection name for method RemoveNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="a20e3-130">10: Abrufen einer Firewall und Zuweisen der Firewall</span><span class="sxs-lookup"><span data-stu-id="a20e3-130">10:  Retrieve a firewall and then allocate the firewall</span></span>
```
$vnet=Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName "rgName"
$publicIp=Get-AzPublicIpAddress -Name "firewallpip" -ResourceGroupName "rgName"
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.Allocate($vnet, $publicIp)
```

<span data-ttu-id="a20e3-131">Dieses Beispiel ruft eine Firewall ab und ruft "Allocate" für die Firewall auf, um den Firewalldienst mit der Konfiguration (Anwendungs- und Netzwerkregelsammlungen) zu starten, die der Firewall zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a20e3-131">This example retrieves a firewall and calls Allocate on the firewall to start the firewall service using the configuration (application and network rule collections) associated with the firewall.</span></span>

## <span data-ttu-id="a20e3-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a20e3-132">PARAMETERS</span></span>

### <span data-ttu-id="a20e3-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a20e3-133">-DefaultProfile</span></span>
<span data-ttu-id="a20e3-134">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a20e3-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a20e3-135">-Name</span><span class="sxs-lookup"><span data-stu-id="a20e3-135">-Name</span></span>
<span data-ttu-id="a20e3-136">Gibt den Namen der Firewall an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="a20e3-136">Specifies the name of the Firewall that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a20e3-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a20e3-137">-ResourceGroupName</span></span>
<span data-ttu-id="a20e3-138">Gibt den Namen der Ressourcengruppe an, zu der die Firewall gehört.</span><span class="sxs-lookup"><span data-stu-id="a20e3-138">Specifies the name of the resource group that Firewall belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a20e3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a20e3-139">CommonParameters</span></span>
<span data-ttu-id="a20e3-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a20e3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a20e3-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a20e3-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a20e3-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a20e3-142">INPUTS</span></span>

### <span data-ttu-id="a20e3-143">System.String</span><span class="sxs-lookup"><span data-stu-id="a20e3-143">System.String</span></span>

## <span data-ttu-id="a20e3-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a20e3-144">OUTPUTS</span></span>

### <span data-ttu-id="a20e3-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="a20e3-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="a20e3-146">System.Collections.Generic.IEnumerable'1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="a20e3-146">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a20e3-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a20e3-147">NOTES</span></span>

## <span data-ttu-id="a20e3-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a20e3-148">RELATED LINKS</span></span>

[<span data-ttu-id="a20e3-149">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="a20e3-149">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="a20e3-150">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="a20e3-150">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="a20e3-151">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="a20e3-151">Set-AzFirewall</span></span>](./Set-AzFirewall.md)
