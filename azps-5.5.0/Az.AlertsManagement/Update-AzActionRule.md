---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
ms.openlocfilehash: 2af687a79255d5e5ab4b49135bf8a8f7b8f819f1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171983"
---
# <span data-ttu-id="5617a-101">Update-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="5617a-101">Update-AzActionRule</span></span>

## <span data-ttu-id="5617a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5617a-102">SYNOPSIS</span></span>
<span data-ttu-id="5617a-103">Aktualisiert Eigenschaften von Aktionsregel.</span><span class="sxs-lookup"><span data-stu-id="5617a-103">Updates action rule properties.</span></span>

## <span data-ttu-id="5617a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5617a-104">SYNTAX</span></span>

### <span data-ttu-id="5617a-105">ByNameSimplifiedPatch (Standard)</span><span class="sxs-lookup"><span data-stu-id="5617a-105">ByNameSimplifiedPatch (Default)</span></span>
```
Update-AzActionRule -Name <String> -ResourceGroupName <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5617a-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5617a-106">ByResourceId</span></span>
```
Update-AzActionRule -ResourceId <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5617a-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5617a-107">ByInputObject</span></span>
```
Update-AzActionRule -InputObject <PSActionRule> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5617a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5617a-108">DESCRIPTION</span></span>
<span data-ttu-id="5617a-109">**Das Cmdlet "Update-AzActionRule"** aktualisiert Eigenschaften von Aktionsregel – Status und Tags.</span><span class="sxs-lookup"><span data-stu-id="5617a-109">**Update-AzActionRule** cmdlet updates action rule properties - status and tags.</span></span>

## <span data-ttu-id="5617a-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5617a-110">EXAMPLES</span></span>

### <span data-ttu-id="5617a-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5617a-111">Example 1</span></span>
```powershell
PS C:\> Update-AzActionRule -ResourceGroupName "test-rg" -Name "Test-ActionRule" -Status "Disabled"
```

<span data-ttu-id="5617a-112">Dieses Cmdlet deaktiviert die Aktionsregel.</span><span class="sxs-lookup"><span data-stu-id="5617a-112">This cmdlet disables the action rule.</span></span> 

## <span data-ttu-id="5617a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5617a-113">PARAMETERS</span></span>

### <span data-ttu-id="5617a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5617a-114">-DefaultProfile</span></span>
<span data-ttu-id="5617a-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5617a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5617a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5617a-116">-InputObject</span></span>
<span data-ttu-id="5617a-117">Die Aktionsregelressource</span><span class="sxs-lookup"><span data-stu-id="5617a-117">The action rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5617a-118">-Name</span><span class="sxs-lookup"><span data-stu-id="5617a-118">-Name</span></span>
<span data-ttu-id="5617a-119">Name der Aktionsregel</span><span class="sxs-lookup"><span data-stu-id="5617a-119">Action rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameSimplifiedPatch
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5617a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5617a-120">-ResourceGroupName</span></span>
<span data-ttu-id="5617a-121">Name der Aktionsregel</span><span class="sxs-lookup"><span data-stu-id="5617a-121">Action rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameSimplifiedPatch
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5617a-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5617a-122">-ResourceId</span></span>
<span data-ttu-id="5617a-123">Die Ressourcen-ID der Aktionsregel</span><span class="sxs-lookup"><span data-stu-id="5617a-123">The resource id of action rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5617a-124">-Status</span><span class="sxs-lookup"><span data-stu-id="5617a-124">-Status</span></span>
<span data-ttu-id="5617a-125">Aktionsregelstatus</span><span class="sxs-lookup"><span data-stu-id="5617a-125">Action rule status</span></span>

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

### <span data-ttu-id="5617a-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="5617a-126">-Tag</span></span>
<span data-ttu-id="5617a-127">Aktionsregeltags</span><span class="sxs-lookup"><span data-stu-id="5617a-127">Action rule tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5617a-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5617a-128">-Confirm</span></span>
<span data-ttu-id="5617a-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5617a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5617a-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5617a-130">-WhatIf</span></span>
<span data-ttu-id="5617a-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5617a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5617a-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5617a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5617a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5617a-133">CommonParameters</span></span>
<span data-ttu-id="5617a-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5617a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5617a-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5617a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5617a-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5617a-136">INPUTS</span></span>

### <span data-ttu-id="5617a-137">System.String</span><span class="sxs-lookup"><span data-stu-id="5617a-137">System.String</span></span>

### <span data-ttu-id="5617a-138">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="5617a-138">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="5617a-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5617a-139">OUTPUTS</span></span>

### <span data-ttu-id="5617a-140">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="5617a-140">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="5617a-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5617a-141">NOTES</span></span>

## <span data-ttu-id="5617a-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5617a-142">RELATED LINKS</span></span>
