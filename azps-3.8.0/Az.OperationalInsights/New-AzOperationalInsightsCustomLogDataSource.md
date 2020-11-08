---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A08AF7C-1E18-40A1-B21E-12F94823D304
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightscustomlogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCustomLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCustomLogDataSource.md
ms.openlocfilehash: ba33d02ec8c47c91865cc2d0f5549e5f446ca2c6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995337"
---
# <span data-ttu-id="1e5fc-101">New-AzOperationalInsightsCustomLogDataSource</span><span class="sxs-lookup"><span data-stu-id="1e5fc-101">New-AzOperationalInsightsCustomLogDataSource</span></span>

## <span data-ttu-id="1e5fc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1e5fc-102">SYNOPSIS</span></span>
<span data-ttu-id="1e5fc-103">Definiert eine benutzerdefinierte Protokoll Sammlungs Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="1e5fc-103">Defines a custom log collection policy.</span></span>

## <span data-ttu-id="1e5fc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e5fc-104">SYNTAX</span></span>

### <span data-ttu-id="1e5fc-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="1e5fc-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsCustomLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e5fc-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="1e5fc-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsCustomLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1e5fc-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1e5fc-107">DESCRIPTION</span></span>
<span data-ttu-id="1e5fc-108">Das Cmdlet **New-AzOperationalInsightsCustomLogDataSource** definiert eine benutzerdefinierte Protokoll Sammlungs Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="1e5fc-108">The **New-AzOperationalInsightsCustomLogDataSource** cmdlet defines a custom log collection policy.</span></span>

## <span data-ttu-id="1e5fc-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1e5fc-109">EXAMPLES</span></span>

## <span data-ttu-id="1e5fc-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e5fc-110">PARAMETERS</span></span>

### <span data-ttu-id="1e5fc-111">-CustomLogRawJson</span><span class="sxs-lookup"><span data-stu-id="1e5fc-111">-CustomLogRawJson</span></span>
<span data-ttu-id="1e5fc-112">Gibt die benutzerdefinierte Sammlungs Richtlinie als unformatierte JSON-Zeichenfolge (JavaScript Object Notation) an.</span><span class="sxs-lookup"><span data-stu-id="1e5fc-112">Specifies the custom collection policy as a raw JavaScript Object Notation (JSON) string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e5fc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e5fc-113">-DefaultProfile</span></span>
<span data-ttu-id="1e5fc-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="1e5fc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e5fc-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1e5fc-115">-Force</span></span>
<span data-ttu-id="1e5fc-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="1e5fc-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e5fc-117">-Name</span><span class="sxs-lookup"><span data-stu-id="1e5fc-117">-Name</span></span>
<span data-ttu-id="1e5fc-118">Gibt einen Namen für die Datenquelle an.</span><span class="sxs-lookup"><span data-stu-id="1e5fc-118">Specifies a name for the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e5fc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e5fc-119">-ResourceGroupName</span></span>
<span data-ttu-id="1e5fc-120">Gibt den Namen einer Ressourcengruppe an, die Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="1e5fc-120">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e5fc-121">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="1e5fc-121">-Workspace</span></span>
<span data-ttu-id="1e5fc-122">Gibt einen Arbeitsbereich an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="1e5fc-122">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e5fc-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1e5fc-123">-WorkspaceName</span></span>
<span data-ttu-id="1e5fc-124">Gibt den Namen eines Arbeitsbereichs an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="1e5fc-124">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e5fc-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1e5fc-125">-Confirm</span></span>
<span data-ttu-id="1e5fc-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1e5fc-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e5fc-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e5fc-127">-WhatIf</span></span>
<span data-ttu-id="1e5fc-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1e5fc-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e5fc-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1e5fc-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e5fc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e5fc-130">CommonParameters</span></span>
<span data-ttu-id="1e5fc-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e5fc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e5fc-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e5fc-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e5fc-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1e5fc-133">INPUTS</span></span>

### <span data-ttu-id="1e5fc-134">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="1e5fc-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="1e5fc-135">System. String</span><span class="sxs-lookup"><span data-stu-id="1e5fc-135">System.String</span></span>

## <span data-ttu-id="1e5fc-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1e5fc-136">OUTPUTS</span></span>

### <span data-ttu-id="1e5fc-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="1e5fc-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="1e5fc-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="1e5fc-138">NOTES</span></span>

## <span data-ttu-id="1e5fc-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1e5fc-139">RELATED LINKS</span></span>

[<span data-ttu-id="1e5fc-140">Deaktivieren-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="1e5fc-140">Disable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzOperationalInsightsLinuxCustomLogCollection.md)

[<span data-ttu-id="1e5fc-141">Enable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="1e5fc-141">Enable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzOperationalInsightsLinuxCustomLogCollection.md)


