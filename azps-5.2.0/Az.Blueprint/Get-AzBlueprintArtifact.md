---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
ms.openlocfilehash: 725dca861c28f0194f800c80bd94d7e17efe15a6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368485"
---
# <span data-ttu-id="0afeb-101">Get-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="0afeb-101">Get-AzBlueprintArtifact</span></span>

## <span data-ttu-id="0afeb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0afeb-102">SYNOPSIS</span></span>
<span data-ttu-id="0afeb-103">Rufen Sie Artefakte aus einer Blaupausendefinition ab.</span><span class="sxs-lookup"><span data-stu-id="0afeb-103">Retrieve artifacts from a blueprint definition.</span></span>

## <span data-ttu-id="0afeb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0afeb-104">SYNTAX</span></span>

```
Get-AzBlueprintArtifact [-Name <String>] -Blueprint <PSBlueprintBase> [-BlueprintVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0afeb-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0afeb-105">DESCRIPTION</span></span>
<span data-ttu-id="0afeb-106">Rufen Sie Artefakte aus einer Blaupausendefinition ab.</span><span class="sxs-lookup"><span data-stu-id="0afeb-106">Retrieve artifacts from a blueprint definition.</span></span> <span data-ttu-id="0afeb-107">Wenn keine Entwurfsdefinitionsversion angegeben ist, wird die Entwurfsversion abgerufen.</span><span class="sxs-lookup"><span data-stu-id="0afeb-107">If a blueprint definition version is not specified, the draft version is retrieved.</span></span> <span data-ttu-id="0afeb-108">Falls keine Entwurfsversion verfügbar ist, wird die neueste veröffentlichte Entwurfsdefinition zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0afeb-108">In the case where there is no draft version, the latest published blueprint definition is returned.</span></span>

## <span data-ttu-id="0afeb-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0afeb-109">EXAMPLES</span></span>

### <span data-ttu-id="0afeb-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0afeb-110">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Get-AzBlueprintArtifact -Blueprint $bp 

DisplayName        : Audit use of classic virtual machines
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/1d84d5fb-01f6-4d12-ba4f-4a26081d403d
Parameters         : {[effect, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      : SimpleBlueprintRG
Id                 : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/artifacts/3ab44511-0228-4275-9641-7e93e6f34178
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : 3ab44511-0228-4275-9641-7e93e6f34178

DisplayName        : Enforce tag and its value
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/1e30110a-5ceb-460c-a204-c1c3969c6d62
Parameters         : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue,
                     Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      :
Id                 : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/artifacts/0e1593da-47d5-4b75-800c-9a797dd23192
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : 0e1593da-47d5-4b75-800c-9a797dd23192
```

<span data-ttu-id="0afeb-111">Rufen Sie Artefakte aus einer Blaupausendefinition ab.</span><span class="sxs-lookup"><span data-stu-id="0afeb-111">Retrieve artifacts from a blueprint definition..</span></span> 

## <span data-ttu-id="0afeb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0afeb-112">PARAMETERS</span></span>

### <span data-ttu-id="0afeb-113">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="0afeb-113">-Blueprint</span></span>
<span data-ttu-id="0afeb-114">"Blueprint"-Objekt.</span><span class="sxs-lookup"><span data-stu-id="0afeb-114">Blueprint object.</span></span>

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

### <span data-ttu-id="0afeb-115">-BlueprintVersion</span><span class="sxs-lookup"><span data-stu-id="0afeb-115">-BlueprintVersion</span></span>
<span data-ttu-id="0afeb-116">Version der Blaupause, um die Artefakte zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0afeb-116">Version of the blueprint to get the artifacts from.</span></span>

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

### <span data-ttu-id="0afeb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0afeb-117">-DefaultProfile</span></span>
<span data-ttu-id="0afeb-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0afeb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0afeb-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0afeb-119">-Name</span></span>
<span data-ttu-id="0afeb-120">Name des Artefakts</span><span class="sxs-lookup"><span data-stu-id="0afeb-120">Name of the artifact</span></span>

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

### <span data-ttu-id="0afeb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0afeb-121">CommonParameters</span></span>
<span data-ttu-id="0afeb-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0afeb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0afeb-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0afeb-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0afeb-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0afeb-124">INPUTS</span></span>

### <span data-ttu-id="0afeb-125">System.String</span><span class="sxs-lookup"><span data-stu-id="0afeb-125">System.String</span></span>

### <span data-ttu-id="0afeb-126">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="0afeb-126">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="0afeb-127">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="0afeb-127">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="0afeb-128">System.Collections.Generic.List'1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="0afeb-128">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="0afeb-129">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="0afeb-129">System.Collections.Hashtable</span></span>

### <span data-ttu-id="0afeb-130">System.String[]</span><span class="sxs-lookup"><span data-stu-id="0afeb-130">System.String[]</span></span>

## <span data-ttu-id="0afeb-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0afeb-131">OUTPUTS</span></span>

### <span data-ttu-id="0afeb-132">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="0afeb-132">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment</span></span>

## <span data-ttu-id="0afeb-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0afeb-133">NOTES</span></span>

## <span data-ttu-id="0afeb-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0afeb-134">RELATED LINKS</span></span>
