---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointscopeitemobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject.md
ms.openlocfilehash: c0ca9e257c0686aa0f4589ef4166fec150f41967
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467336"
---
# <span data-ttu-id="1dbbb-101">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject</span><span class="sxs-lookup"><span data-stu-id="1dbbb-101">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject</span></span>

## <span data-ttu-id="1dbbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dbbb-102">SYNOPSIS</span></span>
<span data-ttu-id="1dbbb-103">Erstellt ein Endpunktelement für den Verbindungsmonitor.</span><span class="sxs-lookup"><span data-stu-id="1dbbb-103">Creates a connection monitor endpoint scope item.</span></span>

## <span data-ttu-id="1dbbb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1dbbb-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject [-DefaultProfile <IAzureContextContainer>]
 -Address <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dbbb-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1dbbb-105">DESCRIPTION</span></span>
<span data-ttu-id="1dbbb-106">Das New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject erstellt ein Endpunktbereichselement.</span><span class="sxs-lookup"><span data-stu-id="1dbbb-106">The New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject cmdlet creates endpoint scope item.</span></span>

## <span data-ttu-id="1dbbb-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1dbbb-107">EXAMPLES</span></span>

### <span data-ttu-id="1dbbb-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1dbbb-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject -Address "10.0.1.0/24"
```


## <span data-ttu-id="1dbbb-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1dbbb-109">PARAMETERS</span></span>

### <span data-ttu-id="1dbbb-110">-Address</span><span class="sxs-lookup"><span data-stu-id="1dbbb-110">-Address</span></span>
<span data-ttu-id="1dbbb-111">Die Adresse des Bereichselements.</span><span class="sxs-lookup"><span data-stu-id="1dbbb-111">The address of the scope item.</span></span>

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

### <span data-ttu-id="1dbbb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dbbb-112">-DefaultProfile</span></span>
<span data-ttu-id="1dbbb-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1dbbb-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dbbb-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1dbbb-114">-Confirm</span></span>
<span data-ttu-id="1dbbb-115">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1dbbb-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dbbb-116">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1dbbb-116">-WhatIf</span></span>
<span data-ttu-id="1dbbb-117">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1dbbb-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dbbb-118">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1dbbb-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dbbb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dbbb-119">CommonParameters</span></span>
<span data-ttu-id="1dbbb-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dbbb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dbbb-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1dbbb-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dbbb-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1dbbb-122">INPUTS</span></span>

### <span data-ttu-id="1dbbb-123">Keine</span><span class="sxs-lookup"><span data-stu-id="1dbbb-123">None</span></span>

## <span data-ttu-id="1dbbb-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1dbbb-124">OUTPUTS</span></span>

### <span data-ttu-id="1dbbb-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem</span><span class="sxs-lookup"><span data-stu-id="1dbbb-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem</span></span>

## <span data-ttu-id="1dbbb-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1dbbb-126">NOTES</span></span>

## <span data-ttu-id="1dbbb-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1dbbb-127">RELATED LINKS</span></span>
