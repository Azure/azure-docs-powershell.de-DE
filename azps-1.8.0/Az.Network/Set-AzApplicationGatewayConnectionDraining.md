---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: d04dc0c3d9d446941870f30578f50d5ecd795009
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660271"
---
# <span data-ttu-id="2340a-101">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="2340a-101">Set-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="2340a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2340a-102">SYNOPSIS</span></span>
<span data-ttu-id="2340a-103">Ändert die Konfiguration der Verbindungs Entwässerung eines Back-End-HTTP-Einstellungs Objekts.</span><span class="sxs-lookup"><span data-stu-id="2340a-103">Modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="2340a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2340a-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 -Enabled <Boolean> -DrainTimeoutInSec <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2340a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2340a-105">DESCRIPTION</span></span>
<span data-ttu-id="2340a-106">Das Cmdlet " **festlegen-AzApplicationGatewayWebApplicationFirewallConfiguration** " ändert die Konfiguration der Verbindungs Entwässerung eines Back-End-HTTP-Einstellungs Objekts.</span><span class="sxs-lookup"><span data-stu-id="2340a-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="2340a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2340a-107">EXAMPLES</span></span>

### <span data-ttu-id="2340a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2340a-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Set-AzApplicationGatewayConnectionDraining -BackendHttpSettings $poolSetting02 -Enabled $False -DrainTimeoutInSec 3600
```

<span data-ttu-id="2340a-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="2340a-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="2340a-110">Der zweite Befehl ruft die HTTP-Back-End-Einstellungen mit dem Namen Settings01 für $AppGw ab und speichert die Einstellungen in der $Settings-Variablen.</span><span class="sxs-lookup"><span data-stu-id="2340a-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="2340a-111">Mit dem letzten Befehl wird die Konfiguration der Verbindungs Entwässerung für das in $Settings gespeicherte Back-End-HTTP-Einstellungsobjekt geändert, indem die Einstellung Enabled auf false und DrainTimeoutInSec auf 3600 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2340a-111">The last command modifies the connection draining configuration of the back-end HTTP settings object stored in $Settings by setting Enabled to False and DrainTimeoutInSec to 3600.</span></span>

## <span data-ttu-id="2340a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="2340a-112">PARAMETERS</span></span>

### <span data-ttu-id="2340a-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2340a-113">-BackendHttpSettings</span></span>
<span data-ttu-id="2340a-114">Die HTTP-Back-End-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="2340a-114">The backend http settings</span></span>

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

### <span data-ttu-id="2340a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2340a-115">-DefaultProfile</span></span>
<span data-ttu-id="2340a-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2340a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2340a-117">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="2340a-117">-DrainTimeoutInSec</span></span>
<span data-ttu-id="2340a-118">Die Anzahl der Sekunden, die die Verbindungs Entwässerung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2340a-118">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="2340a-119">Zulässige Werte sind von 1 Sekunde bis 3600 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="2340a-119">Acceptable values are from 1 second to 3600 seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2340a-120">-Aktiviert</span><span class="sxs-lookup"><span data-stu-id="2340a-120">-Enabled</span></span>
<span data-ttu-id="2340a-121">Gibt an, ob die Verbindungs Entwässerung aktiviert ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="2340a-121">Whether connection draining is enabled or not.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2340a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2340a-122">CommonParameters</span></span>
<span data-ttu-id="2340a-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2340a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2340a-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2340a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2340a-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2340a-125">INPUTS</span></span>

### <span data-ttu-id="2340a-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2340a-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="2340a-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2340a-127">OUTPUTS</span></span>

### <span data-ttu-id="2340a-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2340a-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="2340a-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="2340a-129">NOTES</span></span>

## <span data-ttu-id="2340a-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2340a-130">RELATED LINKS</span></span>

[<span data-ttu-id="2340a-131">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2340a-131">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="2340a-132">Get-AzApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2340a-132">Get-AzApplicationGatewayBackendHttpSettings</span></span>](./Get-AzApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="2340a-133">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="2340a-133">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="2340a-134">Neu – AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="2340a-134">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="2340a-135">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="2340a-135">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

