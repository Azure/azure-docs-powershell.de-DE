---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 421bc74fb110aa48ff72388462e5496d9ceb1434
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495861"
---
# <span data-ttu-id="0c59c-101">Set-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="0c59c-101">Set-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="0c59c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0c59c-102">SYNOPSIS</span></span>
<span data-ttu-id="0c59c-103">Ändert die Konfiguration der Verbindungs Entwässerung eines Back-End-HTTP-Einstellungs Objekts.</span><span class="sxs-lookup"><span data-stu-id="0c59c-103">Modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c59c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c59c-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 -Enabled <Boolean> -DrainTimeoutInSec <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c59c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0c59c-105">DESCRIPTION</span></span>
<span data-ttu-id="0c59c-106">Das Cmdlet " **festlegen-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** " ändert die Konfiguration der Verbindungs Entwässerung eines Back-End-HTTP-Einstellungs Objekts.</span><span class="sxs-lookup"><span data-stu-id="0c59c-106">The **Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="0c59c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0c59c-107">EXAMPLES</span></span>

### <span data-ttu-id="0c59c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0c59c-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Set-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings $poolSetting02 -Enabled $False -DrainTimeoutInSec 3600
```

<span data-ttu-id="0c59c-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="0c59c-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="0c59c-110">Der zweite Befehl ruft die HTTP-Back-End-Einstellungen mit dem Namen Settings01 für $AppGw ab und speichert die Einstellungen in der $Settings-Variablen.</span><span class="sxs-lookup"><span data-stu-id="0c59c-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="0c59c-111">Mit dem letzten Befehl wird die Konfiguration der Verbindungs Entwässerung für das in $Settings gespeicherte Back-End-HTTP-Einstellungsobjekt geändert, indem die Einstellung Enabled auf false und DrainTimeoutInSec auf 3600 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0c59c-111">The last command modifies the connection draining configuration of the back-end HTTP settings object stored in $Settings by setting Enabled to False and DrainTimeoutInSec to 3600.</span></span>

## <span data-ttu-id="0c59c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c59c-112">PARAMETERS</span></span>

### <span data-ttu-id="0c59c-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0c59c-113">-BackendHttpSettings</span></span>
<span data-ttu-id="0c59c-114">Die HTTP-Back-End-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="0c59c-114">The backend http settings</span></span>

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

### <span data-ttu-id="0c59c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c59c-115">-DefaultProfile</span></span>
<span data-ttu-id="0c59c-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0c59c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c59c-117">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="0c59c-117">-DrainTimeoutInSec</span></span>
<span data-ttu-id="0c59c-118">Die Anzahl der Sekunden, die die Verbindungs Entwässerung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="0c59c-118">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="0c59c-119">Zulässige Werte sind von 1 Sekunde bis 3600 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="0c59c-119">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="0c59c-120">-Aktiviert</span><span class="sxs-lookup"><span data-stu-id="0c59c-120">-Enabled</span></span>
<span data-ttu-id="0c59c-121">Gibt an, ob die Verbindungs Entwässerung aktiviert ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="0c59c-121">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="0c59c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c59c-122">CommonParameters</span></span>
<span data-ttu-id="0c59c-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c59c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c59c-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c59c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c59c-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0c59c-125">INPUTS</span></span>

### <span data-ttu-id="0c59c-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0c59c-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>
<span data-ttu-id="0c59c-127">Parameter: BackendHttpSettings (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0c59c-127">Parameters: BackendHttpSettings (ByValue)</span></span>

## <span data-ttu-id="0c59c-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0c59c-128">OUTPUTS</span></span>

### <span data-ttu-id="0c59c-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0c59c-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="0c59c-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="0c59c-130">NOTES</span></span>

## <span data-ttu-id="0c59c-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0c59c-131">RELATED LINKS</span></span>

[<span data-ttu-id="0c59c-132">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0c59c-132">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="0c59c-133">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0c59c-133">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./Get-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="0c59c-134">Get-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="0c59c-134">Get-AzureRmApplicationGatewayConnectionDraining</span></span>](./Get-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="0c59c-135">Neu – AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="0c59c-135">New-AzureRmApplicationGatewayConnectionDraining</span></span>](./New-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="0c59c-136">Remove-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="0c59c-136">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>](./Remove-AzureRmApplicationGatewayConnectionDraining.md)

