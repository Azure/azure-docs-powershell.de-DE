---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 26B1921E-6052-471B-B5B6-F2853536A425
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsIISLogCollection.md
ms.openlocfilehash: f48007be3e1209cff65e46c669bce46298182247
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154004"
---
# <span data-ttu-id="f44c7-101">Enable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="f44c7-101">Enable-AzOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="f44c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f44c7-102">SYNOPSIS</span></span>
<span data-ttu-id="f44c7-103">Startet die Sammlung von IIS-Protokollen von Computern in einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="f44c7-103">Starts collection of IIS logs from computers in a workspace.</span></span>

## <span data-ttu-id="f44c7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f44c7-104">SYNTAX</span></span>

### <span data-ttu-id="f44c7-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="f44c7-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f44c7-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f44c7-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f44c7-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f44c7-107">DESCRIPTION</span></span>
<span data-ttu-id="f44c7-108">Das **Cmdlet "Enable-AzOperationalInsightsIISLogCollection"** startet die Sammlung von Internetinformationsdienste (IIS)-Protokollen von verbundenen Computern in einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="f44c7-108">The **Enable-AzOperationalInsightsIISLogCollection** cmdlet starts collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="f44c7-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f44c7-109">EXAMPLES</span></span>

## <span data-ttu-id="f44c7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f44c7-110">PARAMETERS</span></span>

### <span data-ttu-id="f44c7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f44c7-111">-DefaultProfile</span></span>
<span data-ttu-id="f44c7-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f44c7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f44c7-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f44c7-113">-ResourceGroupName</span></span>
<span data-ttu-id="f44c7-114">Gibt den Namen einer Ressourcengruppe an, die Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="f44c7-114">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="f44c7-115">-Workspace</span><span class="sxs-lookup"><span data-stu-id="f44c7-115">-Workspace</span></span>
<span data-ttu-id="f44c7-116">Gibt einen Arbeitsbereich an, in dem dieses Cmdlet betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="f44c7-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="f44c7-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f44c7-117">-WorkspaceName</span></span>
<span data-ttu-id="f44c7-118">Gibt den Namen eines Arbeitsbereichs an, in dem dieses Cmdlet betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="f44c7-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="f44c7-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f44c7-119">-Confirm</span></span>
<span data-ttu-id="f44c7-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f44c7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f44c7-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f44c7-121">-WhatIf</span></span>
<span data-ttu-id="f44c7-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f44c7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f44c7-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f44c7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f44c7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f44c7-124">CommonParameters</span></span>
<span data-ttu-id="f44c7-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f44c7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f44c7-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f44c7-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f44c7-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f44c7-127">INPUTS</span></span>

### <span data-ttu-id="f44c7-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="f44c7-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="f44c7-129">System.String</span><span class="sxs-lookup"><span data-stu-id="f44c7-129">System.String</span></span>

## <span data-ttu-id="f44c7-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f44c7-130">OUTPUTS</span></span>

### <span data-ttu-id="f44c7-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="f44c7-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="f44c7-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f44c7-132">NOTES</span></span>

## <span data-ttu-id="f44c7-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f44c7-133">RELATED LINKS</span></span>

[<span data-ttu-id="f44c7-134">Disable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="f44c7-134">Disable-AzOperationalInsightsIISLogCollection</span></span>](./Disable-AzOperationalInsightsIISLogCollection.md)


