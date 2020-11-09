---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointscopeitemobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject.md
ms.openlocfilehash: c0ca9e257c0686aa0f4589ef4166fec150f41967
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301461"
---
# <span data-ttu-id="90c47-101">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject</span><span class="sxs-lookup"><span data-stu-id="90c47-101">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject</span></span>

## <span data-ttu-id="90c47-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="90c47-102">SYNOPSIS</span></span>
<span data-ttu-id="90c47-103">Erstellt ein Endpunkt Bereichselement für den Verbindungsmonitor.</span><span class="sxs-lookup"><span data-stu-id="90c47-103">Creates a connection monitor endpoint scope item.</span></span>

## <span data-ttu-id="90c47-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="90c47-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject [-DefaultProfile <IAzureContextContainer>]
 -Address <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90c47-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="90c47-105">DESCRIPTION</span></span>
<span data-ttu-id="90c47-106">Mit dem New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject-Cmdlet wird ein Endpunkt Bereichselement erstellt.</span><span class="sxs-lookup"><span data-stu-id="90c47-106">The New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject cmdlet creates endpoint scope item.</span></span>

## <span data-ttu-id="90c47-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="90c47-107">EXAMPLES</span></span>

### <span data-ttu-id="90c47-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="90c47-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject -Address "10.0.1.0/24"
```


## <span data-ttu-id="90c47-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="90c47-109">PARAMETERS</span></span>

### <span data-ttu-id="90c47-110">-Adresse</span><span class="sxs-lookup"><span data-stu-id="90c47-110">-Address</span></span>
<span data-ttu-id="90c47-111">Die Adresse des Bereichselements.</span><span class="sxs-lookup"><span data-stu-id="90c47-111">The address of the scope item.</span></span>

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

### <span data-ttu-id="90c47-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90c47-112">-DefaultProfile</span></span>
<span data-ttu-id="90c47-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="90c47-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90c47-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="90c47-114">-Confirm</span></span>
<span data-ttu-id="90c47-115">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="90c47-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90c47-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90c47-116">-WhatIf</span></span>
<span data-ttu-id="90c47-117">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="90c47-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90c47-118">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="90c47-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90c47-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90c47-119">CommonParameters</span></span>
<span data-ttu-id="90c47-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90c47-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90c47-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90c47-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90c47-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="90c47-122">INPUTS</span></span>

### <span data-ttu-id="90c47-123">Keine</span><span class="sxs-lookup"><span data-stu-id="90c47-123">None</span></span>

## <span data-ttu-id="90c47-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="90c47-124">OUTPUTS</span></span>

### <span data-ttu-id="90c47-125">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcherConnectionMonitorEndpointScopeItem</span><span class="sxs-lookup"><span data-stu-id="90c47-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem</span></span>

## <span data-ttu-id="90c47-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="90c47-126">NOTES</span></span>

## <span data-ttu-id="90c47-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="90c47-127">RELATED LINKS</span></span>
