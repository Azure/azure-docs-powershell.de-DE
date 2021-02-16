---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistrymanifest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryManifest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryManifest.md
ms.openlocfilehash: 85623106a932ba9419da0c07cc4bcb6c52e5e838
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144561"
---
# <span data-ttu-id="aa09a-101">Update-AzContainerRegistryManifest</span><span class="sxs-lookup"><span data-stu-id="aa09a-101">Update-AzContainerRegistryManifest</span></span>

## <span data-ttu-id="aa09a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa09a-102">SYNOPSIS</span></span>
<span data-ttu-id="aa09a-103">Aktualisieren Sie das ACR-Manifest.</span><span class="sxs-lookup"><span data-stu-id="aa09a-103">Update ACR manifest.</span></span> 

## <span data-ttu-id="aa09a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aa09a-104">SYNTAX</span></span>

### <span data-ttu-id="aa09a-105">ByManifestParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="aa09a-105">ByManifestParameterSet (Default)</span></span>
```
Update-AzContainerRegistryManifest -RepositoryName <String> -Manifest <String> [-DeleteEnabled <Boolean>]
 [-WriteEnabled <Boolean>] [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa09a-106">ByTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa09a-106">ByTagParameterSet</span></span>
```
Update-AzContainerRegistryManifest -RepositoryName <String> -Tag <String> [-DeleteEnabled <Boolean>]
 [-WriteEnabled <Boolean>] [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa09a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aa09a-107">DESCRIPTION</span></span>
<span data-ttu-id="aa09a-108">Aktualisieren Sie das ACR-Manifest.</span><span class="sxs-lookup"><span data-stu-id="aa09a-108">Update ACR manifest.</span></span>
<span data-ttu-id="aa09a-109">Um dieses Cmdlet zu verwenden, führen Sie `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="aa09a-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span></span>
<span data-ttu-id="aa09a-110">aus.</span><span class="sxs-lookup"><span data-stu-id="aa09a-110">first.</span></span>

## <span data-ttu-id="aa09a-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="aa09a-111">EXAMPLES</span></span>

### <span data-ttu-id="aa09a-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="aa09a-112">Example 1</span></span>
```powershell
Update-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine -Manifest sha256:185518070891758909c9f839cf4ca393ee977ac378609f700f60a771a2dfe321 -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase
```

<span data-ttu-id="aa09a-113">Updateattribute für manifest sha256:185518070891758909c9f839cf4ca393ee977ac378609f700f60a771a2dfe321 under registry.</span><span class="sxs-lookup"><span data-stu-id="aa09a-113">Update attributes for manifest sha256:185518070891758909c9f839cf4ca393ee977ac378609f700f60a771a2dfe321 under registry.</span></span>

### <span data-ttu-id="aa09a-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="aa09a-114">Example 2</span></span>
```powershell
Update-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine -Tag latest -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase
```

<span data-ttu-id="aa09a-115">Aktualisieren Sie Attribute für manifest mit dem neuesten Tag unter der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="aa09a-115">Update attributes for manifest with tag latest under registry.</span></span>

## <span data-ttu-id="aa09a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa09a-116">PARAMETERS</span></span>

### <span data-ttu-id="aa09a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa09a-117">-DefaultProfile</span></span>
<span data-ttu-id="aa09a-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aa09a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa09a-119">-DeleteEnabled</span><span class="sxs-lookup"><span data-stu-id="aa09a-119">-DeleteEnabled</span></span>
<span data-ttu-id="aa09a-120">"Löschen aktivieren" aus.</span><span class="sxs-lookup"><span data-stu-id="aa09a-120">Delete enable.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa09a-121">-ListEnabled</span><span class="sxs-lookup"><span data-stu-id="aa09a-121">-ListEnabled</span></span>
<span data-ttu-id="aa09a-122">Liste aktiviert.</span><span class="sxs-lookup"><span data-stu-id="aa09a-122">List enable.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa09a-123">-Manifest</span><span class="sxs-lookup"><span data-stu-id="aa09a-123">-Manifest</span></span>
<span data-ttu-id="aa09a-124">Manifestverweis.</span><span class="sxs-lookup"><span data-stu-id="aa09a-124">Manifest reference.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManifestParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa09a-125">-ReadEnabled</span><span class="sxs-lookup"><span data-stu-id="aa09a-125">-ReadEnabled</span></span>
<span data-ttu-id="aa09a-126">"Lesen aktivieren" aus.</span><span class="sxs-lookup"><span data-stu-id="aa09a-126">Read enable.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa09a-127">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="aa09a-127">-RegistryName</span></span>
<span data-ttu-id="aa09a-128">Azure Container Registry Name.</span><span class="sxs-lookup"><span data-stu-id="aa09a-128">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="aa09a-129">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="aa09a-129">-RepositoryName</span></span>
<span data-ttu-id="aa09a-130">Repositoryname.</span><span class="sxs-lookup"><span data-stu-id="aa09a-130">Repository Name.</span></span>

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

### <span data-ttu-id="aa09a-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="aa09a-131">-Tag</span></span>
<span data-ttu-id="aa09a-132">Tag.</span><span class="sxs-lookup"><span data-stu-id="aa09a-132">Tag.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa09a-133">-WriteEnabled</span><span class="sxs-lookup"><span data-stu-id="aa09a-133">-WriteEnabled</span></span>
<span data-ttu-id="aa09a-134">"Schreibzugriff aktivieren" aus.</span><span class="sxs-lookup"><span data-stu-id="aa09a-134">Write enable.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa09a-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa09a-135">-Confirm</span></span>
<span data-ttu-id="aa09a-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aa09a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa09a-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="aa09a-137">-WhatIf</span></span>
<span data-ttu-id="aa09a-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aa09a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa09a-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aa09a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa09a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa09a-140">CommonParameters</span></span>
<span data-ttu-id="aa09a-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa09a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa09a-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aa09a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa09a-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="aa09a-143">INPUTS</span></span>

### <span data-ttu-id="aa09a-144">System.String</span><span class="sxs-lookup"><span data-stu-id="aa09a-144">System.String</span></span>

## <span data-ttu-id="aa09a-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="aa09a-145">OUTPUTS</span></span>

### <span data-ttu-id="aa09a-146">Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttribute</span><span class="sxs-lookup"><span data-stu-id="aa09a-146">Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttribute</span></span>

## <span data-ttu-id="aa09a-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="aa09a-147">NOTES</span></span>

## <span data-ttu-id="aa09a-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="aa09a-148">RELATED LINKS</span></span>
