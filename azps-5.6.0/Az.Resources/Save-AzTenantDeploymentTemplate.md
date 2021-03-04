---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/save-aztenantdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzTenantDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzTenantDeploymentTemplate.md
ms.openlocfilehash: f64b839e4f13a08ed1af1e73fcf4324a98b68a7c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940987"
---
# <span data-ttu-id="21f35-101">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="21f35-101">Save-AzTenantDeploymentTemplate</span></span>

## <span data-ttu-id="21f35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21f35-102">SYNOPSIS</span></span>
<span data-ttu-id="21f35-103">Speichert eine Bereitstellungsvorlage in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="21f35-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="21f35-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="21f35-104">SYNTAX</span></span>

### <span data-ttu-id="21f35-105">SaveByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="21f35-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzTenantDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21f35-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="21f35-106">SaveByDeploymentObject</span></span>
```
Save-AzTenantDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21f35-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="21f35-107">DESCRIPTION</span></span>
<span data-ttu-id="21f35-108">Das **Cmdlet Save-AzTenantDeploymentTemplate**  speichert eine Bereitstellungsvorlage in einer JSON-Datei für eine Bereitstellung im Mandantenbereich.</span><span class="sxs-lookup"><span data-stu-id="21f35-108">The **Save-AzTenantDeploymentTemplate**  cmdlet saves a deployment template to a JSON file for a deployment at tenant scope.</span></span>

## <span data-ttu-id="21f35-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="21f35-109">EXAMPLES</span></span>

### <span data-ttu-id="21f35-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="21f35-110">Example 1</span></span>
```powershell
PS C:\> Save-AzTenantDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="21f35-111">Dieser Befehl ruft die Bereitstellungsvorlage von TestDeployment ab und speichert sie als JSON-Datei im aktuellen Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="21f35-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="21f35-112">Beispiel 2: Erhalten einer Bereitstellung und Speichern der Vorlage</span><span class="sxs-lookup"><span data-stu-id="21f35-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzTenantDeploymentTemplate -Name "RolesDeployment" | Save-AzTenantDeploymentTemplate
```

<span data-ttu-id="21f35-113">Dieser Befehl ruft die Bereitstellung "RolesDeployment" im aktuellen Mandantenbereich ab und speichert seine Vorlage.</span><span class="sxs-lookup"><span data-stu-id="21f35-113">This command gets the deployment "RolesDeployment" at the current tenant scope and saves its template.</span></span>

## <span data-ttu-id="21f35-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="21f35-114">PARAMETERS</span></span>

### <span data-ttu-id="21f35-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21f35-115">-DefaultProfile</span></span>
<span data-ttu-id="21f35-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="21f35-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21f35-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="21f35-117">-DeploymentName</span></span>
<span data-ttu-id="21f35-118">Der Bereitstellungsname.</span><span class="sxs-lookup"><span data-stu-id="21f35-118">The deployment name.</span></span>

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

### <span data-ttu-id="21f35-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="21f35-119">-DeploymentObject</span></span>
<span data-ttu-id="21f35-120">Das Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="21f35-120">The deployment object.</span></span>

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

### <span data-ttu-id="21f35-121">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="21f35-121">-Force</span></span>
<span data-ttu-id="21f35-122">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="21f35-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="21f35-123">-Path</span><span class="sxs-lookup"><span data-stu-id="21f35-123">-Path</span></span>
<span data-ttu-id="21f35-124">Der Ausgabepfad der Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="21f35-124">The output path of the template file.</span></span>

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

### <span data-ttu-id="21f35-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="21f35-125">-Pre</span></span>
<span data-ttu-id="21f35-126">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="21f35-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="21f35-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="21f35-127">-Confirm</span></span>
<span data-ttu-id="21f35-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="21f35-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21f35-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21f35-129">-WhatIf</span></span>
<span data-ttu-id="21f35-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="21f35-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21f35-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="21f35-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21f35-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21f35-132">CommonParameters</span></span>
<span data-ttu-id="21f35-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21f35-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21f35-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="21f35-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21f35-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="21f35-135">INPUTS</span></span>

### <span data-ttu-id="21f35-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEployment</span><span class="sxs-lookup"><span data-stu-id="21f35-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="21f35-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="21f35-137">OUTPUTS</span></span>

### <span data-ttu-id="21f35-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="21f35-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="21f35-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="21f35-139">NOTES</span></span>

## <span data-ttu-id="21f35-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="21f35-140">RELATED LINKS</span></span>
