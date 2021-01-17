---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 26B1921E-6052-471B-B5B6-F2853536A425
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsIISLogCollection.md
ms.openlocfilehash: f48007be3e1209cff65e46c669bce46298182247
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384921"
---
# <span data-ttu-id="5937a-101">Enable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="5937a-101">Enable-AzOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="5937a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5937a-102">SYNOPSIS</span></span>
<span data-ttu-id="5937a-103">Startet die Sammlung von IIS-Protokollen von Computern in einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="5937a-103">Starts collection of IIS logs from computers in a workspace.</span></span>

## <span data-ttu-id="5937a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5937a-104">SYNTAX</span></span>

### <span data-ttu-id="5937a-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="5937a-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5937a-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5937a-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5937a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5937a-107">DESCRIPTION</span></span>
<span data-ttu-id="5937a-108">Das **Cmdlet "Enable-AzOperationalInsightsIISLogCollection"** startet die Sammlung von Internetinformationsdienste (IIS)-Protokollen von verbundenen Computern in einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="5937a-108">The **Enable-AzOperationalInsightsIISLogCollection** cmdlet starts collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="5937a-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5937a-109">EXAMPLES</span></span>

## <span data-ttu-id="5937a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5937a-110">PARAMETERS</span></span>

### <span data-ttu-id="5937a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5937a-111">-DefaultProfile</span></span>
<span data-ttu-id="5937a-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="5937a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5937a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5937a-113">-ResourceGroupName</span></span>
<span data-ttu-id="5937a-114">Gibt den Namen einer Ressourcengruppe an, die Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="5937a-114">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="5937a-115">-Workspace</span><span class="sxs-lookup"><span data-stu-id="5937a-115">-Workspace</span></span>
<span data-ttu-id="5937a-116">Gibt einen Arbeitsbereich an, in dem dieses Cmdlet arbeitet.</span><span class="sxs-lookup"><span data-stu-id="5937a-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="5937a-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5937a-117">-WorkspaceName</span></span>
<span data-ttu-id="5937a-118">Gibt den Namen eines Arbeitsbereichs an, in dem dieses Cmdlet betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="5937a-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="5937a-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5937a-119">-Confirm</span></span>
<span data-ttu-id="5937a-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5937a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5937a-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5937a-121">-WhatIf</span></span>
<span data-ttu-id="5937a-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5937a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5937a-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5937a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5937a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5937a-124">CommonParameters</span></span>
<span data-ttu-id="5937a-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5937a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5937a-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5937a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5937a-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5937a-127">INPUTS</span></span>

### <span data-ttu-id="5937a-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="5937a-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="5937a-129">System.String</span><span class="sxs-lookup"><span data-stu-id="5937a-129">System.String</span></span>

## <span data-ttu-id="5937a-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5937a-130">OUTPUTS</span></span>

### <span data-ttu-id="5937a-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="5937a-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="5937a-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5937a-132">NOTES</span></span>

## <span data-ttu-id="5937a-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5937a-133">RELATED LINKS</span></span>

[<span data-ttu-id="5937a-134">Disable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="5937a-134">Disable-AzOperationalInsightsIISLogCollection</span></span>](./Disable-AzOperationalInsightsIISLogCollection.md)


