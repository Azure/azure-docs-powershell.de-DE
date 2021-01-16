---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azmanagementgroupdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzManagementGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzManagementGroupDeploymentTemplate.md
ms.openlocfilehash: f45602ad2515a90e39e45edb80ca1cb0bf051f00
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98301435"
---
# <span data-ttu-id="4e387-101">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="4e387-101">Save-AzManagementGroupDeploymentTemplate</span></span>

## <span data-ttu-id="4e387-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e387-102">SYNOPSIS</span></span>
<span data-ttu-id="4e387-103">Speichert eine Bereitstellungsvorlage in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="4e387-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="4e387-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4e387-104">SYNTAX</span></span>

### <span data-ttu-id="4e387-105">SaveByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="4e387-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzManagementGroupDeploymentTemplate -ManagementGroupId <String> -DeploymentName <String> [-Path <String>]
 [-Force] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e387-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="4e387-106">SaveByDeploymentObject</span></span>
```
Save-AzManagementGroupDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e387-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4e387-107">DESCRIPTION</span></span>
<span data-ttu-id="4e387-108">Das **Cmdlet "Save-AzManagementGroupDeploymentTemplate"**  speichert eine Bereitstellungsvorlage in einer JSON-Datei für eine Bereitstellung bei einer Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="4e387-108">The **Save-AzManagementGroupDeploymentTemplate**  cmdlet saves a deployment template to a JSON file for a deployment at a management group.</span></span>

## <span data-ttu-id="4e387-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4e387-109">EXAMPLES</span></span>

### <span data-ttu-id="4e387-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4e387-110">Example 1</span></span>
```powershell
PS C:\> Save-AzManagementGroupDeploymentTemplate -ManagementGroupId "myMG" -DeploymentName "TestDeployment"
```

<span data-ttu-id="4e387-111">Dieser Befehl ruft die Bereitstellungsvorlage von TestDeployment ab und speichert sie als JSON-Datei im aktuellen Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="4e387-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="4e387-112">Beispiel 2: Erhalten einer Bereitstellung und Speichern der Vorlage</span><span class="sxs-lookup"><span data-stu-id="4e387-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentTemplate -ManagementGroupId "myMG" -Name "RolesDeployment" | Save-AzManagementGroupDeploymentTemplate
```

<span data-ttu-id="4e387-113">Dieser Befehl ruft die Bereitstellung "RolesDeployment" bei der Verwaltungsgruppe "myMG" ab und speichert die Vorlage.</span><span class="sxs-lookup"><span data-stu-id="4e387-113">This command gets the deployment "RolesDeployment" at the management group "myMG" and saves its template.</span></span>

## <span data-ttu-id="4e387-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e387-114">PARAMETERS</span></span>

### <span data-ttu-id="4e387-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e387-115">-DefaultProfile</span></span>
<span data-ttu-id="4e387-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4e387-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e387-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="4e387-117">-DeploymentName</span></span>
<span data-ttu-id="4e387-118">Der Bereitstellungsname.</span><span class="sxs-lookup"><span data-stu-id="4e387-118">The deployment name.</span></span>

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

### <span data-ttu-id="4e387-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="4e387-119">-DeploymentObject</span></span>
<span data-ttu-id="4e387-120">Das Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="4e387-120">The deployment object.</span></span>

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

### <span data-ttu-id="4e387-121">-Force</span><span class="sxs-lookup"><span data-stu-id="4e387-121">-Force</span></span>
<span data-ttu-id="4e387-122">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="4e387-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4e387-123">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="4e387-123">-ManagementGroupId</span></span>
<span data-ttu-id="4e387-124">Die ID der Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="4e387-124">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e387-125">-Path</span><span class="sxs-lookup"><span data-stu-id="4e387-125">-Path</span></span>
<span data-ttu-id="4e387-126">Der Ausgabepfad der Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="4e387-126">The output path of the template file.</span></span>

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

### <span data-ttu-id="4e387-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="4e387-127">-Pre</span></span>
<span data-ttu-id="4e387-128">Gibt bei Festlegung an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch ermittelt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4e387-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="4e387-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e387-129">-Confirm</span></span>
<span data-ttu-id="4e387-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4e387-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e387-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4e387-131">-WhatIf</span></span>
<span data-ttu-id="4e387-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4e387-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e387-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4e387-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e387-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e387-134">CommonParameters</span></span>
<span data-ttu-id="4e387-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e387-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e387-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e387-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e387-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4e387-137">INPUTS</span></span>

### <span data-ttu-id="4e387-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="4e387-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="4e387-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4e387-139">OUTPUTS</span></span>

### <span data-ttu-id="4e387-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="4e387-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="4e387-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4e387-141">NOTES</span></span>

## <span data-ttu-id="4e387-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4e387-142">RELATED LINKS</span></span>
