---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
ms.openlocfilehash: ad0db70d513ffeea688344df612cab942ae6ec53
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159148"
---
# <span data-ttu-id="8229a-101">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="8229a-101">Get-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="8229a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8229a-102">SYNOPSIS</span></span>
<span data-ttu-id="8229a-103">Ruft die vpn-Ipsec-Parameter ab, die auf dem virtuellen Netzwerkgateway für Punkt-zu-Website-Verbindungen festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="8229a-103">Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>

## <span data-ttu-id="8229a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8229a-104">SYNTAX</span></span>

```
Get-AzVpnClientIpsecParameter [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8229a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8229a-105">DESCRIPTION</span></span>
<span data-ttu-id="8229a-106">Das virtuelle Netzwerkgateway ist das Objekt, das Ihr Gateway in Azure darstellt.</span><span class="sxs-lookup"><span data-stu-id="8229a-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="8229a-107">Das **Cmdlet "Get-AzVpnClientIpsecParameter"** gibt das Objekt Ihrer Vpn-Ipsec-Parameter zurück, die auf dem Gateway in Azure basierend auf dem Gatewaynamen und dem Namen der Ressourcengruppe festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="8229a-107">The **Get-AzVpnClientIpsecParameter** cmdlet returns the object of your vpn ipsec parameters set on gateway in Azure based on Gateway Name and Resource Group Name.</span></span>

## <span data-ttu-id="8229a-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8229a-108">EXAMPLES</span></span>

### <span data-ttu-id="8229a-109">Beispiel 1: Ruft die vpn-Ipsec-Parameter ab, die auf dem virtuellen Netzwerkgateway für Punkt-zu-Website-Verbindungen festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="8229a-109">Example 1: Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>
```powershell
PS C:\> $VpnClientIPsecParameters = Get-AzVpnClientIpsecParameter -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="8229a-110">Gibt das Objekt der vpn-ipsec-Parameter zurück, die auf dem virtuellen Netzwerkgateway mit dem Namen "myGateway" in der Ressourcengruppe "myRG" festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="8229a-110">Returns the object of the vpn ipsec parameters set on the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="8229a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8229a-111">PARAMETERS</span></span>

### <span data-ttu-id="8229a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8229a-112">-DefaultProfile</span></span>
<span data-ttu-id="8229a-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8229a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8229a-114">-Name</span><span class="sxs-lookup"><span data-stu-id="8229a-114">-Name</span></span>
<span data-ttu-id="8229a-115">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="8229a-115">The resource name.</span></span>

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

### <span data-ttu-id="8229a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8229a-116">-ResourceGroupName</span></span>
<span data-ttu-id="8229a-117">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8229a-117">The resource group name.</span></span>

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

### <span data-ttu-id="8229a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8229a-118">CommonParameters</span></span>
<span data-ttu-id="8229a-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8229a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8229a-120">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8229a-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8229a-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8229a-121">INPUTS</span></span>

### <span data-ttu-id="8229a-122">System.String</span><span class="sxs-lookup"><span data-stu-id="8229a-122">System.String</span></span>

## <span data-ttu-id="8229a-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8229a-123">OUTPUTS</span></span>

### <span data-ttu-id="8229a-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="8229a-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="8229a-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8229a-125">NOTES</span></span>

## <span data-ttu-id="8229a-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8229a-126">RELATED LINKS</span></span>

[<span data-ttu-id="8229a-127">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="8229a-127">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="8229a-128">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="8229a-128">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="8229a-129">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="8229a-129">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
