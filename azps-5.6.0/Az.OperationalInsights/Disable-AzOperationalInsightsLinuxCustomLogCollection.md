---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: EF3FE3F1-1C8F-41EB-990E-F2B30BD9D082
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/disable-azoperationalinsightslinuxcustomlogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxCustomLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxCustomLogCollection.md
ms.openlocfilehash: db1e013fb1d8cdf72841e7b51f29481742d5f023
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942379"
---
# <span data-ttu-id="bd794-101">Disable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="bd794-101">Disable-AzOperationalInsightsLinuxCustomLogCollection</span></span>

## <span data-ttu-id="bd794-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd794-102">SYNOPSIS</span></span>
<span data-ttu-id="bd794-103">Beendet die Sammlung von benutzerdefinierten Protokollen von Linux-Computern.</span><span class="sxs-lookup"><span data-stu-id="bd794-103">Stops collection of custom logs from Linux computers.</span></span>

## <span data-ttu-id="bd794-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bd794-104">SYNTAX</span></span>

### <span data-ttu-id="bd794-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="bd794-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsLinuxCustomLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd794-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="bd794-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsLinuxCustomLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd794-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bd794-107">DESCRIPTION</span></span>
<span data-ttu-id="bd794-108">Das **Cmdlet Disable-AzOperationalInsightsLinuxCustomLogCollection** beendet die Sammlung von benutzerdefinierten Protokollen von verbundenen Linux-Computern in einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="bd794-108">The **Disable-AzOperationalInsightsLinuxCustomLogCollection** cmdlet stops collection of custom logs from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="bd794-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bd794-109">EXAMPLES</span></span>

## <span data-ttu-id="bd794-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="bd794-110">PARAMETERS</span></span>

### <span data-ttu-id="bd794-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd794-111">-DefaultProfile</span></span>
<span data-ttu-id="bd794-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="bd794-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd794-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd794-113">-ResourceGroupName</span></span>
<span data-ttu-id="bd794-114">Gibt den Namen einer Ressourcengruppe an, die Linux-Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="bd794-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="bd794-115">-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="bd794-115">-Workspace</span></span>
<span data-ttu-id="bd794-116">Gibt einen Arbeitsbereich an, in dem dieses Cmdlet verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bd794-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="bd794-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bd794-117">-WorkspaceName</span></span>
<span data-ttu-id="bd794-118">Gibt den Namen eines Arbeitsbereichs an, in dem dieses Cmdlet verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bd794-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="bd794-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bd794-119">-Confirm</span></span>
<span data-ttu-id="bd794-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bd794-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd794-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd794-121">-WhatIf</span></span>
<span data-ttu-id="bd794-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bd794-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd794-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bd794-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd794-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd794-124">CommonParameters</span></span>
<span data-ttu-id="bd794-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd794-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd794-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd794-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd794-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bd794-127">INPUTS</span></span>

### <span data-ttu-id="bd794-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="bd794-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="bd794-129">System.String</span><span class="sxs-lookup"><span data-stu-id="bd794-129">System.String</span></span>

## <span data-ttu-id="bd794-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bd794-130">OUTPUTS</span></span>

### <span data-ttu-id="bd794-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="bd794-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="bd794-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="bd794-132">NOTES</span></span>
* <span data-ttu-id="bd794-133">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, operational, insights</span><span class="sxs-lookup"><span data-stu-id="bd794-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="bd794-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="bd794-134">RELATED LINKS</span></span>

[<span data-ttu-id="bd794-135">Enable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="bd794-135">Enable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzOperationalInsightsLinuxCustomLogCollection.md)


