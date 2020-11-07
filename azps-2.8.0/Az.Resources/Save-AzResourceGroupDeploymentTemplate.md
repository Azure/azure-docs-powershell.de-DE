---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8BB4AD6B-EBE3-442A-83E7-B77A31573208
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azresourcegroupdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzResourceGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzResourceGroupDeploymentTemplate.md
ms.openlocfilehash: f9532ebaffaaae6a1429cb7ce8680283572c1775
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823387"
---
# <span data-ttu-id="2b041-101">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="2b041-101">Save-AzResourceGroupDeploymentTemplate</span></span>

## <span data-ttu-id="2b041-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2b041-102">SYNOPSIS</span></span>
<span data-ttu-id="2b041-103">Speichert eine Bereitstellungsvorlage einer Ressourcengruppe in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="2b041-103">Saves a resource group deployment template to a file.</span></span>

## <span data-ttu-id="2b041-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b041-104">SYNTAX</span></span>

```
Save-AzResourceGroupDeploymentTemplate -ResourceGroupName <String> -DeploymentName <String> [-Path <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2b041-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2b041-105">DESCRIPTION</span></span>
<span data-ttu-id="2b041-106">Das Cmdlet **Save-AzResourceGroupDeploymentTemplate**  speichert eine Vorlage für die Ressourcengruppen Bereitstellung in einer JSON-Datei.</span><span class="sxs-lookup"><span data-stu-id="2b041-106">The **Save-AzResourceGroupDeploymentTemplate**  cmdlet saves a resource group deployment template to a JSON file.</span></span>

## <span data-ttu-id="2b041-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2b041-107">EXAMPLES</span></span>

### <span data-ttu-id="2b041-108">Beispiel 1: Speichern einer Bereitstellungsvorlage</span><span class="sxs-lookup"><span data-stu-id="2b041-108">Example 1: Save a deployment template</span></span>
```
PS C:\>Save-AzResourceGroupDeploymentTemplate -DeploymentName "TestDeployment" -ResourceGroupName "TestGroup"
```

<span data-ttu-id="2b041-109">Dieser Befehl ruft die Bereitstellungsvorlage aus TestDeployment ab und speichert Sie als JSON-Datei im aktuellen Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="2b041-109">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

## <span data-ttu-id="2b041-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b041-110">PARAMETERS</span></span>

### <span data-ttu-id="2b041-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2b041-111">-ApiVersion</span></span>
<span data-ttu-id="2b041-112">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="2b041-112">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="2b041-113">Wenn keine Angabe erfolgt, wird die neueste API-Version verwendet.</span><span class="sxs-lookup"><span data-stu-id="2b041-113">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="2b041-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b041-114">-DefaultProfile</span></span>
<span data-ttu-id="2b041-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="2b041-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2b041-116">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="2b041-116">-DeploymentName</span></span>
<span data-ttu-id="2b041-117">Gibt den Namen der Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="2b041-117">Specifies the name of the deployment.</span></span>

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

### <span data-ttu-id="2b041-118">-Force</span><span class="sxs-lookup"><span data-stu-id="2b041-118">-Force</span></span>
<span data-ttu-id="2b041-119">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="2b041-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2b041-120">-Path</span><span class="sxs-lookup"><span data-stu-id="2b041-120">-Path</span></span>
<span data-ttu-id="2b041-121">Gibt den Ausgabepfad der Vorlagendatei an.</span><span class="sxs-lookup"><span data-stu-id="2b041-121">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="2b041-122">-Pre</span><span class="sxs-lookup"><span data-stu-id="2b041-122">-Pre</span></span>
<span data-ttu-id="2b041-123">Gibt an, dass dieses Cmdlet Vorabversion-API-Versionen verwendet, wenn automatisch ermittelt wird, welche API-Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2b041-123">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="2b041-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b041-124">-ResourceGroupName</span></span>
<span data-ttu-id="2b041-125">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="2b041-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2b041-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2b041-126">-Confirm</span></span>
<span data-ttu-id="2b041-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2b041-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b041-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b041-128">-WhatIf</span></span>
<span data-ttu-id="2b041-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2b041-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b041-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2b041-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b041-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b041-131">CommonParameters</span></span>
<span data-ttu-id="2b041-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b041-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b041-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b041-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b041-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2b041-134">INPUTS</span></span>

### <span data-ttu-id="2b041-135">System. String</span><span class="sxs-lookup"><span data-stu-id="2b041-135">System.String</span></span>

## <span data-ttu-id="2b041-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2b041-136">OUTPUTS</span></span>

### <span data-ttu-id="2b041-137">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="2b041-137">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="2b041-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="2b041-138">NOTES</span></span>

## <span data-ttu-id="2b041-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2b041-139">RELATED LINKS</span></span>
