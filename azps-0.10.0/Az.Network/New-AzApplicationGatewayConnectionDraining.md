---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 813569705831dcd3d8c379b3c40078184498899e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841439"
---
# <span data-ttu-id="b3baa-101">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="b3baa-101">New-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="b3baa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b3baa-102">SYNOPSIS</span></span>
<span data-ttu-id="b3baa-103">Erstellt eine neue Verbindungs Entwässerungs Konfiguration für HTTP-Back-End-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="b3baa-103">Creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="b3baa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3baa-104">SYNTAX</span></span>

```
New-AzApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3baa-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b3baa-105">DESCRIPTION</span></span>
<span data-ttu-id="b3baa-106">Das Cmdlet **New-AzApplicationGatewayConnectionDraining** erstellt eine neue Verbindungs Entwässerungs Konfiguration für HTTP-Back-End-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="b3baa-106">The **New-AzApplicationGatewayConnectionDraining** cmdlet creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="b3baa-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b3baa-107">EXAMPLES</span></span>

### <span data-ttu-id="b3baa-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b3baa-108">Example 1</span></span>
```
PS C:\> $connectionDraining = New-AzApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

<span data-ttu-id="b3baa-109">Der Befehl erstellt eine neue Verbindungs Entwässerungs Konfiguration mit aktiviertem Satz auf true und DrainTimeoutInSec auf 42 Sekunden festgelegt und speichert Sie in $connectionDraining.</span><span class="sxs-lookup"><span data-stu-id="b3baa-109">The command creates a new connection draining configuration with Enabled set to True and DrainTimeoutInSec set to 42 seconds and stores it in $connectionDraining.</span></span>

## <span data-ttu-id="b3baa-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3baa-110">PARAMETERS</span></span>

### <span data-ttu-id="b3baa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3baa-111">-DefaultProfile</span></span>
<span data-ttu-id="b3baa-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b3baa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3baa-113">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="b3baa-113">-DrainTimeoutInSec</span></span>
<span data-ttu-id="b3baa-114">Die Anzahl der Sekunden, die die Verbindungs Entwässerung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b3baa-114">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="b3baa-115">Zulässige Werte sind von 1 Sekunde bis 3600 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="b3baa-115">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="b3baa-116">-Aktiviert</span><span class="sxs-lookup"><span data-stu-id="b3baa-116">-Enabled</span></span>
<span data-ttu-id="b3baa-117">Gibt an, ob die Verbindungs Entwässerung aktiviert ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="b3baa-117">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="b3baa-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3baa-118">CommonParameters</span></span>
<span data-ttu-id="b3baa-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3baa-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3baa-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3baa-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3baa-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b3baa-121">INPUTS</span></span>

### <span data-ttu-id="b3baa-122">Keine</span><span class="sxs-lookup"><span data-stu-id="b3baa-122">None</span></span>

## <span data-ttu-id="b3baa-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b3baa-123">OUTPUTS</span></span>

### <span data-ttu-id="b3baa-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="b3baa-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="b3baa-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="b3baa-125">NOTES</span></span>

## <span data-ttu-id="b3baa-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b3baa-126">RELATED LINKS</span></span>

[<span data-ttu-id="b3baa-127">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="b3baa-127">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="b3baa-128">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="b3baa-128">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="b3baa-129">Satz-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="b3baa-129">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

