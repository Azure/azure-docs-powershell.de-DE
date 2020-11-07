---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnSite.md
ms.openlocfilehash: 0c6ede26826547e525610c76f4a2883f9b738b33
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821683"
---
# <span data-ttu-id="5b304-101">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="5b304-101">Get-AzVpnSite</span></span>

## <span data-ttu-id="5b304-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5b304-102">SYNOPSIS</span></span>
<span data-ttu-id="5b304-103">Ruft eine Azure VpnSite-Ressource nach Namen ab oder listet alle VpnSites in einer ResourceGroup oder Abonnement-Nr auf.</span><span class="sxs-lookup"><span data-stu-id="5b304-103">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

<span data-ttu-id="5b304-104">Hierbei handelt es sich um eine RM-Darstellung von Kunden Zweigen, die für S2S-Konnektivität mit einem virtuellen Kortex-Hub in Azure hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="5b304-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="5b304-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b304-105">SYNTAX</span></span>

### <span data-ttu-id="5b304-106">ListBySubscriptionId (Standard)</span><span class="sxs-lookup"><span data-stu-id="5b304-106">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnSite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b304-107">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b304-107">ListByResourceGroupName</span></span>
```
Get-AzVpnSite [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5b304-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5b304-108">DESCRIPTION</span></span>
<span data-ttu-id="5b304-109">Ruft eine Azure VpnSite-Ressource nach Namen ab oder listet alle VpnSites in einer ResourceGroup oder Abonnement-Nr auf.</span><span class="sxs-lookup"><span data-stu-id="5b304-109">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

## <span data-ttu-id="5b304-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5b304-110">EXAMPLES</span></span>

### <span data-ttu-id="5b304-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5b304-111">Example 1</span></span>

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

<span data-ttu-id="5b304-112">Das obige wird eine Ressourcengruppe erstellen, virtuelles WAN in West US in "testRG" Ressourcengruppe in Azure.</span><span class="sxs-lookup"><span data-stu-id="5b304-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="5b304-113">Anschließend wird ein VpnSite erstellt, um einen Kunden Zweig darzustellen und mit dem virtuellen WAN zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="5b304-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="5b304-114">Nachdem die Website erstellt wurde, wird die Website mit dem Befehl Get-AzVpnSite abgerufen.</span><span class="sxs-lookup"><span data-stu-id="5b304-114">Once the site is created, it gets the site using the Get-AzVpnSite command.</span></span>

### <span data-ttu-id="5b304-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5b304-115">Example 2</span></span>

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

<span data-ttu-id="5b304-116">Dieses Cmdlet ruft alle Websites ab, die mit "Test" beginnen.</span><span class="sxs-lookup"><span data-stu-id="5b304-116">This cmdlet gets all Sites that start with "test".</span></span>

## <span data-ttu-id="5b304-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b304-117">PARAMETERS</span></span>

### <span data-ttu-id="5b304-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b304-118">-DefaultProfile</span></span>
<span data-ttu-id="5b304-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5b304-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b304-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5b304-120">-Name</span></span>
<span data-ttu-id="5b304-121">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="5b304-121">The resource name.</span></span>

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

### <span data-ttu-id="5b304-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b304-122">-ResourceGroupName</span></span>
<span data-ttu-id="5b304-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5b304-123">The resource group name.</span></span>

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

### <span data-ttu-id="5b304-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b304-124">CommonParameters</span></span>
<span data-ttu-id="5b304-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b304-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b304-126">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5b304-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b304-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5b304-127">INPUTS</span></span>

### <span data-ttu-id="5b304-128">Keine</span><span class="sxs-lookup"><span data-stu-id="5b304-128">None</span></span>

## <span data-ttu-id="5b304-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5b304-129">OUTPUTS</span></span>

### <span data-ttu-id="5b304-130">Microsoft. Azure. Commands. Network. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="5b304-130">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="5b304-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="5b304-131">NOTES</span></span>

## <span data-ttu-id="5b304-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5b304-132">RELATED LINKS</span></span>

[<span data-ttu-id="5b304-133">Neu – AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="5b304-133">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="5b304-134">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="5b304-134">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="5b304-135">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="5b304-135">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
