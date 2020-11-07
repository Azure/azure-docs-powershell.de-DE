---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 1ff3e4f4a69309d2dfa5655fefac3d1c5a0e933f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846712"
---
# <span data-ttu-id="89049-101">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="89049-101">Get-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="89049-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="89049-102">SYNOPSIS</span></span>
<span data-ttu-id="89049-103">Ruft die VPN-IPSec-Parameter ab, die auf dem virtuellen Netzwerk Gateway für Point-to-Site-Verbindungen festzulegen sind.</span><span class="sxs-lookup"><span data-stu-id="89049-103">Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>

## <span data-ttu-id="89049-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="89049-104">SYNTAX</span></span>

```
Get-AzVpnClientIpsecParameter [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89049-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="89049-105">DESCRIPTION</span></span>
<span data-ttu-id="89049-106">Das virtuelle Netzwerkgateway ist das Objekt, das Ihr Gateway in Azure darstellt.</span><span class="sxs-lookup"><span data-stu-id="89049-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="89049-107">Das Cmdlet " **Get-AzVpnClientIpsecParameter** " gibt das Objekt Ihrer VPN-IPSec-Parameter zurück, die auf Gateway in Azure basierend auf dem Namen des Gatewayservers und der Ressourcengruppe eingestellt sind.</span><span class="sxs-lookup"><span data-stu-id="89049-107">The **Get-AzVpnClientIpsecParameter** cmdlet returns the object of your vpn ipsec parameters set on gateway in Azure based on Gateway Name and Resource Group Name.</span></span>

## <span data-ttu-id="89049-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="89049-108">EXAMPLES</span></span>

### <span data-ttu-id="89049-109">1: Ruft die VPN-IPSec-Parameter ab, die auf dem virtuellen Netzwerk Gateway für Point-to-Site-Verbindungen festzulegen sind.</span><span class="sxs-lookup"><span data-stu-id="89049-109">1: Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>
```
PS C:\> $VpnClientIPsecParameters = Get-AzVpnClientIpsecParameter -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="89049-110">Gibt das Objekt der VPN-IPSec-Parameter zurück, die auf dem virtuellen Netzwerk Gateway mit dem Namen "mygateway" innerhalb der Ressourcengruppe "myRG" gesetzt sind.</span><span class="sxs-lookup"><span data-stu-id="89049-110">Returns the object of the vpn ipsec parameters set on the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="89049-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="89049-111">PARAMETERS</span></span>

### <span data-ttu-id="89049-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89049-112">-DefaultProfile</span></span>
<span data-ttu-id="89049-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="89049-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89049-114">-Name</span><span class="sxs-lookup"><span data-stu-id="89049-114">-Name</span></span>
<span data-ttu-id="89049-115">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="89049-115">The resource name.</span></span>

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

### <span data-ttu-id="89049-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89049-116">-ResourceGroupName</span></span>
<span data-ttu-id="89049-117">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="89049-117">The resource group name.</span></span>

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

### <span data-ttu-id="89049-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89049-118">CommonParameters</span></span>
<span data-ttu-id="89049-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89049-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89049-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="89049-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89049-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="89049-121">INPUTS</span></span>

### <span data-ttu-id="89049-122">System. String</span><span class="sxs-lookup"><span data-stu-id="89049-122">System.String</span></span>

## <span data-ttu-id="89049-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="89049-123">OUTPUTS</span></span>

### <span data-ttu-id="89049-124">Microsoft. Azure. Commands. Network. Models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="89049-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="89049-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="89049-125">NOTES</span></span>

## <span data-ttu-id="89049-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="89049-126">RELATED LINKS</span></span>

[<span data-ttu-id="89049-127">Neu – AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="89049-127">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="89049-128">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="89049-128">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="89049-129">Satz-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="89049-129">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
