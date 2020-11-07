---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8BB4AD6B-EBE3-442A-83E7-B77A31573208
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-Azresourcegroupdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Save-AzResourceGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Save-AzResourceGroupDeploymentTemplate.md
ms.openlocfilehash: 1ffdcef1bb27ec06873c12f64a135adc0e433929
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843211"
---
# <span data-ttu-id="c05a4-101">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="c05a4-101">Save-AzResourceGroupDeploymentTemplate</span></span>

## <span data-ttu-id="c05a4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c05a4-102">SYNOPSIS</span></span>
<span data-ttu-id="c05a4-103">Speichert eine Bereitstellungsvorlage einer Ressourcengruppe in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="c05a4-103">Saves a resource group deployment template to a file.</span></span>

## <span data-ttu-id="c05a4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c05a4-104">SYNTAX</span></span>

```
Save-AzResourceGroupDeploymentTemplate -ResourceGroupName <String> -DeploymentName <String>
 [-Path <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c05a4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c05a4-105">DESCRIPTION</span></span>
<span data-ttu-id="c05a4-106">Das Cmdlet **Save-AzResourceGroupDeploymentTemplate**  speichert eine Vorlage für die Ressourcengruppen Bereitstellung in einer JSON-Datei.</span><span class="sxs-lookup"><span data-stu-id="c05a4-106">The **Save-AzResourceGroupDeploymentTemplate**  cmdlet saves a resource group deployment template to a JSON file.</span></span>

## <span data-ttu-id="c05a4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c05a4-107">EXAMPLES</span></span>

### <span data-ttu-id="c05a4-108">Beispiel 1: Speichern einer Bereitstellungsvorlage</span><span class="sxs-lookup"><span data-stu-id="c05a4-108">Example 1: Save a deployment template</span></span>
```
PS C:\>Save-AzResourceGroupDeploymentTemplate -DeploymentName "TestDeployment" -ResourceGroupName "TestGroup"
```

<span data-ttu-id="c05a4-109">Dieser Befehl ruft die Bereitstellungsvorlage aus TestDeployment ab und speichert Sie als JSON-Datei im aktuellen Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="c05a4-109">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

## <span data-ttu-id="c05a4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c05a4-110">PARAMETERS</span></span>

### <span data-ttu-id="c05a4-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c05a4-111">-ApiVersion</span></span>
<span data-ttu-id="c05a4-112">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="c05a4-112">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c05a4-113">Wenn keine Angabe erfolgt, wird die neueste API-Version verwendet.</span><span class="sxs-lookup"><span data-stu-id="c05a4-113">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="c05a4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c05a4-114">-DefaultProfile</span></span>
<span data-ttu-id="c05a4-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c05a4-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c05a4-116">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="c05a4-116">-DeploymentName</span></span>
<span data-ttu-id="c05a4-117">Gibt den Namen der Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="c05a4-117">Specifies the name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c05a4-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c05a4-118">-Force</span></span>
<span data-ttu-id="c05a4-119">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="c05a4-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c05a4-120">-Information</span><span class="sxs-lookup"><span data-stu-id="c05a4-120">-InformationAction</span></span>
<span data-ttu-id="c05a4-121">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="c05a4-121">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="c05a4-122">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c05a4-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c05a4-123">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="c05a4-123">Continue</span></span>
- <span data-ttu-id="c05a4-124">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="c05a4-124">Ignore</span></span>
- <span data-ttu-id="c05a4-125">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="c05a4-125">Inquire</span></span>
- <span data-ttu-id="c05a4-126">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c05a4-126">SilentlyContinue</span></span>
- <span data-ttu-id="c05a4-127">Beenden</span><span class="sxs-lookup"><span data-stu-id="c05a4-127">Stop</span></span>
- <span data-ttu-id="c05a4-128">Anhalten</span><span class="sxs-lookup"><span data-stu-id="c05a4-128">Suspend</span></span>

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

### <span data-ttu-id="c05a4-129">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c05a4-129">-InformationVariable</span></span>
<span data-ttu-id="c05a4-130">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="c05a4-130">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c05a4-131">-Path</span><span class="sxs-lookup"><span data-stu-id="c05a4-131">-Path</span></span>
<span data-ttu-id="c05a4-132">Gibt den Ausgabepfad der Vorlagendatei an.</span><span class="sxs-lookup"><span data-stu-id="c05a4-132">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="c05a4-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="c05a4-133">-Pre</span></span>
<span data-ttu-id="c05a4-134">Gibt an, dass dieses Cmdlet Vorabversion-API-Versionen verwendet, wenn automatisch ermittelt wird, welche API-Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c05a4-134">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="c05a4-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c05a4-135">-ResourceGroupName</span></span>
<span data-ttu-id="c05a4-136">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="c05a4-136">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c05a4-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c05a4-137">-Confirm</span></span>
<span data-ttu-id="c05a4-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c05a4-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c05a4-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c05a4-139">-WhatIf</span></span>
<span data-ttu-id="c05a4-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c05a4-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c05a4-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c05a4-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c05a4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c05a4-142">CommonParameters</span></span>
<span data-ttu-id="c05a4-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c05a4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c05a4-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c05a4-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c05a4-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c05a4-145">INPUTS</span></span>

## <span data-ttu-id="c05a4-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c05a4-146">OUTPUTS</span></span>

## <span data-ttu-id="c05a4-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="c05a4-147">NOTES</span></span>

## <span data-ttu-id="c05a4-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c05a4-148">RELATED LINKS</span></span>
