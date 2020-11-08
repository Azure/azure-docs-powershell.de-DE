---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTemplateSpec.md
ms.openlocfilehash: b19653570c7bfbf62cb94107bb2fa354a9fda3f1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177247"
---
# <span data-ttu-id="60a45-101">New-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="60a45-101">New-AzTemplateSpec</span></span>

## <span data-ttu-id="60a45-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="60a45-102">SYNOPSIS</span></span>
<span data-ttu-id="60a45-103">Erstellt eine neue Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="60a45-103">Creates a new Template Spec.</span></span>

## <span data-ttu-id="60a45-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="60a45-104">SYNTAX</span></span>

### <span data-ttu-id="60a45-105">FromJsonStringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="60a45-105">FromJsonStringParameterSet (Default)</span></span>
```
New-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] -TemplateJson <String> [-VersionDescription <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60a45-106">FromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="60a45-106">FromJsonFileParameterSet</span></span>
```
New-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] -TemplateFile <String> [-VersionDescription <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60a45-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="60a45-107">DESCRIPTION</span></span>
<span data-ttu-id="60a45-108">Erstellt eine neue Vorlagen Spezifikationsversion mit dem angegebenen Arm-Vorlageninhalt.</span><span class="sxs-lookup"><span data-stu-id="60a45-108">Creates a new Template Spec version with the specified ARM Template content.</span></span> <span data-ttu-id="60a45-109">Der Inhalt kann entweder aus einer unformatierten JSON-Zeichenfolge (unter Verwendung des **FromJsonStringParameterSet** -Parametersatzes) oder aus einer angegebenen JSON-Datei (mit **FromJsonFileParameterSet** -Parametersatz) stammen.</span><span class="sxs-lookup"><span data-stu-id="60a45-109">The content can either come from a raw JSON string (using **FromJsonStringParameterSet** parameter set) or from a specified JSON file (using **FromJsonFileParameterSet** parameter set).</span></span>  

<span data-ttu-id="60a45-110">Wenn die Stamm Vorlagenspezifikation noch nicht vorhanden ist, wird Sie zusammen mit der Vorlage spec-Version erstellt.</span><span class="sxs-lookup"><span data-stu-id="60a45-110">If the root Template Spec does not already exist it will be created along with the Template Spec version.</span></span> <span data-ttu-id="60a45-111">Wenn bereits eine Vorlagenspezifikation mit dem angegebenen Namen vorhanden ist, wird Sie und die angegebene Version aktualisiert (alle anderen vorhandenen Versionen werden beibehalten).</span><span class="sxs-lookup"><span data-stu-id="60a45-111">If a Template Spec already exists with the given name, it and the specified version will be updated (any other existing versions will be preserved).</span></span>

## <span data-ttu-id="60a45-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="60a45-112">EXAMPLES</span></span>

### <span data-ttu-id="60a45-113">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="60a45-113">Example 1:</span></span>
```powershell
PS C:\> $templateJson = @"
{
    "$schema": "http://schema.management.azure.com/schemas/2015-01-01/deploymentTemplate.json#",
    "contentVersion": "1.0.0.0",
    "parameters": {},
    "resources": []
}
"@
PS C:\> New-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v1.0' -Location 'West US' -TemplateJson $templateJson
```

<span data-ttu-id="60a45-114">Erstellt eine neue Vorlagen Spezifikationsversion "v 1.0" in einer Vorlagenspezifikation mit dem Namen "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="60a45-114">Creates a new Template Spec version "v1.0" in a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="60a45-115">Die angegebene Version hat $templateJson als Arm-Vorlageninhalt der Version.</span><span class="sxs-lookup"><span data-stu-id="60a45-115">The specified version will have $templateJson as the version's ARM Template content.</span></span>

 <span data-ttu-id="60a45-116">**Hinweis:** Bei der Arm-Vorlage im Beispiel handelt es sich um eine No-op-Datei, da Sie keine tatsächlichen Ressourcen enthält.</span><span class="sxs-lookup"><span data-stu-id="60a45-116">**Note:** The ARM Template in the example is a no-op as it contains no actual resources.</span></span>

### <span data-ttu-id="60a45-117">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="60a45-117">Example 2:</span></span>
```powershell
PS C:\> New-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v2.0' -Location 'West US' -TemplateFile 'myTemplateContent.json'
```

<span data-ttu-id="60a45-118">Erstellt eine neue Vorlagen Spezifikationsversion "v 2.0" in einer Vorlagenspezifikation mit dem Namen "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="60a45-118">Creates a new Template Spec version "v2.0" in a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="60a45-119">In der angegebenen Version ist der Inhalt der lokalen Datei "myTemplateContent.jsauf" als Inhalt der Arm-Vorlage der Version enthalten.</span><span class="sxs-lookup"><span data-stu-id="60a45-119">The specified version will have the content from the local file "myTemplateContent.json" as the version's ARM Template content.</span></span>

## <span data-ttu-id="60a45-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="60a45-120">PARAMETERS</span></span>

### <span data-ttu-id="60a45-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60a45-121">-DefaultProfile</span></span>
<span data-ttu-id="60a45-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="60a45-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60a45-123">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="60a45-123">-Description</span></span>
<span data-ttu-id="60a45-124">Die Beschreibung der Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="60a45-124">The description of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60a45-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="60a45-125">-DisplayName</span></span>
<span data-ttu-id="60a45-126">Der Anzeigename der Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="60a45-126">The display name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60a45-127">-Force</span><span class="sxs-lookup"><span data-stu-id="60a45-127">-Force</span></span>
<span data-ttu-id="60a45-128">Wenn Sie eine vorhandene Version überschreiben, müssen Sie keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="60a45-128">Do not ask for confirmation when overwriting an existing version.</span></span>

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

### <span data-ttu-id="60a45-129">-Standort</span><span class="sxs-lookup"><span data-stu-id="60a45-129">-Location</span></span>
<span data-ttu-id="60a45-130">Der Speicherort der Vorlagenspezifikation. Nur erforderlich, wenn die Vorlagenspezifikation noch nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="60a45-130">The location of the template spec. Only required if the template spec does not already exist.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60a45-131">-Name</span><span class="sxs-lookup"><span data-stu-id="60a45-131">-Name</span></span>
<span data-ttu-id="60a45-132">Der Name der Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="60a45-132">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60a45-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60a45-133">-ResourceGroupName</span></span>
<span data-ttu-id="60a45-134">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="60a45-134">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60a45-135">-Vorlagendatei</span><span class="sxs-lookup"><span data-stu-id="60a45-135">-TemplateFile</span></span>
<span data-ttu-id="60a45-136">Der Dateipfad zu der JSON-Datei für die lokale Azure Resource Manager-Vorlage.</span><span class="sxs-lookup"><span data-stu-id="60a45-136">The file path to the local Azure Resource Manager template JSON file.</span></span>

```yaml
Type: System.String
Parameter Sets: FromJsonFileParameterSet
Aliases: InputFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60a45-137">-TemplateJson</span><span class="sxs-lookup"><span data-stu-id="60a45-137">-TemplateJson</span></span>
<span data-ttu-id="60a45-138">Die Azure Resource Manager-Vorlage JSON.</span><span class="sxs-lookup"><span data-stu-id="60a45-138">The Azure Resource Manager template JSON.</span></span>

```yaml
Type: System.String
Parameter Sets: FromJsonStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60a45-139">-Version</span><span class="sxs-lookup"><span data-stu-id="60a45-139">-Version</span></span>
<span data-ttu-id="60a45-140">Die Version der Vorlagenspezifikation.</span><span class="sxs-lookup"><span data-stu-id="60a45-140">The version of the template spec.</span></span>

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

### <span data-ttu-id="60a45-141">-VersionDescription</span><span class="sxs-lookup"><span data-stu-id="60a45-141">-VersionDescription</span></span>
<span data-ttu-id="60a45-142">Die Beschreibung der Version.</span><span class="sxs-lookup"><span data-stu-id="60a45-142">The description of the version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60a45-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="60a45-143">-Confirm</span></span>
<span data-ttu-id="60a45-144">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="60a45-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60a45-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60a45-145">-WhatIf</span></span>
<span data-ttu-id="60a45-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="60a45-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="60a45-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="60a45-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60a45-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60a45-148">CommonParameters</span></span>
<span data-ttu-id="60a45-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60a45-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60a45-150">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60a45-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60a45-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="60a45-151">INPUTS</span></span>

### <span data-ttu-id="60a45-152">System. String</span><span class="sxs-lookup"><span data-stu-id="60a45-152">System.String</span></span>

## <span data-ttu-id="60a45-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="60a45-153">OUTPUTS</span></span>

### <span data-ttu-id="60a45-154">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="60a45-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="60a45-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="60a45-155">NOTES</span></span>

## <span data-ttu-id="60a45-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="60a45-156">RELATED LINKS</span></span>
