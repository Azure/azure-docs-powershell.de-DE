---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: fdd461ea2908e59ba824b09a49bed3b6b8f4d38f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176175"
---
# <span data-ttu-id="37f8b-101">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="37f8b-101">Remove-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="37f8b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="37f8b-102">SYNOPSIS</span></span>
<span data-ttu-id="37f8b-103">Entfernt eine Umleitungs Konfiguration von einem vorhandenen Anwendungs Gateway.</span><span class="sxs-lookup"><span data-stu-id="37f8b-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="37f8b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="37f8b-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37f8b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="37f8b-105">DESCRIPTION</span></span>
<span data-ttu-id="37f8b-106">Das Cmdlet **Remove-AzApplicationGatewayRedirectConfiguration** entfernt eine Umleitungs Konfiguration von einem vorhandenen Anwendungs Gateway.</span><span class="sxs-lookup"><span data-stu-id="37f8b-106">The **Remove-AzApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="37f8b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="37f8b-107">EXAMPLES</span></span>

### <span data-ttu-id="37f8b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="37f8b-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="37f8b-109">Der erste Befehl ruft ein Anwendungsgateway ab und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="37f8b-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="37f8b-110">Mit dem zweiten Befehl wird die Umleitungs Konfiguration mit dem Namen Redirect01 aus dem Anwendungsgateway entfernt, das in $AppGw gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="37f8b-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="37f8b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="37f8b-111">PARAMETERS</span></span>

### <span data-ttu-id="37f8b-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="37f8b-112">-ApplicationGateway</span></span>
<span data-ttu-id="37f8b-113">Die applicationGateway</span><span class="sxs-lookup"><span data-stu-id="37f8b-113">The applicationGateway</span></span>

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

### <span data-ttu-id="37f8b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37f8b-114">-DefaultProfile</span></span>
<span data-ttu-id="37f8b-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="37f8b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37f8b-116">-Name</span><span class="sxs-lookup"><span data-stu-id="37f8b-116">-Name</span></span>
<span data-ttu-id="37f8b-117">Der Name der Umleitungs Konfiguration</span><span class="sxs-lookup"><span data-stu-id="37f8b-117">The name of the redirect configuration</span></span>

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

### <span data-ttu-id="37f8b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37f8b-118">CommonParameters</span></span>
<span data-ttu-id="37f8b-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37f8b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37f8b-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37f8b-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37f8b-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="37f8b-121">INPUTS</span></span>

### <span data-ttu-id="37f8b-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="37f8b-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="37f8b-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="37f8b-123">OUTPUTS</span></span>

### <span data-ttu-id="37f8b-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="37f8b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="37f8b-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="37f8b-125">NOTES</span></span>

## <span data-ttu-id="37f8b-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="37f8b-126">RELATED LINKS</span></span>

[<span data-ttu-id="37f8b-127">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="37f8b-127">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="37f8b-128">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="37f8b-128">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="37f8b-129">Neu – AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="37f8b-129">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="37f8b-130">Satz-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="37f8b-130">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
