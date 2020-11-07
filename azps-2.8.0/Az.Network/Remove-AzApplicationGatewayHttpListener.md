---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C90AF6C-3193-4D75-A78F-3EC315C6D7DF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: beceb6788fd2d7498fc886cfbc22aec5ad3a9e23
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821435"
---
# <span data-ttu-id="35c97-101">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="35c97-101">Remove-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="35c97-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="35c97-102">SYNOPSIS</span></span>
<span data-ttu-id="35c97-103">Entfernt einen HTTP-Listener von einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="35c97-103">Removes an HTTP listener from an application gateway.</span></span>

## <span data-ttu-id="35c97-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="35c97-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListener -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35c97-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="35c97-105">DESCRIPTION</span></span>
<span data-ttu-id="35c97-106">Das Cmdlet **Remove-AzApplicationGatewayHttpListener** entfernt einen HTTP-Listener aus einem Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="35c97-106">The **Remove-AzApplicationGatewayHttpListener** cmdlet removes an HTTP listener from an Azure application gateway.</span></span>

## <span data-ttu-id="35c97-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="35c97-107">EXAMPLES</span></span>

### <span data-ttu-id="35c97-108">Beispiel 1: Entfernen eines Application Gateway HTTP-Listeners</span><span class="sxs-lookup"><span data-stu-id="35c97-108">Example 1: Remove an application gateway HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener02"
```

<span data-ttu-id="35c97-109">Der erste Befehl ruft ein Anwendungsgateway ab und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="35c97-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="35c97-110">Mit dem zweiten Befehl wird der HTTP-Listener mit dem Namen Listener02 aus dem Anwendungsgateway entfernt, das in $AppGw gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="35c97-110">The second command removes the HTTP listener named Listener02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="35c97-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="35c97-111">PARAMETERS</span></span>

### <span data-ttu-id="35c97-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="35c97-112">-ApplicationGateway</span></span>
<span data-ttu-id="35c97-113">Gibt das Anwendungsgateway an, aus dem ein HTTP-Listener entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="35c97-113">Specifies the application gateway from which to remove an HTTP listener.</span></span>

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

### <span data-ttu-id="35c97-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35c97-114">-DefaultProfile</span></span>
<span data-ttu-id="35c97-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="35c97-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35c97-116">-Name</span><span class="sxs-lookup"><span data-stu-id="35c97-116">-Name</span></span>
<span data-ttu-id="35c97-117">Gibt den Namen des HTTP-Listener an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="35c97-117">Specifies the name of the HTTP listener that this cmdlet removes.</span></span>

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

### <span data-ttu-id="35c97-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35c97-118">CommonParameters</span></span>
<span data-ttu-id="35c97-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35c97-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35c97-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35c97-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35c97-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="35c97-121">INPUTS</span></span>

### <span data-ttu-id="35c97-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="35c97-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="35c97-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="35c97-123">OUTPUTS</span></span>

### <span data-ttu-id="35c97-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="35c97-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="35c97-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="35c97-125">NOTES</span></span>

## <span data-ttu-id="35c97-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="35c97-126">RELATED LINKS</span></span>

[<span data-ttu-id="35c97-127">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="35c97-127">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="35c97-128">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="35c97-128">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="35c97-129">Neu – AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="35c97-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="35c97-130">Satz-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="35c97-130">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


