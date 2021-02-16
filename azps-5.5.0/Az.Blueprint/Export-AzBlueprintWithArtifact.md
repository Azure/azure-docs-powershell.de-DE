---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/export-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
ms.openlocfilehash: 647d626a0b4d59f219020d66c3c1ec8a5218355b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145121"
---
# <span data-ttu-id="e6ea3-101">Export-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="e6ea3-101">Export-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="e6ea3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6ea3-102">SYNOPSIS</span></span>
<span data-ttu-id="e6ea3-103">Exportieren Sie die angegebene Blaupausendefinition als JSON-Datei an den angegebenen Ausgabespeicherort.</span><span class="sxs-lookup"><span data-stu-id="e6ea3-103">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

## <span data-ttu-id="e6ea3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e6ea3-104">SYNTAX</span></span>

```
Export-AzBlueprintWithArtifact -Blueprint <PSBlueprintBase> -OutputPath <String> [-Version <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6ea3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e6ea3-105">DESCRIPTION</span></span>
<span data-ttu-id="e6ea3-106">Exportieren Sie eine Blaupausendefinition mit ihren Artefakten, und speichern Sie sie auf der Festplatte.</span><span class="sxs-lookup"><span data-stu-id="e6ea3-106">Export a blueprint definition with its artifacts and save to disk.</span></span> <span data-ttu-id="e6ea3-107">Dieses Cmdlet exportiert die neueste Version (Entwurf oder Veröffentlichung) der Blaupause.</span><span class="sxs-lookup"><span data-stu-id="e6ea3-107">This cmdlet exports the latest version(draft or published) of the blueprint.</span></span>

## <span data-ttu-id="e6ea3-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e6ea3-108">EXAMPLES</span></span>

### <span data-ttu-id="e6ea3-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e6ea3-109">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Export-AzBlueprintWithArtifact -Blueprint $bp -Version 1.0 -OutputPath C:\Blueprints
```

<span data-ttu-id="e6ea3-110">Exportieren Sie eine Blaupausendefinition mit ihren Artefakten, und speichern Sie sie auf der Festplatte.</span><span class="sxs-lookup"><span data-stu-id="e6ea3-110">Export a blueprint definition with its artifacts and save to disk.</span></span>

## <span data-ttu-id="e6ea3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6ea3-111">PARAMETERS</span></span>

### <span data-ttu-id="e6ea3-112">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="e6ea3-112">-Blueprint</span></span>
<span data-ttu-id="e6ea3-113">Das zu exportierende Entwurfsdefinitionsobjekt.</span><span class="sxs-lookup"><span data-stu-id="e6ea3-113">The blueprint definition object to export.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6ea3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6ea3-114">-DefaultProfile</span></span>
<span data-ttu-id="e6ea3-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e6ea3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6ea3-116">-Force</span><span class="sxs-lookup"><span data-stu-id="e6ea3-116">-Force</span></span>
<span data-ttu-id="e6ea3-117">Wenn dies auf "true" festgelegt ist, wird bei der Ausführung keine Bestätigung verlangt.</span><span class="sxs-lookup"><span data-stu-id="e6ea3-117">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="e6ea3-118">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="e6ea3-118">-OutputPath</span></span>
<span data-ttu-id="e6ea3-119">Pfad zu einer Datei auf dem Datenträger, in die die "Blueprint"-Definition im JSON-Format exportiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e6ea3-119">Path to a file on disk where to export the Blueprint definition in JSON format.</span></span>

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

### <span data-ttu-id="e6ea3-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e6ea3-120">-PassThru</span></span>
<span data-ttu-id="e6ea3-121">Nach dem Festlegen gibt das Cmdlet ein Objekt zurück, das die exportierte Blaupausendefinition darstellt.</span><span class="sxs-lookup"><span data-stu-id="e6ea3-121">When set, the cmdlet will return an object representing the exported blueprint definition.</span></span> <span data-ttu-id="e6ea3-122">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="e6ea3-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e6ea3-123">-Version</span><span class="sxs-lookup"><span data-stu-id="e6ea3-123">-Version</span></span>
<span data-ttu-id="e6ea3-124">Veröffentlichte Entwurfsdefinitionsversion.</span><span class="sxs-lookup"><span data-stu-id="e6ea3-124">Published blueprint definition version.</span></span>

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

### <span data-ttu-id="e6ea3-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6ea3-125">-Confirm</span></span>
<span data-ttu-id="e6ea3-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e6ea3-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6ea3-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e6ea3-127">-WhatIf</span></span>
<span data-ttu-id="e6ea3-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e6ea3-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e6ea3-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e6ea3-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6ea3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6ea3-130">CommonParameters</span></span>
<span data-ttu-id="e6ea3-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6ea3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6ea3-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6ea3-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6ea3-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e6ea3-133">INPUTS</span></span>

### <span data-ttu-id="e6ea3-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="e6ea3-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="e6ea3-135">System.String</span><span class="sxs-lookup"><span data-stu-id="e6ea3-135">System.String</span></span>

## <span data-ttu-id="e6ea3-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e6ea3-136">OUTPUTS</span></span>

### <span data-ttu-id="e6ea3-137">System.String</span><span class="sxs-lookup"><span data-stu-id="e6ea3-137">System.String</span></span>

## <span data-ttu-id="e6ea3-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e6ea3-138">NOTES</span></span>

## <span data-ttu-id="e6ea3-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e6ea3-139">RELATED LINKS</span></span>
