---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azmanagementgroupdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzManagementGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzManagementGroupDeploymentTemplate.md
ms.openlocfilehash: f45602ad2515a90e39e45edb80ca1cb0bf051f00
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301005"
---
# <span data-ttu-id="c5e2a-101">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="c5e2a-101">Save-AzManagementGroupDeploymentTemplate</span></span>

## <span data-ttu-id="c5e2a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c5e2a-102">SYNOPSIS</span></span>
<span data-ttu-id="c5e2a-103">Speichert eine Bereitstellungsvorlage in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="c5e2a-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="c5e2a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5e2a-104">SYNTAX</span></span>

### <span data-ttu-id="c5e2a-105">SaveByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c5e2a-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzManagementGroupDeploymentTemplate -ManagementGroupId <String> -DeploymentName <String> [-Path <String>]
 [-Force] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5e2a-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="c5e2a-106">SaveByDeploymentObject</span></span>
```
Save-AzManagementGroupDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5e2a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c5e2a-107">DESCRIPTION</span></span>
<span data-ttu-id="c5e2a-108">Das Cmdlet **Save-AzManagementGroupDeploymentTemplate**  speichert eine Bereitstellungsvorlage in einer JSON-Datei für eine Bereitstellung in einer Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="c5e2a-108">The **Save-AzManagementGroupDeploymentTemplate**  cmdlet saves a deployment template to a JSON file for a deployment at a management group.</span></span>

## <span data-ttu-id="c5e2a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c5e2a-109">EXAMPLES</span></span>

### <span data-ttu-id="c5e2a-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c5e2a-110">Example 1</span></span>
```powershell
PS C:\> Save-AzManagementGroupDeploymentTemplate -ManagementGroupId "myMG" -DeploymentName "TestDeployment"
```

<span data-ttu-id="c5e2a-111">Dieser Befehl ruft die Bereitstellungsvorlage aus TestDeployment ab und speichert Sie als JSON-Datei im aktuellen Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="c5e2a-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="c5e2a-112">Beispiel 2: Abrufen einer Bereitstellung und Speichern der Vorlage</span><span class="sxs-lookup"><span data-stu-id="c5e2a-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentTemplate -ManagementGroupId "myMG" -Name "RolesDeployment" | Save-AzManagementGroupDeploymentTemplate
```

<span data-ttu-id="c5e2a-113">Dieser Befehl ruft die Bereitstellung "RolesDeployment" in der Verwaltungsgruppe "myMG" ab und speichert Ihre Vorlage.</span><span class="sxs-lookup"><span data-stu-id="c5e2a-113">This command gets the deployment "RolesDeployment" at the management group "myMG" and saves its template.</span></span>

## <span data-ttu-id="c5e2a-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5e2a-114">PARAMETERS</span></span>

### <span data-ttu-id="c5e2a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5e2a-115">-DefaultProfile</span></span>
<span data-ttu-id="c5e2a-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c5e2a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5e2a-117">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="c5e2a-117">-DeploymentName</span></span>
<span data-ttu-id="c5e2a-118">Der Bereitstellungsname.</span><span class="sxs-lookup"><span data-stu-id="c5e2a-118">The deployment name.</span></span>

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

### <span data-ttu-id="c5e2a-119">-Deploymentobject</span><span class="sxs-lookup"><span data-stu-id="c5e2a-119">-DeploymentObject</span></span>
<span data-ttu-id="c5e2a-120">Das Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="c5e2a-120">The deployment object.</span></span>

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

### <span data-ttu-id="c5e2a-121">-Force</span><span class="sxs-lookup"><span data-stu-id="c5e2a-121">-Force</span></span>
<span data-ttu-id="c5e2a-122">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="c5e2a-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c5e2a-123">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="c5e2a-123">-ManagementGroupId</span></span>
<span data-ttu-id="c5e2a-124">Die Verwaltungsgruppen-ID.</span><span class="sxs-lookup"><span data-stu-id="c5e2a-124">The management group id.</span></span>

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

### <span data-ttu-id="c5e2a-125">-Path</span><span class="sxs-lookup"><span data-stu-id="c5e2a-125">-Path</span></span>
<span data-ttu-id="c5e2a-126">Der Ausgabepfad der Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="c5e2a-126">The output path of the template file.</span></span>

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

### <span data-ttu-id="c5e2a-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="c5e2a-127">-Pre</span></span>
<span data-ttu-id="c5e2a-128">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="c5e2a-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c5e2a-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c5e2a-129">-Confirm</span></span>
<span data-ttu-id="c5e2a-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c5e2a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5e2a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5e2a-131">-WhatIf</span></span>
<span data-ttu-id="c5e2a-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c5e2a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5e2a-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c5e2a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5e2a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5e2a-134">CommonParameters</span></span>
<span data-ttu-id="c5e2a-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5e2a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5e2a-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5e2a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5e2a-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c5e2a-137">INPUTS</span></span>

### <span data-ttu-id="c5e2a-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="c5e2a-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="c5e2a-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c5e2a-139">OUTPUTS</span></span>

### <span data-ttu-id="c5e2a-140">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="c5e2a-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="c5e2a-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="c5e2a-141">NOTES</span></span>

## <span data-ttu-id="c5e2a-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c5e2a-142">RELATED LINKS</span></span>
