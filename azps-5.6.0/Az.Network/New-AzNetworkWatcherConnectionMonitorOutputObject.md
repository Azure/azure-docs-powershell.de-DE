---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkwatcherconnectionmonitoroutputobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
ms.openlocfilehash: 895659481999ab5801538bec3b88765e1d48aeca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921864"
---
# <span data-ttu-id="e59cd-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="e59cd-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="e59cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e59cd-102">SYNOPSIS</span></span>
<span data-ttu-id="e59cd-103">Erstellen sie das Ausgabezielobjekt des Verbindungsmonitors.</span><span class="sxs-lookup"><span data-stu-id="e59cd-103">Create connection monitor output destination object.</span></span>

## <span data-ttu-id="e59cd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e59cd-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorOutputObject [-OutputType <String>] -WorkspaceResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e59cd-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e59cd-105">DESCRIPTION</span></span>
<span data-ttu-id="e59cd-106">Das New-AzNetworkWatcherConnectionMonitorOutputObject-Cmdlet erstellt das Ausgabezielobjekt des Verbindungsmonitors.</span><span class="sxs-lookup"><span data-stu-id="e59cd-106">The New-AzNetworkWatcherConnectionMonitorOutputObject cmdlet creates connection monitor output destination object.</span></span>

## <span data-ttu-id="e59cd-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e59cd-107">EXAMPLES</span></span>

### <span data-ttu-id="e59cd-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e59cd-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorOutputObject -OutputType "workspace" -WorkspaceResourceId MyWSResourceId
```

<span data-ttu-id="e59cd-109">Geben Sie ein: "Workspace" WorkspaceSettings : { "WorkspaceResourceId": "MyWSResourceId" }</span><span class="sxs-lookup"><span data-stu-id="e59cd-109">Type              : "workspace" WorkspaceSettings : { "WorkspaceResourceId": "MyWSResourceId" }</span></span>

## <span data-ttu-id="e59cd-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e59cd-110">PARAMETERS</span></span>

### <span data-ttu-id="e59cd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e59cd-111">-DefaultProfile</span></span>
<span data-ttu-id="e59cd-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e59cd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e59cd-113">-OutputType</span><span class="sxs-lookup"><span data-stu-id="e59cd-113">-OutputType</span></span>
<span data-ttu-id="e59cd-114">Ausgabezieltyp des Verbindungsmonitors.</span><span class="sxs-lookup"><span data-stu-id="e59cd-114">Connection monitor output destination type.</span></span> <span data-ttu-id="e59cd-115">Derzeit wird nur \" Arbeitsbereich \" unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e59cd-115">Currently, only \"Workspace\" is supported.</span></span>

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

### <span data-ttu-id="e59cd-116">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="e59cd-116">-WorkspaceResourceId</span></span>
<span data-ttu-id="e59cd-117">Ressourcen-ID des Arbeitsbereichs für die Protokollanalyse.</span><span class="sxs-lookup"><span data-stu-id="e59cd-117">Log analytics workspace resource ID.</span></span>

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

### <span data-ttu-id="e59cd-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e59cd-118">-Confirm</span></span>
<span data-ttu-id="e59cd-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e59cd-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e59cd-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e59cd-120">-WhatIf</span></span>
<span data-ttu-id="e59cd-121">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e59cd-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e59cd-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e59cd-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e59cd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e59cd-123">CommonParameters</span></span>
<span data-ttu-id="e59cd-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e59cd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e59cd-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e59cd-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e59cd-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e59cd-126">INPUTS</span></span>

### <span data-ttu-id="e59cd-127">Keine</span><span class="sxs-lookup"><span data-stu-id="e59cd-127">None</span></span>

## <span data-ttu-id="e59cd-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e59cd-128">OUTPUTS</span></span>

### <span data-ttu-id="e59cd-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="e59cd-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="e59cd-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e59cd-130">NOTES</span></span>

## <span data-ttu-id="e59cd-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e59cd-131">RELATED LINKS</span></span>
