---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitoroutputobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
ms.openlocfilehash: ec1bba32027d3ec96aef61f3abec7d51cec5c35b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372208"
---
# <span data-ttu-id="04227-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="04227-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="04227-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04227-102">SYNOPSIS</span></span>
<span data-ttu-id="04227-103">Erstellen Sie das Ausgabezielobjekt des Verbindungsmonitors.</span><span class="sxs-lookup"><span data-stu-id="04227-103">Create connection monitor output destination object.</span></span>

## <span data-ttu-id="04227-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="04227-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorOutputObject [-OutputType <String>] -WorkspaceResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04227-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="04227-105">DESCRIPTION</span></span>
<span data-ttu-id="04227-106">Das New-AzNetworkWatcherConnectionMonitorOutputObject erstellt ein Ausgabezielobjekt für den Verbindungsmonitor.</span><span class="sxs-lookup"><span data-stu-id="04227-106">The New-AzNetworkWatcherConnectionMonitorOutputObject cmdlet creates connection monitor output destination object.</span></span>

## <span data-ttu-id="04227-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="04227-107">EXAMPLES</span></span>

### <span data-ttu-id="04227-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="04227-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorOutputObject -OutputType "workspace" -WorkspaceResourceId MyWSResourceId
```

<span data-ttu-id="04227-109">Typ: "workspace" WorkspaceSettings : { "WorkspaceResourceId": "MyWSResourceId" }</span><span class="sxs-lookup"><span data-stu-id="04227-109">Type              : "workspace" WorkspaceSettings : { "WorkspaceResourceId": "MyWSResourceId" }</span></span>

## <span data-ttu-id="04227-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04227-110">PARAMETERS</span></span>

### <span data-ttu-id="04227-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04227-111">-DefaultProfile</span></span>
<span data-ttu-id="04227-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="04227-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04227-113">-OutputType</span><span class="sxs-lookup"><span data-stu-id="04227-113">-OutputType</span></span>
<span data-ttu-id="04227-114">Ausgabezieltyp des Verbindungsmonitors.</span><span class="sxs-lookup"><span data-stu-id="04227-114">Connection monitor output destination type.</span></span> <span data-ttu-id="04227-115">Derzeit wird nur \" Arbeitsbereich \" unterstützt.</span><span class="sxs-lookup"><span data-stu-id="04227-115">Currently, only \"Workspace\" is supported.</span></span>

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

### <span data-ttu-id="04227-116">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="04227-116">-WorkspaceResourceId</span></span>
<span data-ttu-id="04227-117">Ressourcen-ID des Analysearbeitsbereichs protokollieren.</span><span class="sxs-lookup"><span data-stu-id="04227-117">Log analytics workspace resource ID.</span></span>

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

### <span data-ttu-id="04227-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="04227-118">-Confirm</span></span>
<span data-ttu-id="04227-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="04227-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04227-120">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="04227-120">-WhatIf</span></span>
<span data-ttu-id="04227-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="04227-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04227-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="04227-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04227-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04227-123">CommonParameters</span></span>
<span data-ttu-id="04227-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04227-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04227-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="04227-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04227-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="04227-126">INPUTS</span></span>

### <span data-ttu-id="04227-127">Keine</span><span class="sxs-lookup"><span data-stu-id="04227-127">None</span></span>

## <span data-ttu-id="04227-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="04227-128">OUTPUTS</span></span>

### <span data-ttu-id="04227-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="04227-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="04227-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="04227-130">NOTES</span></span>

## <span data-ttu-id="04227-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="04227-131">RELATED LINKS</span></span>
