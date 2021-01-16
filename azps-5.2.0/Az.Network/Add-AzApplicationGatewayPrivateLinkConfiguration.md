---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 2083dd00c5163a67492ff9973fdf7399d67d7cb6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98299131"
---
# <span data-ttu-id="16809-101">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="16809-101">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="16809-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16809-102">SYNOPSIS</span></span>
<span data-ttu-id="16809-103">Fügt einem Anwendungsgateway eine Konfiguration für private Links hinzu.</span><span class="sxs-lookup"><span data-stu-id="16809-103">Adds a private link configuration to an application gateway.</span></span>

## <span data-ttu-id="16809-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="16809-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="16809-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="16809-105">DESCRIPTION</span></span>
<span data-ttu-id="16809-106">Das **Cmdlet "Add-AzApplicationGatewayPrivateLinkConfiguration"** fügt einem Anwendungsgateway eine Konfiguration für private Links hinzu.</span><span class="sxs-lookup"><span data-stu-id="16809-106">The **Add-AzApplicationGatewayPrivateLinkConfiguration** cmdlet adds a private link configuration to an application gateway.</span></span>

## <span data-ttu-id="16809-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="16809-107">EXAMPLES</span></span>

### <span data-ttu-id="16809-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="16809-108">Example 1</span></span>
```powershell
PS C:\> $PrivateLinkIpConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "ipConfig01" -Subnet $subnet -Primary
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01" -IpConfiguration $PrivateLinkIpConfiguration
```

<span data-ttu-id="16809-109">Der erste Befehl erstellt eine privateLinkIpConfiguration und speichert sie in der $PrivateLinkIpConfiguration Variable.</span><span class="sxs-lookup"><span data-stu-id="16809-109">The first command creates a privateLinkIpConfiguration and stores it in the $PrivateLinkIpConfiguration variable.</span></span>
<span data-ttu-id="16809-110">Der zweite Befehl ruft das Anwendungsgateway namens ApplicationGateway01 ab, das zur Ressourcengruppe "ResourceGroup01" gehört, und speichert es in der $AppGw Variable.</span><span class="sxs-lookup"><span data-stu-id="16809-110">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="16809-111">Mit dem dritten Befehl wird die Konfiguration privater Links namens "privateLinkConfig01" für das Gateway in $AppGw</span><span class="sxs-lookup"><span data-stu-id="16809-111">The third command adds the private link configuration named privateLinkConfig01, for the gateway in $AppGw</span></span>

## <span data-ttu-id="16809-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16809-112">PARAMETERS</span></span>

### <span data-ttu-id="16809-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="16809-113">-ApplicationGateway</span></span>
<span data-ttu-id="16809-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="16809-114">The applicationGateway</span></span>

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

### <span data-ttu-id="16809-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16809-115">-DefaultProfile</span></span>
<span data-ttu-id="16809-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="16809-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16809-117">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="16809-117">-IpConfiguration</span></span>
<span data-ttu-id="16809-118">Die Liste der "ipConfiguration"</span><span class="sxs-lookup"><span data-stu-id="16809-118">The list of ipConfiguration</span></span>

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

### <span data-ttu-id="16809-119">-Name</span><span class="sxs-lookup"><span data-stu-id="16809-119">-Name</span></span>
<span data-ttu-id="16809-120">Der Name der Konfiguration "privateLink"</span><span class="sxs-lookup"><span data-stu-id="16809-120">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="16809-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16809-121">CommonParameters</span></span>
<span data-ttu-id="16809-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16809-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16809-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16809-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16809-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="16809-124">INPUTS</span></span>

### <span data-ttu-id="16809-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="16809-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="16809-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="16809-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="16809-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="16809-127">OUTPUTS</span></span>

### <span data-ttu-id="16809-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="16809-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="16809-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="16809-129">NOTES</span></span>

## <span data-ttu-id="16809-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="16809-130">RELATED LINKS</span></span>

[<span data-ttu-id="16809-131">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="16809-131">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="16809-132">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="16809-132">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="16809-133">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="16809-133">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="16809-134">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="16809-134">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)