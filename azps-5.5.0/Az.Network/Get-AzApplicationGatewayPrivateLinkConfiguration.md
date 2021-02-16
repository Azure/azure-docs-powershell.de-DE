---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 2c9f006c9e719380abd1f1f5dbb6c6233346a563
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170057"
---
# <span data-ttu-id="4d776-101">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d776-101">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="4d776-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d776-102">SYNOPSIS</span></span>
<span data-ttu-id="4d776-103">Ruft die Konfiguration eines privaten Links für ein Anwendungsgateway ab.</span><span class="sxs-lookup"><span data-stu-id="4d776-103">Gets the private link configuration of an application gateway.</span></span>

## <span data-ttu-id="4d776-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4d776-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d776-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4d776-105">DESCRIPTION</span></span>
<span data-ttu-id="4d776-106">Das **Cmdlet "Get-AzApplicationGatewayPrivateLinkConfiguration"** ruft die Konfiguration eines privaten Links eines Anwendungsgateways ab.</span><span class="sxs-lookup"><span data-stu-id="4d776-106">The **Get-AzApplicationGatewayPrivateLinkConfiguration** cmdlet gets the private link configuration of an application gateway.</span></span>

## <span data-ttu-id="4d776-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4d776-107">EXAMPLES</span></span>

### <span data-ttu-id="4d776-108">Beispiel 1: Erhalten einer angegebenen Konfiguration für private Links</span><span class="sxs-lookup"><span data-stu-id="4d776-108">Example 1 : Get a specified private link configuration</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfiguration = Get-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -ApplicationGateway $AppGw
```

<span data-ttu-id="4d776-109">Der erste Befehl ruft ein Anwendungsgateway namens ApplicationGateway01 aus der Ressourcengruppe "ResourceGroup01" ab und speichert es in der $AppGw Variable.</span><span class="sxs-lookup"><span data-stu-id="4d776-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4d776-110">Der zweite Befehl ruft die Konfiguration für private Links mit dem Namen "privateLinkConfig01" aus $AppGw und speichert sie in der $PrivateLinkConfiguration Variable.</span><span class="sxs-lookup"><span data-stu-id="4d776-110">The second command gets the private link configuration named privateLinkConfig01 from $AppGw and stores it in the $PrivateLinkConfiguration variable.</span></span>

### <span data-ttu-id="4d776-111">Beispiel 2: Erhalten einer Liste der Konfiguration privater Links</span><span class="sxs-lookup"><span data-stu-id="4d776-111">Example 2 : Get a list of private link configuration</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfigurations = Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="4d776-112">Der erste Befehl ruft ein Anwendungsgateway namens ApplicationGateway01 aus der Ressourcengruppe "ResourceGroup01" ab und speichert es in der $AppGw Variable.</span><span class="sxs-lookup"><span data-stu-id="4d776-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4d776-113">Der zweite Befehl ruft alle Konfigurationen privater Links aus $AppGw und speichert sie in der $PrivateLinkConfigurations Variable.</span><span class="sxs-lookup"><span data-stu-id="4d776-113">The second command gets all the private link configurations from $AppGw and stores it in the $PrivateLinkConfigurations variable.</span></span>

## <span data-ttu-id="4d776-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d776-114">PARAMETERS</span></span>

### <span data-ttu-id="4d776-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4d776-115">-ApplicationGateway</span></span>
<span data-ttu-id="4d776-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4d776-116">The applicationGateway</span></span>

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

### <span data-ttu-id="4d776-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d776-117">-DefaultProfile</span></span>
<span data-ttu-id="4d776-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4d776-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d776-119">-Name</span><span class="sxs-lookup"><span data-stu-id="4d776-119">-Name</span></span>
<span data-ttu-id="4d776-120">Der Name der Konfiguration "privateLink" des Anwendungsgateways</span><span class="sxs-lookup"><span data-stu-id="4d776-120">The name of the application gateway privateLink configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d776-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d776-121">CommonParameters</span></span>
<span data-ttu-id="4d776-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d776-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d776-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4d776-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d776-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4d776-124">INPUTS</span></span>

### <span data-ttu-id="4d776-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4d776-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4d776-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4d776-126">OUTPUTS</span></span>

### <span data-ttu-id="4d776-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d776-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="4d776-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4d776-128">NOTES</span></span>

## <span data-ttu-id="4d776-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4d776-129">RELATED LINKS</span></span>

[<span data-ttu-id="4d776-130">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d776-130">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="4d776-131">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d776-131">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="4d776-132">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d776-132">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="4d776-133">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d776-133">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)