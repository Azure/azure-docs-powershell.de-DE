---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnSite.md
ms.openlocfilehash: 0277e61a6b1b180691908b2e86c0050eb8d62b1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482322"
---
# <span data-ttu-id="57521-101">Get-AzureRmVpnSite</span><span class="sxs-lookup"><span data-stu-id="57521-101">Get-AzureRmVpnSite</span></span>

## <span data-ttu-id="57521-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="57521-102">SYNOPSIS</span></span>
<span data-ttu-id="57521-103">Ruft eine Azure VpnSite-Ressource nach Namen ab oder listet alle VpnSites in einer ResourceGroup oder Abonnement-Nr auf.</span><span class="sxs-lookup"><span data-stu-id="57521-103">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

<span data-ttu-id="57521-104">Hierbei handelt es sich um eine RM-Darstellung von Kunden Zweigen, die für S2S-Konnektivität mit einem virtuellen Kortex-Hub in Azure hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="57521-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57521-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="57521-105">SYNTAX</span></span>

### <span data-ttu-id="57521-106">ListBySubscriptionId (Standard)</span><span class="sxs-lookup"><span data-stu-id="57521-106">ListBySubscriptionId (Default)</span></span>
```
Get-AzureRmVpnSite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57521-107">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57521-107">ListByResourceGroupName</span></span>
```
Get-AzureRmVpnSite -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="57521-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="57521-108">DESCRIPTION</span></span>
<span data-ttu-id="57521-109">Ruft eine Azure VpnSite-Ressource nach Namen ab oder listet alle VpnSites in einer ResourceGroup oder Abonnement-Nr auf.</span><span class="sxs-lookup"><span data-stu-id="57521-109">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

## <span data-ttu-id="57521-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="57521-110">EXAMPLES</span></span>

### <span data-ttu-id="57521-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="57521-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"

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

<span data-ttu-id="57521-112">Das obige wird eine Ressourcengruppe erstellen, virtuelles WAN in West US in "testRG" Ressourcengruppe in Azure.</span><span class="sxs-lookup"><span data-stu-id="57521-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="57521-113">Anschließend wird ein VpnSite erstellt, um einen Kunden Zweig darzustellen und mit dem virtuellen WAN zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="57521-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="57521-114">Nachdem die Website erstellt wurde, wird die Website mit dem Befehl Get-AzureRmVpnSite abgerufen.</span><span class="sxs-lookup"><span data-stu-id="57521-114">Once the site is created, it gets the site using the Get-AzureRmVpnSite command.</span></span>

## <span data-ttu-id="57521-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="57521-115">PARAMETERS</span></span>

### <span data-ttu-id="57521-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57521-116">-DefaultProfile</span></span>
<span data-ttu-id="57521-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="57521-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57521-118">-Name</span><span class="sxs-lookup"><span data-stu-id="57521-118">-Name</span></span>
<span data-ttu-id="57521-119">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="57521-119">The resource name.</span></span>

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

### <span data-ttu-id="57521-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57521-120">-ResourceGroupName</span></span>
<span data-ttu-id="57521-121">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="57521-121">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57521-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57521-122">CommonParameters</span></span>
<span data-ttu-id="57521-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57521-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57521-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57521-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57521-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="57521-125">INPUTS</span></span>

### <span data-ttu-id="57521-126">Keine</span><span class="sxs-lookup"><span data-stu-id="57521-126">None</span></span>

## <span data-ttu-id="57521-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="57521-127">OUTPUTS</span></span>

### <span data-ttu-id="57521-128">Microsoft. Azure. Commands. Network. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="57521-128">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="57521-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="57521-129">NOTES</span></span>

## <span data-ttu-id="57521-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="57521-130">RELATED LINKS</span></span>
