---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: f5a0c703640d540dfd5a47f643694f56f87e0438
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663786"
---
# <span data-ttu-id="ab2d4-101">Remove-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="ab2d4-101">Remove-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="ab2d4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ab2d4-102">SYNOPSIS</span></span>
<span data-ttu-id="ab2d4-103">Entfernt eine Umleitungs Konfiguration von einem vorhandenen Anwendungs Gateway.</span><span class="sxs-lookup"><span data-stu-id="ab2d4-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab2d4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab2d4-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab2d4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ab2d4-105">DESCRIPTION</span></span>
<span data-ttu-id="ab2d4-106">Das Cmdlet **Remove-AzureRmApplicationGatewayRedirectConfiguration** entfernt eine Umleitungs Konfiguration von einem vorhandenen Anwendungs Gateway.</span><span class="sxs-lookup"><span data-stu-id="ab2d4-106">The **Remove-AzureRmApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="ab2d4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ab2d4-107">EXAMPLES</span></span>

### <span data-ttu-id="ab2d4-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ab2d4-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="ab2d4-109">Der erste Befehl ruft ein Anwendungsgateway ab und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="ab2d4-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="ab2d4-110">Mit dem zweiten Befehl wird die Umleitungs Konfiguration mit dem Namen Redirect01 aus dem Anwendungsgateway entfernt, das in $AppGw gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="ab2d4-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="ab2d4-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab2d4-111">PARAMETERS</span></span>

### <span data-ttu-id="ab2d4-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ab2d4-112">-ApplicationGateway</span></span>
<span data-ttu-id="ab2d4-113">Die applicationGateway</span><span class="sxs-lookup"><span data-stu-id="ab2d4-113">The applicationGateway</span></span>

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

### <span data-ttu-id="ab2d4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab2d4-114">-DefaultProfile</span></span>
<span data-ttu-id="ab2d4-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ab2d4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab2d4-116">-Name</span><span class="sxs-lookup"><span data-stu-id="ab2d4-116">-Name</span></span>
<span data-ttu-id="ab2d4-117">Der Name der Umleitungs Konfiguration</span><span class="sxs-lookup"><span data-stu-id="ab2d4-117">The name of the redirect configuration</span></span>

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

### <span data-ttu-id="ab2d4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab2d4-118">CommonParameters</span></span>
<span data-ttu-id="ab2d4-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab2d4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab2d4-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab2d4-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab2d4-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ab2d4-121">INPUTS</span></span>

### <span data-ttu-id="ab2d4-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ab2d4-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ab2d4-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ab2d4-123">OUTPUTS</span></span>

### <span data-ttu-id="ab2d4-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ab2d4-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ab2d4-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="ab2d4-125">NOTES</span></span>

## <span data-ttu-id="ab2d4-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ab2d4-126">RELATED LINKS</span></span>

