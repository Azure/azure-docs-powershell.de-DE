---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/get-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
ms.openlocfilehash: d64f77bc8662ec4d03619333beaa124eaf90e309
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922467"
---
# <span data-ttu-id="bc626-101">Get-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="bc626-101">Get-AzBlueprintArtifact</span></span>

## <span data-ttu-id="bc626-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc626-102">SYNOPSIS</span></span>
<span data-ttu-id="bc626-103">Rufen Sie Artefakte aus einer Blaupausendefinition ab.</span><span class="sxs-lookup"><span data-stu-id="bc626-103">Retrieve artifacts from a blueprint definition.</span></span>

## <span data-ttu-id="bc626-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bc626-104">SYNTAX</span></span>

```
Get-AzBlueprintArtifact [-Name <String>] -Blueprint <PSBlueprintBase> [-BlueprintVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc626-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bc626-105">DESCRIPTION</span></span>
<span data-ttu-id="bc626-106">Rufen Sie Artefakte aus einer Blaupausendefinition ab.</span><span class="sxs-lookup"><span data-stu-id="bc626-106">Retrieve artifacts from a blueprint definition.</span></span> <span data-ttu-id="bc626-107">Wenn keine Blaupausendefinitionsversion angegeben ist, wird die Entwurfsversion abgerufen.</span><span class="sxs-lookup"><span data-stu-id="bc626-107">If a blueprint definition version is not specified, the draft version is retrieved.</span></span> <span data-ttu-id="bc626-108">Ist keine Entwurfsversion verfügbar, wird die neueste veröffentlichte Blaupausendefinition zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bc626-108">In the case where there is no draft version, the latest published blueprint definition is returned.</span></span>

## <span data-ttu-id="bc626-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bc626-109">EXAMPLES</span></span>

### <span data-ttu-id="bc626-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bc626-110">Example 1</span></span>
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

<span data-ttu-id="bc626-111">Rufen Sie Artefakte aus einer Blaupausendefinition ab.</span><span class="sxs-lookup"><span data-stu-id="bc626-111">Retrieve artifacts from a blueprint definition..</span></span> 

## <span data-ttu-id="bc626-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="bc626-112">PARAMETERS</span></span>

### <span data-ttu-id="bc626-113">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="bc626-113">-Blueprint</span></span>
<span data-ttu-id="bc626-114">Blueprint-Objekt.</span><span class="sxs-lookup"><span data-stu-id="bc626-114">Blueprint object.</span></span>

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

### <span data-ttu-id="bc626-115">-BlueprintVersion</span><span class="sxs-lookup"><span data-stu-id="bc626-115">-BlueprintVersion</span></span>
<span data-ttu-id="bc626-116">Version der Blaupause, aus der die Artefakte erhalten werden.</span><span class="sxs-lookup"><span data-stu-id="bc626-116">Version of the blueprint to get the artifacts from.</span></span>

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

### <span data-ttu-id="bc626-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc626-117">-DefaultProfile</span></span>
<span data-ttu-id="bc626-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bc626-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc626-119">-Name</span><span class="sxs-lookup"><span data-stu-id="bc626-119">-Name</span></span>
<span data-ttu-id="bc626-120">Name des Artefakts</span><span class="sxs-lookup"><span data-stu-id="bc626-120">Name of the artifact</span></span>

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

### <span data-ttu-id="bc626-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc626-121">CommonParameters</span></span>
<span data-ttu-id="bc626-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc626-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc626-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc626-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc626-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bc626-124">INPUTS</span></span>

### <span data-ttu-id="bc626-125">System.String</span><span class="sxs-lookup"><span data-stu-id="bc626-125">System.String</span></span>

### <span data-ttu-id="bc626-126">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="bc626-126">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="bc626-127">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="bc626-127">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="bc626-128">System.Collections.Generic.List'1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="bc626-128">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="bc626-129">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="bc626-129">System.Collections.Hashtable</span></span>

### <span data-ttu-id="bc626-130">System.String[]</span><span class="sxs-lookup"><span data-stu-id="bc626-130">System.String[]</span></span>

## <span data-ttu-id="bc626-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bc626-131">OUTPUTS</span></span>

### <span data-ttu-id="bc626-132">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="bc626-132">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment</span></span>

## <span data-ttu-id="bc626-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="bc626-133">NOTES</span></span>

## <span data-ttu-id="bc626-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="bc626-134">RELATED LINKS</span></span>
