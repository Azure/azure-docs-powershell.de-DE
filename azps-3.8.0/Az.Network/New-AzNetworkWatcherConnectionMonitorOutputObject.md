---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitoroutputobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
ms.openlocfilehash: 9f5c09e87e8d02276352cd10c2a7aba937822af2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995722"
---
# <span data-ttu-id="0198e-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="0198e-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="0198e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0198e-102">SYNOPSIS</span></span>
<span data-ttu-id="0198e-103">Zielobjekt für Ausgabe des Verbindungs Monitors erstellen</span><span class="sxs-lookup"><span data-stu-id="0198e-103">Create connection monitor output destination object.</span></span>

## <span data-ttu-id="0198e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0198e-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorOutputObject [-OutputType <String>] -WorkspaceResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0198e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0198e-105">DESCRIPTION</span></span>
<span data-ttu-id="0198e-106">Das New-AzNetworkWatcherConnectionMonitorOutputObject-Cmdlet erstellt das Ausgabeziel Objekt des Verbindungs Monitors.</span><span class="sxs-lookup"><span data-stu-id="0198e-106">The New-AzNetworkWatcherConnectionMonitorOutputObject cmdlet creates connection monitor output destination object.</span></span>

## <span data-ttu-id="0198e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0198e-107">EXAMPLES</span></span>

### <span data-ttu-id="0198e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0198e-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorOutputObject -OutputType "workspace" -ResourcWorkspaceResourceId MyWSResourceId
```

<span data-ttu-id="0198e-109">Geben Sie Folgendes ein: "Arbeitsbereich" WorkspaceSettings: {"WorkspaceResourceId": "MyWSResourceId"}</span><span class="sxs-lookup"><span data-stu-id="0198e-109">Type              : "workspace" WorkspaceSettings : { "WorkspaceResourceId": "MyWSResourceId" }</span></span>

## <span data-ttu-id="0198e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0198e-110">PARAMETERS</span></span>

### <span data-ttu-id="0198e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0198e-111">-DefaultProfile</span></span>
<span data-ttu-id="0198e-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0198e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0198e-113">-OutputType</span><span class="sxs-lookup"><span data-stu-id="0198e-113">-OutputType</span></span>
<span data-ttu-id="0198e-114">Zieltyp für die Ausgabe des Verbindungs Monitors</span><span class="sxs-lookup"><span data-stu-id="0198e-114">Connection monitor output destination type.</span></span> <span data-ttu-id="0198e-115">Derzeit wird nur \" Arbeitsbereich \" unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0198e-115">Currently, only \"Workspace\" is supported.</span></span>

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

### <span data-ttu-id="0198e-116">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="0198e-116">-WorkspaceResourceId</span></span>
<span data-ttu-id="0198e-117">Ressourcen-ID des Protokollanalyse Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="0198e-117">Log analytics workspace resource ID.</span></span>

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

### <span data-ttu-id="0198e-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0198e-118">-Confirm</span></span>
<span data-ttu-id="0198e-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0198e-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0198e-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0198e-120">-WhatIf</span></span>
<span data-ttu-id="0198e-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0198e-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0198e-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0198e-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0198e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0198e-123">CommonParameters</span></span>
<span data-ttu-id="0198e-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0198e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0198e-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0198e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0198e-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0198e-126">INPUTS</span></span>

### <span data-ttu-id="0198e-127">Keine</span><span class="sxs-lookup"><span data-stu-id="0198e-127">None</span></span>

## <span data-ttu-id="0198e-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0198e-128">OUTPUTS</span></span>

### <span data-ttu-id="0198e-129">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="0198e-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="0198e-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="0198e-130">NOTES</span></span>

## <span data-ttu-id="0198e-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0198e-131">RELATED LINKS</span></span>
