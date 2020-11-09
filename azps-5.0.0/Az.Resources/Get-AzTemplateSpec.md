---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
ms.openlocfilehash: be3a16707303016e22be8052721efcb35c608b3e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301072"
---
# <span data-ttu-id="12e36-101">Get-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="12e36-101">Get-AzTemplateSpec</span></span>

## <span data-ttu-id="12e36-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="12e36-102">SYNOPSIS</span></span>
<span data-ttu-id="12e36-103">Abrufen oder Auflisten von Vorlagen Spezifikationen</span><span class="sxs-lookup"><span data-stu-id="12e36-103">Gets or lists Template Specs</span></span>

## <span data-ttu-id="12e36-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="12e36-104">SYNTAX</span></span>

### <span data-ttu-id="12e36-105">ListTemplateSpecsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="12e36-105">ListTemplateSpecsParameterSet (Default)</span></span>
```
Get-AzTemplateSpec [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="12e36-106">GetTemplateSpecByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="12e36-106">GetTemplateSpecByNameParameterSet</span></span>
```
Get-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12e36-107">GetTemplateSpecByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="12e36-107">GetTemplateSpecByIdParameterSet</span></span>
```
Get-AzTemplateSpec [[-Version] <String>] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="12e36-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="12e36-108">DESCRIPTION</span></span>
<span data-ttu-id="12e36-109">Dieses Cmdlet kann verwendet werden, um Vorlagen Spezifikationen in einer Abonnement-oder Ressourcengruppe aufzulisten oder eine bestimmte Vorlagenspezifikation nach Name oder ID abzurufen. Wenn Sie eine bestimmte Vorlagenspezifikation nach Name/ID abrufen, kann eine bestimmte Version optional abgerufen werden, indem Sie über den Parameter **-Version** einen Versionsnamen angeben.</span><span class="sxs-lookup"><span data-stu-id="12e36-109">This cmdlet can be used to list Template Specs in a subscription/resource group or get a specific Template Spec by name or id. When getting a specific Template Spec by name/id a specific version can optionally be retrieved by specifying a version name through the **-Version** parameter.</span></span> <span data-ttu-id="12e36-110">Wenn **-Version** verwendet wird, sind nur die spezifischen Versionsdetails in \* enthalten *. Versionen* des zurückgegebenen Vorlagen Spezifikations Objekts.</span><span class="sxs-lookup"><span data-stu-id="12e36-110">When **-Version** is used, only the specific version details will be present within \* *.Versions* on the returned Template Spec object.</span></span> <span data-ttu-id="12e36-111">Wenn beim Abrufen einer Vorlagenspezifikation nach Name/ID keine bestimmte Version angegeben ist, sind alle Versionen in der \* enthalten *. Versions* -Eigenschaft des zurückgegebenen Objekts.</span><span class="sxs-lookup"><span data-stu-id="12e36-111">If no specific version is specified when retrieving a Template Spec by name/id, all versions will be present within the  \* *.Versions* property of the returned object.</span></span>

<span data-ttu-id="12e36-112">**Hinweis** : Wenn Sie alle Vorlagen Spezifikationen innerhalb eines Abonnements oder einer Ressourcengruppe auflisten, werden die einzelnen Vorlagen Spezifikationen "zurückgegeben *. Versions "* -Eigenschaft ist *null*.</span><span class="sxs-lookup"><span data-stu-id="12e36-112">**Note** : When listing all Template Specs within a subscription or resource group, each returned Template Spec's *".Versions"* property will be *null*.</span></span> <span data-ttu-id="12e36-113">Versionsinformationen werden nur berücksichtigt, wenn-Name oder-Resourcen-Parameter bereitgestellt werden (z. b.: Sie fordern eine bestimmte Vorlagenspezifikation/-Version an).</span><span class="sxs-lookup"><span data-stu-id="12e36-113">Version information is only included when -Name or -ResourceId parameters are provided (eg: you are requesting a specific template spec/version).</span></span>

## <span data-ttu-id="12e36-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="12e36-114">EXAMPLES</span></span>

### <span data-ttu-id="12e36-115">Beispiel 1: Auflisten von Vorlagen Spezifikationen im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="12e36-115">Example 1: List Template Specs in current subscription</span></span>
```powershell
PS C:\> Get-AzTemplateSpec
```

<span data-ttu-id="12e36-116">Listet alle Vorlagen Spezifikationen im aktuellen Abonnement auf.</span><span class="sxs-lookup"><span data-stu-id="12e36-116">Lists all Template Specs in the current subscription.</span></span>

### <span data-ttu-id="12e36-117">Beispiel 2: Auflisten von Vorlagen Spezifikationen in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="12e36-117">Example 2: List Template Specs in a resource group</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG'
```

<span data-ttu-id="12e36-118">Listet alle Vorlagen Spezifikationen in der Ressourcengruppe "myRG" des aktuellen Abonnements auf.</span><span class="sxs-lookup"><span data-stu-id="12e36-118">Lists all Template Specs in the resource group 'myRG' of the current subscription.</span></span>

### <span data-ttu-id="12e36-119">Beispiel 3: Abrufen der Vorlagenspezifikation (mit allen Versionen) nach Name</span><span class="sxs-lookup"><span data-stu-id="12e36-119">Example 3: Get Template Spec (with all versions) by name</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

<span data-ttu-id="12e36-120">Ruft Informationen zur Vorlagenspezifikation mit dem Namen "MyTemplateSpec" innerhalb der Ressourcengruppe "myRG" ab.</span><span class="sxs-lookup"><span data-stu-id="12e36-120">Gets information about the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

<span data-ttu-id="12e36-121">**Hinweis** : alle Versionen der Vorlage spec sind in der " *. Versions* "-Eigenschaft des Rückgabe Objekts.</span><span class="sxs-lookup"><span data-stu-id="12e36-121">**Note** : All of the Template Spec's versions will be present within the " *.Versions* " property of the return object.</span></span>

### <span data-ttu-id="12e36-122">Beispiel 4: Abrufen der Vorlagenspezifikation (bestimmte Version) nach Name</span><span class="sxs-lookup"><span data-stu-id="12e36-122">Example 4: Get Template Spec (specific version) by name</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="12e36-123">Ruft Informationen zur Version "v 1.0" der Vorlagenspezifikation mit dem Namen "MyTemplateSpec" innerhalb der Ressourcengruppe "myRG" ab.</span><span class="sxs-lookup"><span data-stu-id="12e36-123">Gets information about version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

<span data-ttu-id="12e36-124">**Hinweis** : die *". Versions "* -Eigenschaft des zurückgegebenen Objekts enthält nur die angeforderte bestimmte Version.</span><span class="sxs-lookup"><span data-stu-id="12e36-124">**Note** : The *".Versions"* property of the returned object will contain only the specific version requested.</span></span>

### <span data-ttu-id="12e36-125">Beispiel 5: Abrufen der Vorlagenspezifikation (mit allen Versionen) nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="12e36-125">Example 5: Get Template Spec (with all versions) by resource id</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec'
```

<span data-ttu-id="12e36-126">Ruft Informationen zur Vorlagenspezifikation mit dem Namen "MyTemplateSpec" innerhalb der Ressourcengruppe "myRG" des Abonnement- \{ subId ab \} .</span><span class="sxs-lookup"><span data-stu-id="12e36-126">Gets information about the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

<span data-ttu-id="12e36-127">**Hinweis** : alle Versionen der Vorlage spec sind in der " *. Versions* "-Eigenschaft des Rückgabe Objekts.</span><span class="sxs-lookup"><span data-stu-id="12e36-127">**Note** : All of the Template Spec's versions will be present within the " *.Versions* " property of the return object.</span></span>

### <span data-ttu-id="12e36-128">Beispiel 6: Abrufen der Vorlagenspezifikation (bestimmte Version) nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="12e36-128">Example 6: Get Template Spec (specific version) by resource id</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="12e36-129">Ruft Informationen zur Version "v 1.0" der Vorlagenspezifikation mit dem Namen "MyTemplateSpec" innerhalb der Ressourcengruppe "myRG" des Abonnement- \{ subId ab \} .</span><span class="sxs-lookup"><span data-stu-id="12e36-129">Gets information about version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

<span data-ttu-id="12e36-130">**Hinweis** : die *". Versions "* -Eigenschaft des zurückgegebenen Objekts enthält nur die angeforderte bestimmte Version.</span><span class="sxs-lookup"><span data-stu-id="12e36-130">**Note** : The *".Versions"* property of the returned object will contain only the specific version requested.</span></span>

## <span data-ttu-id="12e36-131">Parameter</span><span class="sxs-lookup"><span data-stu-id="12e36-131">PARAMETERS</span></span>

### <span data-ttu-id="12e36-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12e36-132">-DefaultProfile</span></span>
<span data-ttu-id="12e36-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="12e36-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12e36-134">-Name</span><span class="sxs-lookup"><span data-stu-id="12e36-134">-Name</span></span>
<span data-ttu-id="12e36-135">Der Name der Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="12e36-135">The name of the template spec.</span></span>

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

### <span data-ttu-id="12e36-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12e36-136">-ResourceGroupName</span></span>
<span data-ttu-id="12e36-137">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="12e36-137">The name of the resource group.</span></span>

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

### <span data-ttu-id="12e36-138">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="12e36-138">-ResourceId</span></span>
<span data-ttu-id="12e36-139">Die vollqualifizierte Ressourcen-ID der Vorlagenspezifikation. Beispiel:/Subscriptions/{subId}/resourceGroups/{rgName}/Providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="12e36-139">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

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

### <span data-ttu-id="12e36-140">-Version</span><span class="sxs-lookup"><span data-stu-id="12e36-140">-Version</span></span>
<span data-ttu-id="12e36-141">Die Version der Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="12e36-141">The version of the template spec.</span></span>

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

### <span data-ttu-id="12e36-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12e36-142">CommonParameters</span></span>
<span data-ttu-id="12e36-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12e36-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12e36-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12e36-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12e36-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="12e36-145">INPUTS</span></span>

### <span data-ttu-id="12e36-146">System. String</span><span class="sxs-lookup"><span data-stu-id="12e36-146">System.String</span></span>

## <span data-ttu-id="12e36-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="12e36-147">OUTPUTS</span></span>

### <span data-ttu-id="12e36-148">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="12e36-148">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="12e36-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="12e36-149">NOTES</span></span>

## <span data-ttu-id="12e36-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="12e36-150">RELATED LINKS</span></span>
