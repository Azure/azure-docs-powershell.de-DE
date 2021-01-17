---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 78af871cf476ee80c57e22e2469b48bb4d4337a1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378676"
---
# <span data-ttu-id="fbcf9-101">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="fbcf9-101">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="fbcf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbcf9-102">SYNOPSIS</span></span>
<span data-ttu-id="fbcf9-103">Ändert eine PrivateLink-Konfiguration für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="fbcf9-103">Modifies an PrivateLink Configuration for an application gateway.</span></span>

## <span data-ttu-id="fbcf9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fbcf9-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbcf9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fbcf9-105">DESCRIPTION</span></span>
<span data-ttu-id="fbcf9-106">Das **Cmdlet "Set-AzApplicationGatewayPrivateLinkConfiguration"** ändert eine privateLink-Konfiguration für ein Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="fbcf9-106">The **Set-AzApplicationGatewayPrivateLinkConfiguration** cmdlet modifies an privateLink configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="fbcf9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fbcf9-107">EXAMPLES</span></span>

### <span data-ttu-id="fbcf9-108">Beispiel 1: Festlegen einer PrivateLink-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="fbcf9-108">Example 1: Set a PrivateLink Configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration01
```

<span data-ttu-id="fbcf9-109">Der erste Befehl ruft das Anwendungsgateway namens ApplicationGateway01 ab, das zur Ressourcengruppe "ResourceGroup01" gehört, und speichert es in der $AppGw Variable.</span><span class="sxs-lookup"><span data-stu-id="fbcf9-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="fbcf9-110">Der zweite Befehl legt die privateLink-Konfiguration mit dem Namen "privateLinkConfig01" so fest, dass die in $privateLinkIpConfiguration 01 gespeicherte IP-Konfiguration verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fbcf9-110">The second command sets the privateLink configuration with name privateLinkConfig01 to use the ip configuration stored in $privateLinkIpConfiguration01</span></span>

## <span data-ttu-id="fbcf9-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fbcf9-111">PARAMETERS</span></span>

### <span data-ttu-id="fbcf9-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fbcf9-112">-ApplicationGateway</span></span>
<span data-ttu-id="fbcf9-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fbcf9-113">The applicationGateway</span></span>

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

### <span data-ttu-id="fbcf9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbcf9-114">-DefaultProfile</span></span>
<span data-ttu-id="fbcf9-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fbcf9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbcf9-116">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="fbcf9-116">-IpConfiguration</span></span>
<span data-ttu-id="fbcf9-117">Die Liste der "ipConfiguration"</span><span class="sxs-lookup"><span data-stu-id="fbcf9-117">The list of ipConfiguration</span></span>

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

### <span data-ttu-id="fbcf9-118">-Name</span><span class="sxs-lookup"><span data-stu-id="fbcf9-118">-Name</span></span>
<span data-ttu-id="fbcf9-119">Der Name der Konfiguration "privateLink"</span><span class="sxs-lookup"><span data-stu-id="fbcf9-119">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="fbcf9-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fbcf9-120">-Confirm</span></span>
<span data-ttu-id="fbcf9-121">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fbcf9-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbcf9-122">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fbcf9-122">-WhatIf</span></span>
<span data-ttu-id="fbcf9-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fbcf9-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbcf9-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fbcf9-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbcf9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbcf9-125">CommonParameters</span></span>
<span data-ttu-id="fbcf9-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbcf9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbcf9-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fbcf9-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbcf9-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fbcf9-128">INPUTS</span></span>

### <span data-ttu-id="fbcf9-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fbcf9-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="fbcf9-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="fbcf9-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="fbcf9-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fbcf9-131">OUTPUTS</span></span>

### <span data-ttu-id="fbcf9-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fbcf9-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fbcf9-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fbcf9-133">NOTES</span></span>

## <span data-ttu-id="fbcf9-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fbcf9-134">RELATED LINKS</span></span>

[<span data-ttu-id="fbcf9-135">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="fbcf9-135">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="fbcf9-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="fbcf9-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="fbcf9-137">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="fbcf9-137">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="fbcf9-138">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="fbcf9-138">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)