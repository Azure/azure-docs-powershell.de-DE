---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 679a1311526f7fa5028c83e6571001d14b2ff3f5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468128"
---
# <span data-ttu-id="a0cec-101">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="a0cec-101">New-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="a0cec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0cec-102">SYNOPSIS</span></span>
<span data-ttu-id="a0cec-103">Erstellt eine neue Konfiguration zur Entleerung der Verbindung für back-end-HTTP-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="a0cec-103">Creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="a0cec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a0cec-104">SYNTAX</span></span>

```
New-AzApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0cec-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0cec-105">DESCRIPTION</span></span>
<span data-ttu-id="a0cec-106">Das **Cmdlet "New-AzApplicationGatewayConnectionDraining"** erstellt eine neue Konfiguration zur Entleerung der Verbindung für Back-End-HTTP-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="a0cec-106">The **New-AzApplicationGatewayConnectionDraining** cmdlet creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="a0cec-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a0cec-107">EXAMPLES</span></span>

### <span data-ttu-id="a0cec-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a0cec-108">Example 1</span></span>
```
PS C:\> $connectionDraining = New-AzApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

<span data-ttu-id="a0cec-109">Der Befehl erstellt eine neue Konfiguration zur Entleerung der Verbindung, bei der "Enabled" auf "True" und "DrainTimeoutInSec" auf 42 Sekunden festgelegt ist, und speichert sie in $connectionDraining.</span><span class="sxs-lookup"><span data-stu-id="a0cec-109">The command creates a new connection draining configuration with Enabled set to True and DrainTimeoutInSec set to 42 seconds and stores it in $connectionDraining.</span></span>

## <span data-ttu-id="a0cec-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0cec-110">PARAMETERS</span></span>

### <span data-ttu-id="a0cec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0cec-111">-DefaultProfile</span></span>
<span data-ttu-id="a0cec-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a0cec-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0cec-113">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="a0cec-113">-DrainTimeoutInSec</span></span>
<span data-ttu-id="a0cec-114">Die Anzahl der Sekunden, für die die Verbindungsentleerung aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="a0cec-114">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="a0cec-115">Zulässige Werte liegen zwischen einer Sekunde und 3600 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="a0cec-115">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="a0cec-116">-Enabled</span><span class="sxs-lookup"><span data-stu-id="a0cec-116">-Enabled</span></span>
<span data-ttu-id="a0cec-117">Ob die Verbindungsentleerung aktiviert ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="a0cec-117">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="a0cec-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0cec-118">CommonParameters</span></span>
<span data-ttu-id="a0cec-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0cec-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0cec-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0cec-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0cec-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a0cec-121">INPUTS</span></span>

### <span data-ttu-id="a0cec-122">Keine</span><span class="sxs-lookup"><span data-stu-id="a0cec-122">None</span></span>

## <span data-ttu-id="a0cec-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a0cec-123">OUTPUTS</span></span>

### <span data-ttu-id="a0cec-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="a0cec-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="a0cec-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a0cec-125">NOTES</span></span>

## <span data-ttu-id="a0cec-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a0cec-126">RELATED LINKS</span></span>

[<span data-ttu-id="a0cec-127">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="a0cec-127">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="a0cec-128">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="a0cec-128">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="a0cec-129">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="a0cec-129">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

