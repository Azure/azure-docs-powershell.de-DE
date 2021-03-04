---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 0bc3d62ad690ab8bed961045ce46448af8700bd8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933920"
---
# <span data-ttu-id="a8822-101">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8822-101">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="a8822-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8822-102">SYNOPSIS</span></span>
<span data-ttu-id="a8822-103">Fügt einem Anwendungsgateway eine private Linkkonfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="a8822-103">Adds a private link configuration to an application gateway.</span></span>

## <span data-ttu-id="a8822-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a8822-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a8822-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a8822-105">DESCRIPTION</span></span>
<span data-ttu-id="a8822-106">Das **Cmdlet Add-AzApplicationGatewayPrivateLinkConfiguration** fügt einem Anwendungsgateway eine private Linkkonfiguration hinzu.</span><span class="sxs-lookup"><span data-stu-id="a8822-106">The **Add-AzApplicationGatewayPrivateLinkConfiguration** cmdlet adds a private link configuration to an application gateway.</span></span>

## <span data-ttu-id="a8822-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a8822-107">EXAMPLES</span></span>

### <span data-ttu-id="a8822-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a8822-108">Example 1</span></span>
```powershell
PS C:\> $PrivateLinkIpConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "ipConfig01" -Subnet $subnet -Primary
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01" -IpConfiguration $PrivateLinkIpConfiguration
```

<span data-ttu-id="a8822-109">Mit dem ersten Befehl wird eine privateLinkIpConfiguration erstellt und in der $PrivateLinkIpConfiguration gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a8822-109">The first command creates a privateLinkIpConfiguration and stores it in the $PrivateLinkIpConfiguration variable.</span></span>
<span data-ttu-id="a8822-110">Der zweite Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe "ResourceGroup01" gehört, und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="a8822-110">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a8822-111">Mit dem dritten Befehl wird die private Linkkonfiguration mit dem Namen privateLinkConfig01 für das Gateway in $AppGw</span><span class="sxs-lookup"><span data-stu-id="a8822-111">The third command adds the private link configuration named privateLinkConfig01, for the gateway in $AppGw</span></span>

## <span data-ttu-id="a8822-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a8822-112">PARAMETERS</span></span>

### <span data-ttu-id="a8822-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a8822-113">-ApplicationGateway</span></span>
<span data-ttu-id="a8822-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a8822-114">The applicationGateway</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8822-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8822-115">-DefaultProfile</span></span>
<span data-ttu-id="a8822-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a8822-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8822-117">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8822-117">-IpConfiguration</span></span>
<span data-ttu-id="a8822-118">Die Liste der ipConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8822-118">The list of ipConfiguration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8822-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a8822-119">-Name</span></span>
<span data-ttu-id="a8822-120">Der Name der privateLink-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="a8822-120">The name of the privateLink configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8822-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8822-121">CommonParameters</span></span>
<span data-ttu-id="a8822-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8822-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8822-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8822-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8822-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a8822-124">INPUTS</span></span>

### <span data-ttu-id="a8822-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a8822-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="a8822-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="a8822-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="a8822-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a8822-127">OUTPUTS</span></span>

### <span data-ttu-id="a8822-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a8822-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a8822-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a8822-129">NOTES</span></span>

## <span data-ttu-id="a8822-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a8822-130">RELATED LINKS</span></span>

[<span data-ttu-id="a8822-131">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8822-131">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="a8822-132">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8822-132">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="a8822-133">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8822-133">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="a8822-134">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8822-134">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)