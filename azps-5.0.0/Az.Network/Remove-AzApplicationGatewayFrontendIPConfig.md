---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 289B761C-1A1D-46D2-8755-B6B6A4758EFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: d376bc1e70d0441f139b64c19466a88daf6877c4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176299"
---
# <span data-ttu-id="a1a28-101">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="a1a28-101">Remove-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="a1a28-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a1a28-102">SYNOPSIS</span></span>
<span data-ttu-id="a1a28-103">Entfernt eine Front-End-IP-Konfiguration von einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="a1a28-103">Removes a front-end IP configuration from an application gateway.</span></span>

## <span data-ttu-id="a1a28-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1a28-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendIPConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1a28-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1a28-105">DESCRIPTION</span></span>
<span data-ttu-id="a1a28-106">Das Cmdlet **Remove-AzApplicationGatewayFrontendIPConfig** entfernt die Frontend-IP aus einem Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="a1a28-106">The **Remove-AzApplicationGatewayFrontendIPConfig** cmdlet removes frontend IP from an Azure application gateway.</span></span>

## <span data-ttu-id="a1a28-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a1a28-107">EXAMPLES</span></span>

### <span data-ttu-id="a1a28-108">Beispiel 1: Entfernen einer Front-End-IP-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="a1a28-108">Example 1: Remove a front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIP02"
```

<span data-ttu-id="a1a28-109">Der erste Befehl ruft ein Anwendungsgateway mit dem Namen ApplicationGateway01 ab und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="a1a28-109">The first command gets an application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a1a28-110">Der zweite Befehl entfernt die Front-End-IP-Konfiguration mit dem Namen FrontEndIP02 aus dem Anwendungsgateway, das in $AppGw gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="a1a28-110">The second command removes the front-end IP configuration named FrontEndIP02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="a1a28-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1a28-111">PARAMETERS</span></span>

### <span data-ttu-id="a1a28-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a1a28-112">-ApplicationGateway</span></span>
<span data-ttu-id="a1a28-113">Gibt ein Anwendungsgateway an, aus dem eine Front-End-IP-Konfiguration entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a1a28-113">Specifies an application gateway from which to remove a front-end IP configuration.</span></span>

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

### <span data-ttu-id="a1a28-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1a28-114">-DefaultProfile</span></span>
<span data-ttu-id="a1a28-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a1a28-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1a28-116">-Name</span><span class="sxs-lookup"><span data-stu-id="a1a28-116">-Name</span></span>
<span data-ttu-id="a1a28-117">Gibt den Namen einer zu entfernenden Front-End-IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="a1a28-117">Specifies the name of a front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="a1a28-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1a28-118">CommonParameters</span></span>
<span data-ttu-id="a1a28-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1a28-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1a28-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1a28-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1a28-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a1a28-121">INPUTS</span></span>

### <span data-ttu-id="a1a28-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a1a28-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a1a28-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a1a28-123">OUTPUTS</span></span>

### <span data-ttu-id="a1a28-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a1a28-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a1a28-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="a1a28-125">NOTES</span></span>

## <span data-ttu-id="a1a28-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a1a28-126">RELATED LINKS</span></span>

[<span data-ttu-id="a1a28-127">Add-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="a1a28-127">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="a1a28-128">Get-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="a1a28-128">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="a1a28-129">Neu – AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="a1a28-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="a1a28-130">Satz-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="a1a28-130">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


