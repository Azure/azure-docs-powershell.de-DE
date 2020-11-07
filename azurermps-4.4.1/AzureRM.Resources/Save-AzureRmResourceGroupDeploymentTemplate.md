---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 8BB4AD6B-EBE3-442A-83E7-B77A31573208
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Save-AzureRmResourceGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Save-AzureRmResourceGroupDeploymentTemplate.md
ms.openlocfilehash: 8f146c6516226c800f45489e1f7fa5d37173e151
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664986"
---
# <span data-ttu-id="ecc88-101">Save-AzureRmResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="ecc88-101">Save-AzureRmResourceGroupDeploymentTemplate</span></span>

## <span data-ttu-id="ecc88-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ecc88-102">SYNOPSIS</span></span>
<span data-ttu-id="ecc88-103">Speichert eine Bereitstellungsvorlage einer Ressourcengruppe in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="ecc88-103">Saves a resource group deployment template to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ecc88-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ecc88-104">SYNTAX</span></span>

```
Save-AzureRmResourceGroupDeploymentTemplate -ResourceGroupName <String> -DeploymentName <String>
 [-Path <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ecc88-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ecc88-105">DESCRIPTION</span></span>
<span data-ttu-id="ecc88-106">Das Cmdlet **Save-AzureRmResourceGroupDeploymentTemplate**  speichert eine Vorlage für die Ressourcengruppen Bereitstellung in einer JSON-Datei.</span><span class="sxs-lookup"><span data-stu-id="ecc88-106">The **Save-AzureRmResourceGroupDeploymentTemplate**  cmdlet saves a resource group deployment template to a JSON file.</span></span>

## <span data-ttu-id="ecc88-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ecc88-107">EXAMPLES</span></span>

### <span data-ttu-id="ecc88-108">Beispiel 1: Speichern einer Bereitstellungsvorlage</span><span class="sxs-lookup"><span data-stu-id="ecc88-108">Example 1: Save a deployment template</span></span>
```
PS C:\>Save-AzureRmResourceGroupDeploymentTemplate -DeploymentName "TestDeployment" -ResourceGroupName "TestGroup"
```

<span data-ttu-id="ecc88-109">Dieser Befehl ruft die Bereitstellungsvorlage aus TestDeployment ab und speichert Sie als JSON-Datei im aktuellen Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="ecc88-109">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

## <span data-ttu-id="ecc88-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ecc88-110">PARAMETERS</span></span>

### <span data-ttu-id="ecc88-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ecc88-111">-ApiVersion</span></span>
<span data-ttu-id="ecc88-112">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="ecc88-112">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="ecc88-113">Wenn keine Angabe erfolgt, wird die neueste API-Version verwendet.</span><span class="sxs-lookup"><span data-stu-id="ecc88-113">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="ecc88-114">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="ecc88-114">-DeploymentName</span></span>
<span data-ttu-id="ecc88-115">Gibt den Namen der Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="ecc88-115">Specifies the name of the deployment.</span></span>

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

### <span data-ttu-id="ecc88-116">-Force</span><span class="sxs-lookup"><span data-stu-id="ecc88-116">-Force</span></span>
<span data-ttu-id="ecc88-117">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="ecc88-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ecc88-118">-Information</span><span class="sxs-lookup"><span data-stu-id="ecc88-118">-InformationAction</span></span>
<span data-ttu-id="ecc88-119">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="ecc88-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ecc88-120">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ecc88-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ecc88-121">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="ecc88-121">Continue</span></span>
- <span data-ttu-id="ecc88-122">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="ecc88-122">Ignore</span></span>
- <span data-ttu-id="ecc88-123">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="ecc88-123">Inquire</span></span>
- <span data-ttu-id="ecc88-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ecc88-124">SilentlyContinue</span></span>
- <span data-ttu-id="ecc88-125">Beenden</span><span class="sxs-lookup"><span data-stu-id="ecc88-125">Stop</span></span>
- <span data-ttu-id="ecc88-126">Anhalten</span><span class="sxs-lookup"><span data-stu-id="ecc88-126">Suspend</span></span>

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

### <span data-ttu-id="ecc88-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ecc88-127">-InformationVariable</span></span>
<span data-ttu-id="ecc88-128">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="ecc88-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ecc88-129">-Path</span><span class="sxs-lookup"><span data-stu-id="ecc88-129">-Path</span></span>
<span data-ttu-id="ecc88-130">Gibt den Ausgabepfad der Vorlagendatei an.</span><span class="sxs-lookup"><span data-stu-id="ecc88-130">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="ecc88-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="ecc88-131">-Pre</span></span>
<span data-ttu-id="ecc88-132">Gibt an, dass dieses Cmdlet Vorabversion-API-Versionen verwendet, wenn automatisch ermittelt wird, welche API-Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ecc88-132">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="ecc88-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecc88-133">-ResourceGroupName</span></span>
<span data-ttu-id="ecc88-134">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ecc88-134">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ecc88-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ecc88-135">-Confirm</span></span>
<span data-ttu-id="ecc88-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ecc88-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecc88-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecc88-137">-WhatIf</span></span>
<span data-ttu-id="ecc88-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ecc88-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecc88-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ecc88-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecc88-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecc88-140">-DefaultProfile</span></span>
<span data-ttu-id="ecc88-141">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ecc88-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecc88-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecc88-142">CommonParameters</span></span>
<span data-ttu-id="ecc88-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecc88-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecc88-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecc88-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecc88-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ecc88-145">INPUTS</span></span>

## <span data-ttu-id="ecc88-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ecc88-146">OUTPUTS</span></span>

### <span data-ttu-id="ecc88-147">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="ecc88-147">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="ecc88-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="ecc88-148">NOTES</span></span>

## <span data-ttu-id="ecc88-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ecc88-149">RELATED LINKS</span></span>

