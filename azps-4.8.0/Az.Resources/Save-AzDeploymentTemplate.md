---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentTemplate.md
ms.openlocfilehash: aa34157f556de3fe0acc5d8197caaa1a14dc364d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165632"
---
# <span data-ttu-id="dbef1-101">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="dbef1-101">Save-AzDeploymentTemplate</span></span>

## <span data-ttu-id="dbef1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dbef1-102">SYNOPSIS</span></span>
<span data-ttu-id="dbef1-103">Speichert eine Bereitstellungsvorlage in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="dbef1-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="dbef1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dbef1-104">SYNTAX</span></span>

### <span data-ttu-id="dbef1-105">SaveByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="dbef1-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbef1-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="dbef1-106">SaveByDeploymentObject</span></span>
```
Save-AzDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbef1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dbef1-107">DESCRIPTION</span></span>
<span data-ttu-id="dbef1-108">Das **Save-AzDeploymentTemplate-**  Cmdlet speichert eine Bereitstellungsvorlage in einer JSON-Datei.</span><span class="sxs-lookup"><span data-stu-id="dbef1-108">The **Save-AzDeploymentTemplate**  cmdlet saves a deployment template to a JSON file.</span></span>

## <span data-ttu-id="dbef1-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dbef1-109">EXAMPLES</span></span>

### <span data-ttu-id="dbef1-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dbef1-110">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="dbef1-111">Dieser Befehl ruft die Bereitstellungsvorlage aus TestDeployment ab und speichert Sie als JSON-Datei im aktuellen Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="dbef1-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="dbef1-112">Beispiel 2: Abrufen einer Bereitstellung und Speichern der Vorlage</span><span class="sxs-lookup"><span data-stu-id="dbef1-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzDeployment -Name "RolesDeployment" | Save-AzDeploymentTemplate
```

<span data-ttu-id="dbef1-113">Dieser Befehl ruft die Bereitstellung "RolesDeployment" im aktuellen Abonnement Bereich ab und speichert dessen Vorlage.</span><span class="sxs-lookup"><span data-stu-id="dbef1-113">This command gets the deployment "RolesDeployment" at the current subscription scope and saves its template.</span></span>

## <span data-ttu-id="dbef1-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="dbef1-114">PARAMETERS</span></span>

### <span data-ttu-id="dbef1-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="dbef1-115">-ApiVersion</span></span>
<span data-ttu-id="dbef1-116">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dbef1-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="dbef1-117">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="dbef1-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="dbef1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbef1-118">-DefaultProfile</span></span>
<span data-ttu-id="dbef1-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dbef1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbef1-120">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="dbef1-120">-DeploymentName</span></span>
<span data-ttu-id="dbef1-121">Der Bereitstellungsname.</span><span class="sxs-lookup"><span data-stu-id="dbef1-121">The deployment name.</span></span>

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

### <span data-ttu-id="dbef1-122">-Deploymentobject</span><span class="sxs-lookup"><span data-stu-id="dbef1-122">-DeploymentObject</span></span>
<span data-ttu-id="dbef1-123">Das Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="dbef1-123">The deployment object.</span></span>

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

### <span data-ttu-id="dbef1-124">-Force</span><span class="sxs-lookup"><span data-stu-id="dbef1-124">-Force</span></span>
<span data-ttu-id="dbef1-125">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="dbef1-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="dbef1-126">-Path</span><span class="sxs-lookup"><span data-stu-id="dbef1-126">-Path</span></span>
<span data-ttu-id="dbef1-127">Der Ausgabepfad der Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="dbef1-127">The output path of the template file.</span></span>

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

### <span data-ttu-id="dbef1-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="dbef1-128">-Pre</span></span>
<span data-ttu-id="dbef1-129">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="dbef1-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="dbef1-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dbef1-130">-Confirm</span></span>
<span data-ttu-id="dbef1-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dbef1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbef1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbef1-132">-WhatIf</span></span>
<span data-ttu-id="dbef1-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dbef1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbef1-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dbef1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbef1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbef1-135">CommonParameters</span></span>
<span data-ttu-id="dbef1-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbef1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbef1-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dbef1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbef1-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dbef1-138">INPUTS</span></span>

### <span data-ttu-id="dbef1-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="dbef1-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="dbef1-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dbef1-140">OUTPUTS</span></span>

### <span data-ttu-id="dbef1-141">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="dbef1-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="dbef1-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="dbef1-142">NOTES</span></span>

## <span data-ttu-id="dbef1-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dbef1-143">RELATED LINKS</span></span>
