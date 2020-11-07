---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
ms.openlocfilehash: d837355891f3b8095da0380fd91a9ac58a74acff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821699"
---
# <span data-ttu-id="8e5ad-101">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="8e5ad-101">Get-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="8e5ad-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8e5ad-102">SYNOPSIS</span></span>
<span data-ttu-id="8e5ad-103">Ruft die VPN-IPSec-Parameter ab, die auf dem virtuellen Netzwerk Gateway für Point-to-Site-Verbindungen festzulegen sind.</span><span class="sxs-lookup"><span data-stu-id="8e5ad-103">Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>

## <span data-ttu-id="8e5ad-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e5ad-104">SYNTAX</span></span>

```
Get-AzVpnClientIpsecParameter [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e5ad-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8e5ad-105">DESCRIPTION</span></span>
<span data-ttu-id="8e5ad-106">Das virtuelle Netzwerkgateway ist das Objekt, das Ihr Gateway in Azure darstellt.</span><span class="sxs-lookup"><span data-stu-id="8e5ad-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="8e5ad-107">Das Cmdlet " **Get-AzVpnClientIpsecParameter** " gibt das Objekt Ihrer VPN-IPSec-Parameter zurück, die auf Gateway in Azure basierend auf dem Namen des Gatewayservers und der Ressourcengruppe eingestellt sind.</span><span class="sxs-lookup"><span data-stu-id="8e5ad-107">The **Get-AzVpnClientIpsecParameter** cmdlet returns the object of your vpn ipsec parameters set on gateway in Azure based on Gateway Name and Resource Group Name.</span></span>

## <span data-ttu-id="8e5ad-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8e5ad-108">EXAMPLES</span></span>

### <span data-ttu-id="8e5ad-109">1: Ruft die VPN-IPSec-Parameter ab, die auf dem virtuellen Netzwerk Gateway für Point-to-Site-Verbindungen festzulegen sind.</span><span class="sxs-lookup"><span data-stu-id="8e5ad-109">1: Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>
```
PS C:\> $VpnClientIPsecParameters = Get-AzVpnClientIpsecParameter -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="8e5ad-110">Gibt das Objekt der VPN-IPSec-Parameter zurück, die auf dem virtuellen Netzwerk Gateway mit dem Namen "mygateway" innerhalb der Ressourcengruppe "myRG" gesetzt sind.</span><span class="sxs-lookup"><span data-stu-id="8e5ad-110">Returns the object of the vpn ipsec parameters set on the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="8e5ad-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e5ad-111">PARAMETERS</span></span>

### <span data-ttu-id="8e5ad-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e5ad-112">-DefaultProfile</span></span>
<span data-ttu-id="8e5ad-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8e5ad-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e5ad-114">-Name</span><span class="sxs-lookup"><span data-stu-id="8e5ad-114">-Name</span></span>
<span data-ttu-id="8e5ad-115">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="8e5ad-115">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e5ad-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e5ad-116">-ResourceGroupName</span></span>
<span data-ttu-id="8e5ad-117">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8e5ad-117">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e5ad-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e5ad-118">CommonParameters</span></span>
<span data-ttu-id="8e5ad-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e5ad-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e5ad-120">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e5ad-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e5ad-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8e5ad-121">INPUTS</span></span>

### <span data-ttu-id="8e5ad-122">System. String</span><span class="sxs-lookup"><span data-stu-id="8e5ad-122">System.String</span></span>

## <span data-ttu-id="8e5ad-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8e5ad-123">OUTPUTS</span></span>

### <span data-ttu-id="8e5ad-124">Microsoft. Azure. Commands. Network. Models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="8e5ad-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="8e5ad-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="8e5ad-125">NOTES</span></span>

## <span data-ttu-id="8e5ad-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8e5ad-126">RELATED LINKS</span></span>

[<span data-ttu-id="8e5ad-127">Neu – AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="8e5ad-127">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="8e5ad-128">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="8e5ad-128">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="8e5ad-129">Satz-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="8e5ad-129">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
