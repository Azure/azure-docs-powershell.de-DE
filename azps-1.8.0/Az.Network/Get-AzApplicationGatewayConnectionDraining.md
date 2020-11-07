---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: e50917224ef791dbc85c24ceb79cfc7ce05f7d29
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660866"
---
# <span data-ttu-id="0e284-101">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="0e284-101">Get-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="0e284-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0e284-102">SYNOPSIS</span></span>
<span data-ttu-id="0e284-103">Ruft die Konfiguration der Verbindungs Entwässerung eines Back-End-HTTP-Einstellungs Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="0e284-103">Gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="0e284-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e284-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e284-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0e284-105">DESCRIPTION</span></span>
<span data-ttu-id="0e284-106">Das Cmdlet " **Get-AzApplicationGatewayConnectionDraining** " Ruft die Verbindungs Entwässerungs Konfiguration eines Back-End-HTTP-Einstellungs Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="0e284-106">The **Get-AzApplicationGatewayConnectionDraining** cmdlet gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="0e284-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0e284-107">EXAMPLES</span></span>

### <span data-ttu-id="0e284-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0e284-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> $ConnectionDraining = Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="0e284-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="0e284-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="0e284-110">Der zweite Befehl ruft die HTTP-Back-End-Einstellungen mit dem Namen Settings01 für $AppGw ab und speichert die Einstellungen in der $Settings-Variablen.</span><span class="sxs-lookup"><span data-stu-id="0e284-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="0e284-111">Der letzte Befehl ruft die Konfiguration der Konfiguration aus den Back-End-HTTP-Einstellungen ab $Settings und speichert Sie in der $ConnectionDraining-Variablen.</span><span class="sxs-lookup"><span data-stu-id="0e284-111">The last command gets the connection draining configuration from the back-end HTTP settings $Settings and stores it in the $ConnectionDraining variable.</span></span>

## <span data-ttu-id="0e284-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e284-112">PARAMETERS</span></span>

### <span data-ttu-id="0e284-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0e284-113">-BackendHttpSettings</span></span>
<span data-ttu-id="0e284-114">Die HTTP-Back-End-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="0e284-114">The backend http settings</span></span>

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

### <span data-ttu-id="0e284-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e284-115">-DefaultProfile</span></span>
<span data-ttu-id="0e284-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0e284-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e284-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e284-117">CommonParameters</span></span>
<span data-ttu-id="0e284-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e284-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e284-119">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0e284-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e284-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0e284-120">INPUTS</span></span>

### <span data-ttu-id="0e284-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0e284-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="0e284-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0e284-122">OUTPUTS</span></span>

### <span data-ttu-id="0e284-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="0e284-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="0e284-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="0e284-124">NOTES</span></span>

## <span data-ttu-id="0e284-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0e284-125">RELATED LINKS</span></span>

[<span data-ttu-id="0e284-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0e284-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="0e284-127">Get-AzApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0e284-127">Get-AzApplicationGatewayBackendHttpSettings</span></span>](./Get-AzApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="0e284-128">Neu – AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="0e284-128">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="0e284-129">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="0e284-129">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="0e284-130">Satz-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="0e284-130">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)
