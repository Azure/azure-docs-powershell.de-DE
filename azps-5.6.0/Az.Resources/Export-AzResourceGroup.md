---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 63BBDF98-75FC-4A44-9FD0-95AD21ED93A6
online version: https://docs.microsoft.com/powershell/module/az.resources/export-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
ms.openlocfilehash: 1f4f518cb203414392fe8d3f01fc0031be7f79e5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929859"
---
# <span data-ttu-id="12e8d-101">Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="12e8d-101">Export-AzResourceGroup</span></span>

## <span data-ttu-id="12e8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12e8d-102">SYNOPSIS</span></span>
<span data-ttu-id="12e8d-103">Erfasst eine Ressourcengruppe als Vorlage und speichert sie in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="12e8d-103">Captures a resource group as a template and saves it to a file.</span></span>

## <span data-ttu-id="12e8d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12e8d-104">SYNTAX</span></span>

```
Export-AzResourceGroup -ResourceGroupName <String> [-Path <String>] [-IncludeParameterDefaultValue]
 [-IncludeComments] [-SkipResourceNameParameterization] [-SkipAllParameterization] [-Resource <String[]>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="12e8d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="12e8d-105">DESCRIPTION</span></span>
<span data-ttu-id="12e8d-106">Das **Cmdlet Export-AzResourceGroup** erfasst die angegebene Ressourcengruppe als Vorlage und speichert sie in einer JSON-Datei. Dies kann in Szenarien nützlich sein, in denen Sie bereits einige Ressourcen in Ihrer Ressourcengruppe erstellt haben und dann die Vorteile der Verwendung von vorlagengestützten Bereitstellungen nutzen möchten.</span><span class="sxs-lookup"><span data-stu-id="12e8d-106">The **Export-AzResourceGroup** cmdlet captures the specified resource group as a template and saves it to a JSON file.This can be useful in scenarios where you have already created some resources in your resource group, and then want to leverage the benefits of using template backed deployments.</span></span>
<span data-ttu-id="12e8d-107">Dieses Cmdlet bietet Ihnen einen einfachen Einstieg, indem sie die Vorlage für Ihre vorhandenen Ressourcen in der Ressourcengruppe generiert.</span><span class="sxs-lookup"><span data-stu-id="12e8d-107">This cmdlet gives you an easy start by generating the template for your existing resources in the resource group.</span></span>
<span data-ttu-id="12e8d-108">In einigen Fällen kann dieses Cmdlet einige Teile der Vorlage nicht generieren.</span><span class="sxs-lookup"><span data-stu-id="12e8d-108">There might be some cases where this cmdlet fails to generate some parts of the template.</span></span>
<span data-ttu-id="12e8d-109">Warnmeldungen informieren Sie über die Ressourcen, die fehlgeschlagen sind.</span><span class="sxs-lookup"><span data-stu-id="12e8d-109">Warning messages will inform you of the resources that failed.</span></span>
<span data-ttu-id="12e8d-110">Die Vorlage wird weiterhin für die erfolgreichen Teile generiert.</span><span class="sxs-lookup"><span data-stu-id="12e8d-110">The template will still be generated for the parts that were successful.</span></span>

## <span data-ttu-id="12e8d-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="12e8d-111">EXAMPLES</span></span>

### <span data-ttu-id="12e8d-112">Beispiel 1: Exportieren einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="12e8d-112">Example 1: Export a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup"
```

<span data-ttu-id="12e8d-113">Mit diesem Befehl wird die Ressourcengruppe testGroup als Vorlage erfasst und in einer JSON-Datei im aktuellen Verzeichnis gespeichert.</span><span class="sxs-lookup"><span data-stu-id="12e8d-113">This command captures the resource group named TestGroup as a template, and saves it to a JSON file in the current directory.</span></span>

### <span data-ttu-id="12e8d-114">Beispiel 2: Exportieren einer einzelnen Ressource aus einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="12e8d-114">Example 2: Export a single resource from a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup" -Resource "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Compute/virtualMachines/TestVirtualMachine"
```

<span data-ttu-id="12e8d-115">Mit diesem Befehl wird die Virtual Machine-Ressource mit dem Namen "TestVirtualMachine" aus der Ressourcengruppe "TestGruppe" als Vorlage erfasst und in einer JSON-Datei im aktuellen Verzeichnis gespeichert.</span><span class="sxs-lookup"><span data-stu-id="12e8d-115">This command captures the Virtual Machine resource named "TestVirtualMachine" from the "TestGroup" resource group as a template, and saves it to a JSON file in the current directory.</span></span>

### <span data-ttu-id="12e8d-116">Beispiel 3: Exportieren einer Auswahl von Ressourcen aus einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="12e8d-116">Example 3: Export a selection of resources from a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup" -SkipAllParameterization -Resource @(
  "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Compute/virtualMachines/TestVm",
  "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Network/networkInterfaces/TestNic"
)
```

<span data-ttu-id="12e8d-117">Mit diesem Befehl werden zwei Ressourcen aus der Ressourcengruppe "TestGruppe" als Vorlage erfasst und in einer JSON-Datei im aktuellen Verzeichnis gespeichert.</span><span class="sxs-lookup"><span data-stu-id="12e8d-117">This command captures two resources from the "TestGroup" resource group as a template, and saves it to a JSON file in the current directory.</span></span> <span data-ttu-id="12e8d-118">Die generierte Vorlage enthält keine generierten Parameter.</span><span class="sxs-lookup"><span data-stu-id="12e8d-118">The generated template will not contain any generated parameters.</span></span>

## <span data-ttu-id="12e8d-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="12e8d-119">PARAMETERS</span></span>

### <span data-ttu-id="12e8d-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="12e8d-120">-ApiVersion</span></span>
<span data-ttu-id="12e8d-121">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="12e8d-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="12e8d-122">Wenn nicht angegeben, wird die neueste API-Version verwendet.</span><span class="sxs-lookup"><span data-stu-id="12e8d-122">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="12e8d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12e8d-123">-DefaultProfile</span></span>
<span data-ttu-id="12e8d-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="12e8d-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12e8d-125">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="12e8d-125">-Force</span></span>
<span data-ttu-id="12e8d-126">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="12e8d-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="12e8d-127">-IncludeComments</span><span class="sxs-lookup"><span data-stu-id="12e8d-127">-IncludeComments</span></span>
<span data-ttu-id="12e8d-128">Gibt an, dass mit diesem Vorgang die Vorlage mit Kommentaren exportiert wird.</span><span class="sxs-lookup"><span data-stu-id="12e8d-128">Indicates that this operation exports the template with comments.</span></span>

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

### <span data-ttu-id="12e8d-129">-IncludeParameterDefaultValue</span><span class="sxs-lookup"><span data-stu-id="12e8d-129">-IncludeParameterDefaultValue</span></span>
<span data-ttu-id="12e8d-130">Gibt an, dass dieser Vorgang den Vorlagenparameter mit dem Standardwert exportiert.</span><span class="sxs-lookup"><span data-stu-id="12e8d-130">Indicates that this operation exports the template parameter with the default value.</span></span>

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

### <span data-ttu-id="12e8d-131">-Path</span><span class="sxs-lookup"><span data-stu-id="12e8d-131">-Path</span></span>
<span data-ttu-id="12e8d-132">Gibt den Ausgabepfad der Vorlagendatei an.</span><span class="sxs-lookup"><span data-stu-id="12e8d-132">Specifies the output path of the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12e8d-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="12e8d-133">-Pre</span></span>
<span data-ttu-id="12e8d-134">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen verwendet, wenn automatisch bestimmt wird, welche API-Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="12e8d-134">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="12e8d-135">-Ressource</span><span class="sxs-lookup"><span data-stu-id="12e8d-135">-Resource</span></span>
<span data-ttu-id="12e8d-136">Eine Liste von resourceIds, nach der die Ergebnisse gefiltert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="12e8d-136">A list of resourceIds to filter the results by.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e8d-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12e8d-137">-ResourceGroupName</span></span>
<span data-ttu-id="12e8d-138">Gibt den Namen der zu exportierenden Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="12e8d-138">Specifies the name of the resource group to export.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12e8d-139">-SkipAllParameterization</span><span class="sxs-lookup"><span data-stu-id="12e8d-139">-SkipAllParameterization</span></span>
<span data-ttu-id="12e8d-140">Überspringen Sie alle Parameterisierungen.</span><span class="sxs-lookup"><span data-stu-id="12e8d-140">Skip all parameterization.</span></span>

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

### <span data-ttu-id="12e8d-141">-SkipResourceNameParameterization</span><span class="sxs-lookup"><span data-stu-id="12e8d-141">-SkipResourceNameParameterization</span></span>
<span data-ttu-id="12e8d-142">Überspringen sie die Parameterisierung des Ressourcennamens.</span><span class="sxs-lookup"><span data-stu-id="12e8d-142">Skip resource name parameterization.</span></span>

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

### <span data-ttu-id="12e8d-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="12e8d-143">-Confirm</span></span>
<span data-ttu-id="12e8d-144">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="12e8d-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12e8d-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12e8d-145">-WhatIf</span></span>
<span data-ttu-id="12e8d-146">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="12e8d-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12e8d-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="12e8d-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12e8d-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12e8d-148">CommonParameters</span></span>
<span data-ttu-id="12e8d-149">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12e8d-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12e8d-150">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12e8d-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12e8d-151">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="12e8d-151">INPUTS</span></span>

### <span data-ttu-id="12e8d-152">System.String</span><span class="sxs-lookup"><span data-stu-id="12e8d-152">System.String</span></span>

## <span data-ttu-id="12e8d-153">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="12e8d-153">OUTPUTS</span></span>

### <span data-ttu-id="12e8d-154">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="12e8d-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="12e8d-155">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="12e8d-155">NOTES</span></span>

## <span data-ttu-id="12e8d-156">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="12e8d-156">RELATED LINKS</span></span>

[<span data-ttu-id="12e8d-157">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="12e8d-157">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)


