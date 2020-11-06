---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6C90AF6C-3193-4D75-A78F-3EC315C6D7DF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: 58c7e2770380d309125b3e242c854fcdb86a8f08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497073"
---
# <span data-ttu-id="32213-101">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="32213-101">Remove-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="32213-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="32213-102">SYNOPSIS</span></span>
<span data-ttu-id="32213-103">Entfernt einen HTTP-Listener von einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="32213-103">Removes an HTTP listener from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32213-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="32213-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayHttpListener -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32213-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="32213-105">DESCRIPTION</span></span>
<span data-ttu-id="32213-106">Das Cmdlet **Remove-AzureRmApplicationGatewayHttpListener** entfernt einen HTTP-Listener aus einem Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="32213-106">The **Remove-AzureRmApplicationGatewayHttpListener** cmdlet removes an HTTP listener from an Azure application gateway.</span></span>

## <span data-ttu-id="32213-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="32213-107">EXAMPLES</span></span>

### <span data-ttu-id="32213-108">Beispiel 1: Entfernen eines Application Gateway HTTP-Listeners</span><span class="sxs-lookup"><span data-stu-id="32213-108">Example 1: Remove an application gateway HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener02"
```

<span data-ttu-id="32213-109">Der erste Befehl ruft ein Anwendungsgateway ab und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="32213-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="32213-110">Mit dem zweiten Befehl wird der HTTP-Listener mit dem Namen Listener02 aus dem Anwendungsgateway entfernt, das in $AppGw gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="32213-110">The second command removes the HTTP listener named Listener02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="32213-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="32213-111">PARAMETERS</span></span>

### <span data-ttu-id="32213-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="32213-112">-ApplicationGateway</span></span>
<span data-ttu-id="32213-113">Gibt das Anwendungsgateway an, aus dem ein HTTP-Listener entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="32213-113">Specifies the application gateway from which to remove an HTTP listener.</span></span>

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

### <span data-ttu-id="32213-114">-Name</span><span class="sxs-lookup"><span data-stu-id="32213-114">-Name</span></span>
<span data-ttu-id="32213-115">Gibt den Namen des HTTP-Listener an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="32213-115">Specifies the name of the HTTP listener that this cmdlet removes.</span></span>

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

### <span data-ttu-id="32213-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32213-116">-DefaultProfile</span></span>
<span data-ttu-id="32213-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="32213-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32213-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32213-118">CommonParameters</span></span>
<span data-ttu-id="32213-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32213-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32213-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32213-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32213-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="32213-121">INPUTS</span></span>

### <span data-ttu-id="32213-122">System. String</span><span class="sxs-lookup"><span data-stu-id="32213-122">System.String</span></span>

## <span data-ttu-id="32213-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="32213-123">OUTPUTS</span></span>

### <span data-ttu-id="32213-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="32213-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="32213-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="32213-125">NOTES</span></span>

## <span data-ttu-id="32213-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="32213-126">RELATED LINKS</span></span>

[<span data-ttu-id="32213-127">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="32213-127">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="32213-128">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="32213-128">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="32213-129">Neu – AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="32213-129">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="32213-130">Satz-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="32213-130">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


