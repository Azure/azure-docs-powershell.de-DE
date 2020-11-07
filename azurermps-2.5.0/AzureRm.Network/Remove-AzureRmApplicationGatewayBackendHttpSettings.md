---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
ms.openlocfilehash: 71ce0dd8d4c5988dfc5cd4226ee76dcec46042ff
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849116"
---
# <span data-ttu-id="0acc4-101">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0acc4-101">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="0acc4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0acc4-102">SYNOPSIS</span></span>
<span data-ttu-id="0acc4-103">Entfernt die Back-End-HTTP-Einstellungen von einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="0acc4-103">Removes back-end HTTP settings from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0acc4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0acc4-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayBackendHttpSettings -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0acc4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0acc4-105">DESCRIPTION</span></span>
<span data-ttu-id="0acc4-106">Das Remove-AzureRmApplicationGatewayBackendHttpSettings-Cmdlet entfernt http-Einstellungen (Back-End-Hypertext-Übertragungsprotokoll) von einem Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="0acc4-106">The Remove-AzureRmApplicationGatewayBackendHttpSettings cmdlet removes back-end Hypertext Transfer Protocol (HTTP) settings from an Azure application gateway.</span></span>

## <span data-ttu-id="0acc4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0acc4-107">EXAMPLES</span></span>

### <span data-ttu-id="0acc4-108">Beispiel 1: Entfernen von Back-End-HTTP-Einstellungen von einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="0acc4-108">Example 1: Remove back-end HTTP settings from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw -Name "BackEndSetting02"
```

<span data-ttu-id="0acc4-109">Der erste Befehl ruft ein Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="0acc4-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="0acc4-110">Der zweite Befehl entfernt die Back-End-HTTP-Einstellung mit dem Namen BackEndSetting02 aus dem Anwendungsgateway, das in $AppGw gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="0acc4-110">The second command removes the back-end HTTP setting named BackEndSetting02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="0acc4-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="0acc4-111">PARAMETERS</span></span>

### <span data-ttu-id="0acc4-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0acc4-112">-ApplicationGateway</span></span>
<span data-ttu-id="0acc4-113">Gibt das Anwendungsgateway an, von dem dieses Cmdlet die Back-End-HTTP-Einstellungen entfernt.</span><span class="sxs-lookup"><span data-stu-id="0acc4-113">Specifies the application gateway from which this cmdlet removes back-end HTTP settings.</span></span>

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

### <span data-ttu-id="0acc4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0acc4-114">-DefaultProfile</span></span>
<span data-ttu-id="0acc4-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0acc4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0acc4-116">-Name</span><span class="sxs-lookup"><span data-stu-id="0acc4-116">-Name</span></span>
<span data-ttu-id="0acc4-117">Gibt den Namen der Back-End-HTTP-Einstellungen an, die von diesem Cmdlet entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="0acc4-117">Specifies the name of the back-end HTTP settings that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0acc4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0acc4-118">CommonParameters</span></span>
<span data-ttu-id="0acc4-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0acc4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0acc4-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0acc4-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0acc4-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0acc4-121">INPUTS</span></span>

### <span data-ttu-id="0acc4-122">System. String</span><span class="sxs-lookup"><span data-stu-id="0acc4-122">System.String</span></span>

## <span data-ttu-id="0acc4-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0acc4-123">OUTPUTS</span></span>

### <span data-ttu-id="0acc4-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0acc4-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0acc4-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="0acc4-125">NOTES</span></span>

## <span data-ttu-id="0acc4-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0acc4-126">RELATED LINKS</span></span>

[<span data-ttu-id="0acc4-127">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0acc4-127">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="0acc4-128">Neu – AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0acc4-128">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="0acc4-129">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0acc4-129">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="0acc4-130">Satz-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0acc4-130">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

