---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/save-azurermdeploymenttemplate
schema: 2.0.0
ms.openlocfilehash: d8adaee3e6dacafb4391f350ef567117dc3442c2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850212"
---
# <span data-ttu-id="c6108-101">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="c6108-101">Save-AzureRmDeploymentTemplate</span></span>

## <span data-ttu-id="c6108-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c6108-102">SYNOPSIS</span></span>
<span data-ttu-id="c6108-103">Speichert eine Bereitstellungsvorlage in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="c6108-103">Saves a deployment template to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6108-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6108-104">SYNTAX</span></span>

### <span data-ttu-id="c6108-105">SaveByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c6108-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzureRmDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6108-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="c6108-106">SaveByDeploymentObject</span></span>
```
Save-AzureRmDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c6108-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c6108-107">DESCRIPTION</span></span>
<span data-ttu-id="c6108-108">Das **Save-AzureRmDeploymentTemplate-**  Cmdlet speichert eine Bereitstellungsvorlage in einer JSON-Datei.</span><span class="sxs-lookup"><span data-stu-id="c6108-108">The **Save-AzureRmDeploymentTemplate**  cmdlet saves a deployment template to a JSON file.</span></span>

## <span data-ttu-id="c6108-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c6108-109">EXAMPLES</span></span>

### <span data-ttu-id="c6108-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c6108-110">Example 1</span></span>
```powershell
PS C:\> Save-AzureRmDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="c6108-111">Dieser Befehl ruft die Bereitstellungsvorlage aus TestDeployment ab und speichert Sie als JSON-Datei im aktuellen Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="c6108-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="c6108-112">Beispiel 2: Abrufen einer Bereitstellung und Speichern der Vorlage</span><span class="sxs-lookup"><span data-stu-id="c6108-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzureRmDeployment -Name "RolesDeployment" | Save-AzureRmDeploymentTemplate
```

<span data-ttu-id="c6108-113">Dieser Befehl ruft die Bereitstellung "RolesDeployment" im aktuellen Abonnement Bereich ab und speichert dessen Vorlage.</span><span class="sxs-lookup"><span data-stu-id="c6108-113">This command gets the deployment "RolesDeployment" at the current subscription scope and saves its template.</span></span>

## <span data-ttu-id="c6108-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6108-114">PARAMETERS</span></span>

### <span data-ttu-id="c6108-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c6108-115">-ApiVersion</span></span>
<span data-ttu-id="c6108-116">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c6108-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="c6108-117">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="c6108-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="c6108-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6108-118">-DefaultProfile</span></span>
<span data-ttu-id="c6108-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c6108-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6108-120">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="c6108-120">-DeploymentName</span></span>
<span data-ttu-id="c6108-121">Der Bereitstellungsname.</span><span class="sxs-lookup"><span data-stu-id="c6108-121">The deployment name.</span></span>

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

### <span data-ttu-id="c6108-122">-Deploymentobject</span><span class="sxs-lookup"><span data-stu-id="c6108-122">-DeploymentObject</span></span>
<span data-ttu-id="c6108-123">Das Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="c6108-123">The deployment object.</span></span>

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

### <span data-ttu-id="c6108-124">-Force</span><span class="sxs-lookup"><span data-stu-id="c6108-124">-Force</span></span>
<span data-ttu-id="c6108-125">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="c6108-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c6108-126">-Path</span><span class="sxs-lookup"><span data-stu-id="c6108-126">-Path</span></span>
<span data-ttu-id="c6108-127">Der Ausgabepfad der Vorlagendatei.</span><span class="sxs-lookup"><span data-stu-id="c6108-127">The output path of the template file.</span></span>

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

### <span data-ttu-id="c6108-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="c6108-128">-Pre</span></span>
<span data-ttu-id="c6108-129">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="c6108-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c6108-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c6108-130">-Confirm</span></span>
<span data-ttu-id="c6108-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c6108-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6108-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6108-132">-WhatIf</span></span>
<span data-ttu-id="c6108-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c6108-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6108-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c6108-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6108-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6108-135">CommonParameters</span></span>
<span data-ttu-id="c6108-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6108-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6108-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6108-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6108-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c6108-138">INPUTS</span></span>

### <span data-ttu-id="c6108-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c6108-139">System.String</span></span>

## <span data-ttu-id="c6108-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c6108-140">OUTPUTS</span></span>

### <span data-ttu-id="c6108-141">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels</span><span class="sxs-lookup"><span data-stu-id="c6108-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels</span></span>

## <span data-ttu-id="c6108-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="c6108-142">NOTES</span></span>

## <span data-ttu-id="c6108-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c6108-143">RELATED LINKS</span></span>
