---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientIpsecParameter.md
ms.openlocfilehash: 539ae515d664aaeb01ca824603cd8ee3ed38f0fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482350"
---
# <span data-ttu-id="d9064-101">Get-AzureRmVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="d9064-101">Get-AzureRmVpnClientIpsecParameter</span></span>

## <span data-ttu-id="d9064-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d9064-102">SYNOPSIS</span></span>
<span data-ttu-id="d9064-103">Ruft die VPN-IPSec-Parameter ab, die auf dem virtuellen Netzwerk Gateway für Point-to-Site-Verbindungen festzulegen sind.</span><span class="sxs-lookup"><span data-stu-id="d9064-103">Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9064-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9064-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientIpsecParameter [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9064-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9064-105">DESCRIPTION</span></span>
<span data-ttu-id="d9064-106">Das virtuelle Netzwerkgateway ist das Objekt, das Ihr Gateway in Azure darstellt.</span><span class="sxs-lookup"><span data-stu-id="d9064-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="d9064-107">Das Cmdlet " **Get-AzureRmVpnClientIpsecParameter** " gibt das Objekt Ihrer VPN-IPSec-Parameter zurück, die auf Gateway in Azure basierend auf dem Namen des Gatewayservers und der Ressourcengruppe eingestellt sind.</span><span class="sxs-lookup"><span data-stu-id="d9064-107">The **Get-AzureRmVpnClientIpsecParameter** cmdlet returns the object of your vpn ipsec parameters set on gateway in Azure based on Gateway Name and Resource Group Name.</span></span>

## <span data-ttu-id="d9064-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d9064-108">EXAMPLES</span></span>

### <span data-ttu-id="d9064-109">1: Ruft die VPN-IPSec-Parameter ab, die auf dem virtuellen Netzwerk Gateway für Point-to-Site-Verbindungen festzulegen sind.</span><span class="sxs-lookup"><span data-stu-id="d9064-109">1: Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>
```
PS C:\> $VpnClientIPsecParameters = Get-AzureRmVpnClientIpsecParameter -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="d9064-110">Gibt das Objekt der VPN-IPSec-Parameter zurück, die auf dem virtuellen Netzwerk Gateway mit dem Namen "mygateway" innerhalb der Ressourcengruppe "myRG" gesetzt sind.</span><span class="sxs-lookup"><span data-stu-id="d9064-110">Returns the object of the vpn ipsec parameters set on the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="d9064-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9064-111">PARAMETERS</span></span>

### <span data-ttu-id="d9064-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9064-112">-DefaultProfile</span></span>
<span data-ttu-id="d9064-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d9064-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9064-114">-Name</span><span class="sxs-lookup"><span data-stu-id="d9064-114">-Name</span></span>
<span data-ttu-id="d9064-115">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="d9064-115">The resource name.</span></span>

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

### <span data-ttu-id="d9064-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9064-116">-ResourceGroupName</span></span>
<span data-ttu-id="d9064-117">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d9064-117">The resource group name.</span></span>

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

### <span data-ttu-id="d9064-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9064-118">CommonParameters</span></span>
<span data-ttu-id="d9064-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9064-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9064-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9064-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9064-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d9064-121">INPUTS</span></span>

### <span data-ttu-id="d9064-122">System. String</span><span class="sxs-lookup"><span data-stu-id="d9064-122">System.String</span></span>

## <span data-ttu-id="d9064-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d9064-123">OUTPUTS</span></span>

### <span data-ttu-id="d9064-124">Microsoft. Azure. Commands. Network. Models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="d9064-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="d9064-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="d9064-125">NOTES</span></span>

## <span data-ttu-id="d9064-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d9064-126">RELATED LINKS</span></span>
