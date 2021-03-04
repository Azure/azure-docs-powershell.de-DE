---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
ms.openlocfilehash: 6383a1fb0a6dbaa20bee50a268d8f78abf59de65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932320"
---
# <span data-ttu-id="edccb-101">Remove-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="edccb-101">Remove-AzTemplateSpec</span></span>

## <span data-ttu-id="edccb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edccb-102">SYNOPSIS</span></span>
<span data-ttu-id="edccb-103">Entfernt eine Vorlagenspezifikation</span><span class="sxs-lookup"><span data-stu-id="edccb-103">Removes a Template Spec</span></span>

## <span data-ttu-id="edccb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="edccb-104">SYNTAX</span></span>

### <span data-ttu-id="edccb-105">RemoveByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="edccb-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzTemplateSpec [-Force] [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edccb-106">RemoveByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="edccb-106">RemoveByIdParameterSet</span></span>
```
Remove-AzTemplateSpec [-Force] [[-Version] <String>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edccb-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="edccb-107">DESCRIPTION</span></span>
<span data-ttu-id="edccb-108">Entfernt eine angegebene Vorlagenspezifikation. Wenn der Parameter **Version -Version** bereitgestellt wird, wird nur die angegebene Version entfernt.</span><span class="sxs-lookup"><span data-stu-id="edccb-108">Removes a specified Template Spec. If the version **-Version** parameter is provided, only the specified version will be removed.</span></span> <span data-ttu-id="edccb-109">Wenn keine bestimmte Version bereitgestellt wird, werden die Vorlagenspezifikation und alle ihre Versionen entfernt.</span><span class="sxs-lookup"><span data-stu-id="edccb-109">If no specific version is provided, the Template Spec and all of its versions will be removed.</span></span> <span data-ttu-id="edccb-110">Wenn das **-Force-Flag** vorhanden ist, wird keine Bestätigungsaufforderung zum Entfernen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="edccb-110">If the **-Force** flag is present there will be no confirmation prompt for removal.</span></span>

## <span data-ttu-id="edccb-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="edccb-111">EXAMPLES</span></span>

### <span data-ttu-id="edccb-112">Beispiel 1: Entfernen einer bestimmten Version nach Name</span><span class="sxs-lookup"><span data-stu-id="edccb-112">Example 1: Removing a specific version by name</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="edccb-113">Entfernt Version "v1.0" der Vorlagenspezifikation mit dem Namen "MyTemplateSpec" innerhalb der Ressourcengruppe "myRG".</span><span class="sxs-lookup"><span data-stu-id="edccb-113">Removes version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

### <span data-ttu-id="edccb-114">Beispiel 2: Entfernen einer bestimmten Version nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="edccb-114">Example 2: Removing a specific version by resource id</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="edccb-115">Entfernt Version "v1.0" der Vorlagenspezifikation mit dem Namen "MyTemplateSpec" innerhalb der Ressourcengruppe "myRG" der SubId des \{ \} Abonnements.</span><span class="sxs-lookup"><span data-stu-id="edccb-115">Removes version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

### <span data-ttu-id="edccb-116">Beispiel 3: Entfernen einer Vorlagenspezifikation und aller Versionen nach Name</span><span class="sxs-lookup"><span data-stu-id="edccb-116">Example 3: Removing a Template Spec and all versions by name</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

<span data-ttu-id="edccb-117">Entfernt die Vorlagenspezifikation mit dem Namen "MyTemplateSpec" und alle versionen innerhalb der Ressourcengruppe "myRG".</span><span class="sxs-lookup"><span data-stu-id="edccb-117">Removes the Template Spec named 'MyTemplateSpec' and all of its versions within the resource group 'myRG'.</span></span>

### <span data-ttu-id="edccb-118">Beispiel 3: Entfernen einer Vorlagenspezifikation und aller Versionen nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="edccb-118">Example 3: Removing a Template Spec and all versions by resource id</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -ResourceGroupName 'myRG'
```

<span data-ttu-id="edccb-119">Entfernt die Vorlagenspezifikation mit dem Namen "MyTemplateSpec" und alle versionen innerhalb der Ressourcengruppe "myRG" der \{ SubId des \} Abonnements.</span><span class="sxs-lookup"><span data-stu-id="edccb-119">Removes the Template Spec named 'MyTemplateSpec' and all of its versions within the resource group 'myRG' of subscription \{subId\}.</span></span>

## <span data-ttu-id="edccb-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="edccb-120">PARAMETERS</span></span>

### <span data-ttu-id="edccb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edccb-121">-DefaultProfile</span></span>
<span data-ttu-id="edccb-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="edccb-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edccb-123">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="edccb-123">-Force</span></span>
<span data-ttu-id="edccb-124">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="edccb-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="edccb-125">-Name</span><span class="sxs-lookup"><span data-stu-id="edccb-125">-Name</span></span>
<span data-ttu-id="edccb-126">Der Name der Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="edccb-126">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edccb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edccb-127">-ResourceGroupName</span></span>
<span data-ttu-id="edccb-128">Der Name der Ressourcengruppe der Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="edccb-128">The name of the template spec's resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edccb-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="edccb-129">-ResourceId</span></span>
<span data-ttu-id="edccb-130">Die vollqualifizierte Ressourcen-ID der Vorlagenspezifikation. Beispiel: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="edccb-130">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edccb-131">-Version</span><span class="sxs-lookup"><span data-stu-id="edccb-131">-Version</span></span>
<span data-ttu-id="edccb-132">Die Version der Zu löschende Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="edccb-132">The version of the template spec to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edccb-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="edccb-133">-Confirm</span></span>
<span data-ttu-id="edccb-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="edccb-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edccb-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edccb-135">-WhatIf</span></span>
<span data-ttu-id="edccb-136">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="edccb-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="edccb-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="edccb-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edccb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edccb-138">CommonParameters</span></span>
<span data-ttu-id="edccb-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edccb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edccb-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="edccb-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edccb-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="edccb-141">INPUTS</span></span>

### <span data-ttu-id="edccb-142">System.String</span><span class="sxs-lookup"><span data-stu-id="edccb-142">System.String</span></span>

## <span data-ttu-id="edccb-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="edccb-143">OUTPUTS</span></span>

### <span data-ttu-id="edccb-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="edccb-144">System.Boolean</span></span>

## <span data-ttu-id="edccb-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="edccb-145">NOTES</span></span>

## <span data-ttu-id="edccb-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="edccb-146">RELATED LINKS</span></span>
