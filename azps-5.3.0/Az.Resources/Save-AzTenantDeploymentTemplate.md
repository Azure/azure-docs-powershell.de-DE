---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-aztenantdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzTenantDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzTenantDeploymentTemplate.md
ms.openlocfilehash: dcee9317e6aad113088dc3498a337e16e61b6320
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472452"
---
# <span data-ttu-id="4c379-101">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="4c379-101">Save-AzTenantDeploymentTemplate</span></span>

## <span data-ttu-id="4c379-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c379-102">SYNOPSIS</span></span>
<span data-ttu-id="4c379-103">Speichert eine Bereitstellungsvorlage in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="4c379-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="4c379-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4c379-104">SYNTAX</span></span>

### <span data-ttu-id="4c379-105">SaveByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="4c379-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzTenantDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c379-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="4c379-106">SaveByDeploymentObject</span></span>
```
Save-AzTenantDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c379-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4c379-107">DESCRIPTION</span></span>
<span data-ttu-id="4c379-108">Das **Cmdlet "Save-AzTenantDeploymentTemplate"**  speichert eine Bereitstellungsvorlage in einer JSON-Datei für eine Bereitstellung im Mandantenbereich.</span><span class="sxs-lookup"><span data-stu-id="4c379-108">The **Save-AzTenantDeploymentTemplate**  cmdlet saves a deployment template to a JSON file for a deployment at tenant scope.</span></span>

## <span data-ttu-id="4c379-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4c379-109">EXAMPLES</span></span>

### <span data-ttu-id="4c379-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4c379-110">Example 1</span></span>
```powershell
PS C:\> Save-AzTenantDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="4c379-111">Dieser Befehl ruft die Bereitstellungsvorlage von TestDeployment ab und speichert sie als JSON-Datei im aktuellen Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="4c379-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="4c379-112">Beispiel 2: Erhalten einer Bereitstellung und Speichern der Vorlage</span><span class="sxs-lookup"><span data-stu-id="4c379-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzTenantDeploymentTemplate -Name "RolesDeployment" | Save-AzTenantDeploymentTemplate
```

<span data-ttu-id="4c379-113">Dieser Befehl ruft die Bereitstellung "RolesDeployment" im aktuellen Mandantenbereich ab und speichert die Vorlage.</span><span class="sxs-lookup"><span data-stu-id="4c379-113">This command gets the deployment "RolesDeployment" at the current tenant scope and saves its template.</span></span>

## <span data-ttu-id="4c379-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c379-114">PARAMETERS</span></span>

### <span data-ttu-id="4c379-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c379-115">-DefaultProfile</span></span>
<span data-ttu-id="4c379-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4c379-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c379-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="4c379-117">-DeploymentName</span></span>
<span data-ttu-id="4c379-118">Der Bereitstellungsname.</span><span class="sxs-lookup"><span data-stu-id="4c379-118">The deployment name.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveByDeploymentName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c379-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="4c379-119">-DeploymentObject</span></span>
<span data-ttu-id="4c379-120">Das Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="4c379-120">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: SaveByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c379-121">-Force</span><span class="sxs-lookup"><span data-stu-id="4c379-121">-Force</span></span>
<span data-ttu-id="4c379-122">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="4c379-122">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c379-123">-Path</span><span class="sxs-lookup"><span data-stu-id="4c379-123">-Path</span></span>
<span data-ttu-id="4c379-124">Der Ausgabepfad der Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="4c379-124">The output path of the template file.</span></span>

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

### <span data-ttu-id="4c379-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="4c379-125">-Pre</span></span>
<span data-ttu-id="4c379-126">Gibt bei Festlegung an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch ermittelt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4c379-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c379-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c379-127">-Confirm</span></span>
<span data-ttu-id="4c379-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4c379-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c379-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4c379-129">-WhatIf</span></span>
<span data-ttu-id="4c379-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4c379-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c379-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4c379-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c379-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c379-132">CommonParameters</span></span>
<span data-ttu-id="4c379-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c379-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c379-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4c379-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c379-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4c379-135">INPUTS</span></span>

### <span data-ttu-id="4c379-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="4c379-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="4c379-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4c379-137">OUTPUTS</span></span>

### <span data-ttu-id="4c379-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="4c379-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="4c379-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4c379-139">NOTES</span></span>

## <span data-ttu-id="4c379-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4c379-140">RELATED LINKS</span></span>
