---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A08AF7C-1E18-40A1-B21E-12F94823D304
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightscustomlogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCustomLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCustomLogDataSource.md
ms.openlocfilehash: ba33d02ec8c47c91865cc2d0f5549e5f446ca2c6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468812"
---
# <span data-ttu-id="bebd5-101">New-AzOperationalInsightsCustomLogDataSource</span><span class="sxs-lookup"><span data-stu-id="bebd5-101">New-AzOperationalInsightsCustomLogDataSource</span></span>

## <span data-ttu-id="bebd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bebd5-102">SYNOPSIS</span></span>
<span data-ttu-id="bebd5-103">Definiert eine benutzerdefinierte Protokollsammlungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="bebd5-103">Defines a custom log collection policy.</span></span>

## <span data-ttu-id="bebd5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bebd5-104">SYNTAX</span></span>

### <span data-ttu-id="bebd5-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="bebd5-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsCustomLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bebd5-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="bebd5-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsCustomLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bebd5-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bebd5-107">DESCRIPTION</span></span>
<span data-ttu-id="bebd5-108">Das **Cmdlet "New-AzOperationalInsightsCustomLogDataSource"** definiert eine benutzerdefinierte Protokollsammlungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="bebd5-108">The **New-AzOperationalInsightsCustomLogDataSource** cmdlet defines a custom log collection policy.</span></span>

## <span data-ttu-id="bebd5-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bebd5-109">EXAMPLES</span></span>

## <span data-ttu-id="bebd5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bebd5-110">PARAMETERS</span></span>

### <span data-ttu-id="bebd5-111">-CustomLogRawJson</span><span class="sxs-lookup"><span data-stu-id="bebd5-111">-CustomLogRawJson</span></span>
<span data-ttu-id="bebd5-112">Gibt die benutzerdefinierte Sammlungsrichtlinie als unformatierte JavaScript Object Notation (JSON)-Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="bebd5-112">Specifies the custom collection policy as a raw JavaScript Object Notation (JSON) string.</span></span>

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

### <span data-ttu-id="bebd5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bebd5-113">-DefaultProfile</span></span>
<span data-ttu-id="bebd5-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="bebd5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bebd5-115">-Force</span><span class="sxs-lookup"><span data-stu-id="bebd5-115">-Force</span></span>
<span data-ttu-id="bebd5-116">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="bebd5-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bebd5-117">-Name</span><span class="sxs-lookup"><span data-stu-id="bebd5-117">-Name</span></span>
<span data-ttu-id="bebd5-118">Gibt einen Namen für die Datenquelle an.</span><span class="sxs-lookup"><span data-stu-id="bebd5-118">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="bebd5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bebd5-119">-ResourceGroupName</span></span>
<span data-ttu-id="bebd5-120">Gibt den Namen einer Ressourcengruppe an, die Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="bebd5-120">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="bebd5-121">-Workspace</span><span class="sxs-lookup"><span data-stu-id="bebd5-121">-Workspace</span></span>
<span data-ttu-id="bebd5-122">Gibt einen Arbeitsbereich an, in dem dieses Cmdlet betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="bebd5-122">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="bebd5-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bebd5-123">-WorkspaceName</span></span>
<span data-ttu-id="bebd5-124">Gibt den Namen eines Arbeitsbereichs an, in dem dieses Cmdlet betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="bebd5-124">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="bebd5-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bebd5-125">-Confirm</span></span>
<span data-ttu-id="bebd5-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bebd5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bebd5-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="bebd5-127">-WhatIf</span></span>
<span data-ttu-id="bebd5-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bebd5-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bebd5-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bebd5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bebd5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bebd5-130">CommonParameters</span></span>
<span data-ttu-id="bebd5-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bebd5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bebd5-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bebd5-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bebd5-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bebd5-133">INPUTS</span></span>

### <span data-ttu-id="bebd5-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="bebd5-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="bebd5-135">System.String</span><span class="sxs-lookup"><span data-stu-id="bebd5-135">System.String</span></span>

## <span data-ttu-id="bebd5-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bebd5-136">OUTPUTS</span></span>

### <span data-ttu-id="bebd5-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="bebd5-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="bebd5-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bebd5-138">NOTES</span></span>

## <span data-ttu-id="bebd5-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bebd5-139">RELATED LINKS</span></span>

[<span data-ttu-id="bebd5-140">Disable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="bebd5-140">Disable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzOperationalInsightsLinuxCustomLogCollection.md)

[<span data-ttu-id="bebd5-141">Enable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="bebd5-141">Enable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzOperationalInsightsLinuxCustomLogCollection.md)


