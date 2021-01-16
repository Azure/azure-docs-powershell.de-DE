---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/export-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzTemplateSpec.md
ms.openlocfilehash: 9b0db1cc72064b502b9961fba73598b94790af1a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98306003"
---
# <span data-ttu-id="c4651-101">Export-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="c4651-101">Export-AzTemplateSpec</span></span>

## <span data-ttu-id="c4651-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4651-102">SYNOPSIS</span></span>
<span data-ttu-id="c4651-103">Exportiert eine Vorlagenspezifikation in das lokale Dateisystem</span><span class="sxs-lookup"><span data-stu-id="c4651-103">Exports a Template Spec to the local filesystem</span></span>

## <span data-ttu-id="c4651-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c4651-104">SYNTAX</span></span>

### <span data-ttu-id="c4651-105">ExportByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c4651-105">ExportByNameParameterSet (Default)</span></span>
```
Export-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> -OutputFolder <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4651-106">ExportByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4651-106">ExportByIdParameterSet</span></span>
```
Export-AzTemplateSpec [-ResourceId] <String> -Version <String> -OutputFolder <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4651-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c4651-107">DESCRIPTION</span></span>
<span data-ttu-id="c4651-108">Exportiert eine bestimmte Version einer Vorlagenspezifikation in das lokale Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="c4651-108">Exports a specific Template Spec version to the local filesystem.</span></span>

## <span data-ttu-id="c4651-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c4651-109">EXAMPLES</span></span>

### <span data-ttu-id="c4651-110">Beispiel 1: Exportieren nach Name</span><span class="sxs-lookup"><span data-stu-id="c4651-110">Example 1: Export by name</span></span>
```powershell
PS C:\> Export-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0' -OutputFolder 'v1'
```

<span data-ttu-id="c4651-111">Exportiert Version 'v1.0' des Vorlagenspezifikationen namens 'MyTemplateSpec' innerhalb der Ressourcengruppe 'myRG' in den lokalen Ausgabeordner "v1".</span><span class="sxs-lookup"><span data-stu-id="c4651-111">Exports version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' to the local output folder "v1".</span></span>

### <span data-ttu-id="c4651-112">Beispiel 2: Exportieren nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="c4651-112">Example 2: Export by resource id</span></span>
```powershell
PS C:\> Export-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0' -OutputFolder 'v1'
```

<span data-ttu-id="c4651-113">Exportiert Version 'v1.0' der Vorlagenspezifikation mit dem Namen 'MyTemplateSpec' innerhalb der Ressourcengruppe 'myRG' der subId des Abonnements in den lokalen Ausgabeordner \{ \} "v1".</span><span class="sxs-lookup"><span data-stu-id="c4651-113">Exports version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\} to the local output folder "v1".</span></span>

## <span data-ttu-id="c4651-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4651-114">PARAMETERS</span></span>

### <span data-ttu-id="c4651-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4651-115">-DefaultProfile</span></span>
<span data-ttu-id="c4651-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c4651-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4651-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c4651-117">-Name</span></span>
<span data-ttu-id="c4651-118">Der Name der Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="c4651-118">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4651-119">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="c4651-119">-OutputFolder</span></span>
<span data-ttu-id="c4651-120">Der Pfad zu dem Ordner, in den die Version der Vorlagenspezifikation ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c4651-120">The path to the folder where the template spec version will be output to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4651-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4651-121">-ResourceGroupName</span></span>
<span data-ttu-id="c4651-122">Der Name der Ressourcengruppe der Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="c4651-122">The name of the template spec's resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4651-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4651-123">-ResourceId</span></span>
<span data-ttu-id="c4651-124">Die vollqualifizierte Ressourcen-ID der Vorlagenspezifikation. Beispiel: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="c4651-124">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4651-125">-Version</span><span class="sxs-lookup"><span data-stu-id="c4651-125">-Version</span></span>
<span data-ttu-id="c4651-126">Die Version der zu exportierende Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="c4651-126">The version of the template spec to export.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4651-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4651-127">-Confirm</span></span>
<span data-ttu-id="c4651-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c4651-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4651-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c4651-129">-WhatIf</span></span>
<span data-ttu-id="c4651-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c4651-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c4651-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c4651-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4651-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4651-132">CommonParameters</span></span>
<span data-ttu-id="c4651-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4651-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4651-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c4651-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4651-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c4651-135">INPUTS</span></span>

### <span data-ttu-id="c4651-136">System.String</span><span class="sxs-lookup"><span data-stu-id="c4651-136">System.String</span></span>

## <span data-ttu-id="c4651-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c4651-137">OUTPUTS</span></span>

### <span data-ttu-id="c4651-138">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="c4651-138">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c4651-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c4651-139">NOTES</span></span>

## <span data-ttu-id="c4651-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c4651-140">RELATED LINKS</span></span>
