---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistrytag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryTag.md
ms.openlocfilehash: 48fb77eb9c718a09a7e13e6d6ab5af5bfc60c912
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171060"
---
# <span data-ttu-id="8cc62-101">Update-AzContainerRegistryTag</span><span class="sxs-lookup"><span data-stu-id="8cc62-101">Update-AzContainerRegistryTag</span></span>

## <span data-ttu-id="8cc62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8cc62-102">SYNOPSIS</span></span>
<span data-ttu-id="8cc62-103">Aktualisieren Sie das ACR-Tag.</span><span class="sxs-lookup"><span data-stu-id="8cc62-103">Update ACR tag.</span></span>

## <span data-ttu-id="8cc62-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8cc62-104">SYNTAX</span></span>

```
Update-AzContainerRegistryTag -RepositoryName <String> -Name <String> [-DeleteEnabled <Boolean>]
 [-WriteEnabled <Boolean>] [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cc62-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8cc62-105">DESCRIPTION</span></span>
<span data-ttu-id="8cc62-106">Aktualisieren Sie das ACR-Tag.</span><span class="sxs-lookup"><span data-stu-id="8cc62-106">Update ACR tag.</span></span>
<span data-ttu-id="8cc62-107">Um dieses Cmdlet zu verwenden, führen Sie `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="8cc62-107">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span></span>
<span data-ttu-id="8cc62-108">aus.</span><span class="sxs-lookup"><span data-stu-id="8cc62-108">first.</span></span>

## <span data-ttu-id="8cc62-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8cc62-109">EXAMPLES</span></span>

### <span data-ttu-id="8cc62-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8cc62-110">Example 1</span></span>
```powershell
Update-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine -Name latest -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute
```

<span data-ttu-id="8cc62-111">Aktualisieren Sie Attribute für das neueste Tag in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="8cc62-111">Update attributes for tag latest under registry.</span></span>

## <span data-ttu-id="8cc62-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8cc62-112">PARAMETERS</span></span>

### <span data-ttu-id="8cc62-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cc62-113">-DefaultProfile</span></span>
<span data-ttu-id="8cc62-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8cc62-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cc62-115">-DeleteEnabled</span><span class="sxs-lookup"><span data-stu-id="8cc62-115">-DeleteEnabled</span></span>
<span data-ttu-id="8cc62-116">"Löschen aktivieren" aus.</span><span class="sxs-lookup"><span data-stu-id="8cc62-116">Delete enable.</span></span>

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

### <span data-ttu-id="8cc62-117">-ListEnabled</span><span class="sxs-lookup"><span data-stu-id="8cc62-117">-ListEnabled</span></span>
<span data-ttu-id="8cc62-118">Liste aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8cc62-118">List enable.</span></span>

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

### <span data-ttu-id="8cc62-119">-Name</span><span class="sxs-lookup"><span data-stu-id="8cc62-119">-Name</span></span>
<span data-ttu-id="8cc62-120">Tag.</span><span class="sxs-lookup"><span data-stu-id="8cc62-120">Tag.</span></span>

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

### <span data-ttu-id="8cc62-121">-ReadEnabled</span><span class="sxs-lookup"><span data-stu-id="8cc62-121">-ReadEnabled</span></span>
<span data-ttu-id="8cc62-122">"Lesen aktivieren" aus.</span><span class="sxs-lookup"><span data-stu-id="8cc62-122">Read enable.</span></span>

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

### <span data-ttu-id="8cc62-123">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="8cc62-123">-RegistryName</span></span>
<span data-ttu-id="8cc62-124">Azure Container Registry Name.</span><span class="sxs-lookup"><span data-stu-id="8cc62-124">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="8cc62-125">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="8cc62-125">-RepositoryName</span></span>
<span data-ttu-id="8cc62-126">Repositoryname.</span><span class="sxs-lookup"><span data-stu-id="8cc62-126">Repository Name.</span></span>

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

### <span data-ttu-id="8cc62-127">-WriteEnabled</span><span class="sxs-lookup"><span data-stu-id="8cc62-127">-WriteEnabled</span></span>
<span data-ttu-id="8cc62-128">"Schreibzugriff aktivieren" aus.</span><span class="sxs-lookup"><span data-stu-id="8cc62-128">Write enable.</span></span>

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

### <span data-ttu-id="8cc62-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8cc62-129">-Confirm</span></span>
<span data-ttu-id="8cc62-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8cc62-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cc62-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8cc62-131">-WhatIf</span></span>
<span data-ttu-id="8cc62-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8cc62-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cc62-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8cc62-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cc62-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cc62-134">CommonParameters</span></span>
<span data-ttu-id="8cc62-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cc62-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cc62-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8cc62-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cc62-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8cc62-137">INPUTS</span></span>

### <span data-ttu-id="8cc62-138">System.String</span><span class="sxs-lookup"><span data-stu-id="8cc62-138">System.String</span></span>

## <span data-ttu-id="8cc62-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8cc62-139">OUTPUTS</span></span>

### <span data-ttu-id="8cc62-140">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span><span class="sxs-lookup"><span data-stu-id="8cc62-140">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span></span>

## <span data-ttu-id="8cc62-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8cc62-141">NOTES</span></span>

## <span data-ttu-id="8cc62-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8cc62-142">RELATED LINKS</span></span>
