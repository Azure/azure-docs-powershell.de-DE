---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/export-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
ms.openlocfilehash: 2c349d99e8a3529d4f1423a43bd31ab2500664c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652354"
---
# <span data-ttu-id="ee0c5-101">Export-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="ee0c5-101">Export-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="ee0c5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ee0c5-102">SYNOPSIS</span></span>
<span data-ttu-id="ee0c5-103">Exportieren Sie die angegebene Blueprint-Definition in die angegebene Ausgabeposition als JSON-Datei.</span><span class="sxs-lookup"><span data-stu-id="ee0c5-103">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

## <span data-ttu-id="ee0c5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee0c5-104">SYNTAX</span></span>

```
Export-AzBlueprintWithArtifact -Blueprint <PSBlueprintBase> -OutputPath <String> [-Version <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee0c5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ee0c5-105">DESCRIPTION</span></span>
<span data-ttu-id="ee0c5-106">Exportieren Sie eine Blueprint-Definition mit ihren Artefakten, und speichern Sie Sie auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="ee0c5-106">Export a blueprint definition with its artifacts and save to disk.</span></span> <span data-ttu-id="ee0c5-107">Mit diesem Cmdlet wird die neueste Version (Entwurf oder Veröffentlichung) des Blueprints exportiert.</span><span class="sxs-lookup"><span data-stu-id="ee0c5-107">This cmdlet exports the latest version(draft or published) of the blueprint.</span></span>

## <span data-ttu-id="ee0c5-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ee0c5-108">EXAMPLES</span></span>

### <span data-ttu-id="ee0c5-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ee0c5-109">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Export-AzBlueprintWithArtifact -Blueprint $bp -Version 1.0 -OutputPath C:\Blueprints
```

<span data-ttu-id="ee0c5-110">Exportieren Sie eine Blueprint-Definition mit ihren Artefakten, und speichern Sie Sie auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="ee0c5-110">Export a blueprint definition with its artifacts and save to disk.</span></span>

## <span data-ttu-id="ee0c5-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee0c5-111">PARAMETERS</span></span>

### <span data-ttu-id="ee0c5-112">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="ee0c5-112">-Blueprint</span></span>
<span data-ttu-id="ee0c5-113">Das zu exportierende Blueprint-Definitionsobjekt.</span><span class="sxs-lookup"><span data-stu-id="ee0c5-113">The blueprint definition object to export.</span></span>

```yaml
Type: PSBlueprintBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee0c5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee0c5-114">-DefaultProfile</span></span>
<span data-ttu-id="ee0c5-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ee0c5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee0c5-116">-Force</span><span class="sxs-lookup"><span data-stu-id="ee0c5-116">-Force</span></span>
<span data-ttu-id="ee0c5-117">Wenn die Ausführung auf "true" festgelegt ist, werden Sie nicht aufgefordert, eine Bestätigung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ee0c5-117">When set to true, execution will not ask for a confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee0c5-118">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="ee0c5-118">-OutputPath</span></span>
<span data-ttu-id="ee0c5-119">Pfad zu einer Datei auf dem Datenträger, auf der die Blueprint-Definition im JSON-Format exportiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ee0c5-119">Path to a file on disk where to export the Blueprint definition in JSON format.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee0c5-120">-Version</span><span class="sxs-lookup"><span data-stu-id="ee0c5-120">-Version</span></span>
<span data-ttu-id="ee0c5-121">Veröffentlichte Blueprint-Definitionsversion.</span><span class="sxs-lookup"><span data-stu-id="ee0c5-121">Published blueprint definition version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee0c5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee0c5-122">CommonParameters</span></span>
<span data-ttu-id="ee0c5-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee0c5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ee0c5-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee0c5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee0c5-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ee0c5-125">INPUTS</span></span>

### <span data-ttu-id="ee0c5-126">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="ee0c5-126">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="ee0c5-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ee0c5-127">System.String</span></span>

## <span data-ttu-id="ee0c5-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ee0c5-128">OUTPUTS</span></span>

### <span data-ttu-id="ee0c5-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ee0c5-129">System.String</span></span>

## <span data-ttu-id="ee0c5-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="ee0c5-130">NOTES</span></span>

## <span data-ttu-id="ee0c5-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ee0c5-131">RELATED LINKS</span></span>
