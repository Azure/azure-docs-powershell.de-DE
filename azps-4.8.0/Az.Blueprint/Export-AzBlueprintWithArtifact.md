---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/export-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
ms.openlocfilehash: 647d626a0b4d59f219020d66c3c1ec8a5218355b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008689"
---
# <span data-ttu-id="a6f29-101">Export-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="a6f29-101">Export-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="a6f29-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a6f29-102">SYNOPSIS</span></span>
<span data-ttu-id="a6f29-103">Exportieren Sie die angegebene Blueprint-Definition in die angegebene Ausgabeposition als JSON-Datei.</span><span class="sxs-lookup"><span data-stu-id="a6f29-103">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

## <span data-ttu-id="a6f29-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6f29-104">SYNTAX</span></span>

```
Export-AzBlueprintWithArtifact -Blueprint <PSBlueprintBase> -OutputPath <String> [-Version <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6f29-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a6f29-105">DESCRIPTION</span></span>
<span data-ttu-id="a6f29-106">Exportieren Sie eine Blueprint-Definition mit ihren Artefakten, und speichern Sie Sie auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="a6f29-106">Export a blueprint definition with its artifacts and save to disk.</span></span> <span data-ttu-id="a6f29-107">Mit diesem Cmdlet wird die neueste Version (Entwurf oder Veröffentlichung) des Blueprints exportiert.</span><span class="sxs-lookup"><span data-stu-id="a6f29-107">This cmdlet exports the latest version(draft or published) of the blueprint.</span></span>

## <span data-ttu-id="a6f29-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a6f29-108">EXAMPLES</span></span>

### <span data-ttu-id="a6f29-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a6f29-109">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Export-AzBlueprintWithArtifact -Blueprint $bp -Version 1.0 -OutputPath C:\Blueprints
```

<span data-ttu-id="a6f29-110">Exportieren Sie eine Blueprint-Definition mit ihren Artefakten, und speichern Sie Sie auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="a6f29-110">Export a blueprint definition with its artifacts and save to disk.</span></span>

## <span data-ttu-id="a6f29-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6f29-111">PARAMETERS</span></span>

### <span data-ttu-id="a6f29-112">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="a6f29-112">-Blueprint</span></span>
<span data-ttu-id="a6f29-113">Das zu exportierende Blueprint-Definitionsobjekt.</span><span class="sxs-lookup"><span data-stu-id="a6f29-113">The blueprint definition object to export.</span></span>

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

### <span data-ttu-id="a6f29-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6f29-114">-DefaultProfile</span></span>
<span data-ttu-id="a6f29-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a6f29-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6f29-116">-Force</span><span class="sxs-lookup"><span data-stu-id="a6f29-116">-Force</span></span>
<span data-ttu-id="a6f29-117">Wenn die Ausführung auf "true" festgelegt ist, werden Sie nicht aufgefordert, eine Bestätigung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a6f29-117">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="a6f29-118">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="a6f29-118">-OutputPath</span></span>
<span data-ttu-id="a6f29-119">Pfad zu einer Datei auf dem Datenträger, auf der die Blueprint-Definition im JSON-Format exportiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a6f29-119">Path to a file on disk where to export the Blueprint definition in JSON format.</span></span>

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

### <span data-ttu-id="a6f29-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6f29-120">-PassThru</span></span>
<span data-ttu-id="a6f29-121">Wenn festgesetzt, gibt das Cmdlet ein Objekt zurück, das die exportierte Blueprint-Definition darstellt.</span><span class="sxs-lookup"><span data-stu-id="a6f29-121">When set, the cmdlet will return an object representing the exported blueprint definition.</span></span> <span data-ttu-id="a6f29-122">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="a6f29-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a6f29-123">-Version</span><span class="sxs-lookup"><span data-stu-id="a6f29-123">-Version</span></span>
<span data-ttu-id="a6f29-124">Veröffentlichte Blueprint-Definitionsversion.</span><span class="sxs-lookup"><span data-stu-id="a6f29-124">Published blueprint definition version.</span></span>

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

### <span data-ttu-id="a6f29-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a6f29-125">-Confirm</span></span>
<span data-ttu-id="a6f29-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a6f29-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6f29-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6f29-127">-WhatIf</span></span>
<span data-ttu-id="a6f29-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a6f29-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a6f29-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a6f29-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6f29-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6f29-130">CommonParameters</span></span>
<span data-ttu-id="a6f29-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6f29-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6f29-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6f29-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6f29-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a6f29-133">INPUTS</span></span>

### <span data-ttu-id="a6f29-134">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="a6f29-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="a6f29-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a6f29-135">System.String</span></span>

## <span data-ttu-id="a6f29-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a6f29-136">OUTPUTS</span></span>

### <span data-ttu-id="a6f29-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a6f29-137">System.String</span></span>

## <span data-ttu-id="a6f29-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="a6f29-138">NOTES</span></span>

## <span data-ttu-id="a6f29-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a6f29-139">RELATED LINKS</span></span>
