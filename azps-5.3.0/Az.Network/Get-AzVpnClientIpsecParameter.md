---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
ms.openlocfilehash: ad0db70d513ffeea688344df612cab942ae6ec53
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379684"
---
# <span data-ttu-id="65694-101">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="65694-101">Get-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="65694-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65694-102">SYNOPSIS</span></span>
<span data-ttu-id="65694-103">Ruft die vpn-Ipsec-Parameter ab, die auf dem virtuellen Netzwerkgateway für Punkt-zu-Website-Verbindungen festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="65694-103">Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>

## <span data-ttu-id="65694-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="65694-104">SYNTAX</span></span>

```
Get-AzVpnClientIpsecParameter [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65694-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="65694-105">DESCRIPTION</span></span>
<span data-ttu-id="65694-106">Das virtuelle Netzwerkgateway ist das Objekt, das Ihr Gateway in Azure darstellt.</span><span class="sxs-lookup"><span data-stu-id="65694-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="65694-107">Das **Cmdlet "Get-AzVpnClientIpsecParameter"** gibt das Objekt Ihrer Vpn-IPSec-Parameter zurück, die auf dem Gateway in Azure basierend auf dem Namen des Gateways und der Ressourcengruppe festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="65694-107">The **Get-AzVpnClientIpsecParameter** cmdlet returns the object of your vpn ipsec parameters set on gateway in Azure based on Gateway Name and Resource Group Name.</span></span>

## <span data-ttu-id="65694-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="65694-108">EXAMPLES</span></span>

### <span data-ttu-id="65694-109">Beispiel 1: Ruft die vpn-Ipsec-Parameter ab, die auf dem virtuellen Netzwerkgateway für Punkt-zu-Website-Verbindungen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="65694-109">Example 1: Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>
```powershell
PS C:\> $VpnClientIPsecParameters = Get-AzVpnClientIpsecParameter -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="65694-110">Gibt das Objekt der vpn-ipsec-Parameter zurück, die auf dem virtuellen Netzwerkgateway mit dem Namen "myGateway" in der Ressourcengruppe "myRG" festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="65694-110">Returns the object of the vpn ipsec parameters set on the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="65694-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65694-111">PARAMETERS</span></span>

### <span data-ttu-id="65694-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65694-112">-DefaultProfile</span></span>
<span data-ttu-id="65694-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="65694-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65694-114">-Name</span><span class="sxs-lookup"><span data-stu-id="65694-114">-Name</span></span>
<span data-ttu-id="65694-115">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="65694-115">The resource name.</span></span>

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

### <span data-ttu-id="65694-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65694-116">-ResourceGroupName</span></span>
<span data-ttu-id="65694-117">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="65694-117">The resource group name.</span></span>

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

### <span data-ttu-id="65694-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65694-118">CommonParameters</span></span>
<span data-ttu-id="65694-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65694-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65694-120">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65694-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65694-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="65694-121">INPUTS</span></span>

### <span data-ttu-id="65694-122">System.String</span><span class="sxs-lookup"><span data-stu-id="65694-122">System.String</span></span>

## <span data-ttu-id="65694-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="65694-123">OUTPUTS</span></span>

### <span data-ttu-id="65694-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="65694-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="65694-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="65694-125">NOTES</span></span>

## <span data-ttu-id="65694-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="65694-126">RELATED LINKS</span></span>

[<span data-ttu-id="65694-127">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="65694-127">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="65694-128">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="65694-128">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="65694-129">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="65694-129">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
