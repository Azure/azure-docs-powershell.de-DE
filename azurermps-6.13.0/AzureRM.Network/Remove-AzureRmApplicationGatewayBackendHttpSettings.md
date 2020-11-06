---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayBackendHttpSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayBackendHttpSettings.md
ms.openlocfilehash: 036fef4e43d8d754bd0798e72159cba367a3e2f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480286"
---
# <span data-ttu-id="b1a98-101">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b1a98-101">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="b1a98-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b1a98-102">SYNOPSIS</span></span>
<span data-ttu-id="b1a98-103">Entfernt die Back-End-HTTP-Einstellungen von einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="b1a98-103">Removes back-end HTTP settings from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1a98-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1a98-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayBackendHttpSettings -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1a98-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b1a98-105">DESCRIPTION</span></span>
<span data-ttu-id="b1a98-106">Das Remove-AzureRmApplicationGatewayBackendHttpSettings-Cmdlet entfernt http-Einstellungen (Back-End-Hypertext-Übertragungsprotokoll) von einem Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="b1a98-106">The Remove-AzureRmApplicationGatewayBackendHttpSettings cmdlet removes back-end Hypertext Transfer Protocol (HTTP) settings from an Azure application gateway.</span></span>

## <span data-ttu-id="b1a98-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b1a98-107">EXAMPLES</span></span>

### <span data-ttu-id="b1a98-108">Beispiel 1: Entfernen von Back-End-HTTP-Einstellungen von einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="b1a98-108">Example 1: Remove back-end HTTP settings from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw -Name "BackEndSetting02"
```

<span data-ttu-id="b1a98-109">Der erste Befehl ruft ein Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="b1a98-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b1a98-110">Der zweite Befehl entfernt die Back-End-HTTP-Einstellung mit dem Namen BackEndSetting02 aus dem Anwendungsgateway, das in $AppGw gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="b1a98-110">The second command removes the back-end HTTP setting named BackEndSetting02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="b1a98-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1a98-111">PARAMETERS</span></span>

### <span data-ttu-id="b1a98-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b1a98-112">-ApplicationGateway</span></span>
<span data-ttu-id="b1a98-113">Gibt das Anwendungsgateway an, von dem dieses Cmdlet die Back-End-HTTP-Einstellungen entfernt.</span><span class="sxs-lookup"><span data-stu-id="b1a98-113">Specifies the application gateway from which this cmdlet removes back-end HTTP settings.</span></span>

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

### <span data-ttu-id="b1a98-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1a98-114">-DefaultProfile</span></span>
<span data-ttu-id="b1a98-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b1a98-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1a98-116">-Name</span><span class="sxs-lookup"><span data-stu-id="b1a98-116">-Name</span></span>
<span data-ttu-id="b1a98-117">Gibt den Namen der Back-End-HTTP-Einstellungen an, die von diesem Cmdlet entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="b1a98-117">Specifies the name of the back-end HTTP settings that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b1a98-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1a98-118">CommonParameters</span></span>
<span data-ttu-id="b1a98-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1a98-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1a98-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1a98-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1a98-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b1a98-121">INPUTS</span></span>

### <span data-ttu-id="b1a98-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b1a98-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="b1a98-123">Parameter: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b1a98-123">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="b1a98-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b1a98-124">OUTPUTS</span></span>

### <span data-ttu-id="b1a98-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b1a98-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b1a98-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="b1a98-126">NOTES</span></span>

## <span data-ttu-id="b1a98-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b1a98-127">RELATED LINKS</span></span>

[<span data-ttu-id="b1a98-128">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b1a98-128">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="b1a98-129">Neu – AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b1a98-129">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="b1a98-130">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b1a98-130">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="b1a98-131">Satz-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b1a98-131">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

