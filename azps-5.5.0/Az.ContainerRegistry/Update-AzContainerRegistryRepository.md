---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistryrepository
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryRepository.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryRepository.md
ms.openlocfilehash: ce6f235669ebe4a32958229422f4612f3b8cb340
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164116"
---
# <span data-ttu-id="abaca-101">Update-AzContainerRegistryRepository</span><span class="sxs-lookup"><span data-stu-id="abaca-101">Update-AzContainerRegistryRepository</span></span>

## <span data-ttu-id="abaca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abaca-102">SYNOPSIS</span></span>
<span data-ttu-id="abaca-103">Aktualisieren Sie das ACR-Repository.</span><span class="sxs-lookup"><span data-stu-id="abaca-103">Update ACR repository.</span></span>

## <span data-ttu-id="abaca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="abaca-104">SYNTAX</span></span>

```
Update-AzContainerRegistryRepository -Name <String> [-DeleteEnabled <Boolean>] [-WriteEnabled <Boolean>]
 [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abaca-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="abaca-105">DESCRIPTION</span></span>
<span data-ttu-id="abaca-106">Aktualisieren Sie das ACR-Repository.</span><span class="sxs-lookup"><span data-stu-id="abaca-106">Update ACR repository.</span></span>

## <span data-ttu-id="abaca-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="abaca-107">EXAMPLES</span></span>

### <span data-ttu-id="abaca-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="abaca-108">Example 1</span></span>
```powershell
Update-AzContainerRegistryRepository -RegistryName registry -Name test/busybox8 -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry             : registry.azurecr.io
ImageName            : test/busybox8
CreatedTime          : 2020-12-11T08:57:56.2070002Z
LastUpdateTime       : 2020-12-11T08:57:56.5188237Z
ManifestCount        : 1
TagCount             : 1
ChangeableAttributes : Microsoft.Azure.Commands.ContainerRegistry.Models.PSChangeableAttribute
```

<span data-ttu-id="abaca-109">Aktualisieren Sie Attribute für das Repository alpine unter der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="abaca-109">Update attributes for repository alpine under registry.</span></span>

## <span data-ttu-id="abaca-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="abaca-110">PARAMETERS</span></span>

### <span data-ttu-id="abaca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abaca-111">-DefaultProfile</span></span>
<span data-ttu-id="abaca-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="abaca-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abaca-113">-DeleteEnabled</span><span class="sxs-lookup"><span data-stu-id="abaca-113">-DeleteEnabled</span></span>
<span data-ttu-id="abaca-114">"Löschen aktivieren" aus.</span><span class="sxs-lookup"><span data-stu-id="abaca-114">Delete enable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abaca-115">-ListEnabled</span><span class="sxs-lookup"><span data-stu-id="abaca-115">-ListEnabled</span></span>
<span data-ttu-id="abaca-116">Liste aktiviert.</span><span class="sxs-lookup"><span data-stu-id="abaca-116">List enable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abaca-117">-Name</span><span class="sxs-lookup"><span data-stu-id="abaca-117">-Name</span></span>
<span data-ttu-id="abaca-118">Repositoryname.</span><span class="sxs-lookup"><span data-stu-id="abaca-118">Repository Name.</span></span>

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

### <span data-ttu-id="abaca-119">-ReadEnabled</span><span class="sxs-lookup"><span data-stu-id="abaca-119">-ReadEnabled</span></span>
<span data-ttu-id="abaca-120">"Lesen aktivieren" aus.</span><span class="sxs-lookup"><span data-stu-id="abaca-120">Read enable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abaca-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="abaca-121">-RegistryName</span></span>
<span data-ttu-id="abaca-122">Azure Container Registry Name.</span><span class="sxs-lookup"><span data-stu-id="abaca-122">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="abaca-123">-WriteEnabled</span><span class="sxs-lookup"><span data-stu-id="abaca-123">-WriteEnabled</span></span>
<span data-ttu-id="abaca-124">"Schreibzugriff aktivieren" aus.</span><span class="sxs-lookup"><span data-stu-id="abaca-124">Write enable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abaca-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="abaca-125">-Confirm</span></span>
<span data-ttu-id="abaca-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="abaca-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abaca-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="abaca-127">-WhatIf</span></span>
<span data-ttu-id="abaca-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="abaca-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abaca-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="abaca-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abaca-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abaca-130">CommonParameters</span></span>
<span data-ttu-id="abaca-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abaca-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abaca-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="abaca-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abaca-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="abaca-133">INPUTS</span></span>

### <span data-ttu-id="abaca-134">System.String</span><span class="sxs-lookup"><span data-stu-id="abaca-134">System.String</span></span>

## <span data-ttu-id="abaca-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="abaca-135">OUTPUTS</span></span>

### <span data-ttu-id="abaca-136">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span><span class="sxs-lookup"><span data-stu-id="abaca-136">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span></span>

## <span data-ttu-id="abaca-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="abaca-137">NOTES</span></span>

## <span data-ttu-id="abaca-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="abaca-138">RELATED LINKS</span></span>
