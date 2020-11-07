---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 8BB4AD6B-EBE3-442A-83E7-B77A31573208
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/save-azurermresourcegroupdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Save-AzureRmResourceGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Save-AzureRmResourceGroupDeploymentTemplate.md
ms.openlocfilehash: 3f73a7d4192f6e77b66698cd84f65b40bc5505fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664513"
---
# <span data-ttu-id="9310f-101">Save-AzureRmResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="9310f-101">Save-AzureRmResourceGroupDeploymentTemplate</span></span>

## <span data-ttu-id="9310f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9310f-102">SYNOPSIS</span></span>
<span data-ttu-id="9310f-103">Speichert eine Bereitstellungsvorlage einer Ressourcengruppe in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="9310f-103">Saves a resource group deployment template to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9310f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9310f-104">SYNTAX</span></span>

```
Save-AzureRmResourceGroupDeploymentTemplate -ResourceGroupName <String> -DeploymentName <String>
 [-Path <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9310f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9310f-105">DESCRIPTION</span></span>
<span data-ttu-id="9310f-106">Das Cmdlet **Save-AzureRmResourceGroupDeploymentTemplate**  speichert eine Vorlage für die Ressourcengruppen Bereitstellung in einer JSON-Datei.</span><span class="sxs-lookup"><span data-stu-id="9310f-106">The **Save-AzureRmResourceGroupDeploymentTemplate**  cmdlet saves a resource group deployment template to a JSON file.</span></span>

## <span data-ttu-id="9310f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9310f-107">EXAMPLES</span></span>

### <span data-ttu-id="9310f-108">Beispiel 1: Speichern einer Bereitstellungsvorlage</span><span class="sxs-lookup"><span data-stu-id="9310f-108">Example 1: Save a deployment template</span></span>
```
PS C:\>Save-AzureRmResourceGroupDeploymentTemplate -DeploymentName "TestDeployment" -ResourceGroupName "TestGroup"
```

<span data-ttu-id="9310f-109">Dieser Befehl ruft die Bereitstellungsvorlage aus TestDeployment ab und speichert Sie als JSON-Datei im aktuellen Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="9310f-109">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

## <span data-ttu-id="9310f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9310f-110">PARAMETERS</span></span>

### <span data-ttu-id="9310f-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9310f-111">-ApiVersion</span></span>
<span data-ttu-id="9310f-112">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="9310f-112">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="9310f-113">Wenn keine Angabe erfolgt, wird die neueste API-Version verwendet.</span><span class="sxs-lookup"><span data-stu-id="9310f-113">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="9310f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9310f-114">-DefaultProfile</span></span>
<span data-ttu-id="9310f-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9310f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9310f-116">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="9310f-116">-DeploymentName</span></span>
<span data-ttu-id="9310f-117">Gibt den Namen der Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="9310f-117">Specifies the name of the deployment.</span></span>

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

### <span data-ttu-id="9310f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="9310f-118">-Force</span></span>
<span data-ttu-id="9310f-119">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="9310f-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9310f-120">-Information</span><span class="sxs-lookup"><span data-stu-id="9310f-120">-InformationAction</span></span>
<span data-ttu-id="9310f-121">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="9310f-121">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="9310f-122">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="9310f-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9310f-123">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="9310f-123">Continue</span></span>
- <span data-ttu-id="9310f-124">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="9310f-124">Ignore</span></span>
- <span data-ttu-id="9310f-125">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="9310f-125">Inquire</span></span>
- <span data-ttu-id="9310f-126">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9310f-126">SilentlyContinue</span></span>
- <span data-ttu-id="9310f-127">Beenden</span><span class="sxs-lookup"><span data-stu-id="9310f-127">Stop</span></span>
- <span data-ttu-id="9310f-128">Anhalten</span><span class="sxs-lookup"><span data-stu-id="9310f-128">Suspend</span></span>

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

### <span data-ttu-id="9310f-129">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9310f-129">-InformationVariable</span></span>
<span data-ttu-id="9310f-130">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="9310f-130">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9310f-131">-Path</span><span class="sxs-lookup"><span data-stu-id="9310f-131">-Path</span></span>
<span data-ttu-id="9310f-132">Gibt den Ausgabepfad der Vorlagendatei an.</span><span class="sxs-lookup"><span data-stu-id="9310f-132">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="9310f-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="9310f-133">-Pre</span></span>
<span data-ttu-id="9310f-134">Gibt an, dass dieses Cmdlet Vorabversion-API-Versionen verwendet, wenn automatisch ermittelt wird, welche API-Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9310f-134">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="9310f-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9310f-135">-ResourceGroupName</span></span>
<span data-ttu-id="9310f-136">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="9310f-136">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="9310f-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9310f-137">-Confirm</span></span>
<span data-ttu-id="9310f-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9310f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9310f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9310f-139">-WhatIf</span></span>
<span data-ttu-id="9310f-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9310f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9310f-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9310f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9310f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9310f-142">CommonParameters</span></span>
<span data-ttu-id="9310f-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9310f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9310f-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9310f-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9310f-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9310f-145">INPUTS</span></span>

## <span data-ttu-id="9310f-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9310f-146">OUTPUTS</span></span>

## <span data-ttu-id="9310f-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="9310f-147">NOTES</span></span>

## <span data-ttu-id="9310f-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9310f-148">RELATED LINKS</span></span>
