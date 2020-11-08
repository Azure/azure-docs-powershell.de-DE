---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentTemplate.md
ms.openlocfilehash: dc6f7c5b66d72ae5c01ecbb8ec93fa737199d06e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180021"
---
# <span data-ttu-id="935c6-101">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="935c6-101">Save-AzDeploymentTemplate</span></span>

## <span data-ttu-id="935c6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="935c6-102">SYNOPSIS</span></span>
<span data-ttu-id="935c6-103">Speichert eine Bereitstellungsvorlage in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="935c6-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="935c6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="935c6-104">SYNTAX</span></span>

### <span data-ttu-id="935c6-105">SaveByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="935c6-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="935c6-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="935c6-106">SaveByDeploymentObject</span></span>
```
Save-AzDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="935c6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="935c6-107">DESCRIPTION</span></span>
<span data-ttu-id="935c6-108">Das **Save-AzDeploymentTemplate-**  Cmdlet speichert eine Bereitstellungsvorlage in einer JSON-Datei.</span><span class="sxs-lookup"><span data-stu-id="935c6-108">The **Save-AzDeploymentTemplate**  cmdlet saves a deployment template to a JSON file.</span></span>

## <span data-ttu-id="935c6-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="935c6-109">EXAMPLES</span></span>

### <span data-ttu-id="935c6-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="935c6-110">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="935c6-111">Dieser Befehl ruft die Bereitstellungsvorlage aus TestDeployment ab und speichert Sie als JSON-Datei im aktuellen Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="935c6-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="935c6-112">Beispiel 2: Abrufen einer Bereitstellung und Speichern der Vorlage</span><span class="sxs-lookup"><span data-stu-id="935c6-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzDeployment -Name "RolesDeployment" | Save-AzDeploymentTemplate
```

<span data-ttu-id="935c6-113">Dieser Befehl ruft die Bereitstellung "RolesDeployment" im aktuellen Abonnement Bereich ab und speichert dessen Vorlage.</span><span class="sxs-lookup"><span data-stu-id="935c6-113">This command gets the deployment "RolesDeployment" at the current subscription scope and saves its template.</span></span>

## <span data-ttu-id="935c6-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="935c6-114">PARAMETERS</span></span>

### <span data-ttu-id="935c6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="935c6-115">-DefaultProfile</span></span>
<span data-ttu-id="935c6-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="935c6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="935c6-117">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="935c6-117">-DeploymentName</span></span>
<span data-ttu-id="935c6-118">Der Bereitstellungsname.</span><span class="sxs-lookup"><span data-stu-id="935c6-118">The deployment name.</span></span>

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

### <span data-ttu-id="935c6-119">-Deploymentobject</span><span class="sxs-lookup"><span data-stu-id="935c6-119">-DeploymentObject</span></span>
<span data-ttu-id="935c6-120">Das Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="935c6-120">The deployment object.</span></span>

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

### <span data-ttu-id="935c6-121">-Force</span><span class="sxs-lookup"><span data-stu-id="935c6-121">-Force</span></span>
<span data-ttu-id="935c6-122">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="935c6-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="935c6-123">-Path</span><span class="sxs-lookup"><span data-stu-id="935c6-123">-Path</span></span>
<span data-ttu-id="935c6-124">Der Ausgabepfad der Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="935c6-124">The output path of the template file.</span></span>

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

### <span data-ttu-id="935c6-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="935c6-125">-Pre</span></span>
<span data-ttu-id="935c6-126">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="935c6-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="935c6-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="935c6-127">-Confirm</span></span>
<span data-ttu-id="935c6-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="935c6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="935c6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="935c6-129">-WhatIf</span></span>
<span data-ttu-id="935c6-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="935c6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="935c6-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="935c6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="935c6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="935c6-132">CommonParameters</span></span>
<span data-ttu-id="935c6-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="935c6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="935c6-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="935c6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="935c6-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="935c6-135">INPUTS</span></span>

### <span data-ttu-id="935c6-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="935c6-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="935c6-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="935c6-137">OUTPUTS</span></span>

### <span data-ttu-id="935c6-138">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="935c6-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="935c6-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="935c6-139">NOTES</span></span>

## <span data-ttu-id="935c6-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="935c6-140">RELATED LINKS</span></span>
