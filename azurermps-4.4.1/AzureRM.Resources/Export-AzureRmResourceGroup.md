---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 63BBDF98-75FC-4A44-9FD0-95AD21ED93A6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Export-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Export-AzureRmResourceGroup.md
ms.openlocfilehash: 3b83b18bf7a795dd8df3c93a7fd2f8b25974ce35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481634"
---
# <span data-ttu-id="aaf71-101">Export-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="aaf71-101">Export-AzureRmResourceGroup</span></span>

## <span data-ttu-id="aaf71-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aaf71-102">SYNOPSIS</span></span>
<span data-ttu-id="aaf71-103">Zeichnet eine Ressourcengruppe als Vorlage auf und speichert Sie in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="aaf71-103">Captures a resource group as a template and saves it to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aaf71-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aaf71-104">SYNTAX</span></span>

```
Export-AzureRmResourceGroup -ResourceGroupName <String> [-Path <String>] [-IncludeParameterDefaultValue]
 [-IncludeComments] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aaf71-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aaf71-105">DESCRIPTION</span></span>
<span data-ttu-id="aaf71-106">Das Cmdlet **Export-AzureRmResourceGroup** erfasst die angegebene Ressourcengruppe als Vorlage und speichert Sie in einer JSON-Datei. Dies kann in Szenarien hilfreich sein, in denen Sie bereits einige Ressourcen in ihrer Ressourcengruppe erstellt haben und dann die Vorteile der Verwendung von Vorlagen gesicherten Bereitstellungen nutzen möchten.</span><span class="sxs-lookup"><span data-stu-id="aaf71-106">The **Export-AzureRmResourceGroup** cmdlet captures the specified resource group as a template and saves it to a JSON file.This can be useful in scenarios where you have already created some resources in your resource group, and then want to leverage the benefits of using template backed deployments.</span></span>
<span data-ttu-id="aaf71-107">Dieses Cmdlet bietet Ihnen einen einfachen Anfang, indem Sie die Vorlage für Ihre vorhandenen Ressourcen in der Ressourcengruppe generieren.</span><span class="sxs-lookup"><span data-stu-id="aaf71-107">This cmdlet gives you an easy start by generating the template for your existing resources in the resource group.</span></span>

<span data-ttu-id="aaf71-108">In einigen Fällen kann dieses Cmdlet einige Teile der Vorlage nicht generieren.</span><span class="sxs-lookup"><span data-stu-id="aaf71-108">There might be some cases where this cmdlet fails to generate some parts of the template.</span></span>
<span data-ttu-id="aaf71-109">Warnmeldungen informieren Sie über die fehlerhaften Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="aaf71-109">Warning messages will inform you of the resources that failed.</span></span>
<span data-ttu-id="aaf71-110">Die Vorlage wird weiterhin für die Teile generiert, die erfolgreich waren.</span><span class="sxs-lookup"><span data-stu-id="aaf71-110">The template will still be generated for the parts that were successful.</span></span>

## <span data-ttu-id="aaf71-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aaf71-111">EXAMPLES</span></span>

### <span data-ttu-id="aaf71-112">Beispiel 1: Exportieren einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="aaf71-112">Example 1: Export a resource group</span></span>
```
PS C:\>Export-AzureRmResourceGroup -ResourceGroupName "TestGroup"
```

<span data-ttu-id="aaf71-113">Dieser Befehl zeichnet die Ressourcengruppe "testgroup" als Vorlage auf und speichert Sie in einer JSON-Datei im aktuellen Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="aaf71-113">This command captures the resource group named TestGroup as a template, and saves it to a JSON file in the current directory.</span></span>

## <span data-ttu-id="aaf71-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="aaf71-114">PARAMETERS</span></span>

### <span data-ttu-id="aaf71-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="aaf71-115">-ApiVersion</span></span>
<span data-ttu-id="aaf71-116">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="aaf71-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="aaf71-117">Wenn keine Angabe erfolgt, wird die neueste API-Version verwendet.</span><span class="sxs-lookup"><span data-stu-id="aaf71-117">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="aaf71-118">-Force</span><span class="sxs-lookup"><span data-stu-id="aaf71-118">-Force</span></span>
<span data-ttu-id="aaf71-119">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="aaf71-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="aaf71-120">-IncludeComments</span><span class="sxs-lookup"><span data-stu-id="aaf71-120">-IncludeComments</span></span>
<span data-ttu-id="aaf71-121">Gibt an, dass diese Operation die Vorlage mit Kommentaren exportiert.</span><span class="sxs-lookup"><span data-stu-id="aaf71-121">Indicates that this operation exports the template with comments.</span></span>

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

### <span data-ttu-id="aaf71-122">-IncludeParameterDefaultValue</span><span class="sxs-lookup"><span data-stu-id="aaf71-122">-IncludeParameterDefaultValue</span></span>
<span data-ttu-id="aaf71-123">Gibt an, dass dieser Vorgang den Vorlagenparameter mit dem Standardwert exportiert.</span><span class="sxs-lookup"><span data-stu-id="aaf71-123">Indicates that this operation exports the template parameter with the default value.</span></span>

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

### <span data-ttu-id="aaf71-124">-Information</span><span class="sxs-lookup"><span data-stu-id="aaf71-124">-InformationAction</span></span>
<span data-ttu-id="aaf71-125">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="aaf71-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="aaf71-126">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="aaf71-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aaf71-127">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="aaf71-127">Continue</span></span>
- <span data-ttu-id="aaf71-128">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="aaf71-128">Ignore</span></span>
- <span data-ttu-id="aaf71-129">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="aaf71-129">Inquire</span></span>
- <span data-ttu-id="aaf71-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="aaf71-130">SilentlyContinue</span></span>
- <span data-ttu-id="aaf71-131">Beenden</span><span class="sxs-lookup"><span data-stu-id="aaf71-131">Stop</span></span>
- <span data-ttu-id="aaf71-132">Anhalten</span><span class="sxs-lookup"><span data-stu-id="aaf71-132">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaf71-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="aaf71-133">-InformationVariable</span></span>
<span data-ttu-id="aaf71-134">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="aaf71-134">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaf71-135">-Path</span><span class="sxs-lookup"><span data-stu-id="aaf71-135">-Path</span></span>
<span data-ttu-id="aaf71-136">Gibt den Ausgabepfad der Vorlagendatei an.</span><span class="sxs-lookup"><span data-stu-id="aaf71-136">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="aaf71-137">-Pre</span><span class="sxs-lookup"><span data-stu-id="aaf71-137">-Pre</span></span>
<span data-ttu-id="aaf71-138">Gibt an, dass dieses Cmdlet Vorabversion-API-Versionen verwendet, wenn automatisch ermittelt wird, welche API-Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="aaf71-138">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="aaf71-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaf71-139">-ResourceGroupName</span></span>
<span data-ttu-id="aaf71-140">Gibt den Namen der zu exportierenden Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="aaf71-140">Specifies the name of the resource group to export.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaf71-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="aaf71-141">-Confirm</span></span>
<span data-ttu-id="aaf71-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aaf71-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaf71-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aaf71-143">-WhatIf</span></span>
<span data-ttu-id="aaf71-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aaf71-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aaf71-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aaf71-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaf71-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaf71-146">-DefaultProfile</span></span>
<span data-ttu-id="aaf71-147">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="aaf71-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaf71-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaf71-148">CommonParameters</span></span>
<span data-ttu-id="aaf71-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaf71-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaf71-150">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaf71-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaf71-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aaf71-151">INPUTS</span></span>

## <span data-ttu-id="aaf71-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aaf71-152">OUTPUTS</span></span>

### <span data-ttu-id="aaf71-153">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="aaf71-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="aaf71-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="aaf71-154">NOTES</span></span>

## <span data-ttu-id="aaf71-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aaf71-155">RELATED LINKS</span></span>

[<span data-ttu-id="aaf71-156">Finden-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="aaf71-156">Find-AzureRmResourceGroup</span></span>](./Find-AzureRmResourceGroup.md)


