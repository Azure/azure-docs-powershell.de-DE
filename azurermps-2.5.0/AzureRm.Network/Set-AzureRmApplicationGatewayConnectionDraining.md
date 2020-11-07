---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayconnectiondraining
schema: 2.0.0
ms.openlocfilehash: ab876b5bc0ea63a2299ec17168b56125c9dbcdba
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849095"
---
# <span data-ttu-id="10840-101">Set-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="10840-101">Set-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="10840-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="10840-102">SYNOPSIS</span></span>
<span data-ttu-id="10840-103">Ändert die Konfiguration der Verbindungs Entwässerung eines Back-End-HTTP-Einstellungs Objekts.</span><span class="sxs-lookup"><span data-stu-id="10840-103">Modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10840-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="10840-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 -Enabled <Boolean> -DrainTimeoutInSec <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10840-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10840-105">DESCRIPTION</span></span>
<span data-ttu-id="10840-106">Das Cmdlet " **festlegen-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** " ändert die Konfiguration der Verbindungs Entwässerung eines Back-End-HTTP-Einstellungs Objekts.</span><span class="sxs-lookup"><span data-stu-id="10840-106">The **Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="10840-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="10840-107">EXAMPLES</span></span>

### <span data-ttu-id="10840-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="10840-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Set-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings $poolSetting02 -Enabled $False -DrainTimeoutInSec 3600
```

<span data-ttu-id="10840-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 in der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="10840-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="10840-110">Der zweite Befehl ruft die HTTP-Back-End-Einstellungen mit dem Namen Settings01 für $AppGw ab und speichert die Einstellungen in der $Settings-Variablen.</span><span class="sxs-lookup"><span data-stu-id="10840-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="10840-111">Mit dem letzten Befehl wird die Konfiguration der Verbindungs Entwässerung für das in $Settings gespeicherte Back-End-HTTP-Einstellungsobjekt geändert, indem die Einstellung Enabled auf false und DrainTimeoutInSec auf 3600 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="10840-111">The last command modifies the connection draining configuration of the back-end HTTP settings object stored in $Settings by setting Enabled to False and DrainTimeoutInSec to 3600.</span></span>

## <span data-ttu-id="10840-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="10840-112">PARAMETERS</span></span>

### <span data-ttu-id="10840-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="10840-113">-BackendHttpSettings</span></span>
<span data-ttu-id="10840-114">Die HTTP-Back-End-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="10840-114">The backend http settings</span></span>

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

### <span data-ttu-id="10840-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10840-115">-DefaultProfile</span></span>
<span data-ttu-id="10840-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="10840-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10840-117">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="10840-117">-DrainTimeoutInSec</span></span>
<span data-ttu-id="10840-118">Die Anzahl der Sekunden, die die Verbindungs Entwässerung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="10840-118">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="10840-119">Zulässige Werte sind von 1 Sekunde bis 3600 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="10840-119">Acceptable values are from 1 second to 3600 seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10840-120">-Aktiviert</span><span class="sxs-lookup"><span data-stu-id="10840-120">-Enabled</span></span>
<span data-ttu-id="10840-121">Gibt an, ob die Verbindungs Entwässerung aktiviert ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="10840-121">Whether connection draining is enabled or not.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10840-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10840-122">CommonParameters</span></span>
<span data-ttu-id="10840-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10840-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10840-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10840-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10840-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="10840-125">INPUTS</span></span>

### <span data-ttu-id="10840-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="10840-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="10840-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="10840-127">OUTPUTS</span></span>

### <span data-ttu-id="10840-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="10840-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="10840-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="10840-129">NOTES</span></span>

## <span data-ttu-id="10840-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="10840-130">RELATED LINKS</span></span>

[<span data-ttu-id="10840-131">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="10840-131">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="10840-132">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="10840-132">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./Get-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="10840-133">Get-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="10840-133">Get-AzureRmApplicationGatewayConnectionDraining</span></span>](./Get-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="10840-134">Neu – AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="10840-134">New-AzureRmApplicationGatewayConnectionDraining</span></span>](./New-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="10840-135">Remove-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="10840-135">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>](./Remove-AzureRmApplicationGatewayConnectionDraining.md)

