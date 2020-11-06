---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 289B761C-1A1D-46D2-8755-B6B6A4758EFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 94cb9e07bc5d4b8d59e543c39ddada5386ebcb27
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479490"
---
# <span data-ttu-id="91f45-101">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="91f45-101">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="91f45-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="91f45-102">SYNOPSIS</span></span>
<span data-ttu-id="91f45-103">Entfernt eine Front-End-IP-Konfiguration von einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="91f45-103">Removes a front-end IP configuration from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91f45-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="91f45-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayFrontendIPConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91f45-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="91f45-105">DESCRIPTION</span></span>
<span data-ttu-id="91f45-106">Das Cmdlet **Remove-AzureRmApplicationGatewayFrontendIPConfig** entfernt die Frontend-IP aus einem Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="91f45-106">The **Remove-AzureRmApplicationGatewayFrontendIPConfig** cmdlet removes frontend IP from an Azure application gateway.</span></span>

## <span data-ttu-id="91f45-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="91f45-107">EXAMPLES</span></span>

### <span data-ttu-id="91f45-108">Beispiel 1: Entfernen einer Front-End-IP-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="91f45-108">Example 1: Remove a front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIP02"
```

<span data-ttu-id="91f45-109">Der erste Befehl ruft ein Anwendungsgateway mit dem Namen ApplicationGateway01 ab und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="91f45-109">The first command gets an application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="91f45-110">Der zweite Befehl entfernt die Front-End-IP-Konfiguration mit dem Namen FrontEndIP02 aus dem Anwendungsgateway, das in $AppGw gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="91f45-110">The second command removes the front-end IP configuration named FrontEndIP02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="91f45-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="91f45-111">PARAMETERS</span></span>

### <span data-ttu-id="91f45-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="91f45-112">-ApplicationGateway</span></span>
<span data-ttu-id="91f45-113">Gibt ein Anwendungsgateway an, aus dem eine Front-End-IP-Konfiguration entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="91f45-113">Specifies an application gateway from which to remove a front-end IP configuration.</span></span>

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

### <span data-ttu-id="91f45-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91f45-114">-DefaultProfile</span></span>
<span data-ttu-id="91f45-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="91f45-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91f45-116">-Name</span><span class="sxs-lookup"><span data-stu-id="91f45-116">-Name</span></span>
<span data-ttu-id="91f45-117">Gibt den Namen einer zu entfernenden Front-End-IP-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="91f45-117">Specifies the name of a front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="91f45-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91f45-118">CommonParameters</span></span>
<span data-ttu-id="91f45-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91f45-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91f45-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91f45-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91f45-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="91f45-121">INPUTS</span></span>

### <span data-ttu-id="91f45-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="91f45-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="91f45-123">Parameter: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="91f45-123">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="91f45-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="91f45-124">OUTPUTS</span></span>

### <span data-ttu-id="91f45-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="91f45-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="91f45-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="91f45-126">NOTES</span></span>

## <span data-ttu-id="91f45-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="91f45-127">RELATED LINKS</span></span>

[<span data-ttu-id="91f45-128">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="91f45-128">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="91f45-129">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="91f45-129">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="91f45-130">Neu – AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="91f45-130">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="91f45-131">Satz-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="91f45-131">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Set-AzureRmApplicationGatewayFrontendIPConfig.md)


