---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-aztenantdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzTenantDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzTenantDeploymentTemplate.md
ms.openlocfilehash: 79a60294126a990d191e4838a91c0f6554bea43b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165629"
---
# <span data-ttu-id="6cb9d-101">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="6cb9d-101">Save-AzTenantDeploymentTemplate</span></span>

## <span data-ttu-id="6cb9d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6cb9d-102">SYNOPSIS</span></span>
<span data-ttu-id="6cb9d-103">Speichert eine Bereitstellungsvorlage in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="6cb9d-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="6cb9d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6cb9d-104">SYNTAX</span></span>

### <span data-ttu-id="6cb9d-105">SaveByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="6cb9d-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzTenantDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cb9d-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="6cb9d-106">SaveByDeploymentObject</span></span>
```
Save-AzTenantDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6cb9d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6cb9d-107">DESCRIPTION</span></span>
<span data-ttu-id="6cb9d-108">Das Cmdlet **Save-AzTenantDeploymentTemplate**  speichert eine Bereitstellungsvorlage in einer JSON-Datei für eine Bereitstellung im MANDANTENBEREICH.</span><span class="sxs-lookup"><span data-stu-id="6cb9d-108">The **Save-AzTenantDeploymentTemplate**  cmdlet saves a deployment template to a JSON file for a deployment at tenant scope.</span></span>

## <span data-ttu-id="6cb9d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6cb9d-109">EXAMPLES</span></span>

### <span data-ttu-id="6cb9d-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6cb9d-110">Example 1</span></span>
```powershell
PS C:\> Save-AzTenantDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="6cb9d-111">Dieser Befehl ruft die Bereitstellungsvorlage aus TestDeployment ab und speichert Sie als JSON-Datei im aktuellen Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="6cb9d-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="6cb9d-112">Beispiel 2: Abrufen einer Bereitstellung und Speichern der Vorlage</span><span class="sxs-lookup"><span data-stu-id="6cb9d-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzTenantDeploymentTemplate -Name "RolesDeployment" | Save-AzTenantDeploymentTemplate
```

<span data-ttu-id="6cb9d-113">Dieser Befehl ruft die Bereitstellung "RolesDeployment" im aktuellen MANDANTENBEREICH ab und speichert dessen Vorlage.</span><span class="sxs-lookup"><span data-stu-id="6cb9d-113">This command gets the deployment "RolesDeployment" at the current tenant scope and saves its template.</span></span>

## <span data-ttu-id="6cb9d-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="6cb9d-114">PARAMETERS</span></span>

### <span data-ttu-id="6cb9d-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6cb9d-115">-ApiVersion</span></span>
<span data-ttu-id="6cb9d-116">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6cb9d-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="6cb9d-117">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="6cb9d-117">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cb9d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cb9d-118">-DefaultProfile</span></span>
<span data-ttu-id="6cb9d-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6cb9d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cb9d-120">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="6cb9d-120">-DeploymentName</span></span>
<span data-ttu-id="6cb9d-121">Der Bereitstellungsname.</span><span class="sxs-lookup"><span data-stu-id="6cb9d-121">The deployment name.</span></span>

```yaml
Type: String
Parameter Sets: SaveByDeploymentName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cb9d-122">-Deploymentobject</span><span class="sxs-lookup"><span data-stu-id="6cb9d-122">-DeploymentObject</span></span>
<span data-ttu-id="6cb9d-123">Das Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="6cb9d-123">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: SaveByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6cb9d-124">-Force</span><span class="sxs-lookup"><span data-stu-id="6cb9d-124">-Force</span></span>
<span data-ttu-id="6cb9d-125">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="6cb9d-125">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cb9d-126">-Path</span><span class="sxs-lookup"><span data-stu-id="6cb9d-126">-Path</span></span>
<span data-ttu-id="6cb9d-127">Der Ausgabepfad der Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="6cb9d-127">The output path of the template file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cb9d-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="6cb9d-128">-Pre</span></span>
<span data-ttu-id="6cb9d-129">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="6cb9d-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cb9d-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6cb9d-130">-Confirm</span></span>
<span data-ttu-id="6cb9d-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6cb9d-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cb9d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cb9d-132">-WhatIf</span></span>
<span data-ttu-id="6cb9d-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6cb9d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cb9d-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6cb9d-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cb9d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cb9d-135">CommonParameters</span></span>
<span data-ttu-id="6cb9d-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cb9d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cb9d-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6cb9d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cb9d-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6cb9d-138">INPUTS</span></span>

### <span data-ttu-id="6cb9d-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="6cb9d-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="6cb9d-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6cb9d-140">OUTPUTS</span></span>

### <span data-ttu-id="6cb9d-141">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="6cb9d-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="6cb9d-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="6cb9d-142">NOTES</span></span>

## <span data-ttu-id="6cb9d-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6cb9d-143">RELATED LINKS</span></span>
