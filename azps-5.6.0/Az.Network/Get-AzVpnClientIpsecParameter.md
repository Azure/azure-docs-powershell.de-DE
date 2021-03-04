---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 3be81626dc48f66fd7aac71c23c2cd9168dab336
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945935"
---
# <span data-ttu-id="6a696-101">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="6a696-101">Get-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="6a696-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a696-102">SYNOPSIS</span></span>
<span data-ttu-id="6a696-103">Ruft die vpn-Ipsec-Parameter ab, die für Das Virtuelle Netzwerkgateway für Punkt-zu-Website-Verbindungen festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="6a696-103">Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>

## <span data-ttu-id="6a696-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6a696-104">SYNTAX</span></span>

```
Get-AzVpnClientIpsecParameter [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a696-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6a696-105">DESCRIPTION</span></span>
<span data-ttu-id="6a696-106">Das Virtual Network Gateway ist das Objekt, das Ihr Gateway in Azure darstellt.</span><span class="sxs-lookup"><span data-stu-id="6a696-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="6a696-107">Das **Get-AzVpnClientIpsecParameter-Cmdlet** gibt das -Objekt Ihrer vpn-ipsec-Parameter zurück, die auf dem Gateway in Azure basierend auf Gatewayname und Ressourcengruppenname festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="6a696-107">The **Get-AzVpnClientIpsecParameter** cmdlet returns the object of your vpn ipsec parameters set on gateway in Azure based on Gateway Name and Resource Group Name.</span></span>

## <span data-ttu-id="6a696-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6a696-108">EXAMPLES</span></span>

### <span data-ttu-id="6a696-109">Beispiel 1: Ruft die vpn-Ipsec-Parameter ab, die für Das Virtuelle Netzwerkgateway für Punkt auf Websiteverbindungen festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="6a696-109">Example 1: Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>
```powershell
PS C:\> $VpnClientIPsecParameters = Get-AzVpnClientIpsecParameter -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="6a696-110">Gibt das Objekt der vpn-ipsec-Parameter zurück, die im Virtual Network Gateway mit dem Namen "myGateway" innerhalb der Ressourcengruppe "myRG" festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="6a696-110">Returns the object of the vpn ipsec parameters set on the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="6a696-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6a696-111">PARAMETERS</span></span>

### <span data-ttu-id="6a696-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a696-112">-DefaultProfile</span></span>
<span data-ttu-id="6a696-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6a696-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a696-114">-Name</span><span class="sxs-lookup"><span data-stu-id="6a696-114">-Name</span></span>
<span data-ttu-id="6a696-115">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="6a696-115">The resource name.</span></span>

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

### <span data-ttu-id="6a696-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a696-116">-ResourceGroupName</span></span>
<span data-ttu-id="6a696-117">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6a696-117">The resource group name.</span></span>

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

### <span data-ttu-id="6a696-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a696-118">CommonParameters</span></span>
<span data-ttu-id="6a696-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a696-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a696-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a696-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a696-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6a696-121">INPUTS</span></span>

### <span data-ttu-id="6a696-122">System.String</span><span class="sxs-lookup"><span data-stu-id="6a696-122">System.String</span></span>

## <span data-ttu-id="6a696-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6a696-123">OUTPUTS</span></span>

### <span data-ttu-id="6a696-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="6a696-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="6a696-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6a696-125">NOTES</span></span>

## <span data-ttu-id="6a696-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6a696-126">RELATED LINKS</span></span>

[<span data-ttu-id="6a696-127">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="6a696-127">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="6a696-128">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="6a696-128">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="6a696-129">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="6a696-129">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
