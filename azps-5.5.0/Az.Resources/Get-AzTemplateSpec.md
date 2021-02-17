---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
ms.openlocfilehash: be3a16707303016e22be8052721efcb35c608b3e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160009"
---
# <span data-ttu-id="8176c-101">Get-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="8176c-101">Get-AzTemplateSpec</span></span>

## <span data-ttu-id="8176c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8176c-102">SYNOPSIS</span></span>
<span data-ttu-id="8176c-103">Ruft Vorlagenspezifikationen ab oder listet vorlagenspezifikationen auf</span><span class="sxs-lookup"><span data-stu-id="8176c-103">Gets or lists Template Specs</span></span>

## <span data-ttu-id="8176c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8176c-104">SYNTAX</span></span>

### <span data-ttu-id="8176c-105">ListTemplateSpecsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8176c-105">ListTemplateSpecsParameterSet (Default)</span></span>
```
Get-AzTemplateSpec [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8176c-106">GetTemplateSpecByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8176c-106">GetTemplateSpecByNameParameterSet</span></span>
```
Get-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8176c-107">GetTemplateSpecByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8176c-107">GetTemplateSpecByIdParameterSet</span></span>
```
Get-AzTemplateSpec [[-Version] <String>] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8176c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8176c-108">DESCRIPTION</span></span>
<span data-ttu-id="8176c-109">Dieses Cmdlet kann verwendet werden, um Vorlagenspezifikationen in einer Abonnement-/Ressourcengruppe auflisten oder eine bestimmte Vorlagenspezifikation nach Name oder ID zu erhalten. Beim Abrufen einer bestimmten Vorlagenspezifikation nach Name/ID kann optional eine bestimmte Version abgerufen werden, indem über den Parameter **"-Version"** ein Versionsname angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8176c-109">This cmdlet can be used to list Template Specs in a subscription/resource group or get a specific Template Spec by name or id. When getting a specific Template Spec by name/id a specific version can optionally be retrieved by specifying a version name through the **-Version** parameter.</span></span> <span data-ttu-id="8176c-110">Wenn **"-Version"** verwendet wird, sind in \* nur die jeweiligen Versionsdetails *vorhanden. Versionen* des zurückgegebenen Vorlagenspezifikationenobjekts.</span><span class="sxs-lookup"><span data-stu-id="8176c-110">When **-Version** is used, only the specific version details will be present within \**.Versions* on the returned Template Spec object.</span></span> <span data-ttu-id="8176c-111">Wenn beim Abrufen einer Vorlagenspezifikation nach Name/ID keine bestimmte Version angegeben wird, sind alle Versionen im \**vorhanden. Eigenschaft* "Versions" des zurückgegebenen Objekts.</span><span class="sxs-lookup"><span data-stu-id="8176c-111">If no specific version is specified when retrieving a Template Spec by name/id, all versions will be present within the  \**.Versions* property of the returned object.</span></span>

<span data-ttu-id="8176c-112">**Hinweis:** Wenn Sie alle Vorlagenspezifikationen in einem Abonnement oder einer Ressourcengruppe auflisten, wird für jede zurückgegebene Vorlagenspezifikation *". Die Eigenschaft "Versionen"* ist *null.*</span><span class="sxs-lookup"><span data-stu-id="8176c-112">**Note**: When listing all Template Specs within a subscription or resource group, each returned Template Spec's *".Versions"* property will be *null*.</span></span> <span data-ttu-id="8176c-113">Versionsinformationen sind nur enthalten, wenn die Parameter "-Name" oder "-ResourceId" bereitgestellt werden (z. B.: Sie fordern eine bestimmte Vorlagenspezifikation/Version an).</span><span class="sxs-lookup"><span data-stu-id="8176c-113">Version information is only included when -Name or -ResourceId parameters are provided (eg: you are requesting a specific template spec/version).</span></span>

## <span data-ttu-id="8176c-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8176c-114">EXAMPLES</span></span>

### <span data-ttu-id="8176c-115">Beispiel 1: Listenvorlagenspezifikationen im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="8176c-115">Example 1: List Template Specs in current subscription</span></span>
```powershell
PS C:\> Get-AzTemplateSpec
```

<span data-ttu-id="8176c-116">Listet alle Vorlagenspezifikationen im aktuellen Abonnement auf.</span><span class="sxs-lookup"><span data-stu-id="8176c-116">Lists all Template Specs in the current subscription.</span></span>

### <span data-ttu-id="8176c-117">Beispiel 2: Listenvorlagenspezifikationen in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="8176c-117">Example 2: List Template Specs in a resource group</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG'
```

<span data-ttu-id="8176c-118">Listet alle Vorlagenspezifikationen in der Ressourcengruppe "myRG" des aktuellen Abonnements auf.</span><span class="sxs-lookup"><span data-stu-id="8176c-118">Lists all Template Specs in the resource group 'myRG' of the current subscription.</span></span>

### <span data-ttu-id="8176c-119">Beispiel 3: Vorlagenspezifikation (mit allen Versionen) nach Name</span><span class="sxs-lookup"><span data-stu-id="8176c-119">Example 3: Get Template Spec (with all versions) by name</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

<span data-ttu-id="8176c-120">Ruft Informationen zum Vorlagenspezifikationentyp "MyTemplateSpec" in der Ressourcengruppe "myRG" ab.</span><span class="sxs-lookup"><span data-stu-id="8176c-120">Gets information about the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

<span data-ttu-id="8176c-121">**Hinweis:** Alle Versionen der Vorlagenspezifikationen sind im "*enthalten. Versions*"-Eigenschaft des Rückgabeobjekts.</span><span class="sxs-lookup"><span data-stu-id="8176c-121">**Note**: All of the Template Spec's versions will be present within the "*.Versions*" property of the return object.</span></span>

### <span data-ttu-id="8176c-122">Beispiel 4: Vorlagenspezifikation (bestimmte Version) nach Name</span><span class="sxs-lookup"><span data-stu-id="8176c-122">Example 4: Get Template Spec (specific version) by name</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="8176c-123">Ruft Informationen zur Version 'v1.0' des Vorlagenspezifikationen namens 'MyTemplateSpec' in der Ressourcengruppe 'myRG' ab.</span><span class="sxs-lookup"><span data-stu-id="8176c-123">Gets information about version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

<span data-ttu-id="8176c-124">**Hinweis:** Das *". Die Eigenschaft "Versionen"* des zurückgegebenen Objekts enthält nur die angeforderte Version.</span><span class="sxs-lookup"><span data-stu-id="8176c-124">**Note**: The *".Versions"* property of the returned object will contain only the specific version requested.</span></span>

### <span data-ttu-id="8176c-125">Beispiel 5: Vorlagenspezifikation (mit allen Versionen) nach Ressourcen-ID erhalten</span><span class="sxs-lookup"><span data-stu-id="8176c-125">Example 5: Get Template Spec (with all versions) by resource id</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec'
```

<span data-ttu-id="8176c-126">Ruft Informationen zur Vorlagenspezifikation mit dem Namen "MyTemplateSpec" in der Ressourcengruppe "myRG" von \{ "subId" für Abonnements \} ab.</span><span class="sxs-lookup"><span data-stu-id="8176c-126">Gets information about the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

<span data-ttu-id="8176c-127">**Hinweis:** Alle Versionen der Vorlagenspezifikationen sind im "*enthalten. Versions*"-Eigenschaft des Rückgabeobjekts.</span><span class="sxs-lookup"><span data-stu-id="8176c-127">**Note**: All of the Template Spec's versions will be present within the "*.Versions*" property of the return object.</span></span>

### <span data-ttu-id="8176c-128">Beispiel 6: Vorlagenspezifikation (bestimmte Version) nach Ressourcen-ID erhalten</span><span class="sxs-lookup"><span data-stu-id="8176c-128">Example 6: Get Template Spec (specific version) by resource id</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="8176c-129">Ruft Informationen zur Version 'v1.0' des Vorlagenspezifikationen namens 'MyTemplateSpec' in der Ressourcengruppe 'myRG' von subscription \{ subId \} ab.</span><span class="sxs-lookup"><span data-stu-id="8176c-129">Gets information about version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

<span data-ttu-id="8176c-130">**Hinweis:** Das *". Die Eigenschaft "Versionen"* des zurückgegebenen Objekts enthält nur die angeforderte Version.</span><span class="sxs-lookup"><span data-stu-id="8176c-130">**Note**: The *".Versions"* property of the returned object will contain only the specific version requested.</span></span>

## <span data-ttu-id="8176c-131">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8176c-131">PARAMETERS</span></span>

### <span data-ttu-id="8176c-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8176c-132">-DefaultProfile</span></span>
<span data-ttu-id="8176c-133">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8176c-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8176c-134">-Name</span><span class="sxs-lookup"><span data-stu-id="8176c-134">-Name</span></span>
<span data-ttu-id="8176c-135">Der Name der Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="8176c-135">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8176c-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8176c-136">-ResourceGroupName</span></span>
<span data-ttu-id="8176c-137">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8176c-137">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ListTemplateSpecsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8176c-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8176c-138">-ResourceId</span></span>
<span data-ttu-id="8176c-139">Die vollqualifizierte Ressourcen-ID der Vorlagenspezifikation. Beispiel: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="8176c-139">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8176c-140">-Version</span><span class="sxs-lookup"><span data-stu-id="8176c-140">-Version</span></span>
<span data-ttu-id="8176c-141">Die Version der Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="8176c-141">The version of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet, GetTemplateSpecByIdParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8176c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8176c-142">CommonParameters</span></span>
<span data-ttu-id="8176c-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8176c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8176c-144">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8176c-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8176c-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8176c-145">INPUTS</span></span>

### <span data-ttu-id="8176c-146">System.String</span><span class="sxs-lookup"><span data-stu-id="8176c-146">System.String</span></span>

## <span data-ttu-id="8176c-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8176c-147">OUTPUTS</span></span>

### <span data-ttu-id="8176c-148">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="8176c-148">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="8176c-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8176c-149">NOTES</span></span>

## <span data-ttu-id="8176c-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8176c-150">RELATED LINKS</span></span>
