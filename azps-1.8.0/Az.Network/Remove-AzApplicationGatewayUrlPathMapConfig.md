---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 27561ec3592633e1e7c668a4d901ba1e7d39c050
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660397"
---
# <span data-ttu-id="42ae1-101">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="42ae1-101">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="42ae1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="42ae1-102">SYNOPSIS</span></span>
<span data-ttu-id="42ae1-103">Entfernt URL-Pfad Zuordnungen zu einem Back-End-Serverpool.</span><span class="sxs-lookup"><span data-stu-id="42ae1-103">Removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="42ae1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="42ae1-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42ae1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42ae1-105">DESCRIPTION</span></span>
<span data-ttu-id="42ae1-106">Das Cmdlet **Remove-AzApplicationGatewayUrlPathMapConfig** entfernt URL-Pfad Zuordnungen zu einem Back-End-Serverpool.</span><span class="sxs-lookup"><span data-stu-id="42ae1-106">The **Remove-AzApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="42ae1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="42ae1-107">EXAMPLES</span></span>

### <span data-ttu-id="42ae1-108">Beispiel 1: Entfernen einer URL-Pfadzuordnung von einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="42ae1-108">Example 1: Remove an URL path mapping from an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Remove-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "map01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="42ae1-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen appGwName ab und speichert das Ergebnis in der $appgw Variablen.</span><span class="sxs-lookup"><span data-stu-id="42ae1-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="42ae1-110">Der zweite Befehl entfernt die URL-Pfadzuordnung mit dem Namen map01 aus dem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="42ae1-110">The second command removes the URL path mapping named map01 from the application gateway.</span></span>
<span data-ttu-id="42ae1-111">Der dritte Befehl aktualisiert das Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="42ae1-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="42ae1-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="42ae1-112">PARAMETERS</span></span>

### <span data-ttu-id="42ae1-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="42ae1-113">-ApplicationGateway</span></span>
<span data-ttu-id="42ae1-114">Gibt das Anwendungsgateway an, auf das dieses Cmdlet die URL-Pfad Zuordnungskonfiguration entfernt.</span><span class="sxs-lookup"><span data-stu-id="42ae1-114">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="42ae1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42ae1-115">-DefaultProfile</span></span>
<span data-ttu-id="42ae1-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="42ae1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42ae1-117">-Name</span><span class="sxs-lookup"><span data-stu-id="42ae1-117">-Name</span></span>
<span data-ttu-id="42ae1-118">Gibt den URL-Pfad Zuordnungsnamen an, den dieses Cmdlet vom Back-End-Server entfernt.</span><span class="sxs-lookup"><span data-stu-id="42ae1-118">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

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

### <span data-ttu-id="42ae1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42ae1-119">CommonParameters</span></span>
<span data-ttu-id="42ae1-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42ae1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42ae1-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42ae1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42ae1-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="42ae1-122">INPUTS</span></span>

### <span data-ttu-id="42ae1-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="42ae1-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="42ae1-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="42ae1-124">OUTPUTS</span></span>

### <span data-ttu-id="42ae1-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="42ae1-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="42ae1-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="42ae1-126">NOTES</span></span>

## <span data-ttu-id="42ae1-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="42ae1-127">RELATED LINKS</span></span>

[<span data-ttu-id="42ae1-128">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="42ae1-128">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="42ae1-129">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="42ae1-129">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="42ae1-130">Neu – AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="42ae1-130">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="42ae1-131">Satz-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="42ae1-131">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


