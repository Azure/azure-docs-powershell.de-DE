---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/export-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzTemplateSpec.md
ms.openlocfilehash: eb6311dacd05f539cf508657e52637524ea98ea7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929856"
---
# <span data-ttu-id="31b15-101">Export-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="31b15-101">Export-AzTemplateSpec</span></span>

## <span data-ttu-id="31b15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31b15-102">SYNOPSIS</span></span>
<span data-ttu-id="31b15-103">Exportiert eine Vorlagenspezifikation in das lokale Dateisystem</span><span class="sxs-lookup"><span data-stu-id="31b15-103">Exports a Template Spec to the local filesystem</span></span>

## <span data-ttu-id="31b15-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="31b15-104">SYNTAX</span></span>

### <span data-ttu-id="31b15-105">ExportByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="31b15-105">ExportByNameParameterSet (Default)</span></span>
```
Export-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> -OutputFolder <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31b15-106">ExportByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="31b15-106">ExportByIdParameterSet</span></span>
```
Export-AzTemplateSpec [-ResourceId] <String> -Version <String> -OutputFolder <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31b15-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="31b15-107">DESCRIPTION</span></span>
<span data-ttu-id="31b15-108">Exportiert eine bestimmte Version der Vorlagenspezifikation in das lokale Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="31b15-108">Exports a specific Template Spec version to the local filesystem.</span></span>

## <span data-ttu-id="31b15-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="31b15-109">EXAMPLES</span></span>

### <span data-ttu-id="31b15-110">Beispiel 1: Exportieren nach Name</span><span class="sxs-lookup"><span data-stu-id="31b15-110">Example 1: Export by name</span></span>
```powershell
PS C:\> Export-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0' -OutputFolder 'v1'
```

<span data-ttu-id="31b15-111">Exportiert Version "v1.0" der Vorlagenspezifikation mit dem Namen "MyTemplateSpec" innerhalb der Ressourcengruppe "myRG" in den lokalen Ausgabeordner "v1".</span><span class="sxs-lookup"><span data-stu-id="31b15-111">Exports version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' to the local output folder "v1".</span></span>

### <span data-ttu-id="31b15-112">Beispiel 2: Exportieren nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="31b15-112">Example 2: Export by resource id</span></span>
```powershell
PS C:\> Export-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0' -OutputFolder 'v1'
```

<span data-ttu-id="31b15-113">Exportiert Version "v1.0" der Vorlagenspezifikation mit dem Namen "MyTemplateSpec" innerhalb der Ressourcengruppe "myRG" der SubId des Abonnements in den lokalen Ausgabeordner \{ \} "v1".</span><span class="sxs-lookup"><span data-stu-id="31b15-113">Exports version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\} to the local output folder "v1".</span></span>

## <span data-ttu-id="31b15-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="31b15-114">PARAMETERS</span></span>

### <span data-ttu-id="31b15-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31b15-115">-DefaultProfile</span></span>
<span data-ttu-id="31b15-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="31b15-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31b15-117">-Name</span><span class="sxs-lookup"><span data-stu-id="31b15-117">-Name</span></span>
<span data-ttu-id="31b15-118">Der Name der Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="31b15-118">The name of the template spec.</span></span>

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

### <span data-ttu-id="31b15-119">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="31b15-119">-OutputFolder</span></span>
<span data-ttu-id="31b15-120">Der Pfad zu dem Ordner, in dem die Vorlagenspezifikationsversion ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="31b15-120">The path to the folder where the template spec version will be output to.</span></span>

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

### <span data-ttu-id="31b15-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31b15-121">-ResourceGroupName</span></span>
<span data-ttu-id="31b15-122">Der Name der Ressourcengruppe der Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="31b15-122">The name of the template spec's resource group.</span></span>

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

### <span data-ttu-id="31b15-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31b15-123">-ResourceId</span></span>
<span data-ttu-id="31b15-124">Die vollqualifizierte Ressourcen-ID der Vorlagenspezifikation. Beispiel: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="31b15-124">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

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

### <span data-ttu-id="31b15-125">-Version</span><span class="sxs-lookup"><span data-stu-id="31b15-125">-Version</span></span>
<span data-ttu-id="31b15-126">Die Version der Zu exportierende Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="31b15-126">The version of the template spec to export.</span></span>

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

### <span data-ttu-id="31b15-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="31b15-127">-Confirm</span></span>
<span data-ttu-id="31b15-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="31b15-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31b15-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31b15-129">-WhatIf</span></span>
<span data-ttu-id="31b15-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="31b15-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="31b15-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="31b15-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31b15-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31b15-132">CommonParameters</span></span>
<span data-ttu-id="31b15-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31b15-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31b15-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="31b15-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31b15-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="31b15-135">INPUTS</span></span>

### <span data-ttu-id="31b15-136">System.String</span><span class="sxs-lookup"><span data-stu-id="31b15-136">System.String</span></span>

## <span data-ttu-id="31b15-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="31b15-137">OUTPUTS</span></span>

### <span data-ttu-id="31b15-138">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="31b15-138">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="31b15-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="31b15-139">NOTES</span></span>

## <span data-ttu-id="31b15-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="31b15-140">RELATED LINKS</span></span>
