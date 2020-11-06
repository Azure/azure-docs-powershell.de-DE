---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: bd9ab62406d033eefe3fb3723d2a2ebf2f9dbb8b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497069"
---
# <span data-ttu-id="a3a72-101">Remove-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3a72-101">Remove-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="a3a72-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a3a72-102">SYNOPSIS</span></span>
<span data-ttu-id="a3a72-103">Entfernt eine Umleitungs Konfiguration von einem vorhandenen Anwendungs Gateway.</span><span class="sxs-lookup"><span data-stu-id="a3a72-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3a72-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3a72-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3a72-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a3a72-105">DESCRIPTION</span></span>
<span data-ttu-id="a3a72-106">Das Cmdlet **Remove-AzureRmApplicationGatewayRedirectConfiguration** entfernt eine Umleitungs Konfiguration von einem vorhandenen Anwendungs Gateway.</span><span class="sxs-lookup"><span data-stu-id="a3a72-106">The **Remove-AzureRmApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="a3a72-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a3a72-107">EXAMPLES</span></span>

### <span data-ttu-id="a3a72-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a3a72-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="a3a72-109">Der erste Befehl ruft ein Anwendungsgateway ab und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="a3a72-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="a3a72-110">Mit dem zweiten Befehl wird die Umleitungs Konfiguration mit dem Namen Redirect01 aus dem Anwendungsgateway entfernt, das in $AppGw gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="a3a72-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="a3a72-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3a72-111">PARAMETERS</span></span>

### <span data-ttu-id="a3a72-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a3a72-112">-ApplicationGateway</span></span>
<span data-ttu-id="a3a72-113">Die applicationGateway</span><span class="sxs-lookup"><span data-stu-id="a3a72-113">The applicationGateway</span></span>

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

### <span data-ttu-id="a3a72-114">-Name</span><span class="sxs-lookup"><span data-stu-id="a3a72-114">-Name</span></span>
<span data-ttu-id="a3a72-115">Der Name der Umleitungs Konfiguration</span><span class="sxs-lookup"><span data-stu-id="a3a72-115">The name of the redirect configuration</span></span>

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

### <span data-ttu-id="a3a72-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3a72-116">-DefaultProfile</span></span>
<span data-ttu-id="a3a72-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a3a72-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3a72-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3a72-118">CommonParameters</span></span>
<span data-ttu-id="a3a72-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3a72-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3a72-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3a72-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3a72-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a3a72-121">INPUTS</span></span>

### <span data-ttu-id="a3a72-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a3a72-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a3a72-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a3a72-123">OUTPUTS</span></span>

### <span data-ttu-id="a3a72-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a3a72-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a3a72-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="a3a72-125">NOTES</span></span>

## <span data-ttu-id="a3a72-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a3a72-126">RELATED LINKS</span></span>

