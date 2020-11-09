---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/import-azcontainerregistryimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Import-AzContainerRegistryImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Import-AzContainerRegistryImage.md
ms.openlocfilehash: 5fee8fec8d7b87629bfa46932662f430534fc695
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296385"
---
# <span data-ttu-id="9ea17-101">Import-AzContainerRegistryImage</span><span class="sxs-lookup"><span data-stu-id="9ea17-101">Import-AzContainerRegistryImage</span></span>

## <span data-ttu-id="9ea17-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9ea17-102">SYNOPSIS</span></span>
<span data-ttu-id="9ea17-103">Importieren Sie ein Bild aus einer Public/Azure-Registrierung in eine Azure Container-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="9ea17-103">Import image from a public/azure registry to an azure container registry.</span></span>

## <span data-ttu-id="9ea17-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ea17-104">SYNTAX</span></span>

### <span data-ttu-id="9ea17-105">ImportImageByResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="9ea17-105">ImportImageByResourceId (Default)</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryResourceId <String> [-Mode <String>] [-TargetTag <String[]>]
 [-UntaggedTargetRepository <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ea17-106">ImportImageByResourceIdWithCredential</span><span class="sxs-lookup"><span data-stu-id="9ea17-106">ImportImageByResourceIdWithCredential</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryResourceId <String> [-Mode <String>] [-TargetTag <String[]>]
 [-UntaggedTargetRepository <String[]>] [-Username <String>] -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ea17-107">ImportImageByRegistryUri</span><span class="sxs-lookup"><span data-stu-id="9ea17-107">ImportImageByRegistryUri</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryUri <String> [-Mode <String>] [-TargetTag <String[]>] [-UntaggedTargetRepository <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ea17-108">ImportImageByRegistryUriWithCredential</span><span class="sxs-lookup"><span data-stu-id="9ea17-108">ImportImageByRegistryUriWithCredential</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryUri <String> [-Mode <String>] [-TargetTag <String[]>] [-UntaggedTargetRepository <String[]>]
 [-Username <String>] -Password <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9ea17-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9ea17-109">DESCRIPTION</span></span>
<span data-ttu-id="9ea17-110">Importieren Sie ein Bild aus einer Public/Azure-Registrierung in eine Azure Container-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="9ea17-110">Import image from a public/azure registry to an azure container registry.</span></span>

## <span data-ttu-id="9ea17-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9ea17-111">EXAMPLES</span></span>

### <span data-ttu-id="9ea17-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9ea17-112">Example 1</span></span>
```powershell
PS C:\> Import-AzContainerRegistryImage -SourceImage library/busybox:latest -ResourceGroupName $resourceGroupName -RegistryName $RegistryName -SourceRegistryUri docker.io -TargetTag busybox:latest
```

<span data-ttu-id="9ea17-113">Importieren Sie busybox in ACR.</span><span class="sxs-lookup"><span data-stu-id="9ea17-113">Import busybox to ACR.</span></span> <span data-ttu-id="9ea17-114">Hinweis</span><span class="sxs-lookup"><span data-stu-id="9ea17-114">Note:</span></span> 
* <span data-ttu-id="9ea17-115">"Bibliothek/" muss vor dem Quell Bild hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="9ea17-115">"library/" need to be add before source image.</span></span> <span data-ttu-id="9ea17-116">"busybox: Latest" => "Library/busybox: Latest"</span><span class="sxs-lookup"><span data-stu-id="9ea17-116">"busybox:latest" => "library/busybox:latest"</span></span>
* <span data-ttu-id="9ea17-117">Anmeldeinformationen erforderlich, wenn die Quell Registrierung nicht öffentlich verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="9ea17-117">Credential needed if source registry is not publicly available</span></span>

### <span data-ttu-id="9ea17-118">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9ea17-118">Example 2</span></span>
```powershell
PS C:\> Import-AzContainerRegistryImage -SourceImage $SourceRegistry.azurecr.io/busybox:latest -ResourceGroupName $resourceGroupName -RegistryName $RegistryName -SourceRegistryResourceId $SourceACRID -TargetTag busybox:latest
```

<span data-ttu-id="9ea17-119">Importieren Sie busybox aus der Quelle ACR in das Ziel ACR.</span><span class="sxs-lookup"><span data-stu-id="9ea17-119">Import busybox from source ACR to target ACR.</span></span> <span data-ttu-id="9ea17-120">Hinweis</span><span class="sxs-lookup"><span data-stu-id="9ea17-120">Note:</span></span> 
* <span data-ttu-id="9ea17-121">Anmeldeinformationen erforderlich, wenn der Administrator Benutzer für die Quell Registrierung deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="9ea17-121">Credential needed if admin user for source registry was disabled.</span></span>

## <span data-ttu-id="9ea17-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ea17-122">PARAMETERS</span></span>

### <span data-ttu-id="9ea17-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ea17-123">-DefaultProfile</span></span>
<span data-ttu-id="9ea17-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9ea17-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ea17-125">-Modus</span><span class="sxs-lookup"><span data-stu-id="9ea17-125">-Mode</span></span>
<span data-ttu-id="9ea17-126">Wenn Force, werden vorhandene Ziel-Tags überschrieben.</span><span class="sxs-lookup"><span data-stu-id="9ea17-126">When Force, any existing target tags will be overwritten.</span></span>
<span data-ttu-id="9ea17-127">Wenn noforce vorhanden ist, wird der Vorgang durch vorhandene Ziel-Tags abgebrochen, bevor ein Kopiervorgang beginnt.</span><span class="sxs-lookup"><span data-stu-id="9ea17-127">When NoForce, any existing target tags will fail the operation before any copying begins.</span></span>

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

### <span data-ttu-id="9ea17-128">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="9ea17-128">-Password</span></span>
<span data-ttu-id="9ea17-129">Das Kennwort, das für die Authentifizierung bei der Quell Registrierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9ea17-129">The password used to authenticate with the source registry.</span></span>

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

### <span data-ttu-id="9ea17-130">-Registryname</span><span class="sxs-lookup"><span data-stu-id="9ea17-130">-RegistryName</span></span>
<span data-ttu-id="9ea17-131">Ziel Registrierungsname</span><span class="sxs-lookup"><span data-stu-id="9ea17-131">Target registry name.</span></span>

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

### <span data-ttu-id="9ea17-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ea17-132">-ResourceGroupName</span></span>
<span data-ttu-id="9ea17-133">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9ea17-133">Resource group name.</span></span>

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

### <span data-ttu-id="9ea17-134">-SourceImage</span><span class="sxs-lookup"><span data-stu-id="9ea17-134">-SourceImage</span></span>
<span data-ttu-id="9ea17-135">Repository-Name des Quellbilds</span><span class="sxs-lookup"><span data-stu-id="9ea17-135">Repository name of the source image.</span></span>

<span data-ttu-id="9ea17-136">Geben Sie ein Bild im Repository an ("Hello-World").</span><span class="sxs-lookup"><span data-stu-id="9ea17-136">Specify an image by repository ('hello-world').</span></span>
<span data-ttu-id="9ea17-137">Dabei wird die Kategorie "aktuell" verwendet.</span><span class="sxs-lookup"><span data-stu-id="9ea17-137">This will use the 'latest' tag.</span></span>

<span data-ttu-id="9ea17-138">Geben Sie ein Bild nach Tag an ("Hello-World: Latest").</span><span class="sxs-lookup"><span data-stu-id="9ea17-138">Specify an image by tag ('hello-world:latest').</span></span>

<span data-ttu-id="9ea17-139">Geben Sie ein Bild von SHA256-basierter Manifest-Digest an (' hello-world@sha256:abc123 ').</span><span class="sxs-lookup"><span data-stu-id="9ea17-139">Specify an image by sha256-based manifest digest ('hello-world@sha256:abc123').</span></span>

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

### <span data-ttu-id="9ea17-140">-SourceRegistryResourceId</span><span class="sxs-lookup"><span data-stu-id="9ea17-140">-SourceRegistryResourceId</span></span>
<span data-ttu-id="9ea17-141">Der Ressourcenbezeichner der Quell-Azure-Container Registrierung.</span><span class="sxs-lookup"><span data-stu-id="9ea17-141">The resource identifier of the source Azure Container Registry.</span></span>

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

### <span data-ttu-id="9ea17-142">-SourceRegistryUri</span><span class="sxs-lookup"><span data-stu-id="9ea17-142">-SourceRegistryUri</span></span>
<span data-ttu-id="9ea17-143">Die Adresse der Quell Registrierung (beispielsweise "MCR.Microsoft.com").</span><span class="sxs-lookup"><span data-stu-id="9ea17-143">The address of the source registry (e.g. 'mcr.microsoft.com').</span></span>

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

### <span data-ttu-id="9ea17-144">-TargetTag</span><span class="sxs-lookup"><span data-stu-id="9ea17-144">-TargetTag</span></span>
<span data-ttu-id="9ea17-145">Liste der Zeichenfolgen im Format Repo \[ :-Tag \] .</span><span class="sxs-lookup"><span data-stu-id="9ea17-145">List of strings of the form repo\[:tag\].</span></span>
<span data-ttu-id="9ea17-146">Wenn "Tag" ausgelassen wird, wird die Quelle verwendet (oder "aktuell", wenn die Quellkategorie ebenfalls ausgelassen wird).</span><span class="sxs-lookup"><span data-stu-id="9ea17-146">When tag is omitted the source will be used (or 'latest' if source tag is also omitted).</span></span>

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

### <span data-ttu-id="9ea17-147">-UntaggedTargetRepository</span><span class="sxs-lookup"><span data-stu-id="9ea17-147">-UntaggedTargetRepository</span></span>
<span data-ttu-id="9ea17-148">Liste der Zeichenfolgen von Repository-Namen, um nur eine Manifestdatei zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="9ea17-148">List of strings of repository names to do a manifest only copy.</span></span>
<span data-ttu-id="9ea17-149">Es wird kein Tag erstellt.</span><span class="sxs-lookup"><span data-stu-id="9ea17-149">No tag will be created.</span></span>

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

### <span data-ttu-id="9ea17-150">-Username</span><span class="sxs-lookup"><span data-stu-id="9ea17-150">-Username</span></span>
<span data-ttu-id="9ea17-151">Der Benutzername, der bei der Quell Registrierung authentifiziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9ea17-151">The username to authenticate with the source registry.</span></span>

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

### <span data-ttu-id="9ea17-152">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9ea17-152">-Confirm</span></span>
<span data-ttu-id="9ea17-153">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9ea17-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ea17-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ea17-154">-WhatIf</span></span>
<span data-ttu-id="9ea17-155">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9ea17-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ea17-156">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9ea17-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ea17-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ea17-157">CommonParameters</span></span>
<span data-ttu-id="9ea17-158">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ea17-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ea17-159">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ea17-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ea17-160">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9ea17-160">INPUTS</span></span>

### <span data-ttu-id="9ea17-161">System. String</span><span class="sxs-lookup"><span data-stu-id="9ea17-161">System.String</span></span>

## <span data-ttu-id="9ea17-162">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9ea17-162">OUTPUTS</span></span>

### <span data-ttu-id="9ea17-163">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9ea17-163">System.Boolean</span></span>

## <span data-ttu-id="9ea17-164">Notizen</span><span class="sxs-lookup"><span data-stu-id="9ea17-164">NOTES</span></span>

## <span data-ttu-id="9ea17-165">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9ea17-165">RELATED LINKS</span></span>
