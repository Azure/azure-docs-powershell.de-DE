---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/restore-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 01354106e3d6ad9fbe33c97f6bcd774c62be7ccf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98296537"
---
# <span data-ttu-id="55569-101">Restore-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="55569-101">Restore-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="55569-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55569-102">SYNOPSIS</span></span>
<span data-ttu-id="55569-103">Wiederherstellen eines gelöschten Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="55569-103">Restore a deleted workspace.</span></span>

## <span data-ttu-id="55569-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="55569-104">SYNTAX</span></span>

```
Restore-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55569-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="55569-105">DESCRIPTION</span></span>
<span data-ttu-id="55569-106">Wiederherstellen eines gelöschten Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="55569-106">Restore a deleted workspace.</span></span>

## <span data-ttu-id="55569-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="55569-107">EXAMPLES</span></span>

### <span data-ttu-id="55569-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="55569-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> $workspace = Restore-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
```

<span data-ttu-id="55569-109">Gelöschten Arbeitsbereich wiederherstellen</span><span class="sxs-lookup"><span data-stu-id="55569-109">Restore deleted workspace.</span></span>

## <span data-ttu-id="55569-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55569-110">PARAMETERS</span></span>

### <span data-ttu-id="55569-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55569-111">-DefaultProfile</span></span>
<span data-ttu-id="55569-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="55569-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55569-113">-Force</span><span class="sxs-lookup"><span data-stu-id="55569-113">-Force</span></span>
<span data-ttu-id="55569-114">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="55569-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="55569-115">-Location</span><span class="sxs-lookup"><span data-stu-id="55569-115">-Location</span></span>
<span data-ttu-id="55569-116">Die geografische Region, in der der Arbeitsbereich erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="55569-116">The geographic region that the workspace will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55569-117">-Name</span><span class="sxs-lookup"><span data-stu-id="55569-117">-Name</span></span>
<span data-ttu-id="55569-118">Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="55569-118">The workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55569-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55569-119">-ResourceGroupName</span></span>
<span data-ttu-id="55569-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="55569-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55569-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="55569-121">-Confirm</span></span>
<span data-ttu-id="55569-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="55569-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55569-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="55569-123">-WhatIf</span></span>
<span data-ttu-id="55569-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="55569-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55569-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="55569-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55569-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55569-126">CommonParameters</span></span>
<span data-ttu-id="55569-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55569-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55569-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55569-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55569-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="55569-129">INPUTS</span></span>

### <span data-ttu-id="55569-130">System.String</span><span class="sxs-lookup"><span data-stu-id="55569-130">System.String</span></span>

## <span data-ttu-id="55569-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="55569-131">OUTPUTS</span></span>

### <span data-ttu-id="55569-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="55569-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="55569-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="55569-133">NOTES</span></span>

## <span data-ttu-id="55569-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="55569-134">RELATED LINKS</span></span>
