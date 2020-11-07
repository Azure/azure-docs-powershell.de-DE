---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsitelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLink.md
ms.openlocfilehash: 7e53c6828fa5c7bae40037f2fd64bb06ddf0be45
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821451"
---
# <span data-ttu-id="b6436-101">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="b6436-101">New-AzVpnSiteLink</span></span>

## <span data-ttu-id="b6436-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b6436-102">SYNOPSIS</span></span>
<span data-ttu-id="b6436-103">Erstellt ein Azure VpnSiteLink-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b6436-103">Creates an Azure VpnSiteLink object.</span></span>

## <span data-ttu-id="b6436-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6436-104">SYNTAX</span></span>

```
New-AzVpnSiteLink -Name <String> -IPAddress <String> [-LinkProviderName <String>] [-LinkSpeedInMbps <UInt32>]
 [-BGPAsn <UInt32>] [-BGPPeeringAddress <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b6436-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b6436-105">DESCRIPTION</span></span>
<span data-ttu-id="b6436-106">Erstellt ein Azure VpnSiteLink-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b6436-106">Creates an Azure VpnSiteLink object.</span></span>

## <span data-ttu-id="b6436-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b6436-107">EXAMPLES</span></span>

### <span data-ttu-id="b6436-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b6436-108">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink)
```

<span data-ttu-id="b6436-109">Das obige wird eine Ressourcengruppe, virtuelles WAN und eine VpnSite mit 1 VpnSiteLinks in West US in der Ressourcengruppe "testRG" in Azure erstellen.</span><span class="sxs-lookup"><span data-stu-id="b6436-109">The above will create a resource group, Virtual WAN and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>

## <span data-ttu-id="b6436-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6436-110">PARAMETERS</span></span>

### <span data-ttu-id="b6436-111">-BGPAsn</span><span class="sxs-lookup"><span data-stu-id="b6436-111">-BGPAsn</span></span>
<span data-ttu-id="b6436-112">Der BGP ASN für diesen VpnSiteLink.</span><span class="sxs-lookup"><span data-stu-id="b6436-112">The BGP ASN for this VpnSiteLink.</span></span>

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

### <span data-ttu-id="b6436-113">-BGPPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="b6436-113">-BGPPeeringAddress</span></span>
<span data-ttu-id="b6436-114">Die BGP-Peering-Adresse für diesen VpnSiteLink.</span><span class="sxs-lookup"><span data-stu-id="b6436-114">The BGP Peering Address for this VpnSiteLink.</span></span>

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

### <span data-ttu-id="b6436-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6436-115">-DefaultProfile</span></span>
<span data-ttu-id="b6436-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b6436-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6436-117">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="b6436-117">-IPAddress</span></span>
<span data-ttu-id="b6436-118">Die IPAddress für den nächsten Hop.</span><span class="sxs-lookup"><span data-stu-id="b6436-118">The Next Hop IpAddress.</span></span>

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

### <span data-ttu-id="b6436-119">-LinkProviderName</span><span class="sxs-lookup"><span data-stu-id="b6436-119">-LinkProviderName</span></span>
<span data-ttu-id="b6436-120">Link Anbieter Name.</span><span class="sxs-lookup"><span data-stu-id="b6436-120">Link Provider Name.</span></span>

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

### <span data-ttu-id="b6436-121">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="b6436-121">-LinkSpeedInMbps</span></span>
<span data-ttu-id="b6436-122">Verbindungsgeschwindigkeit in Mbit/s.</span><span class="sxs-lookup"><span data-stu-id="b6436-122">Link Speed In Mbps.</span></span>

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

### <span data-ttu-id="b6436-123">-Name</span><span class="sxs-lookup"><span data-stu-id="b6436-123">-Name</span></span>
<span data-ttu-id="b6436-124">Namen</span><span class="sxs-lookup"><span data-stu-id="b6436-124">Name</span></span>

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

### <span data-ttu-id="b6436-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6436-125">CommonParameters</span></span>
<span data-ttu-id="b6436-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6436-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6436-127">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6436-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6436-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b6436-128">INPUTS</span></span>

### <span data-ttu-id="b6436-129">Keine</span><span class="sxs-lookup"><span data-stu-id="b6436-129">None</span></span>

## <span data-ttu-id="b6436-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b6436-130">OUTPUTS</span></span>

### <span data-ttu-id="b6436-131">Microsoft. Azure. Commands. Network. Models. PSVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="b6436-131">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span></span>

## <span data-ttu-id="b6436-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="b6436-132">NOTES</span></span>

## <span data-ttu-id="b6436-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b6436-133">RELATED LINKS</span></span>

[<span data-ttu-id="b6436-134">Neu – AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="b6436-134">New-AzVpnSite</span></span>](./New-AzVpnSite.md)