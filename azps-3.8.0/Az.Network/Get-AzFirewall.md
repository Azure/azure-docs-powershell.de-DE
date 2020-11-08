---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 91D58F60-F22A-454A-B04C-E5AEF33E9D06
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewall.md
ms.openlocfilehash: d6657c9402eff46d274d982170e167cd97a29a9a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004291"
---
# <span data-ttu-id="54cef-101">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="54cef-101">Get-AzFirewall</span></span>

## <span data-ttu-id="54cef-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="54cef-102">SYNOPSIS</span></span>
<span data-ttu-id="54cef-103">Ruft eine Azure-Firewall ab.</span><span class="sxs-lookup"><span data-stu-id="54cef-103">Gets a Azure Firewall.</span></span>

## <span data-ttu-id="54cef-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="54cef-104">SYNTAX</span></span>

```
Get-AzFirewall [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="54cef-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="54cef-105">DESCRIPTION</span></span>
<span data-ttu-id="54cef-106">Das Cmdlet " **Get-AzFirewall** " ruft mindestens eine Firewall in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="54cef-106">The **Get-AzFirewall** cmdlet gets one or more Firewalls in a resource group.</span></span>

## <span data-ttu-id="54cef-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="54cef-107">EXAMPLES</span></span>

### <span data-ttu-id="54cef-108">1: Abrufen aller Firewalls in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="54cef-108">1:  Retrieve all Firewalls in a resource group</span></span>
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

<span data-ttu-id="54cef-109">In diesem Beispiel werden alle Firewalls in der Ressourcengruppe "rgName" abgerufen.</span><span class="sxs-lookup"><span data-stu-id="54cef-109">This example retrieves all Firewalls in resource group "rgName".</span></span>

### <span data-ttu-id="54cef-110">2: Abrufen einer Firewall nach Namen</span><span class="sxs-lookup"><span data-stu-id="54cef-110">2:  Retrieve a Firewall by name</span></span>
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

<span data-ttu-id="54cef-111">In diesem Beispiel wird die Firewall mit dem Namen "azFw" in der Ressourcengruppe "rgName" abgerufen.</span><span class="sxs-lookup"><span data-stu-id="54cef-111">This example retrieves Firewall named "azFw" in resource group "rgName".</span></span>

### <span data-ttu-id="54cef-112">3: Abrufen aller Firewalls mit Filterung</span><span class="sxs-lookup"><span data-stu-id="54cef-112">3:  Retrieve all Firewalls with filtering</span></span>
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

<span data-ttu-id="54cef-113">In diesem Beispiel werden alle Firewalls abgerufen, die mit "azFw" beginnen.</span><span class="sxs-lookup"><span data-stu-id="54cef-113">This example retrieves all Firewalls that start with "azFw"</span></span>

### <span data-ttu-id="54cef-114">4: Abrufen einer Firewall und anschließendes Hinzufügen einer Anwendungsregel Sammlung zur Firewall</span><span class="sxs-lookup"><span data-stu-id="54cef-114">4:  Retrieve a firewall and then add a application rule collection to the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$appRule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$appRuleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $appRule -ActionType "Allow"
$azFw.AddApplicationRuleCollection($appRuleCollection)
```

<span data-ttu-id="54cef-115">In diesem Beispiel wird eine Firewall abgerufen und dann der Firewall eine Anwendungsregel Sammlung hinzugefügt, indem die AddApplicationRuleCollection-Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="54cef-115">This example retrieves a firewall, then adds a application rule collection to the firewall by calling method AddApplicationRuleCollection.</span></span>

### <span data-ttu-id="54cef-116">5: Abrufen einer Firewall und anschließendes Hinzufügen einer Netzwerkregel Sammlung zur Firewall</span><span class="sxs-lookup"><span data-stu-id="54cef-116">5:  Retrieve a firewall and then add a network rule collection to the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$netRule = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol "Udp" -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$netRuleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $netRule -ActionType "Allow"
$azFw.AddNetworkRuleCollection($netRuleCollection)
```

<span data-ttu-id="54cef-117">In diesem Beispiel wird eine Firewall abgerufen und dann der Firewall eine Netzwerkregel Sammlung hinzugefügt, indem die AddNetworkRuleCollection-Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="54cef-117">This example retrieves a firewall, then adds a network rule collection to the firewall by calling method AddNetworkRuleCollection.</span></span>

### <span data-ttu-id="54cef-118">6: Abrufen einer Firewall und anschließendes Abrufen einer APP-Regelsammlung nach Namen aus der Firewall</span><span class="sxs-lookup"><span data-stu-id="54cef-118">6:  Retrieve a firewall and then retrieve a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$getAppRc=$azFw.GetApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="54cef-119">In diesem Beispiel wird eine Firewall abgerufen, und dann wird eine Regelsammlung nach Name aufgerufen, die für das GetApplicationRuleCollectionByName-Objekt aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="54cef-119">This example retrieves a firewall and then gets a rule collection by name, calling method GetApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="54cef-120">Der Name der Regelsammlung für Methoden-GetApplicationRuleCollectionByName ist keine Unterscheidung nach Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="54cef-120">The rule collection name for method GetApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="54cef-121">7: Abrufen einer Firewall und Abrufen einer Netzwerkregel Sammlung nach Namen aus der Firewall</span><span class="sxs-lookup"><span data-stu-id="54cef-121">7:  Retrieve a firewall and then retrieve a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$getNetRc=$azFw.GetNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="54cef-122">In diesem Beispiel wird eine Firewall abgerufen, und dann wird eine Regelsammlung nach Name aufgerufen, die für das GetNetworkRuleCollectionByName-Objekt aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="54cef-122">This example retrieves a firewall and then gets a rule collection by name, calling method GetNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="54cef-123">Der Name der Regelsammlung für Methoden-GetNetworkRuleCollectionByName ist keine Unterscheidung nach Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="54cef-123">The rule collection name for method GetNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="54cef-124">8: Abrufen einer Firewall und anschließendes Entfernen einer Anwendungsregel Sammlung nach Namen aus der Firewall</span><span class="sxs-lookup"><span data-stu-id="54cef-124">8:  Retrieve a firewall and then remove a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="54cef-125">In diesem Beispiel wird eine Firewall abgerufen, und anschließend wird eine Regelsammlung nach Name aufgerufen, wobei die RemoveApplicationRuleCollectionByName-Methode für das Firewall-Objekt aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="54cef-125">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="54cef-126">Der Name der Regelsammlung für Methoden-RemoveApplicationRuleCollectionByName ist keine Unterscheidung nach Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="54cef-126">The rule collection name for method RemoveApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="54cef-127">9: Abrufen einer Firewall und Entfernen einer Netzwerkregel Sammlung nach Namen aus der Firewall</span><span class="sxs-lookup"><span data-stu-id="54cef-127">9:  Retrieve a firewall and then remove a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="54cef-128">In diesem Beispiel wird eine Firewall abgerufen, und anschließend wird eine Regelsammlung nach Name aufgerufen, wobei die RemoveNetworkRuleCollectionByName-Methode für das Firewall-Objekt aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="54cef-128">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="54cef-129">Der Name der Regelsammlung für Methoden-RemoveNetworkRuleCollectionByName ist keine Unterscheidung nach Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="54cef-129">The rule collection name for method RemoveNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="54cef-130">10: Abrufen einer Firewall und Zuweisen der Firewall</span><span class="sxs-lookup"><span data-stu-id="54cef-130">10:  Retrieve a firewall and then allocate the firewall</span></span>
```
$vnet=Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName "rgName"
$publicIp=Get-AzPublicIpAddress -Name "firewallpip" -ResourceGroupName "rgName"
$azFw=Get-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.Allocate($vnet, $publicIp)
```

<span data-ttu-id="54cef-131">In diesem Beispiel wird eine Firewall abgerufen und die Zuweisung für die Firewall aufgerufen, um den Firewalldienst mithilfe der Konfiguration (Anwendung und Netzwerkregel Sammlungen) zu starten, die der Firewall zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="54cef-131">This example retrieves a firewall and calls Allocate on the firewall to start the firewall service using the configuration (application and network rule collections) associated with the firewall.</span></span>

## <span data-ttu-id="54cef-132">Parameter</span><span class="sxs-lookup"><span data-stu-id="54cef-132">PARAMETERS</span></span>

### <span data-ttu-id="54cef-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54cef-133">-DefaultProfile</span></span>
<span data-ttu-id="54cef-134">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="54cef-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54cef-135">-Name</span><span class="sxs-lookup"><span data-stu-id="54cef-135">-Name</span></span>
<span data-ttu-id="54cef-136">Gibt den Namen der Firewall an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="54cef-136">Specifies the name of the Firewall that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="54cef-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54cef-137">-ResourceGroupName</span></span>
<span data-ttu-id="54cef-138">Gibt den Namen der Ressourcengruppe an, zu der die Firewall gehört.</span><span class="sxs-lookup"><span data-stu-id="54cef-138">Specifies the name of the resource group that Firewall belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="54cef-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54cef-139">CommonParameters</span></span>
<span data-ttu-id="54cef-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54cef-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54cef-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54cef-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54cef-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="54cef-142">INPUTS</span></span>

### <span data-ttu-id="54cef-143">System. String</span><span class="sxs-lookup"><span data-stu-id="54cef-143">System.String</span></span>

## <span data-ttu-id="54cef-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="54cef-144">OUTPUTS</span></span>

### <span data-ttu-id="54cef-145">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="54cef-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="54cef-146">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. Models. PSAzureFirewall, Microsoft. Azure. PowerShell. Cmdlets. Network, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="54cef-146">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="54cef-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="54cef-147">NOTES</span></span>

## <span data-ttu-id="54cef-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="54cef-148">RELATED LINKS</span></span>

[<span data-ttu-id="54cef-149">Neu – AzFirewall</span><span class="sxs-lookup"><span data-stu-id="54cef-149">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="54cef-150">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="54cef-150">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="54cef-151">Satz-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="54cef-151">Set-AzFirewall</span></span>](./Set-AzFirewall.md)
