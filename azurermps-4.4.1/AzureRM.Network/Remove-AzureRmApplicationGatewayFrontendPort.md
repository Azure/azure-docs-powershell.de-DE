---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A698954A-994E-45AD-BA36-1E03196CFCB0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: 9e3a9a515f7b33e23cb7444baa281e083c3c10ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497077"
---
# <span data-ttu-id="6f779-101">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="6f779-101">Remove-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="6f779-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6f779-102">SYNOPSIS</span></span>
<span data-ttu-id="6f779-103">Entfernt einen Front-End-Port von einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="6f779-103">Removes a front-end port from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f779-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f779-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayFrontendPort -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f779-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6f779-105">DESCRIPTION</span></span>
<span data-ttu-id="6f779-106">Mit dem Cmdlet **Remove-AzureRmApplicationGatewayFrontendPort** wird ein Front-End-Port aus einem Azure Application Gateway entfernt.</span><span class="sxs-lookup"><span data-stu-id="6f779-106">The **Remove-AzureRmApplicationGatewayFrontendPort** cmdlet removes a front-end port from an Azure application gateway.</span></span>

## <span data-ttu-id="6f779-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6f779-107">EXAMPLES</span></span>

### <span data-ttu-id="6f779-108">Beispiel: Entfernen eines Front-End-Ports von einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="6f779-108">Example: Remove a front-end port from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort02"
```

<span data-ttu-id="6f779-109">Der erste Befehl ruft ein Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert das Gateway in $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="6f779-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores the gateway in $AppGw variable.</span></span>

<span data-ttu-id="6f779-110">Der zweite Befehl entfernt den Port mit dem Namen FrontEndPort02 aus dem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="6f779-110">The second command removes the port named FrontEndPort02 from the application gateway.</span></span>

## <span data-ttu-id="6f779-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f779-111">PARAMETERS</span></span>

### <span data-ttu-id="6f779-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6f779-112">-ApplicationGateway</span></span>
<span data-ttu-id="6f779-113">Gibt das Anwendungsgateway an, aus dem ein Front-End-Port entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6f779-113">Specifies the application gateway from which to remove a front-end port.</span></span>

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

### <span data-ttu-id="6f779-114">-Name</span><span class="sxs-lookup"><span data-stu-id="6f779-114">-Name</span></span>
<span data-ttu-id="6f779-115">Gibt den Namen des zu entfernenden Frontend-Ports an.</span><span class="sxs-lookup"><span data-stu-id="6f779-115">Specifies name of the frontend port to remove.</span></span>

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

### <span data-ttu-id="6f779-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f779-116">-DefaultProfile</span></span>
<span data-ttu-id="6f779-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6f779-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f779-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f779-118">CommonParameters</span></span>
<span data-ttu-id="6f779-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f779-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f779-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f779-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f779-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6f779-121">INPUTS</span></span>

### <span data-ttu-id="6f779-122">System. String</span><span class="sxs-lookup"><span data-stu-id="6f779-122">System.String</span></span>

## <span data-ttu-id="6f779-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6f779-123">OUTPUTS</span></span>

### <span data-ttu-id="6f779-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6f779-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6f779-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="6f779-125">NOTES</span></span>

## <span data-ttu-id="6f779-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6f779-126">RELATED LINKS</span></span>

[<span data-ttu-id="6f779-127">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="6f779-127">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="6f779-128">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="6f779-128">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="6f779-129">Neu – AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="6f779-129">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="6f779-130">Satz-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="6f779-130">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)


