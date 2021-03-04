---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
ms.openlocfilehash: 0b2018eecc081f2fcee5da63ed17cc2e01486777
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922672"
---
# <span data-ttu-id="2495a-101">Get-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="2495a-101">Get-AzTemplateSpec</span></span>

## <span data-ttu-id="2495a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2495a-102">SYNOPSIS</span></span>
<span data-ttu-id="2495a-103">Ruft Vorlagenspezifikationen ab oder listet sie auf.</span><span class="sxs-lookup"><span data-stu-id="2495a-103">Gets or lists Template Specs</span></span>

## <span data-ttu-id="2495a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2495a-104">SYNTAX</span></span>

### <span data-ttu-id="2495a-105">ListTemplateSpecsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2495a-105">ListTemplateSpecsParameterSet (Default)</span></span>
```
Get-AzTemplateSpec [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2495a-106">GetTemplateSpecByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2495a-106">GetTemplateSpecByNameParameterSet</span></span>
```
Get-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2495a-107">GetTemplateSpecByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2495a-107">GetTemplateSpecByIdParameterSet</span></span>
```
Get-AzTemplateSpec [[-Version] <String>] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2495a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2495a-108">DESCRIPTION</span></span>
<span data-ttu-id="2495a-109">Dieses Cmdlet kann verwendet werden, um Vorlagenspezifikationen in einer Abonnement-/Ressourcengruppe auflisten oder eine bestimmte Vorlagenspezifikation nach Name oder ID zu erhalten. Beim Abrufen einer bestimmten Vorlagenspezifikation nach Name/ID kann optional eine bestimmte Version abgerufen werden, indem über den **-Version-Parameter** ein Versionsname angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2495a-109">This cmdlet can be used to list Template Specs in a subscription/resource group or get a specific Template Spec by name or id. When getting a specific Template Spec by name/id a specific version can optionally be retrieved by specifying a version name through the **-Version** parameter.</span></span> <span data-ttu-id="2495a-110">Wenn **-Version** verwendet wird, werden in \* nur die spezifischen Versionsdetails vorhanden *sein. Versionen* für das zurückgegebene Template Spec-Objekt.</span><span class="sxs-lookup"><span data-stu-id="2495a-110">When **-Version** is used, only the specific version details will be present within \**.Versions* on the returned Template Spec object.</span></span> <span data-ttu-id="2495a-111">Wenn beim Abrufen einer Vorlagenspezifikation nach Name/ID keine bestimmte Version angegeben wird, sind alle Versionen im \**vorhanden. Versionseigenschaft* des zurückgegebenen Objekts.</span><span class="sxs-lookup"><span data-stu-id="2495a-111">If no specific version is specified when retrieving a Template Spec by name/id, all versions will be present within the  \**.Versions* property of the returned object.</span></span>

<span data-ttu-id="2495a-112">**Hinweis:** Wenn Sie alle Vorlagenspezifikationen in einem Abonnement oder einer Ressourcengruppe auflisten, hat jede Vorlage die "- *zurückgegeben. Versions"-Eigenschaft* ist *null*.</span><span class="sxs-lookup"><span data-stu-id="2495a-112">**Note**: When listing all Template Specs within a subscription or resource group, each returned Template Spec's *".Versions"* property will be *null*.</span></span> <span data-ttu-id="2495a-113">Versionsinformationen sind nur enthalten, wenn -Name- oder -ResourceId-Parameter bereitgestellt werden (z. B.: Sie fordern eine bestimmte Vorlagenspezifikation/-version an).</span><span class="sxs-lookup"><span data-stu-id="2495a-113">Version information is only included when -Name or -ResourceId parameters are provided (eg: you are requesting a specific template spec/version).</span></span>

## <span data-ttu-id="2495a-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2495a-114">EXAMPLES</span></span>

### <span data-ttu-id="2495a-115">Beispiel 1: Listenvorlagenspezifikationen im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="2495a-115">Example 1: List Template Specs in current subscription</span></span>
```powershell
PS C:\> Get-AzTemplateSpec
```

<span data-ttu-id="2495a-116">Listet alle Vorlagenspezifikationen im aktuellen Abonnement auf.</span><span class="sxs-lookup"><span data-stu-id="2495a-116">Lists all Template Specs in the current subscription.</span></span>

### <span data-ttu-id="2495a-117">Beispiel 2: Listenvorlagenspezifikationen in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="2495a-117">Example 2: List Template Specs in a resource group</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG'
```

<span data-ttu-id="2495a-118">Listet alle Vorlagenspezifikationen in der Ressourcengruppe "myRG" des aktuellen Abonnements auf.</span><span class="sxs-lookup"><span data-stu-id="2495a-118">Lists all Template Specs in the resource group 'myRG' of the current subscription.</span></span>

### <span data-ttu-id="2495a-119">Beispiel 3: Vorlagenspezifikation (mit allen Versionen) nach Name</span><span class="sxs-lookup"><span data-stu-id="2495a-119">Example 3: Get Template Spec (with all versions) by name</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

<span data-ttu-id="2495a-120">Ruft Informationen zur Vorlagenspezifikation mit dem Namen "MyTemplateSpec" in der Ressourcengruppe "myRG" ab.</span><span class="sxs-lookup"><span data-stu-id="2495a-120">Gets information about the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

<span data-ttu-id="2495a-121">**Hinweis:** Alle Versionen der Vorlagenspezifikation sind im "*vorhanden. Versions*" -Eigenschaft des Rückgabeobjekts.</span><span class="sxs-lookup"><span data-stu-id="2495a-121">**Note**: All of the Template Spec's versions will be present within the "*.Versions*" property of the return object.</span></span>

### <span data-ttu-id="2495a-122">Beispiel 4: Vorlagenspezifikation (bestimmte Version) nach Name</span><span class="sxs-lookup"><span data-stu-id="2495a-122">Example 4: Get Template Spec (specific version) by name</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="2495a-123">Ruft Informationen zur Version "v1.0" der Vorlagenspezifikation mit dem Namen "MyTemplateSpec" innerhalb der Ressourcengruppe "myRG" ab.</span><span class="sxs-lookup"><span data-stu-id="2495a-123">Gets information about version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

<span data-ttu-id="2495a-124">**Hinweis:** Die *". Die Versions"-Eigenschaft* des zurückgegebenen Objekts enthält nur die angeforderte Version.</span><span class="sxs-lookup"><span data-stu-id="2495a-124">**Note**: The *".Versions"* property of the returned object will contain only the specific version requested.</span></span>

### <span data-ttu-id="2495a-125">Beispiel 5: Vorlagenspezifikation (mit allen Versionen) nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="2495a-125">Example 5: Get Template Spec (with all versions) by resource id</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec'
```

<span data-ttu-id="2495a-126">Ruft Informationen zur Vorlagenspezifikation mit dem Namen "MyTemplateSpec" in der Ressourcengruppe "myRG" der SubId des Abonnements \{ \} ab.</span><span class="sxs-lookup"><span data-stu-id="2495a-126">Gets information about the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

<span data-ttu-id="2495a-127">**Hinweis:** Alle Versionen der Vorlagenspezifikation sind im "*vorhanden. Versions*" -Eigenschaft des Rückgabeobjekts.</span><span class="sxs-lookup"><span data-stu-id="2495a-127">**Note**: All of the Template Spec's versions will be present within the "*.Versions*" property of the return object.</span></span>

### <span data-ttu-id="2495a-128">Beispiel 6: Vorlagenspezifikation (bestimmte Version) nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="2495a-128">Example 6: Get Template Spec (specific version) by resource id</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="2495a-129">Ruft Informationen zur Version "v1.0" der Vorlagenspezifikation mit dem Namen "MyTemplateSpec" in der Ressourcengruppe "myRG" der SubId des Abonnements \{ \} ab.</span><span class="sxs-lookup"><span data-stu-id="2495a-129">Gets information about version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

<span data-ttu-id="2495a-130">**Hinweis:** Die *". Die Versions"-Eigenschaft* des zurückgegebenen Objekts enthält nur die angeforderte Version.</span><span class="sxs-lookup"><span data-stu-id="2495a-130">**Note**: The *".Versions"* property of the returned object will contain only the specific version requested.</span></span>

## <span data-ttu-id="2495a-131">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2495a-131">PARAMETERS</span></span>

### <span data-ttu-id="2495a-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2495a-132">-DefaultProfile</span></span>
<span data-ttu-id="2495a-133">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2495a-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2495a-134">-Name</span><span class="sxs-lookup"><span data-stu-id="2495a-134">-Name</span></span>
<span data-ttu-id="2495a-135">Der Name der Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="2495a-135">The name of the template spec.</span></span>

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

### <span data-ttu-id="2495a-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2495a-136">-ResourceGroupName</span></span>
<span data-ttu-id="2495a-137">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2495a-137">The name of the resource group.</span></span>

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

### <span data-ttu-id="2495a-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2495a-138">-ResourceId</span></span>
<span data-ttu-id="2495a-139">Die vollqualifizierte Ressourcen-ID der Vorlagenspezifikation. Beispiel: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="2495a-139">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

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

### <span data-ttu-id="2495a-140">-Version</span><span class="sxs-lookup"><span data-stu-id="2495a-140">-Version</span></span>
<span data-ttu-id="2495a-141">Die Version der Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="2495a-141">The version of the template spec.</span></span>

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

### <span data-ttu-id="2495a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2495a-142">CommonParameters</span></span>
<span data-ttu-id="2495a-143">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2495a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2495a-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2495a-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2495a-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2495a-145">INPUTS</span></span>

### <span data-ttu-id="2495a-146">System.String</span><span class="sxs-lookup"><span data-stu-id="2495a-146">System.String</span></span>

## <span data-ttu-id="2495a-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2495a-147">OUTPUTS</span></span>

### <span data-ttu-id="2495a-148">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="2495a-148">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="2495a-149">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2495a-149">NOTES</span></span>

## <span data-ttu-id="2495a-150">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2495a-150">RELATED LINKS</span></span>
