---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A08AF7C-1E18-40A1-B21E-12F94823D304
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightscustomlogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCustomLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCustomLogDataSource.md
ms.openlocfilehash: e923d413b889583578efb0ac81f9eb6aeadf72fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931520"
---
# <span data-ttu-id="2280f-101">New-AzOperationalInsightsCustomLogDataSource</span><span class="sxs-lookup"><span data-stu-id="2280f-101">New-AzOperationalInsightsCustomLogDataSource</span></span>

## <span data-ttu-id="2280f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2280f-102">SYNOPSIS</span></span>
<span data-ttu-id="2280f-103">Definiert eine benutzerdefinierte Protokollsammlungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="2280f-103">Defines a custom log collection policy.</span></span>

## <span data-ttu-id="2280f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2280f-104">SYNTAX</span></span>

### <span data-ttu-id="2280f-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="2280f-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsCustomLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2280f-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="2280f-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsCustomLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2280f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2280f-107">DESCRIPTION</span></span>
<span data-ttu-id="2280f-108">Das **Cmdlet New-AzOperationalInsightsCustomLogDataSource** definiert eine benutzerdefinierte Protokollsammlungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="2280f-108">The **New-AzOperationalInsightsCustomLogDataSource** cmdlet defines a custom log collection policy.</span></span>

## <span data-ttu-id="2280f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2280f-109">EXAMPLES</span></span>

## <span data-ttu-id="2280f-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2280f-110">PARAMETERS</span></span>

### <span data-ttu-id="2280f-111">-CustomLogRawJson</span><span class="sxs-lookup"><span data-stu-id="2280f-111">-CustomLogRawJson</span></span>
<span data-ttu-id="2280f-112">Gibt die benutzerdefinierte Sammlungsrichtlinie als unformatierte JSON-Zeichenfolge (JavaScript Object Notation) an.</span><span class="sxs-lookup"><span data-stu-id="2280f-112">Specifies the custom collection policy as a raw JavaScript Object Notation (JSON) string.</span></span>

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

### <span data-ttu-id="2280f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2280f-113">-DefaultProfile</span></span>
<span data-ttu-id="2280f-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="2280f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2280f-115">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="2280f-115">-Force</span></span>
<span data-ttu-id="2280f-116">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="2280f-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2280f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="2280f-117">-Name</span></span>
<span data-ttu-id="2280f-118">Gibt einen Namen für die Datenquelle an.</span><span class="sxs-lookup"><span data-stu-id="2280f-118">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="2280f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2280f-119">-ResourceGroupName</span></span>
<span data-ttu-id="2280f-120">Gibt den Namen einer Ressourcengruppe an, die Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="2280f-120">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="2280f-121">-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="2280f-121">-Workspace</span></span>
<span data-ttu-id="2280f-122">Gibt einen Arbeitsbereich an, in dem dieses Cmdlet verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2280f-122">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="2280f-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2280f-123">-WorkspaceName</span></span>
<span data-ttu-id="2280f-124">Gibt den Namen eines Arbeitsbereichs an, in dem dieses Cmdlet verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2280f-124">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="2280f-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2280f-125">-Confirm</span></span>
<span data-ttu-id="2280f-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2280f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2280f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2280f-127">-WhatIf</span></span>
<span data-ttu-id="2280f-128">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2280f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2280f-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2280f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2280f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2280f-130">CommonParameters</span></span>
<span data-ttu-id="2280f-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2280f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2280f-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2280f-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2280f-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2280f-133">INPUTS</span></span>

### <span data-ttu-id="2280f-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="2280f-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="2280f-135">System.String</span><span class="sxs-lookup"><span data-stu-id="2280f-135">System.String</span></span>

## <span data-ttu-id="2280f-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2280f-136">OUTPUTS</span></span>

### <span data-ttu-id="2280f-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="2280f-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="2280f-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2280f-138">NOTES</span></span>

## <span data-ttu-id="2280f-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2280f-139">RELATED LINKS</span></span>

[<span data-ttu-id="2280f-140">Disable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="2280f-140">Disable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzOperationalInsightsLinuxCustomLogCollection.md)

[<span data-ttu-id="2280f-141">Enable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="2280f-141">Enable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzOperationalInsightsLinuxCustomLogCollection.md)


