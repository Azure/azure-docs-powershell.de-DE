---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 63BBDF98-75FC-4A44-9FD0-95AD21ED93A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/export-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
ms.openlocfilehash: 74605a57ab3f2c0898bf3eeb80950f86d4f65d94
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008264"
---
# <span data-ttu-id="9c94f-101">Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9c94f-101">Export-AzResourceGroup</span></span>

## <span data-ttu-id="9c94f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9c94f-102">SYNOPSIS</span></span>
<span data-ttu-id="9c94f-103">Zeichnet eine Ressourcengruppe als Vorlage auf und speichert Sie in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="9c94f-103">Captures a resource group as a template and saves it to a file.</span></span>

## <span data-ttu-id="9c94f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c94f-104">SYNTAX</span></span>

```
Export-AzResourceGroup -ResourceGroupName <String> [-Path <String>] [-IncludeParameterDefaultValue]
 [-IncludeComments] [-SkipResourceNameParameterization] [-SkipAllParameterization] [-Resource <String[]>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9c94f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9c94f-105">DESCRIPTION</span></span>
<span data-ttu-id="9c94f-106">Das Cmdlet **Export-AzResourceGroup** erfasst die angegebene Ressourcengruppe als Vorlage und speichert Sie in einer JSON-Datei. Dies kann in Szenarien hilfreich sein, in denen Sie bereits einige Ressourcen in ihrer Ressourcengruppe erstellt haben und dann die Vorteile der Verwendung von Vorlagen gesicherten Bereitstellungen nutzen möchten.</span><span class="sxs-lookup"><span data-stu-id="9c94f-106">The **Export-AzResourceGroup** cmdlet captures the specified resource group as a template and saves it to a JSON file.This can be useful in scenarios where you have already created some resources in your resource group, and then want to leverage the benefits of using template backed deployments.</span></span>
<span data-ttu-id="9c94f-107">Dieses Cmdlet bietet Ihnen einen einfachen Anfang, indem Sie die Vorlage für Ihre vorhandenen Ressourcen in der Ressourcengruppe generieren.</span><span class="sxs-lookup"><span data-stu-id="9c94f-107">This cmdlet gives you an easy start by generating the template for your existing resources in the resource group.</span></span>
<span data-ttu-id="9c94f-108">In einigen Fällen kann dieses Cmdlet einige Teile der Vorlage nicht generieren.</span><span class="sxs-lookup"><span data-stu-id="9c94f-108">There might be some cases where this cmdlet fails to generate some parts of the template.</span></span>
<span data-ttu-id="9c94f-109">Warnmeldungen informieren Sie über die fehlerhaften Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="9c94f-109">Warning messages will inform you of the resources that failed.</span></span>
<span data-ttu-id="9c94f-110">Die Vorlage wird weiterhin für die Teile generiert, die erfolgreich waren.</span><span class="sxs-lookup"><span data-stu-id="9c94f-110">The template will still be generated for the parts that were successful.</span></span>

## <span data-ttu-id="9c94f-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9c94f-111">EXAMPLES</span></span>

### <span data-ttu-id="9c94f-112">Beispiel 1: Exportieren einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="9c94f-112">Example 1: Export a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup"
```

<span data-ttu-id="9c94f-113">Dieser Befehl zeichnet die Ressourcengruppe "testgroup" als Vorlage auf und speichert Sie in einer JSON-Datei im aktuellen Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="9c94f-113">This command captures the resource group named TestGroup as a template, and saves it to a JSON file in the current directory.</span></span>

### <span data-ttu-id="9c94f-114">Beispiel 2: Exportieren einer einzelnen Ressource aus einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="9c94f-114">Example 2: Export a single resource from a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup" -Resource "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Compute/virtualMachines/TestVirtualMachine"
```

<span data-ttu-id="9c94f-115">Dieser Befehl zeichnet die Ressource des virtuellen Computers mit dem Namen "TestVirtualMachine" aus der Ressourcengruppe "testgroup" als Vorlage auf und speichert Sie in einer JSON-Datei im aktuellen Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="9c94f-115">This command captures the Virtual Machine resource named "TestVirtualMachine" from the "TestGroup" resource group as a template, and saves it to a JSON file in the current directory.</span></span>

### <span data-ttu-id="9c94f-116">Beispiel 3: Exportieren einer Auswahl von Ressourcen aus einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="9c94f-116">Example 3: Export a selection of resources from a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup" -SkipAllParameterization -Resource @(
  "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Compute/virtualMachines/TestVm",
  "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Network/networkInterfaces/TestNic"
)
```

<span data-ttu-id="9c94f-117">Dieser Befehl zeichnet zwei Ressourcen aus der Ressourcengruppe "testgroup" als Vorlage auf und speichert Sie in einer JSON-Datei im aktuellen Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="9c94f-117">This command captures two resources from the "TestGroup" resource group as a template, and saves it to a JSON file in the current directory.</span></span> <span data-ttu-id="9c94f-118">Die generierte Vorlage enthält keine generierten Parameter.</span><span class="sxs-lookup"><span data-stu-id="9c94f-118">The generated template will not contain any generated parameters.</span></span>

## <span data-ttu-id="9c94f-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c94f-119">PARAMETERS</span></span>

### <span data-ttu-id="9c94f-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9c94f-120">-ApiVersion</span></span>
<span data-ttu-id="9c94f-121">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="9c94f-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="9c94f-122">Wenn keine Angabe erfolgt, wird die neueste API-Version verwendet.</span><span class="sxs-lookup"><span data-stu-id="9c94f-122">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="9c94f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c94f-123">-DefaultProfile</span></span>
<span data-ttu-id="9c94f-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9c94f-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9c94f-125">-Force</span><span class="sxs-lookup"><span data-stu-id="9c94f-125">-Force</span></span>
<span data-ttu-id="9c94f-126">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="9c94f-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9c94f-127">-IncludeComments</span><span class="sxs-lookup"><span data-stu-id="9c94f-127">-IncludeComments</span></span>
<span data-ttu-id="9c94f-128">Gibt an, dass diese Operation die Vorlage mit Kommentaren exportiert.</span><span class="sxs-lookup"><span data-stu-id="9c94f-128">Indicates that this operation exports the template with comments.</span></span>

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

### <span data-ttu-id="9c94f-129">-IncludeParameterDefaultValue</span><span class="sxs-lookup"><span data-stu-id="9c94f-129">-IncludeParameterDefaultValue</span></span>
<span data-ttu-id="9c94f-130">Gibt an, dass dieser Vorgang den Vorlagenparameter mit dem Standardwert exportiert.</span><span class="sxs-lookup"><span data-stu-id="9c94f-130">Indicates that this operation exports the template parameter with the default value.</span></span>

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

### <span data-ttu-id="9c94f-131">-Path</span><span class="sxs-lookup"><span data-stu-id="9c94f-131">-Path</span></span>
<span data-ttu-id="9c94f-132">Gibt den Ausgabepfad der Vorlagendatei an.</span><span class="sxs-lookup"><span data-stu-id="9c94f-132">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="9c94f-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="9c94f-133">-Pre</span></span>
<span data-ttu-id="9c94f-134">Gibt an, dass dieses Cmdlet Vorabversion-API-Versionen verwendet, wenn automatisch ermittelt wird, welche API-Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9c94f-134">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="9c94f-135">-Resource</span><span class="sxs-lookup"><span data-stu-id="9c94f-135">-Resource</span></span>
<span data-ttu-id="9c94f-136">Eine Liste der resourceIds, nach denen die Ergebnisse gefiltert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9c94f-136">A list of resourceIds to filter the results by.</span></span>

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

### <span data-ttu-id="9c94f-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c94f-137">-ResourceGroupName</span></span>
<span data-ttu-id="9c94f-138">Gibt den Namen der zu exportierenden Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="9c94f-138">Specifies the name of the resource group to export.</span></span>

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

### <span data-ttu-id="9c94f-139">-SkipAllParameterization</span><span class="sxs-lookup"><span data-stu-id="9c94f-139">-SkipAllParameterization</span></span>
<span data-ttu-id="9c94f-140">Alle Parametrisierung überspringen.</span><span class="sxs-lookup"><span data-stu-id="9c94f-140">Skip all parameterization.</span></span>

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

### <span data-ttu-id="9c94f-141">-SkipResourceNameParameterization</span><span class="sxs-lookup"><span data-stu-id="9c94f-141">-SkipResourceNameParameterization</span></span>
<span data-ttu-id="9c94f-142">Ressourcennamen-Parametrisierung überspringen</span><span class="sxs-lookup"><span data-stu-id="9c94f-142">Skip resource name parameterization.</span></span>

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

### <span data-ttu-id="9c94f-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9c94f-143">-Confirm</span></span>
<span data-ttu-id="9c94f-144">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9c94f-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c94f-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c94f-145">-WhatIf</span></span>
<span data-ttu-id="9c94f-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9c94f-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c94f-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9c94f-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c94f-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c94f-148">CommonParameters</span></span>
<span data-ttu-id="9c94f-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c94f-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c94f-150">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c94f-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c94f-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9c94f-151">INPUTS</span></span>

### <span data-ttu-id="9c94f-152">System. String</span><span class="sxs-lookup"><span data-stu-id="9c94f-152">System.String</span></span>

## <span data-ttu-id="9c94f-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9c94f-153">OUTPUTS</span></span>

### <span data-ttu-id="9c94f-154">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="9c94f-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="9c94f-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="9c94f-155">NOTES</span></span>

## <span data-ttu-id="9c94f-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9c94f-156">RELATED LINKS</span></span>

[<span data-ttu-id="9c94f-157">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9c94f-157">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)


