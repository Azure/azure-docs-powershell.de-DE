---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: d75cbcbf89fde83419b9a1f97c0f66805258c82d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822939"
---
# <span data-ttu-id="4ff11-101">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ff11-101">Remove-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="4ff11-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4ff11-102">SYNOPSIS</span></span>
<span data-ttu-id="4ff11-103">Entfernt eine Umleitungs Konfiguration von einem vorhandenen Anwendungs Gateway.</span><span class="sxs-lookup"><span data-stu-id="4ff11-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="4ff11-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ff11-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ff11-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4ff11-105">DESCRIPTION</span></span>
<span data-ttu-id="4ff11-106">Das Cmdlet **Remove-AzApplicationGatewayRedirectConfiguration** entfernt eine Umleitungs Konfiguration von einem vorhandenen Anwendungs Gateway.</span><span class="sxs-lookup"><span data-stu-id="4ff11-106">The **Remove-AzApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="4ff11-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4ff11-107">EXAMPLES</span></span>

### <span data-ttu-id="4ff11-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4ff11-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="4ff11-109">Der erste Befehl ruft ein Anwendungsgateway ab und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="4ff11-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4ff11-110">Mit dem zweiten Befehl wird die Umleitungs Konfiguration mit dem Namen Redirect01 aus dem Anwendungsgateway entfernt, das in $AppGw gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="4ff11-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="4ff11-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ff11-111">PARAMETERS</span></span>

### <span data-ttu-id="4ff11-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4ff11-112">-ApplicationGateway</span></span>
<span data-ttu-id="4ff11-113">Die applicationGateway</span><span class="sxs-lookup"><span data-stu-id="4ff11-113">The applicationGateway</span></span>

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

### <span data-ttu-id="4ff11-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ff11-114">-DefaultProfile</span></span>
<span data-ttu-id="4ff11-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4ff11-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ff11-116">-Name</span><span class="sxs-lookup"><span data-stu-id="4ff11-116">-Name</span></span>
<span data-ttu-id="4ff11-117">Der Name der Umleitungs Konfiguration</span><span class="sxs-lookup"><span data-stu-id="4ff11-117">The name of the redirect configuration</span></span>

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

### <span data-ttu-id="4ff11-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ff11-118">CommonParameters</span></span>
<span data-ttu-id="4ff11-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ff11-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ff11-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ff11-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ff11-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4ff11-121">INPUTS</span></span>

### <span data-ttu-id="4ff11-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4ff11-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4ff11-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4ff11-123">OUTPUTS</span></span>

### <span data-ttu-id="4ff11-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4ff11-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4ff11-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="4ff11-125">NOTES</span></span>

## <span data-ttu-id="4ff11-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4ff11-126">RELATED LINKS</span></span>

[<span data-ttu-id="4ff11-127">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ff11-127">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="4ff11-128">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ff11-128">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="4ff11-129">Neu – AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ff11-129">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="4ff11-130">Satz-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ff11-130">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
