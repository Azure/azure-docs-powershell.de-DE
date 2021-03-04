---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/export-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
ms.openlocfilehash: 1e4184b847b260d84d8b3609ade5403367046dd4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950328"
---
# <span data-ttu-id="bf379-101">Export-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="bf379-101">Export-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="bf379-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf379-102">SYNOPSIS</span></span>
<span data-ttu-id="bf379-103">Exportieren Sie die angegebene Blaupausendefinition als JSON-Datei an den angegebenen Ausgabespeicherort.</span><span class="sxs-lookup"><span data-stu-id="bf379-103">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

## <span data-ttu-id="bf379-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bf379-104">SYNTAX</span></span>

```
Export-AzBlueprintWithArtifact -Blueprint <PSBlueprintBase> -OutputPath <String> [-Version <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf379-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bf379-105">DESCRIPTION</span></span>
<span data-ttu-id="bf379-106">Exportieren Sie eine Blaupausendefinition mit ihren Artefakten, und speichern Sie sie auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="bf379-106">Export a blueprint definition with its artifacts and save to disk.</span></span> <span data-ttu-id="bf379-107">Dieses Cmdlet exportiert die neueste Version (Entwurf oder Veröffentlicht) der Blaupause.</span><span class="sxs-lookup"><span data-stu-id="bf379-107">This cmdlet exports the latest version(draft or published) of the blueprint.</span></span>

## <span data-ttu-id="bf379-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bf379-108">EXAMPLES</span></span>

### <span data-ttu-id="bf379-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bf379-109">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Export-AzBlueprintWithArtifact -Blueprint $bp -Version 1.0 -OutputPath C:\Blueprints
```

<span data-ttu-id="bf379-110">Exportieren Sie eine Blaupausendefinition mit ihren Artefakten, und speichern Sie sie auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="bf379-110">Export a blueprint definition with its artifacts and save to disk.</span></span>

## <span data-ttu-id="bf379-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="bf379-111">PARAMETERS</span></span>

### <span data-ttu-id="bf379-112">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="bf379-112">-Blueprint</span></span>
<span data-ttu-id="bf379-113">Das zu exportierende Blaupausendefinitionsobjekt.</span><span class="sxs-lookup"><span data-stu-id="bf379-113">The blueprint definition object to export.</span></span>

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

### <span data-ttu-id="bf379-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf379-114">-DefaultProfile</span></span>
<span data-ttu-id="bf379-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bf379-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf379-116">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="bf379-116">-Force</span></span>
<span data-ttu-id="bf379-117">Wenn die Ausführung auf "true" festgelegt ist, wird keine Bestätigung verlangt.</span><span class="sxs-lookup"><span data-stu-id="bf379-117">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="bf379-118">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="bf379-118">-OutputPath</span></span>
<span data-ttu-id="bf379-119">Pfad zu einer Datei auf dem Datenträger, in der die Blaupausendefinition im JSON-Format exportiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="bf379-119">Path to a file on disk where to export the Blueprint definition in JSON format.</span></span>

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

### <span data-ttu-id="bf379-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bf379-120">-PassThru</span></span>
<span data-ttu-id="bf379-121">Wenn festgelegt, gibt das Cmdlet ein -Objekt zurück, das die exportierte Blaupausendefinition darstellt.</span><span class="sxs-lookup"><span data-stu-id="bf379-121">When set, the cmdlet will return an object representing the exported blueprint definition.</span></span> <span data-ttu-id="bf379-122">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="bf379-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bf379-123">-Version</span><span class="sxs-lookup"><span data-stu-id="bf379-123">-Version</span></span>
<span data-ttu-id="bf379-124">Veröffentlichte Blaupausendefinitionsversion.</span><span class="sxs-lookup"><span data-stu-id="bf379-124">Published blueprint definition version.</span></span>

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

### <span data-ttu-id="bf379-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bf379-125">-Confirm</span></span>
<span data-ttu-id="bf379-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bf379-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf379-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf379-127">-WhatIf</span></span>
<span data-ttu-id="bf379-128">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bf379-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bf379-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bf379-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf379-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf379-130">CommonParameters</span></span>
<span data-ttu-id="bf379-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf379-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf379-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bf379-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf379-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bf379-133">INPUTS</span></span>

### <span data-ttu-id="bf379-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="bf379-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="bf379-135">System.String</span><span class="sxs-lookup"><span data-stu-id="bf379-135">System.String</span></span>

## <span data-ttu-id="bf379-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bf379-136">OUTPUTS</span></span>

### <span data-ttu-id="bf379-137">System.String</span><span class="sxs-lookup"><span data-stu-id="bf379-137">System.String</span></span>

## <span data-ttu-id="bf379-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="bf379-138">NOTES</span></span>

## <span data-ttu-id="bf379-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="bf379-139">RELATED LINKS</span></span>
