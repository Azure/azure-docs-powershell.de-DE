---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 87f6f441220f1f8ab47fee5356bddca8d02b96c0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301839"
---
# <span data-ttu-id="d5e36-101">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d5e36-101">Remove-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="d5e36-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d5e36-102">SYNOPSIS</span></span>
<span data-ttu-id="d5e36-103">Entfernt eine IP-Konfiguration von einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="d5e36-103">Removes an IP configuration from an application gateway.</span></span>

## <span data-ttu-id="d5e36-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5e36-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5e36-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d5e36-105">DESCRIPTION</span></span>
<span data-ttu-id="d5e36-106">Das Cmdlet **Remove-AzApplicationGatewayIPConfiguration** entfernt eine IP-Konfiguration von einem Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="d5e36-106">The **Remove-AzApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="d5e36-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d5e36-107">EXAMPLES</span></span>

### <span data-ttu-id="d5e36-108">Beispiel 1: Entfernen einer IP-Konfiguration von einem Azure Application Gateway</span><span class="sxs-lookup"><span data-stu-id="d5e36-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="d5e36-109">Der erste Befehl ruft ein Anwendungsgateway ab und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="d5e36-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d5e36-110">Der zweite Befehl entfernt die IP-Konfiguration mit dem Namen Subnet02 aus dem Anwendungsgateway, das in $AppGw gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="d5e36-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="d5e36-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5e36-111">PARAMETERS</span></span>

### <span data-ttu-id="d5e36-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d5e36-112">-ApplicationGateway</span></span>
<span data-ttu-id="d5e36-113">Gibt das Anwendungsgateway an, aus dem eine IP-Konfiguration entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d5e36-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5e36-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5e36-114">-DefaultProfile</span></span>
<span data-ttu-id="d5e36-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d5e36-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5e36-116">-Name</span><span class="sxs-lookup"><span data-stu-id="d5e36-116">-Name</span></span>
<span data-ttu-id="d5e36-117">Gibt den Namen der zu entfernenden IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="d5e36-117">Specifies the name of the IP configuration to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5e36-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5e36-118">CommonParameters</span></span>
<span data-ttu-id="d5e36-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5e36-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5e36-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5e36-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5e36-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d5e36-121">INPUTS</span></span>

### <span data-ttu-id="d5e36-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d5e36-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d5e36-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d5e36-123">OUTPUTS</span></span>

### <span data-ttu-id="d5e36-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d5e36-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d5e36-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="d5e36-125">NOTES</span></span>

## <span data-ttu-id="d5e36-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d5e36-126">RELATED LINKS</span></span>

[<span data-ttu-id="d5e36-127">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d5e36-127">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="d5e36-128">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d5e36-128">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="d5e36-129">Neu – AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d5e36-129">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="d5e36-130">Satz-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d5e36-130">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


