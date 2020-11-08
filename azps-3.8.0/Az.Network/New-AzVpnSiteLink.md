---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsitelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLink.md
ms.openlocfilehash: 68df4cd7dc1149b7bb62a148ff7c649ed2418db8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995717"
---
# <span data-ttu-id="d05ed-101">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="d05ed-101">New-AzVpnSiteLink</span></span>

## <span data-ttu-id="d05ed-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d05ed-102">SYNOPSIS</span></span>
<span data-ttu-id="d05ed-103">Erstellt ein Azure VpnSiteLink-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d05ed-103">Creates an Azure VpnSiteLink object.</span></span>

## <span data-ttu-id="d05ed-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d05ed-104">SYNTAX</span></span>

### <span data-ttu-id="d05ed-105">ByVpnSiteLinkIpAddress</span><span class="sxs-lookup"><span data-stu-id="d05ed-105">ByVpnSiteLinkIpAddress</span></span>
```
New-AzVpnSiteLink -Name <String> -IPAddress <String> [-LinkProviderName <String>] [-LinkSpeedInMbps <UInt32>]
 [-BGPAsn <UInt32>] [-BGPPeeringAddress <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d05ed-106">ByVpnSiteLinkFqdn</span><span class="sxs-lookup"><span data-stu-id="d05ed-106">ByVpnSiteLinkFqdn</span></span>
```
New-AzVpnSiteLink -Name <String> -Fqdn <String> [-LinkProviderName <String>] [-LinkSpeedInMbps <UInt32>]
 [-BGPAsn <UInt32>] [-BGPPeeringAddress <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d05ed-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d05ed-107">DESCRIPTION</span></span>
<span data-ttu-id="d05ed-108">Erstellt ein Azure VpnSiteLink-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d05ed-108">Creates an Azure VpnSiteLink object.</span></span>

## <span data-ttu-id="d05ed-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d05ed-109">EXAMPLES</span></span>

### <span data-ttu-id="d05ed-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d05ed-110">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink)
```

<span data-ttu-id="d05ed-111">Das obige wird eine Ressourcengruppe, virtuelles WAN und eine VpnSite mit 1 VpnSiteLinks in West US in der Ressourcengruppe "testRG" in Azure erstellen.</span><span class="sxs-lookup"><span data-stu-id="d05ed-111">The above will create a resource group, Virtual WAN and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>

## <span data-ttu-id="d05ed-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d05ed-112">PARAMETERS</span></span>

### <span data-ttu-id="d05ed-113">-BGPAsn</span><span class="sxs-lookup"><span data-stu-id="d05ed-113">-BGPAsn</span></span>
<span data-ttu-id="d05ed-114">Der BGP ASN für diesen VpnSiteLink.</span><span class="sxs-lookup"><span data-stu-id="d05ed-114">The BGP ASN for this VpnSiteLink.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d05ed-115">-BGPPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="d05ed-115">-BGPPeeringAddress</span></span>
<span data-ttu-id="d05ed-116">Die BGP-Peering-Adresse für diesen VpnSiteLink.</span><span class="sxs-lookup"><span data-stu-id="d05ed-116">The BGP Peering Address for this VpnSiteLink.</span></span>

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

### <span data-ttu-id="d05ed-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d05ed-117">-DefaultProfile</span></span>
<span data-ttu-id="d05ed-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d05ed-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d05ed-119">-FQDN</span><span class="sxs-lookup"><span data-stu-id="d05ed-119">-Fqdn</span></span>
<span data-ttu-id="d05ed-120">Der FQDN des nächsten Hop.</span><span class="sxs-lookup"><span data-stu-id="d05ed-120">The Next Hop Fqdn.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteLinkFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d05ed-121">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="d05ed-121">-IPAddress</span></span>
<span data-ttu-id="d05ed-122">Die IPAddress für den nächsten Hop.</span><span class="sxs-lookup"><span data-stu-id="d05ed-122">The Next Hop IpAddress.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteLinkIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d05ed-123">-LinkProviderName</span><span class="sxs-lookup"><span data-stu-id="d05ed-123">-LinkProviderName</span></span>
<span data-ttu-id="d05ed-124">Link Anbieter Name.</span><span class="sxs-lookup"><span data-stu-id="d05ed-124">Link Provider Name.</span></span>

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

### <span data-ttu-id="d05ed-125">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="d05ed-125">-LinkSpeedInMbps</span></span>
<span data-ttu-id="d05ed-126">Verbindungsgeschwindigkeit in Mbit/s.</span><span class="sxs-lookup"><span data-stu-id="d05ed-126">Link Speed In Mbps.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d05ed-127">-Name</span><span class="sxs-lookup"><span data-stu-id="d05ed-127">-Name</span></span>
<span data-ttu-id="d05ed-128">Namen</span><span class="sxs-lookup"><span data-stu-id="d05ed-128">Name</span></span>

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

### <span data-ttu-id="d05ed-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d05ed-129">CommonParameters</span></span>
<span data-ttu-id="d05ed-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d05ed-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d05ed-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d05ed-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d05ed-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d05ed-132">INPUTS</span></span>

### <span data-ttu-id="d05ed-133">Keine</span><span class="sxs-lookup"><span data-stu-id="d05ed-133">None</span></span>

## <span data-ttu-id="d05ed-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d05ed-134">OUTPUTS</span></span>

### <span data-ttu-id="d05ed-135">Microsoft. Azure. Commands. Network. Models. PSVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="d05ed-135">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span></span>

## <span data-ttu-id="d05ed-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="d05ed-136">NOTES</span></span>

## <span data-ttu-id="d05ed-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d05ed-137">RELATED LINKS</span></span>

[<span data-ttu-id="d05ed-138">Neu – AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="d05ed-138">New-AzVpnSite</span></span>](./New-AzVpnSite.md)