---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: d3f774b078c1069fc5a2c2690996837f17a4c187
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940360"
---
# <span data-ttu-id="82c11-101">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="82c11-101">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="82c11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82c11-102">SYNOPSIS</span></span>
<span data-ttu-id="82c11-103">Ruft die private Linkkonfiguration eines Anwendungsgateways ab.</span><span class="sxs-lookup"><span data-stu-id="82c11-103">Gets the private link configuration of an application gateway.</span></span>

## <span data-ttu-id="82c11-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="82c11-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82c11-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="82c11-105">DESCRIPTION</span></span>
<span data-ttu-id="82c11-106">Das **Cmdlet Get-AzApplicationGatewayPrivateLinkConfiguration** ruft die private Linkkonfiguration eines Anwendungsgateways ab.</span><span class="sxs-lookup"><span data-stu-id="82c11-106">The **Get-AzApplicationGatewayPrivateLinkConfiguration** cmdlet gets the private link configuration of an application gateway.</span></span>

## <span data-ttu-id="82c11-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="82c11-107">EXAMPLES</span></span>

### <span data-ttu-id="82c11-108">Beispiel 1: Erhalten einer angegebenen Konfiguration für private Links</span><span class="sxs-lookup"><span data-stu-id="82c11-108">Example 1 : Get a specified private link configuration</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfiguration = Get-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -ApplicationGateway $AppGw
```

<span data-ttu-id="82c11-109">Der erste Befehl ruft ein Anwendungsgateway namens ApplicationGateway01 aus der Ressourcengruppe "ResourceGroup01" ab und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="82c11-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="82c11-110">Der zweite Befehl ruft die private Linkkonfiguration mit dem Namen privateLinkConfig01 aus $AppGw ab und speichert sie in der $PrivateLinkConfiguration Variablen.</span><span class="sxs-lookup"><span data-stu-id="82c11-110">The second command gets the private link configuration named privateLinkConfig01 from $AppGw and stores it in the $PrivateLinkConfiguration variable.</span></span>

### <span data-ttu-id="82c11-111">Beispiel 2: Eine Liste der Konfiguration privater Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="82c11-111">Example 2 : Get a list of private link configuration</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfigurations = Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="82c11-112">Der erste Befehl ruft ein Anwendungsgateway namens ApplicationGateway01 aus der Ressourcengruppe "ResourceGroup01" ab und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="82c11-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="82c11-113">Der zweite Befehl ruft alle privaten Linkkonfigurationen aus $AppGw und speichert sie in der $PrivateLinkConfigurations-Variable.</span><span class="sxs-lookup"><span data-stu-id="82c11-113">The second command gets all the private link configurations from $AppGw and stores it in the $PrivateLinkConfigurations variable.</span></span>

## <span data-ttu-id="82c11-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="82c11-114">PARAMETERS</span></span>

### <span data-ttu-id="82c11-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="82c11-115">-ApplicationGateway</span></span>
<span data-ttu-id="82c11-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="82c11-116">The applicationGateway</span></span>

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

### <span data-ttu-id="82c11-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82c11-117">-DefaultProfile</span></span>
<span data-ttu-id="82c11-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="82c11-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82c11-119">-Name</span><span class="sxs-lookup"><span data-stu-id="82c11-119">-Name</span></span>
<span data-ttu-id="82c11-120">Der Name der PrivateLink-Konfiguration des Anwendungsgateways</span><span class="sxs-lookup"><span data-stu-id="82c11-120">The name of the application gateway privateLink configuration</span></span>

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

### <span data-ttu-id="82c11-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82c11-121">CommonParameters</span></span>
<span data-ttu-id="82c11-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82c11-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82c11-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="82c11-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82c11-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="82c11-124">INPUTS</span></span>

### <span data-ttu-id="82c11-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="82c11-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="82c11-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="82c11-126">OUTPUTS</span></span>

### <span data-ttu-id="82c11-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="82c11-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="82c11-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="82c11-128">NOTES</span></span>

## <span data-ttu-id="82c11-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="82c11-129">RELATED LINKS</span></span>

[<span data-ttu-id="82c11-130">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="82c11-130">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="82c11-131">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="82c11-131">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="82c11-132">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="82c11-132">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="82c11-133">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="82c11-133">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)