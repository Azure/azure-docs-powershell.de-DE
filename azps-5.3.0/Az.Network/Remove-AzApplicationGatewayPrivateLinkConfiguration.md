---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 8d222f4eaaa9d37a4f87f5f19604bdef9cff9e39
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472218"
---
# <span data-ttu-id="d0401-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0401-101">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="d0401-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0401-102">SYNOPSIS</span></span>
<span data-ttu-id="d0401-103">Entfernt eine privateLink-Konfiguration von einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="d0401-103">Removes a privateLink configuration from an application gateway.</span></span>

## <span data-ttu-id="d0401-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d0401-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayPrivateLinkConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0401-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d0401-105">DESCRIPTION</span></span>
<span data-ttu-id="d0401-106">Das **Cmdlet "Remove-AzApplicationGatewayPrivateLinkConfiguration"** entfernt eine privateLink-Konfiguration aus einem Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="d0401-106">The **Remove-AzApplicationGatewayPrivateLinkConfiguration** cmdlet removes an privateLink configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="d0401-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d0401-107">EXAMPLES</span></span>

### <span data-ttu-id="d0401-108">Beispiel 1: Entfernen einer PrivatenLink-Konfiguration des Anwendungsgateways</span><span class="sxs-lookup"><span data-stu-id="d0401-108">Example 1: Remove an application gateway PrivateLink Configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01"
```

<span data-ttu-id="d0401-109">Der erste Befehl ruft ein Anwendungsgateway ab und speichert es in der $AppGw Variable.</span><span class="sxs-lookup"><span data-stu-id="d0401-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d0401-110">Mit dem zweiten Befehl wird die privateLink-Konfiguration mit dem Namen "privateLinkConfig01" aus dem Anwendungsgateway entfernt, das in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="d0401-110">The second command removes the privateLink configuration named privateLinkConfig01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="d0401-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0401-111">PARAMETERS</span></span>

### <span data-ttu-id="d0401-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d0401-112">-ApplicationGateway</span></span>
<span data-ttu-id="d0401-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d0401-113">The applicationGateway</span></span>

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

### <span data-ttu-id="d0401-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0401-114">-DefaultProfile</span></span>
<span data-ttu-id="d0401-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d0401-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0401-116">-Name</span><span class="sxs-lookup"><span data-stu-id="d0401-116">-Name</span></span>
<span data-ttu-id="d0401-117">Der Name der Konfiguration "privateLink" des Anwendungsgateways</span><span class="sxs-lookup"><span data-stu-id="d0401-117">The name of the application gateway privateLink configuration</span></span>

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

### <span data-ttu-id="d0401-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0401-118">CommonParameters</span></span>
<span data-ttu-id="d0401-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0401-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0401-120">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d0401-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0401-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d0401-121">INPUTS</span></span>

### <span data-ttu-id="d0401-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d0401-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d0401-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d0401-123">OUTPUTS</span></span>

### <span data-ttu-id="d0401-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d0401-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d0401-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d0401-125">NOTES</span></span>

## <span data-ttu-id="d0401-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d0401-126">RELATED LINKS</span></span>

[<span data-ttu-id="d0401-127">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0401-127">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="d0401-128">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0401-128">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="d0401-129">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0401-129">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="d0401-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0401-130">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)