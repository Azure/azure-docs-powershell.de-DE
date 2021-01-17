---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnSite.md
ms.openlocfilehash: 44a40fb446904c8d1bfa40820ae34e0a4aca2caa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365965"
---
# <span data-ttu-id="76908-101">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="76908-101">Get-AzVpnSite</span></span>

## <span data-ttu-id="76908-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76908-102">SYNOPSIS</span></span>
<span data-ttu-id="76908-103">Ruft eine Azure -VpnWebsite-Ressource nach Name ODER ab und listet alle VpnSites in einer Ressourcengruppe oder SubscriptionId auf.</span><span class="sxs-lookup"><span data-stu-id="76908-103">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

<span data-ttu-id="76908-104">Dies ist eine RM-Darstellung von Kundenverzweigungen, die für die Azure für S2S-Konnektivität mit einem virtuellenTex-Hub hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="76908-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="76908-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76908-105">SYNTAX</span></span>

### <span data-ttu-id="76908-106">ListBySubscriptionId (Standard)</span><span class="sxs-lookup"><span data-stu-id="76908-106">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnSite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76908-107">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76908-107">ListByResourceGroupName</span></span>
```
Get-AzVpnSite [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="76908-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="76908-108">DESCRIPTION</span></span>
<span data-ttu-id="76908-109">Ruft eine Azure -VpnSite-Ressource nach Name ODER auf, und führt alle VpnSites in einer Ressourcengruppe oder SubscriptionId auf.</span><span class="sxs-lookup"><span data-stu-id="76908-109">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

## <span data-ttu-id="76908-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="76908-110">EXAMPLES</span></span>

### <span data-ttu-id="76908-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="76908-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"

ResourceGroupName : testRG
Name              : testVpnSite
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="76908-112">Im vorstehenden Beispiel wird in der Ressourcengruppe "testRG" in Azure eine Ressourcengruppe erstellt, virtuelles WAN in west US.</span><span class="sxs-lookup"><span data-stu-id="76908-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="76908-113">Anschließend erstellt sie eine VpnSite zur Darstellung einer Kundenverzweigung und verknüpft sie mit dem virtuellen WAN.</span><span class="sxs-lookup"><span data-stu-id="76908-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="76908-114">Sobald die Website erstellt wurde, ruft sie die Website mithilfe des Befehls Get-AzVpnSite ab.</span><span class="sxs-lookup"><span data-stu-id="76908-114">Once the site is created, it gets the site using the Get-AzVpnSite command.</span></span>

### <span data-ttu-id="76908-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="76908-115">Example 2</span></span>

```powershell
PS C:\> Get-AzVpnSite -Name test*

ResourceGroupName : testRG
Name              : testVpnSite1
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite1
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded

ResourceGroupName : testRG
Name              : testVpnSite2
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite2
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="76908-116">Dieses Cmdlet ruft alle Websites ab, die mit "Test" beginnen.</span><span class="sxs-lookup"><span data-stu-id="76908-116">This cmdlet gets all Sites that start with "test".</span></span>

## <span data-ttu-id="76908-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76908-117">PARAMETERS</span></span>

### <span data-ttu-id="76908-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76908-118">-DefaultProfile</span></span>
<span data-ttu-id="76908-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="76908-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76908-120">-Name</span><span class="sxs-lookup"><span data-stu-id="76908-120">-Name</span></span>
<span data-ttu-id="76908-121">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="76908-121">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnSiteName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76908-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76908-122">-ResourceGroupName</span></span>
<span data-ttu-id="76908-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="76908-123">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76908-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76908-124">CommonParameters</span></span>
<span data-ttu-id="76908-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76908-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76908-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76908-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76908-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="76908-127">INPUTS</span></span>

### <span data-ttu-id="76908-128">Keine</span><span class="sxs-lookup"><span data-stu-id="76908-128">None</span></span>

## <span data-ttu-id="76908-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="76908-129">OUTPUTS</span></span>

### <span data-ttu-id="76908-130">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="76908-130">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="76908-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="76908-131">NOTES</span></span>

## <span data-ttu-id="76908-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="76908-132">RELATED LINKS</span></span>

[<span data-ttu-id="76908-133">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="76908-133">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="76908-134">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="76908-134">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="76908-135">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="76908-135">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
