---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayConnectionDraining.md
ms.openlocfilehash: b1d38cf748adfc2fb9909fd33e5a4406bf293f13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496401"
---
# <span data-ttu-id="25108-101">New-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="25108-101">New-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="25108-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="25108-102">SYNOPSIS</span></span>
<span data-ttu-id="25108-103">Erstellt eine neue Verbindungs Entwässerungs Konfiguration für HTTP-Back-End-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="25108-103">Creates a new connection draining configuration for back-end HTTP settings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25108-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="25108-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25108-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="25108-105">DESCRIPTION</span></span>
<span data-ttu-id="25108-106">Das Cmdlet **New-AzureRmApplicationGatewayConnectionDraining** erstellt eine neue Verbindungs Entwässerungs Konfiguration für HTTP-Back-End-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="25108-106">The **New-AzureRmApplicationGatewayConnectionDraining** cmdlet creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="25108-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="25108-107">EXAMPLES</span></span>

### <span data-ttu-id="25108-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="25108-108">Example 1</span></span>
```
PS C:\> $connectionDraining = New-AzureRmApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

<span data-ttu-id="25108-109">Der Befehl erstellt eine neue Verbindungs Entwässerungs Konfiguration mit aktiviertem Satz auf true und DrainTimeoutInSec auf 42 Sekunden festgelegt und speichert Sie in $connectionDraining.</span><span class="sxs-lookup"><span data-stu-id="25108-109">The command creates a new connection draining configuration with Enabled set to True and DrainTimeoutInSec set to 42 seconds and stores it in $connectionDraining.</span></span>

## <span data-ttu-id="25108-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="25108-110">PARAMETERS</span></span>

### <span data-ttu-id="25108-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25108-111">-DefaultProfile</span></span>
<span data-ttu-id="25108-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="25108-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25108-113">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="25108-113">-DrainTimeoutInSec</span></span>
<span data-ttu-id="25108-114">Die Anzahl der Sekunden, die die Verbindungs Entwässerung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="25108-114">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="25108-115">Zulässige Werte sind von 1 Sekunde bis 3600 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="25108-115">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="25108-116">-Aktiviert</span><span class="sxs-lookup"><span data-stu-id="25108-116">-Enabled</span></span>
<span data-ttu-id="25108-117">Gibt an, ob die Verbindungs Entwässerung aktiviert ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="25108-117">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="25108-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25108-118">CommonParameters</span></span>
<span data-ttu-id="25108-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25108-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25108-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25108-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25108-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="25108-121">INPUTS</span></span>

### <span data-ttu-id="25108-122">Keine</span><span class="sxs-lookup"><span data-stu-id="25108-122">None</span></span>

## <span data-ttu-id="25108-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="25108-123">OUTPUTS</span></span>

### <span data-ttu-id="25108-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="25108-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="25108-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="25108-125">NOTES</span></span>

## <span data-ttu-id="25108-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="25108-126">RELATED LINKS</span></span>

[<span data-ttu-id="25108-127">Get-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="25108-127">Get-AzureRmApplicationGatewayConnectionDraining</span></span>](./Get-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="25108-128">Remove-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="25108-128">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>](./Remove-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="25108-129">Satz-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="25108-129">Set-AzureRmApplicationGatewayConnectionDraining</span></span>](./Set-AzureRmApplicationGatewayConnectionDraining.md)

