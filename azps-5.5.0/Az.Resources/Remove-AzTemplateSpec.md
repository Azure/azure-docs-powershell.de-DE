---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
ms.openlocfilehash: 718de3ac2da38b8ed7950e8f8a59b0d8fc2f4db7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156449"
---
# <span data-ttu-id="28b9e-101">Remove-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="28b9e-101">Remove-AzTemplateSpec</span></span>

## <span data-ttu-id="28b9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28b9e-102">SYNOPSIS</span></span>
<span data-ttu-id="28b9e-103">Entfernt eine Vorlagenspezifikation</span><span class="sxs-lookup"><span data-stu-id="28b9e-103">Removes a Template Spec</span></span>

## <span data-ttu-id="28b9e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="28b9e-104">SYNTAX</span></span>

### <span data-ttu-id="28b9e-105">RemoveByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="28b9e-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzTemplateSpec [-Force] [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28b9e-106">RemoveByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="28b9e-106">RemoveByIdParameterSet</span></span>
```
Remove-AzTemplateSpec [-Force] [[-Version] <String>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28b9e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="28b9e-107">DESCRIPTION</span></span>
<span data-ttu-id="28b9e-108">Entfernt eine angegebene Vorlagenspezifikation. Wenn der Parameter **"Version -Version"** angegeben wird, wird nur die angegebene Version entfernt.</span><span class="sxs-lookup"><span data-stu-id="28b9e-108">Removes a specified Template Spec. If the version **-Version** parameter is provided, only the specified version will be removed.</span></span> <span data-ttu-id="28b9e-109">Wenn keine bestimmte Version bereitgestellt wird, werden die Vorlagenspezifikation und alle versionen entfernt.</span><span class="sxs-lookup"><span data-stu-id="28b9e-109">If no specific version is provided, the Template Spec and all of its versions will be removed.</span></span> <span data-ttu-id="28b9e-110">Wenn das **Kennzeichen "-Force"** vorhanden ist, wird keine Bestätigungsaufforderung zum Entfernen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="28b9e-110">If the **-Force** flag is present there will be no confirmation prompt for removal.</span></span>

## <span data-ttu-id="28b9e-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="28b9e-111">EXAMPLES</span></span>

### <span data-ttu-id="28b9e-112">Beispiel 1: Entfernen einer bestimmten Version nach Name</span><span class="sxs-lookup"><span data-stu-id="28b9e-112">Example 1: Removing a specific version by name</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="28b9e-113">Entfernt version 'v1.0' des Vorlagenspezifikationen namens 'MyTemplateSpec' innerhalb der Ressourcengruppe 'myRG'.</span><span class="sxs-lookup"><span data-stu-id="28b9e-113">Removes version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

### <span data-ttu-id="28b9e-114">Beispiel 2: Entfernen einer bestimmten Version nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="28b9e-114">Example 2: Removing a specific version by resource id</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="28b9e-115">Entfernt version 'v1.0' des Vorlagenspezifikationen namens 'MyTemplateSpec' in der Ressourcengruppe 'myRG' von subscription \{ \} subId.</span><span class="sxs-lookup"><span data-stu-id="28b9e-115">Removes version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

### <span data-ttu-id="28b9e-116">Beispiel 3: Entfernen einer Vorlagenspezifikation und aller Versionen nach Name</span><span class="sxs-lookup"><span data-stu-id="28b9e-116">Example 3: Removing a Template Spec and all versions by name</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

<span data-ttu-id="28b9e-117">Entfernt die Vorlagenspezifikation mit dem Namen "MyTemplateSpec" und alle versionen innerhalb der Ressourcengruppe "myRG".</span><span class="sxs-lookup"><span data-stu-id="28b9e-117">Removes the Template Spec named 'MyTemplateSpec' and all of its versions within the resource group 'myRG'.</span></span>

### <span data-ttu-id="28b9e-118">Beispiel 3: Entfernen einer Vorlagenspezifikation und aller Versionen nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="28b9e-118">Example 3: Removing a Template Spec and all versions by resource id</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -ResourceGroupName 'myRG'
```

<span data-ttu-id="28b9e-119">Entfernt die Vorlagenspezifikation mit dem Namen "MyTemplateSpec" und alle versionen innerhalb der Ressourcengruppe "myRG" der \{ subId des \} Abonnements.</span><span class="sxs-lookup"><span data-stu-id="28b9e-119">Removes the Template Spec named 'MyTemplateSpec' and all of its versions within the resource group 'myRG' of subscription \{subId\}.</span></span>

## <span data-ttu-id="28b9e-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28b9e-120">PARAMETERS</span></span>

### <span data-ttu-id="28b9e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28b9e-121">-DefaultProfile</span></span>
<span data-ttu-id="28b9e-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="28b9e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28b9e-123">-Force</span><span class="sxs-lookup"><span data-stu-id="28b9e-123">-Force</span></span>
<span data-ttu-id="28b9e-124">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="28b9e-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="28b9e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="28b9e-125">-Name</span></span>
<span data-ttu-id="28b9e-126">Der Name der Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="28b9e-126">The name of the template spec.</span></span>

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

### <span data-ttu-id="28b9e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28b9e-127">-ResourceGroupName</span></span>
<span data-ttu-id="28b9e-128">Der Name der Ressourcengruppe der Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="28b9e-128">The name of the template spec's resource group.</span></span>

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

### <span data-ttu-id="28b9e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28b9e-129">-ResourceId</span></span>
<span data-ttu-id="28b9e-130">Die vollqualifizierte Ressourcen-ID der Vorlagenspezifikation. Beispiel: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="28b9e-130">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

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

### <span data-ttu-id="28b9e-131">-Version</span><span class="sxs-lookup"><span data-stu-id="28b9e-131">-Version</span></span>
<span data-ttu-id="28b9e-132">Die Version der Zu löschende Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="28b9e-132">The version of the template spec to delete.</span></span>

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

### <span data-ttu-id="28b9e-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="28b9e-133">-Confirm</span></span>
<span data-ttu-id="28b9e-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="28b9e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28b9e-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="28b9e-135">-WhatIf</span></span>
<span data-ttu-id="28b9e-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="28b9e-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="28b9e-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="28b9e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28b9e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28b9e-138">CommonParameters</span></span>
<span data-ttu-id="28b9e-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28b9e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28b9e-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="28b9e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28b9e-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="28b9e-141">INPUTS</span></span>

### <span data-ttu-id="28b9e-142">System.String</span><span class="sxs-lookup"><span data-stu-id="28b9e-142">System.String</span></span>

## <span data-ttu-id="28b9e-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="28b9e-143">OUTPUTS</span></span>

### <span data-ttu-id="28b9e-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="28b9e-144">System.Boolean</span></span>

## <span data-ttu-id="28b9e-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="28b9e-145">NOTES</span></span>

## <span data-ttu-id="28b9e-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="28b9e-146">RELATED LINKS</span></span>
