---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 147727cffc03de5ba8848705cf79facdbdc43320
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495961"
---
# <span data-ttu-id="05834-101">Get-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="05834-101">Get-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="05834-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="05834-102">SYNOPSIS</span></span>
<span data-ttu-id="05834-103">Ruft die Konfiguration der Verbindungs Entwässerung eines Back-End-HTTP-Einstellungs Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="05834-103">Gets the connection draining configuration of a back-end HTTP settings object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05834-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="05834-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05834-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="05834-105">DESCRIPTION</span></span>
<span data-ttu-id="05834-106">Das Cmdlet " **Get-AzureRmApplicationGatewayConnectionDraining** " Ruft die Verbindungs Entwässerungs Konfiguration eines Back-End-HTTP-Einstellungs Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="05834-106">The **Get-AzureRmApplicationGatewayConnectionDraining** cmdlet gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="05834-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="05834-107">EXAMPLES</span></span>

### <span data-ttu-id="05834-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="05834-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> $ConnectionDraining = Get-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="05834-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="05834-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="05834-110">Der zweite Befehl ruft die HTTP-Back-End-Einstellungen mit dem Namen Settings01 für $AppGw ab und speichert die Einstellungen in der $Settings-Variablen.</span><span class="sxs-lookup"><span data-stu-id="05834-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="05834-111">Der letzte Befehl ruft die Konfiguration der Konfiguration aus den Back-End-HTTP-Einstellungen ab $Settings und speichert Sie in der $ConnectionDraining-Variablen.</span><span class="sxs-lookup"><span data-stu-id="05834-111">The last command gets the connection draining configuration from the back-end HTTP settings $Settings and stores it in the $ConnectionDraining variable.</span></span>

## <span data-ttu-id="05834-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="05834-112">PARAMETERS</span></span>

### <span data-ttu-id="05834-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="05834-113">-BackendHttpSettings</span></span>
<span data-ttu-id="05834-114">Die HTTP-Back-End-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="05834-114">The backend http settings</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05834-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05834-115">-DefaultProfile</span></span>
<span data-ttu-id="05834-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="05834-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05834-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05834-117">CommonParameters</span></span>
<span data-ttu-id="05834-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05834-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05834-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05834-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05834-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="05834-120">INPUTS</span></span>

### <span data-ttu-id="05834-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="05834-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>
<span data-ttu-id="05834-122">Parameter: BackendHttpSettings (ByValue)</span><span class="sxs-lookup"><span data-stu-id="05834-122">Parameters: BackendHttpSettings (ByValue)</span></span>

## <span data-ttu-id="05834-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="05834-123">OUTPUTS</span></span>

### <span data-ttu-id="05834-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="05834-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="05834-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="05834-125">NOTES</span></span>

## <span data-ttu-id="05834-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="05834-126">RELATED LINKS</span></span>

[<span data-ttu-id="05834-127">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="05834-127">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="05834-128">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="05834-128">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./Get-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="05834-129">Neu – AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="05834-129">New-AzureRmApplicationGatewayConnectionDraining</span></span>](./New-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="05834-130">Remove-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="05834-130">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>](./Remove-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="05834-131">Satz-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="05834-131">Set-AzureRmApplicationGatewayConnectionDraining</span></span>](./Set-AzureRmApplicationGatewayConnectionDraining.md)
