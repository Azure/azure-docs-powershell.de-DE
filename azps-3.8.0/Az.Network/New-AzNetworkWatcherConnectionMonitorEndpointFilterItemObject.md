---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointfilteritemobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject.md
ms.openlocfilehash: c06052ee28d849c5d07a941366efd15cbfeefe25
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995732"
---
# <span data-ttu-id="893df-101">New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject</span><span class="sxs-lookup"><span data-stu-id="893df-101">New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject</span></span>

## <span data-ttu-id="893df-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="893df-102">SYNOPSIS</span></span>
<span data-ttu-id="893df-103">Erstellt ein Endpunkt Filterelement für den Verbindungsmonitor.</span><span class="sxs-lookup"><span data-stu-id="893df-103">Creates a connection monitor endpoint filter item.</span></span>

## <span data-ttu-id="893df-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="893df-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject [-Type <String>]
 [-DefaultProfile <IAzureContextContainer>] -Address <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="893df-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="893df-105">DESCRIPTION</span></span>
<span data-ttu-id="893df-106">Das New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject-Cmdlet erstellt Endpunkt Filterelement.</span><span class="sxs-lookup"><span data-stu-id="893df-106">The New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject cmdlet creates endpoint filter item.</span></span>

## <span data-ttu-id="893df-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="893df-107">EXAMPLES</span></span>

### <span data-ttu-id="893df-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="893df-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type "AgentAddress" -Address "10.0.0.1"
```

<span data-ttu-id="893df-109">Geben Sie Folgendes ein: AgentAddress AbschnittFür-Adresse: 10.0.0.1</span><span class="sxs-lookup"><span data-stu-id="893df-109">Type    : AgentAddress Address : 10.0.0.1</span></span>

## <span data-ttu-id="893df-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="893df-110">PARAMETERS</span></span>

### <span data-ttu-id="893df-111">-Adresse</span><span class="sxs-lookup"><span data-stu-id="893df-111">-Address</span></span>
<span data-ttu-id="893df-112">Die Adresse des Filterelements.</span><span class="sxs-lookup"><span data-stu-id="893df-112">The address of the filter item.</span></span>

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

### <span data-ttu-id="893df-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="893df-113">-DefaultProfile</span></span>
<span data-ttu-id="893df-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="893df-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="893df-115">-Typ</span><span class="sxs-lookup"><span data-stu-id="893df-115">-Type</span></span>
<span data-ttu-id="893df-116">Der Typ des Elements, das im Filter enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="893df-116">The type of item included in the filter.</span></span> <span data-ttu-id="893df-117">Derzeit wird nur "AgentAddress AbschnittFür" unterstützt.</span><span class="sxs-lookup"><span data-stu-id="893df-117">Currently only 'AgentAddress' is supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="893df-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="893df-118">-Confirm</span></span>
<span data-ttu-id="893df-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="893df-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="893df-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="893df-120">-WhatIf</span></span>
<span data-ttu-id="893df-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="893df-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="893df-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="893df-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="893df-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="893df-123">CommonParameters</span></span>
<span data-ttu-id="893df-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="893df-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="893df-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="893df-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="893df-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="893df-126">INPUTS</span></span>

### <span data-ttu-id="893df-127">Keine</span><span class="sxs-lookup"><span data-stu-id="893df-127">None</span></span>

## <span data-ttu-id="893df-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="893df-128">OUTPUTS</span></span>

### <span data-ttu-id="893df-129">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorEndpointFilterItem</span><span class="sxs-lookup"><span data-stu-id="893df-129">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorEndpointFilterItem</span></span>

## <span data-ttu-id="893df-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="893df-130">NOTES</span></span>

## <span data-ttu-id="893df-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="893df-131">RELATED LINKS</span></span>
