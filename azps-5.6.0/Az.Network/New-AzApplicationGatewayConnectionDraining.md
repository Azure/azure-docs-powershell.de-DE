---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: b5bfedea118aa3770bac3141d05db379a4655906
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945917"
---
# <span data-ttu-id="9ac64-101">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="9ac64-101">New-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="9ac64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ac64-102">SYNOPSIS</span></span>
<span data-ttu-id="9ac64-103">Erstellt eine neue Verbindungsablaufkonfiguration für Back-End-HTTP-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="9ac64-103">Creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="9ac64-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9ac64-104">SYNTAX</span></span>

```
New-AzApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ac64-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9ac64-105">DESCRIPTION</span></span>
<span data-ttu-id="9ac64-106">Das **Cmdlet New-AzApplicationGatewayConnectionDraining** erstellt eine neue Verbindungsablaufkonfiguration für Back-End-HTTP-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="9ac64-106">The **New-AzApplicationGatewayConnectionDraining** cmdlet creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="9ac64-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9ac64-107">EXAMPLES</span></span>

### <span data-ttu-id="9ac64-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9ac64-108">Example 1</span></span>
```
PS C:\> $connectionDraining = New-AzApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

<span data-ttu-id="9ac64-109">Mit dem Befehl wird eine neue Konfiguration für die Verbindungsentwässerung erstellt, deren Einstellung Auf True und DrainTimeoutInSec auf 42 Sekunden festgelegt ist, und speichert sie in $connectionDraining.</span><span class="sxs-lookup"><span data-stu-id="9ac64-109">The command creates a new connection draining configuration with Enabled set to True and DrainTimeoutInSec set to 42 seconds and stores it in $connectionDraining.</span></span>

## <span data-ttu-id="9ac64-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9ac64-110">PARAMETERS</span></span>

### <span data-ttu-id="9ac64-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ac64-111">-DefaultProfile</span></span>
<span data-ttu-id="9ac64-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9ac64-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ac64-113">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="9ac64-113">-DrainTimeoutInSec</span></span>
<span data-ttu-id="9ac64-114">Die Anzahl der Sekunden, in der die Verbindung entleert wird, ist aktiv.</span><span class="sxs-lookup"><span data-stu-id="9ac64-114">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="9ac64-115">Zulässige Werte liegen zwischen 1 Sekunde und 3600 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="9ac64-115">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="9ac64-116">-Enabled</span><span class="sxs-lookup"><span data-stu-id="9ac64-116">-Enabled</span></span>
<span data-ttu-id="9ac64-117">Ob die Verbindungsentwässerung aktiviert ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="9ac64-117">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="9ac64-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ac64-118">CommonParameters</span></span>
<span data-ttu-id="9ac64-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ac64-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ac64-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ac64-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ac64-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9ac64-121">INPUTS</span></span>

### <span data-ttu-id="9ac64-122">Keine</span><span class="sxs-lookup"><span data-stu-id="9ac64-122">None</span></span>

## <span data-ttu-id="9ac64-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9ac64-123">OUTPUTS</span></span>

### <span data-ttu-id="9ac64-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="9ac64-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="9ac64-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9ac64-125">NOTES</span></span>

## <span data-ttu-id="9ac64-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9ac64-126">RELATED LINKS</span></span>

[<span data-ttu-id="9ac64-127">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="9ac64-127">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="9ac64-128">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="9ac64-128">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="9ac64-129">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="9ac64-129">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

