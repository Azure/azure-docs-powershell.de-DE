---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C90AF6C-3193-4D75-A78F-3EC315C6D7DF
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 46cf3a786642262c1f6d0df0e2c1fd770d61ec6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922360"
---
# <span data-ttu-id="f489f-101">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f489f-101">Remove-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="f489f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f489f-102">SYNOPSIS</span></span>
<span data-ttu-id="f489f-103">Entfernt einen HTTP-Listener aus einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="f489f-103">Removes an HTTP listener from an application gateway.</span></span>

## <span data-ttu-id="f489f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f489f-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListener -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f489f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f489f-105">DESCRIPTION</span></span>
<span data-ttu-id="f489f-106">Das **Cmdlet Remove-AzApplicationGatewayHttpListener** entfernt einen HTTP-Listener aus einem Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="f489f-106">The **Remove-AzApplicationGatewayHttpListener** cmdlet removes an HTTP listener from an Azure application gateway.</span></span>

## <span data-ttu-id="f489f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f489f-107">EXAMPLES</span></span>

### <span data-ttu-id="f489f-108">Beispiel 1: Entfernen eines HTTP-Listeners für das Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="f489f-108">Example 1: Remove an application gateway HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener02"
```

<span data-ttu-id="f489f-109">Der erste Befehl ruft ein Anwendungsgateway ab und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="f489f-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f489f-110">Mit dem zweiten Befehl wird der HTTP-Listener mit dem Namen Listener02 aus dem anwendungsgateway entfernt, das in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f489f-110">The second command removes the HTTP listener named Listener02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="f489f-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f489f-111">PARAMETERS</span></span>

### <span data-ttu-id="f489f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f489f-112">-ApplicationGateway</span></span>
<span data-ttu-id="f489f-113">Gibt das Anwendungsgateway an, aus dem ein HTTP-Listener entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f489f-113">Specifies the application gateway from which to remove an HTTP listener.</span></span>

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

### <span data-ttu-id="f489f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f489f-114">-DefaultProfile</span></span>
<span data-ttu-id="f489f-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f489f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f489f-116">-Name</span><span class="sxs-lookup"><span data-stu-id="f489f-116">-Name</span></span>
<span data-ttu-id="f489f-117">Gibt den Namen des HTTP-Listeners an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="f489f-117">Specifies the name of the HTTP listener that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f489f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f489f-118">CommonParameters</span></span>
<span data-ttu-id="f489f-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f489f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f489f-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f489f-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f489f-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f489f-121">INPUTS</span></span>

### <span data-ttu-id="f489f-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f489f-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f489f-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f489f-123">OUTPUTS</span></span>

### <span data-ttu-id="f489f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f489f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="f489f-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f489f-125">NOTES</span></span>

## <span data-ttu-id="f489f-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f489f-126">RELATED LINKS</span></span>

[<span data-ttu-id="f489f-127">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f489f-127">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="f489f-128">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f489f-128">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="f489f-129">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f489f-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="f489f-130">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f489f-130">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


