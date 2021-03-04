---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointscopeitemobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject.md
ms.openlocfilehash: 298586f11bba29ce44e78bc3c19d4d9fc6be21f2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921875"
---
# <span data-ttu-id="90b68-101">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject</span><span class="sxs-lookup"><span data-stu-id="90b68-101">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject</span></span>

## <span data-ttu-id="90b68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90b68-102">SYNOPSIS</span></span>
<span data-ttu-id="90b68-103">Erstellt ein Element für den Endpunktbereich des Verbindungsmonitors.</span><span class="sxs-lookup"><span data-stu-id="90b68-103">Creates a connection monitor endpoint scope item.</span></span>

## <span data-ttu-id="90b68-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="90b68-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject [-DefaultProfile <IAzureContextContainer>]
 -Address <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90b68-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="90b68-105">DESCRIPTION</span></span>
<span data-ttu-id="90b68-106">Das New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject-Cmdlet erstellt ein Endpunktbereichselement.</span><span class="sxs-lookup"><span data-stu-id="90b68-106">The New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject cmdlet creates endpoint scope item.</span></span>

## <span data-ttu-id="90b68-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="90b68-107">EXAMPLES</span></span>

### <span data-ttu-id="90b68-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="90b68-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject -Address "10.0.1.0/24"
```


## <span data-ttu-id="90b68-109">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="90b68-109">PARAMETERS</span></span>

### <span data-ttu-id="90b68-110">-Adresse</span><span class="sxs-lookup"><span data-stu-id="90b68-110">-Address</span></span>
<span data-ttu-id="90b68-111">Die Adresse des Bereichselements.</span><span class="sxs-lookup"><span data-stu-id="90b68-111">The address of the scope item.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90b68-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90b68-112">-DefaultProfile</span></span>
<span data-ttu-id="90b68-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="90b68-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90b68-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="90b68-114">-Confirm</span></span>
<span data-ttu-id="90b68-115">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="90b68-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90b68-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90b68-116">-WhatIf</span></span>
<span data-ttu-id="90b68-117">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="90b68-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90b68-118">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="90b68-118">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90b68-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90b68-119">CommonParameters</span></span>
<span data-ttu-id="90b68-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90b68-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90b68-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90b68-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90b68-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="90b68-122">INPUTS</span></span>

### <span data-ttu-id="90b68-123">Keine</span><span class="sxs-lookup"><span data-stu-id="90b68-123">None</span></span>

## <span data-ttu-id="90b68-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="90b68-124">OUTPUTS</span></span>

### <span data-ttu-id="90b68-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem</span><span class="sxs-lookup"><span data-stu-id="90b68-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem</span></span>

## <span data-ttu-id="90b68-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="90b68-126">NOTES</span></span>

## <span data-ttu-id="90b68-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="90b68-127">RELATED LINKS</span></span>
