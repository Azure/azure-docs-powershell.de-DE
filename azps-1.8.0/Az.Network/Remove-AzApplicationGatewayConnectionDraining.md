---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 5357b8a0a59fade3e9ff7439da9ac1eeb63f6035
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660429"
---
# <span data-ttu-id="4c5d9-101">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="4c5d9-101">Remove-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="4c5d9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4c5d9-102">SYNOPSIS</span></span>
<span data-ttu-id="4c5d9-103">Entfernt die Konfiguration der Verbindungs Entwässerung eines Back-End-HTTP-Einstellungs Objekts.</span><span class="sxs-lookup"><span data-stu-id="4c5d9-103">Removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="4c5d9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c5d9-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c5d9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4c5d9-105">DESCRIPTION</span></span>
<span data-ttu-id="4c5d9-106">Das Cmdlet **Remove-AzApplicationGatewayConnectionDraining** entfernt die Konfiguration der Verbindungs Entwässerung eines Back-End-HTTP-Einstellungs Objekts.</span><span class="sxs-lookup"><span data-stu-id="4c5d9-106">The **Remove-AzApplicationGatewayConnectionDraining** cmdlet removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="4c5d9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4c5d9-107">EXAMPLES</span></span>

### <span data-ttu-id="4c5d9-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4c5d9-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="4c5d9-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="4c5d9-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4c5d9-110">Der zweite Befehl ruft die HTTP-Back-End-Einstellungen mit dem Namen Settings01 für $AppGw ab und speichert die Einstellungen in der $Settings-Variablen.</span><span class="sxs-lookup"><span data-stu-id="4c5d9-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="4c5d9-111">Der letzte Befehl entfernt die Verbindungs Entwässerungs Konfiguration der in $Settings gespeicherten Back-End-HTTP-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="4c5d9-111">The last command removes the connection draining configuration of the back-end HTTP settings stored in $Settings.</span></span>

## <span data-ttu-id="4c5d9-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="4c5d9-112">PARAMETERS</span></span>

### <span data-ttu-id="4c5d9-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4c5d9-113">-BackendHttpSettings</span></span>
<span data-ttu-id="4c5d9-114">Die HTTP-Back-End-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="4c5d9-114">The backend http settings</span></span>

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

### <span data-ttu-id="4c5d9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c5d9-115">-DefaultProfile</span></span>
<span data-ttu-id="4c5d9-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4c5d9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c5d9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c5d9-117">CommonParameters</span></span>
<span data-ttu-id="4c5d9-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c5d9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c5d9-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c5d9-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c5d9-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4c5d9-120">INPUTS</span></span>

### <span data-ttu-id="4c5d9-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4c5d9-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="4c5d9-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4c5d9-122">OUTPUTS</span></span>

### <span data-ttu-id="4c5d9-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4c5d9-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="4c5d9-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="4c5d9-124">NOTES</span></span>

## <span data-ttu-id="4c5d9-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4c5d9-125">RELATED LINKS</span></span>

[<span data-ttu-id="4c5d9-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4c5d9-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="4c5d9-127">Get-AzApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4c5d9-127">Get-AzApplicationGatewayBackendHttpSettings</span></span>](./Get-AzApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="4c5d9-128">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="4c5d9-128">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="4c5d9-129">Neu – AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="4c5d9-129">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="4c5d9-130">Satz-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="4c5d9-130">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

