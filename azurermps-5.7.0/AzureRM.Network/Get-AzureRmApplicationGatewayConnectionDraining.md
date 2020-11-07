---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 0c50f8b7fdd4a2093a734f3759bf6a893e56a8bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663230"
---
# <span data-ttu-id="e648a-101">Get-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="e648a-101">Get-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="e648a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e648a-102">SYNOPSIS</span></span>
<span data-ttu-id="e648a-103">Ruft die Konfiguration der Verbindungs Entwässerung eines Back-End-HTTP-Einstellungs Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="e648a-103">Gets the connection draining configuration of a back-end HTTP settings object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e648a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e648a-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e648a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e648a-105">DESCRIPTION</span></span>
<span data-ttu-id="e648a-106">Das Cmdlet " **Get-AzureRmApplicationGatewayConnectionDraining** " Ruft die Verbindungs Entwässerungs Konfiguration eines Back-End-HTTP-Einstellungs Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="e648a-106">The **Get-AzureRmApplicationGatewayConnectionDraining** cmdlet gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="e648a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e648a-107">EXAMPLES</span></span>

### <span data-ttu-id="e648a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e648a-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> $ConnectionDraining = Get-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="e648a-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="e648a-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e648a-110">Der zweite Befehl ruft die HTTP-Back-End-Einstellungen mit dem Namen Settings01 für $AppGw ab und speichert die Einstellungen in der $Settings-Variablen.</span><span class="sxs-lookup"><span data-stu-id="e648a-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="e648a-111">Der letzte Befehl ruft die Konfiguration der Konfiguration aus den Back-End-HTTP-Einstellungen ab $Settings und speichert Sie in der $ConnectionDraining-Variablen.</span><span class="sxs-lookup"><span data-stu-id="e648a-111">The last command gets the connection draining configuration from the back-end HTTP settings $Settings and stores it in the $ConnectionDraining variable.</span></span>

## <span data-ttu-id="e648a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e648a-112">PARAMETERS</span></span>

### <span data-ttu-id="e648a-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e648a-113">-BackendHttpSettings</span></span>
<span data-ttu-id="e648a-114">Die HTTP-Back-End-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="e648a-114">The backend http settings</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e648a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e648a-115">-DefaultProfile</span></span>
<span data-ttu-id="e648a-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e648a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e648a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e648a-117">CommonParameters</span></span>
<span data-ttu-id="e648a-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e648a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e648a-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e648a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e648a-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e648a-120">INPUTS</span></span>

### <span data-ttu-id="e648a-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e648a-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="e648a-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e648a-122">OUTPUTS</span></span>

### <span data-ttu-id="e648a-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="e648a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="e648a-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="e648a-124">NOTES</span></span>

## <span data-ttu-id="e648a-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e648a-125">RELATED LINKS</span></span>

[<span data-ttu-id="e648a-126">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e648a-126">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="e648a-127">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e648a-127">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./Get-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="e648a-128">Neu – AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="e648a-128">New-AzureRmApplicationGatewayConnectionDraining</span></span>](./New-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="e648a-129">Remove-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="e648a-129">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>](./Remove-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="e648a-130">Satz-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="e648a-130">Set-AzureRmApplicationGatewayConnectionDraining</span></span>](./Set-AzureRmApplicationGatewayConnectionDraining.md)
