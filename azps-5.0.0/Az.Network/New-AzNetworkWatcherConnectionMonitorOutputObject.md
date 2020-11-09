---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitoroutputobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
ms.openlocfilehash: 9f5c09e87e8d02276352cd10c2a7aba937822af2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302713"
---
# <span data-ttu-id="86ad0-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="86ad0-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="86ad0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="86ad0-102">SYNOPSIS</span></span>
<span data-ttu-id="86ad0-103">Zielobjekt für Ausgabe des Verbindungs Monitors erstellen</span><span class="sxs-lookup"><span data-stu-id="86ad0-103">Create connection monitor output destination object.</span></span>

## <span data-ttu-id="86ad0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="86ad0-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorOutputObject [-OutputType <String>] -WorkspaceResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86ad0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="86ad0-105">DESCRIPTION</span></span>
<span data-ttu-id="86ad0-106">Das New-AzNetworkWatcherConnectionMonitorOutputObject-Cmdlet erstellt das Ausgabeziel Objekt des Verbindungs Monitors.</span><span class="sxs-lookup"><span data-stu-id="86ad0-106">The New-AzNetworkWatcherConnectionMonitorOutputObject cmdlet creates connection monitor output destination object.</span></span>

## <span data-ttu-id="86ad0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="86ad0-107">EXAMPLES</span></span>

### <span data-ttu-id="86ad0-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="86ad0-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorOutputObject -OutputType "workspace" -ResourcWorkspaceResourceId MyWSResourceId
```

<span data-ttu-id="86ad0-109">Geben Sie Folgendes ein: "Arbeitsbereich" WorkspaceSettings: {"WorkspaceResourceId": "MyWSResourceId"}</span><span class="sxs-lookup"><span data-stu-id="86ad0-109">Type              : "workspace" WorkspaceSettings : { "WorkspaceResourceId": "MyWSResourceId" }</span></span>

## <span data-ttu-id="86ad0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="86ad0-110">PARAMETERS</span></span>

### <span data-ttu-id="86ad0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86ad0-111">-DefaultProfile</span></span>
<span data-ttu-id="86ad0-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="86ad0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86ad0-113">-OutputType</span><span class="sxs-lookup"><span data-stu-id="86ad0-113">-OutputType</span></span>
<span data-ttu-id="86ad0-114">Zieltyp für die Ausgabe des Verbindungs Monitors</span><span class="sxs-lookup"><span data-stu-id="86ad0-114">Connection monitor output destination type.</span></span> <span data-ttu-id="86ad0-115">Derzeit wird nur \" Arbeitsbereich \" unterstützt.</span><span class="sxs-lookup"><span data-stu-id="86ad0-115">Currently, only \"Workspace\" is supported.</span></span>

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

### <span data-ttu-id="86ad0-116">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="86ad0-116">-WorkspaceResourceId</span></span>
<span data-ttu-id="86ad0-117">Ressourcen-ID des Protokollanalyse Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="86ad0-117">Log analytics workspace resource ID.</span></span>

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

### <span data-ttu-id="86ad0-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="86ad0-118">-Confirm</span></span>
<span data-ttu-id="86ad0-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="86ad0-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86ad0-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86ad0-120">-WhatIf</span></span>
<span data-ttu-id="86ad0-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="86ad0-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86ad0-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="86ad0-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86ad0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86ad0-123">CommonParameters</span></span>
<span data-ttu-id="86ad0-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86ad0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86ad0-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="86ad0-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86ad0-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="86ad0-126">INPUTS</span></span>

### <span data-ttu-id="86ad0-127">Keine</span><span class="sxs-lookup"><span data-stu-id="86ad0-127">None</span></span>

## <span data-ttu-id="86ad0-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="86ad0-128">OUTPUTS</span></span>

### <span data-ttu-id="86ad0-129">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="86ad0-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="86ad0-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="86ad0-130">NOTES</span></span>

## <span data-ttu-id="86ad0-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="86ad0-131">RELATED LINKS</span></span>
