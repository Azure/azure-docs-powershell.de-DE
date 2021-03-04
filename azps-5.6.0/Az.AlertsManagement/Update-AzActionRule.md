---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/update-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
ms.openlocfilehash: 7dcbf947975719a30282037d592469a986990d50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939787"
---
# <span data-ttu-id="5b3ac-101">Update-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="5b3ac-101">Update-AzActionRule</span></span>

## <span data-ttu-id="5b3ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b3ac-102">SYNOPSIS</span></span>
<span data-ttu-id="5b3ac-103">Aktualisiert die Eigenschaften von Aktionsregel.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-103">Updates action rule properties.</span></span>

## <span data-ttu-id="5b3ac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5b3ac-104">SYNTAX</span></span>

### <span data-ttu-id="5b3ac-105">ByNameSimplifiedPatch (Standard)</span><span class="sxs-lookup"><span data-stu-id="5b3ac-105">ByNameSimplifiedPatch (Default)</span></span>
```
Update-AzActionRule -Name <String> -ResourceGroupName <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b3ac-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5b3ac-106">ByResourceId</span></span>
```
Update-AzActionRule -ResourceId <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b3ac-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5b3ac-107">ByInputObject</span></span>
```
Update-AzActionRule -InputObject <PSActionRule> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b3ac-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5b3ac-108">DESCRIPTION</span></span>
<span data-ttu-id="5b3ac-109">**Das Cmdlet Update-AzActionRule** aktualisiert die Eigenschaften der Aktionsregel – Status und Tags.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-109">**Update-AzActionRule** cmdlet updates action rule properties - status and tags.</span></span>

## <span data-ttu-id="5b3ac-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5b3ac-110">EXAMPLES</span></span>

### <span data-ttu-id="5b3ac-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5b3ac-111">Example 1</span></span>
```powershell
PS C:\> Update-AzActionRule -ResourceGroupName "test-rg" -Name "Test-ActionRule" -Status "Disabled"
```

<span data-ttu-id="5b3ac-112">Dieses Cmdlet deaktiviert die Aktionsregel.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-112">This cmdlet disables the action rule.</span></span> 

## <span data-ttu-id="5b3ac-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5b3ac-113">PARAMETERS</span></span>

### <span data-ttu-id="5b3ac-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b3ac-114">-DefaultProfile</span></span>
<span data-ttu-id="5b3ac-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b3ac-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b3ac-116">-InputObject</span></span>
<span data-ttu-id="5b3ac-117">Die Aktionsregelressource</span><span class="sxs-lookup"><span data-stu-id="5b3ac-117">The action rule resource</span></span>

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

### <span data-ttu-id="5b3ac-118">-Name</span><span class="sxs-lookup"><span data-stu-id="5b3ac-118">-Name</span></span>
<span data-ttu-id="5b3ac-119">Name der Aktionsregel</span><span class="sxs-lookup"><span data-stu-id="5b3ac-119">Action rule name</span></span>

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

### <span data-ttu-id="5b3ac-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b3ac-120">-ResourceGroupName</span></span>
<span data-ttu-id="5b3ac-121">Name der Aktionsregel</span><span class="sxs-lookup"><span data-stu-id="5b3ac-121">Action rule name</span></span>

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

### <span data-ttu-id="5b3ac-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b3ac-122">-ResourceId</span></span>
<span data-ttu-id="5b3ac-123">Die Ressourcen-ID der Aktionsregel</span><span class="sxs-lookup"><span data-stu-id="5b3ac-123">The resource id of action rule</span></span>

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

### <span data-ttu-id="5b3ac-124">-Status</span><span class="sxs-lookup"><span data-stu-id="5b3ac-124">-Status</span></span>
<span data-ttu-id="5b3ac-125">Status der Aktionsregel</span><span class="sxs-lookup"><span data-stu-id="5b3ac-125">Action rule status</span></span>

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

### <span data-ttu-id="5b3ac-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="5b3ac-126">-Tag</span></span>
<span data-ttu-id="5b3ac-127">Aktionsregeltags</span><span class="sxs-lookup"><span data-stu-id="5b3ac-127">Action rule tags</span></span>

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

### <span data-ttu-id="5b3ac-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5b3ac-128">-Confirm</span></span>
<span data-ttu-id="5b3ac-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b3ac-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b3ac-130">-WhatIf</span></span>
<span data-ttu-id="5b3ac-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b3ac-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b3ac-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b3ac-133">CommonParameters</span></span>
<span data-ttu-id="5b3ac-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b3ac-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b3ac-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5b3ac-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b3ac-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5b3ac-136">INPUTS</span></span>

### <span data-ttu-id="5b3ac-137">System.String</span><span class="sxs-lookup"><span data-stu-id="5b3ac-137">System.String</span></span>

### <span data-ttu-id="5b3ac-138">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="5b3ac-138">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="5b3ac-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5b3ac-139">OUTPUTS</span></span>

### <span data-ttu-id="5b3ac-140">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="5b3ac-140">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="5b3ac-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5b3ac-141">NOTES</span></span>

## <span data-ttu-id="5b3ac-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5b3ac-142">RELATED LINKS</span></span>
