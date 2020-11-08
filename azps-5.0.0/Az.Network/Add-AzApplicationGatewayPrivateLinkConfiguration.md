---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 2083dd00c5163a67492ff9973fdf7399d67d7cb6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176779"
---
# <span data-ttu-id="b0e32-101">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="b0e32-101">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="b0e32-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b0e32-102">SYNOPSIS</span></span>
<span data-ttu-id="b0e32-103">Fügt eine private Link Konfiguration zu einem Anwendungsgateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="b0e32-103">Adds a private link configuration to an application gateway.</span></span>

## <span data-ttu-id="b0e32-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0e32-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b0e32-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b0e32-105">DESCRIPTION</span></span>
<span data-ttu-id="b0e32-106">Das Cmdlet **Add-AzApplicationGatewayPrivateLinkConfiguration** fügt eine private Link Konfiguration zu einem Anwendungsgateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="b0e32-106">The **Add-AzApplicationGatewayPrivateLinkConfiguration** cmdlet adds a private link configuration to an application gateway.</span></span>

## <span data-ttu-id="b0e32-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b0e32-107">EXAMPLES</span></span>

### <span data-ttu-id="b0e32-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b0e32-108">Example 1</span></span>
```powershell
PS C:\> $PrivateLinkIpConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "ipConfig01" -Subnet $subnet -Primary
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01" -IpConfiguration $PrivateLinkIpConfiguration
```

<span data-ttu-id="b0e32-109">Der erste Befehl erstellt ein privateLinkIpConfiguration und speichert es in der $PrivateLinkIpConfiguration-Variablen.</span><span class="sxs-lookup"><span data-stu-id="b0e32-109">The first command creates a privateLinkIpConfiguration and stores it in the $PrivateLinkIpConfiguration variable.</span></span>
<span data-ttu-id="b0e32-110">Der zweite Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="b0e32-110">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b0e32-111">Der dritte Befehl fügt die private Link-Konfiguration mit dem Namen "privateLinkConfig01" für das Gateway in $AppGw</span><span class="sxs-lookup"><span data-stu-id="b0e32-111">The third command adds the private link configuration named privateLinkConfig01, for the gateway in $AppGw</span></span>

## <span data-ttu-id="b0e32-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0e32-112">PARAMETERS</span></span>

### <span data-ttu-id="b0e32-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b0e32-113">-ApplicationGateway</span></span>
<span data-ttu-id="b0e32-114">Die applicationGateway</span><span class="sxs-lookup"><span data-stu-id="b0e32-114">The applicationGateway</span></span>

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

### <span data-ttu-id="b0e32-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0e32-115">-DefaultProfile</span></span>
<span data-ttu-id="b0e32-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b0e32-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0e32-117">-IPKonfigurationsdateiAddress</span><span class="sxs-lookup"><span data-stu-id="b0e32-117">-IpConfiguration</span></span>
<span data-ttu-id="b0e32-118">Die Liste der IPKonfigurationsdateiAddress</span><span class="sxs-lookup"><span data-stu-id="b0e32-118">The list of ipConfiguration</span></span>

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

### <span data-ttu-id="b0e32-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b0e32-119">-Name</span></span>
<span data-ttu-id="b0e32-120">Der Name der privateLink-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="b0e32-120">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="b0e32-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0e32-121">CommonParameters</span></span>
<span data-ttu-id="b0e32-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0e32-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0e32-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0e32-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0e32-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b0e32-124">INPUTS</span></span>

### <span data-ttu-id="b0e32-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b0e32-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="b0e32-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayPrivateLinkIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="b0e32-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="b0e32-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b0e32-127">OUTPUTS</span></span>

### <span data-ttu-id="b0e32-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b0e32-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b0e32-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="b0e32-129">NOTES</span></span>

## <span data-ttu-id="b0e32-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b0e32-130">RELATED LINKS</span></span>

[<span data-ttu-id="b0e32-131">Neu – AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="b0e32-131">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="b0e32-132">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="b0e32-132">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="b0e32-133">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="b0e32-133">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="b0e32-134">Satz-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="b0e32-134">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)