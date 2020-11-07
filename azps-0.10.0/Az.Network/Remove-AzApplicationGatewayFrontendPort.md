---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A698954A-994E-45AD-BA36-1E03196CFCB0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 39a2bd8ad1951cba41ff8fffb124c7486680b352
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841204"
---
# <span data-ttu-id="fa65f-101">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="fa65f-101">Remove-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="fa65f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fa65f-102">SYNOPSIS</span></span>
<span data-ttu-id="fa65f-103">Entfernt einen Front-End-Port von einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="fa65f-103">Removes a front-end port from an application gateway.</span></span>

## <span data-ttu-id="fa65f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa65f-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendPort -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa65f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fa65f-105">DESCRIPTION</span></span>
<span data-ttu-id="fa65f-106">Mit dem Cmdlet **Remove-AzApplicationGatewayFrontendPort** wird ein Front-End-Port aus einem Azure Application Gateway entfernt.</span><span class="sxs-lookup"><span data-stu-id="fa65f-106">The **Remove-AzApplicationGatewayFrontendPort** cmdlet removes a front-end port from an Azure application gateway.</span></span>

## <span data-ttu-id="fa65f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fa65f-107">EXAMPLES</span></span>

### <span data-ttu-id="fa65f-108">Beispiel: Entfernen eines Front-End-Ports von einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="fa65f-108">Example: Remove a front-end port from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort02"
```

<span data-ttu-id="fa65f-109">Der erste Befehl ruft ein Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert das Gateway in $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="fa65f-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores the gateway in $AppGw variable.</span></span>

<span data-ttu-id="fa65f-110">Der zweite Befehl entfernt den Port mit dem Namen FrontEndPort02 aus dem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="fa65f-110">The second command removes the port named FrontEndPort02 from the application gateway.</span></span>

## <span data-ttu-id="fa65f-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa65f-111">PARAMETERS</span></span>

### <span data-ttu-id="fa65f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fa65f-112">-ApplicationGateway</span></span>
<span data-ttu-id="fa65f-113">Gibt das Anwendungsgateway an, aus dem ein Front-End-Port entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fa65f-113">Specifies the application gateway from which to remove a front-end port.</span></span>

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

### <span data-ttu-id="fa65f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa65f-114">-DefaultProfile</span></span>
<span data-ttu-id="fa65f-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fa65f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa65f-116">-Name</span><span class="sxs-lookup"><span data-stu-id="fa65f-116">-Name</span></span>
<span data-ttu-id="fa65f-117">Gibt den Namen des zu entfernenden Frontend-Ports an.</span><span class="sxs-lookup"><span data-stu-id="fa65f-117">Specifies name of the frontend port to remove.</span></span>

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

### <span data-ttu-id="fa65f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa65f-118">CommonParameters</span></span>
<span data-ttu-id="fa65f-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa65f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa65f-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa65f-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa65f-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fa65f-121">INPUTS</span></span>

### <span data-ttu-id="fa65f-122">System. String</span><span class="sxs-lookup"><span data-stu-id="fa65f-122">System.String</span></span>

## <span data-ttu-id="fa65f-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fa65f-123">OUTPUTS</span></span>

### <span data-ttu-id="fa65f-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fa65f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fa65f-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="fa65f-125">NOTES</span></span>

## <span data-ttu-id="fa65f-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fa65f-126">RELATED LINKS</span></span>

[<span data-ttu-id="fa65f-127">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="fa65f-127">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="fa65f-128">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="fa65f-128">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="fa65f-129">Neu – AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="fa65f-129">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="fa65f-130">Satz-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="fa65f-130">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


