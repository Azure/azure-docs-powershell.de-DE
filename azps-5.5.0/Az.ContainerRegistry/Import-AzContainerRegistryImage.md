---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/import-azcontainerregistryimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Import-AzContainerRegistryImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Import-AzContainerRegistryImage.md
ms.openlocfilehash: 5fee8fec8d7b87629bfa46932662f430534fc695
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164140"
---
# <span data-ttu-id="fc791-101">Import-AzContainerRegistryImage</span><span class="sxs-lookup"><span data-stu-id="fc791-101">Import-AzContainerRegistryImage</span></span>

## <span data-ttu-id="fc791-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc791-102">SYNOPSIS</span></span>
<span data-ttu-id="fc791-103">Importieren sie ein Bild aus einer öffentlichen/azure-Registrierung in eine Azure-Container-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="fc791-103">Import image from a public/azure registry to an azure container registry.</span></span>

## <span data-ttu-id="fc791-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc791-104">SYNTAX</span></span>

### <span data-ttu-id="fc791-105">ImportImageByResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="fc791-105">ImportImageByResourceId (Default)</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryResourceId <String> [-Mode <String>] [-TargetTag <String[]>]
 [-UntaggedTargetRepository <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fc791-106">ImportImageByResourceIdWithCredential</span><span class="sxs-lookup"><span data-stu-id="fc791-106">ImportImageByResourceIdWithCredential</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryResourceId <String> [-Mode <String>] [-TargetTag <String[]>]
 [-UntaggedTargetRepository <String[]>] [-Username <String>] -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc791-107">ImportImageByRegistryUri</span><span class="sxs-lookup"><span data-stu-id="fc791-107">ImportImageByRegistryUri</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryUri <String> [-Mode <String>] [-TargetTag <String[]>] [-UntaggedTargetRepository <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc791-108">ImportImageByRegistryUriWithCredential</span><span class="sxs-lookup"><span data-stu-id="fc791-108">ImportImageByRegistryUriWithCredential</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryUri <String> [-Mode <String>] [-TargetTag <String[]>] [-UntaggedTargetRepository <String[]>]
 [-Username <String>] -Password <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fc791-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fc791-109">DESCRIPTION</span></span>
<span data-ttu-id="fc791-110">Importieren sie ein Bild aus einer öffentlichen/azure-Registrierung in eine Azure-Container-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="fc791-110">Import image from a public/azure registry to an azure container registry.</span></span>

## <span data-ttu-id="fc791-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fc791-111">EXAMPLES</span></span>

### <span data-ttu-id="fc791-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fc791-112">Example 1</span></span>
```powershell
PS C:\> Import-AzContainerRegistryImage -SourceImage library/busybox:latest -ResourceGroupName $resourceGroupName -RegistryName $RegistryName -SourceRegistryUri docker.io -TargetTag busybox:latest
```

<span data-ttu-id="fc791-113">"Busybox in ACR importieren" aus.</span><span class="sxs-lookup"><span data-stu-id="fc791-113">Import busybox to ACR.</span></span> <span data-ttu-id="fc791-114">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="fc791-114">Note:</span></span> 
* <span data-ttu-id="fc791-115">"library/" muss vor dem Quellbild hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="fc791-115">"library/" need to be add before source image.</span></span> <span data-ttu-id="fc791-116">"busybox:latest" => "library/busybox:latest"</span><span class="sxs-lookup"><span data-stu-id="fc791-116">"busybox:latest" => "library/busybox:latest"</span></span>
* <span data-ttu-id="fc791-117">Anmeldeinformationen erforderlich, wenn die Quellregistrierung nicht öffentlich verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="fc791-117">Credential needed if source registry is not publicly available</span></span>

### <span data-ttu-id="fc791-118">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fc791-118">Example 2</span></span>
```powershell
PS C:\> Import-AzContainerRegistryImage -SourceImage $SourceRegistry.azurecr.io/busybox:latest -ResourceGroupName $resourceGroupName -RegistryName $RegistryName -SourceRegistryResourceId $SourceACRID -TargetTag busybox:latest
```

<span data-ttu-id="fc791-119">"Busybox importieren" aus quell-ACR in Ziel-ACR.</span><span class="sxs-lookup"><span data-stu-id="fc791-119">Import busybox from source ACR to target ACR.</span></span> <span data-ttu-id="fc791-120">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="fc791-120">Note:</span></span> 
* <span data-ttu-id="fc791-121">Anmeldeinformationen, die erforderlich sind, wenn der Administratorbenutzer für die Quellregistrierung deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="fc791-121">Credential needed if admin user for source registry was disabled.</span></span>

## <span data-ttu-id="fc791-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc791-122">PARAMETERS</span></span>

### <span data-ttu-id="fc791-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc791-123">-DefaultProfile</span></span>
<span data-ttu-id="fc791-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fc791-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc791-125">-Mode</span><span class="sxs-lookup"><span data-stu-id="fc791-125">-Mode</span></span>
<span data-ttu-id="fc791-126">Bei "Erzwingen" werden alle vorhandenen Zieltags überschrieben.</span><span class="sxs-lookup"><span data-stu-id="fc791-126">When Force, any existing target tags will be overwritten.</span></span>
<span data-ttu-id="fc791-127">Bei NoForce kann der Vorgang bei allen vorhandenen Zieltags fehlschlagen, bevor das Kopieren beginnt.</span><span class="sxs-lookup"><span data-stu-id="fc791-127">When NoForce, any existing target tags will fail the operation before any copying begins.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Force, NoForce

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc791-128">-Password</span><span class="sxs-lookup"><span data-stu-id="fc791-128">-Password</span></span>
<span data-ttu-id="fc791-129">Das Kennwort für die Authentifizierung bei der Quellregistrierung.</span><span class="sxs-lookup"><span data-stu-id="fc791-129">The password used to authenticate with the source registry.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportImageByResourceIdWithCredential, ImportImageByRegistryUriWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc791-130">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="fc791-130">-RegistryName</span></span>
<span data-ttu-id="fc791-131">Zielregistrierungsname</span><span class="sxs-lookup"><span data-stu-id="fc791-131">Target registry name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc791-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc791-132">-ResourceGroupName</span></span>
<span data-ttu-id="fc791-133">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="fc791-133">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc791-134">-SourceImage</span><span class="sxs-lookup"><span data-stu-id="fc791-134">-SourceImage</span></span>
<span data-ttu-id="fc791-135">Repositoryname des Quellbilds.</span><span class="sxs-lookup"><span data-stu-id="fc791-135">Repository name of the source image.</span></span>

<span data-ttu-id="fc791-136">Geben Sie ein Bild nach Repository an ('hello-world').</span><span class="sxs-lookup"><span data-stu-id="fc791-136">Specify an image by repository ('hello-world').</span></span>
<span data-ttu-id="fc791-137">Dadurch wird das "neueste" Tag verwendet.</span><span class="sxs-lookup"><span data-stu-id="fc791-137">This will use the 'latest' tag.</span></span>

<span data-ttu-id="fc791-138">Geben Sie ein Bild nach Tag an ('hello-world:latest').</span><span class="sxs-lookup"><span data-stu-id="fc791-138">Specify an image by tag ('hello-world:latest').</span></span>

<span data-ttu-id="fc791-139">Geben Sie ein Bild anhand eines sha256-basierten Manifest-Digests an (' hello-world@sha256:abc123 ').</span><span class="sxs-lookup"><span data-stu-id="fc791-139">Specify an image by sha256-based manifest digest ('hello-world@sha256:abc123').</span></span>

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

### <span data-ttu-id="fc791-140">-SourceRegistryResourceId</span><span class="sxs-lookup"><span data-stu-id="fc791-140">-SourceRegistryResourceId</span></span>
<span data-ttu-id="fc791-141">Der Ressourcenbezeichner der Azure-Container-Quellregistrierung.</span><span class="sxs-lookup"><span data-stu-id="fc791-141">The resource identifier of the source Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportImageByResourceId, ImportImageByResourceIdWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc791-142">-SourceRegistryUri</span><span class="sxs-lookup"><span data-stu-id="fc791-142">-SourceRegistryUri</span></span>
<span data-ttu-id="fc791-143">Die Adresse der Quellregistrierung (z. B. "mcr.microsoft.com").</span><span class="sxs-lookup"><span data-stu-id="fc791-143">The address of the source registry (e.g. 'mcr.microsoft.com').</span></span>

```yaml
Type: System.String
Parameter Sets: ImportImageByRegistryUri, ImportImageByRegistryUriWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc791-144">-TargetTag</span><span class="sxs-lookup"><span data-stu-id="fc791-144">-TargetTag</span></span>
<span data-ttu-id="fc791-145">Liste der Zeichenfolgen des Formulars Repository \[ :tag \] .</span><span class="sxs-lookup"><span data-stu-id="fc791-145">List of strings of the form repo\[:tag\].</span></span>
<span data-ttu-id="fc791-146">Wenn das Tag ausgelassen wird, wird die Quelle verwendet (bzw. "neueste", wenn das Quelltag ebenfalls ausgelassen wird).</span><span class="sxs-lookup"><span data-stu-id="fc791-146">When tag is omitted the source will be used (or 'latest' if source tag is also omitted).</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc791-147">-UntaggedTargetRepository</span><span class="sxs-lookup"><span data-stu-id="fc791-147">-UntaggedTargetRepository</span></span>
<span data-ttu-id="fc791-148">Liste der Zeichenfolgen mit Repositorynamen, um nur eine Manifestkopie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="fc791-148">List of strings of repository names to do a manifest only copy.</span></span>
<span data-ttu-id="fc791-149">Es wird kein Tag erstellt.</span><span class="sxs-lookup"><span data-stu-id="fc791-149">No tag will be created.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc791-150">-Username</span><span class="sxs-lookup"><span data-stu-id="fc791-150">-Username</span></span>
<span data-ttu-id="fc791-151">Der Benutzername, der bei der Quellregistrierung authentifiziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="fc791-151">The username to authenticate with the source registry.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportImageByResourceIdWithCredential, ImportImageByRegistryUriWithCredential
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc791-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc791-152">-Confirm</span></span>
<span data-ttu-id="fc791-153">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fc791-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc791-154">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fc791-154">-WhatIf</span></span>
<span data-ttu-id="fc791-155">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fc791-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc791-156">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fc791-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc791-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc791-157">CommonParameters</span></span>
<span data-ttu-id="fc791-158">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc791-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc791-159">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fc791-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc791-160">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fc791-160">INPUTS</span></span>

### <span data-ttu-id="fc791-161">System.String</span><span class="sxs-lookup"><span data-stu-id="fc791-161">System.String</span></span>

## <span data-ttu-id="fc791-162">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fc791-162">OUTPUTS</span></span>

### <span data-ttu-id="fc791-163">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fc791-163">System.Boolean</span></span>

## <span data-ttu-id="fc791-164">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fc791-164">NOTES</span></span>

## <span data-ttu-id="fc791-165">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fc791-165">RELATED LINKS</span></span>
