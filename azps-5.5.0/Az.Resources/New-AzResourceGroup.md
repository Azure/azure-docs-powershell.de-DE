---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
ms.openlocfilehash: 9c4bdfe189c16f3e2f6f90d3197149bdc57c78c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159961"
---
# <span data-ttu-id="4f169-101">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4f169-101">New-AzResourceGroup</span></span>

## <span data-ttu-id="4f169-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f169-102">SYNOPSIS</span></span>
<span data-ttu-id="4f169-103">Erstellt eine Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4f169-103">Creates an Azure resource group.</span></span>

## <span data-ttu-id="4f169-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4f169-104">SYNTAX</span></span>

```
New-AzResourceGroup [-Name] <String> [-Location] <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f169-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4f169-105">DESCRIPTION</span></span>
<span data-ttu-id="4f169-106">Das **Cmdlet "New-AzResourceGroup"** erstellt eine Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4f169-106">The **New-AzResourceGroup** cmdlet creates an Azure resource group.</span></span>
<span data-ttu-id="4f169-107">Sie können eine Ressourcengruppe erstellen, indem Sie nur einen Namen und einen Ort verwenden und dann das Cmdlet New-AzResource verwenden, um Ressourcen zu erstellen, die der Ressourcengruppe hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="4f169-107">You can create a resource group by using just a name and location, and then use the New-AzResource cmdlet to create resources to add to the resource group.</span></span>
<span data-ttu-id="4f169-108">Wenn Sie einer vorhandenen Ressourcengruppe eine Bereitstellung hinzufügen möchten, verwenden Sie das New-AzResourceGroupDeployment-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f169-108">To add a deployment to an existing resource group, use the New-AzResourceGroupDeployment cmdlet.</span></span> <span data-ttu-id="4f169-109">Wenn Sie einer vorhandenen Ressourcengruppe eine Ressource hinzufügen möchten, verwenden Sie das **Cmdlet "New-AzResource".**</span><span class="sxs-lookup"><span data-stu-id="4f169-109">To add a resource to an existing resource group, use the **New-AzResource** cmdlet.</span></span> <span data-ttu-id="4f169-110">Eine Azure-Ressource ist eine vom Benutzer verwaltete Azure-Entität, z. B. ein Datenbankserver, eine Datenbank oder eine Website.</span><span class="sxs-lookup"><span data-stu-id="4f169-110">An Azure resource is a user-managed Azure entity, such as a database server, database, or website.</span></span> <span data-ttu-id="4f169-111">Eine Azure-Ressourcengruppe ist eine Sammlung von Azure-Ressourcen, die als Einheit bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="4f169-111">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>

## <span data-ttu-id="4f169-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4f169-112">EXAMPLES</span></span>

### <span data-ttu-id="4f169-113">Beispiel 1: Erstellen einer leeren Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="4f169-113">Example 1: Create an empty resource group</span></span>
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US"
```

<span data-ttu-id="4f169-114">Mit diesem Befehl wird eine Ressourcengruppe erstellt, die keine Ressourcen hat.</span><span class="sxs-lookup"><span data-stu-id="4f169-114">This command creates a resource group that has no resources.</span></span> <span data-ttu-id="4f169-115">Sie können die **Cmdlets "New-AzResource"** oder **"New-AzResourceGroupDeployment"** verwenden, um dieser Ressourcengruppe Ressourcen und Bereitstellungen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="4f169-115">You can use the **New-AzResource** or **New-AzResourceGroupDeployment** cmdlets to add resources and deployments to this resource group.</span></span>

### <span data-ttu-id="4f169-116">Beispiel 2: Erstellen einer leeren Ressourcengruppe mithilfe von Positionsparametern</span><span class="sxs-lookup"><span data-stu-id="4f169-116">Example 2: Create an empty resource group using positional parameters</span></span>
```
PS> New-AzResourceGroup RG01 "South Central US"
```

<span data-ttu-id="4f169-117">Mit diesem Befehl wird eine Ressourcengruppe erstellt, die keine Ressourcen hat.</span><span class="sxs-lookup"><span data-stu-id="4f169-117">This command creates a resource group that has no resources.</span></span>

### <span data-ttu-id="4f169-118">Beispiel 3: Erstellen einer Ressourcengruppe mit Tags</span><span class="sxs-lookup"><span data-stu-id="4f169-118">Example 3: Create a resource group with tags</span></span>
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US" -Tag @{Empty=$null; Department="Marketing"}
```

<span data-ttu-id="4f169-119">Mit diesem Befehl wird eine leere Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="4f169-119">This command creates an empty resource group.</span></span> <span data-ttu-id="4f169-120">Dieser Befehl ist derselbe wie der Befehl in Beispiel 1, mit dem Ausnahme, dass er der Ressourcengruppe Tags zu weist.</span><span class="sxs-lookup"><span data-stu-id="4f169-120">This command is the same as the command in Example 1, except that it assigns tags to the resource group.</span></span> <span data-ttu-id="4f169-121">Das erste Tag namens "Leer" kann verwendet werden, um Ressourcengruppen zu identifizieren, die keine Ressourcen haben.</span><span class="sxs-lookup"><span data-stu-id="4f169-121">The first tag, named Empty, can be used to identify resource groups that have no resources.</span></span> <span data-ttu-id="4f169-122">Das zweite Tag hat den Namen "Department" und hat den Wert "Marketing".</span><span class="sxs-lookup"><span data-stu-id="4f169-122">The second tag is named Department and has a value of Marketing.</span></span> <span data-ttu-id="4f169-123">Sie können ein solches Tag verwenden, um Ressourcengruppen für Die Verwaltung oder Budgetierung zu kategorisieren.</span><span class="sxs-lookup"><span data-stu-id="4f169-123">You can use a tag such as this one to categorize resource groups for administration or budgeting.</span></span>

## <span data-ttu-id="4f169-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f169-124">PARAMETERS</span></span>

### <span data-ttu-id="4f169-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4f169-125">-ApiVersion</span></span>
<span data-ttu-id="4f169-126">Gibt die vom Ressourcenanbieter unterstützte API-Version an.</span><span class="sxs-lookup"><span data-stu-id="4f169-126">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="4f169-127">Sie können eine andere Version als die Standardversion angeben.</span><span class="sxs-lookup"><span data-stu-id="4f169-127">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="4f169-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f169-128">-DefaultProfile</span></span>
<span data-ttu-id="4f169-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="4f169-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f169-130">-Force</span><span class="sxs-lookup"><span data-stu-id="4f169-130">-Force</span></span>
<span data-ttu-id="4f169-131">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="4f169-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4f169-132">-Location</span><span class="sxs-lookup"><span data-stu-id="4f169-132">-Location</span></span>
<span data-ttu-id="4f169-133">Gibt den Speicherort der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="4f169-133">Specifies the location of the resource group.</span></span> <span data-ttu-id="4f169-134">Geben Sie einen Standort im Azure-Rechenzentrum an, z. B. "Usa, Westen" oder "Südostasien".</span><span class="sxs-lookup"><span data-stu-id="4f169-134">Specify an Azure data center location, such as West US or Southeast Asia.</span></span> <span data-ttu-id="4f169-135">Sie können eine Ressourcengruppe an einem beliebigen Ort platzieren.</span><span class="sxs-lookup"><span data-stu-id="4f169-135">You can place a resource group in any location.</span></span> <span data-ttu-id="4f169-136">Die Ressourcengruppe muss sich nicht am selben Speicherort wie Ihr Abonnement oder an demselben Speicherort wie die Ressourcen befinden.</span><span class="sxs-lookup"><span data-stu-id="4f169-136">The resource group does not have to be in the same location your Azure subscription or in the same location as its resources.</span></span>
<span data-ttu-id="4f169-137">Um festzustellen, welcher Speicherort die einzelnen Ressourcentypen unterstützt, verwenden Sie das Get-AzResourceProvider cmdlet mit dem *Parameter "ProviderNamespace".*</span><span class="sxs-lookup"><span data-stu-id="4f169-137">To determine which location supports each resource type, use the Get-AzResourceProvider cmdlet with the *ProviderNamespace* parameter.</span></span>

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

### <span data-ttu-id="4f169-138">-Name</span><span class="sxs-lookup"><span data-stu-id="4f169-138">-Name</span></span>
<span data-ttu-id="4f169-139">Gibt einen Namen für die Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="4f169-139">Specifies a name for the resource group.</span></span> <span data-ttu-id="4f169-140">Der Ressourcenname muss im Abonnement eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="4f169-140">The resource name must be unique in the subscription.</span></span> <span data-ttu-id="4f169-141">Wenn bereits eine Ressourcengruppe mit diesem Namen vorhanden ist, werden Sie vom Befehl zur Bestätigung aufgefordert, bevor Sie die vorhandene Ressourcengruppe ersetzen.</span><span class="sxs-lookup"><span data-stu-id="4f169-141">If a resource group that has that name already exists, the command prompts you for confirmation before replacing the existing resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f169-142">-Pre</span><span class="sxs-lookup"><span data-stu-id="4f169-142">-Pre</span></span>
<span data-ttu-id="4f169-143">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4f169-143">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4f169-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="4f169-144">-Tag</span></span>
<span data-ttu-id="4f169-145">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="4f169-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4f169-146">Beispiel: @{key0="value0";key1=$null;key2="value2"} Zum Hinzufügen oder Ändern eines Tags müssen Sie die Sammlung von Tags für die Ressourcengruppe ersetzen.</span><span class="sxs-lookup"><span data-stu-id="4f169-146">For example: @{key0="value0";key1=$null;key2="value2"} To add or change a tag, you must replace the collection of tags for the resource group.</span></span>
<span data-ttu-id="4f169-147">Nachdem Sie Ressourcen und Gruppen Tags zugewiesen haben, können Sie den Parameter *"Tag"* von Get-AzResource und Get-AzResourceGroup verwenden, um nach Ressourcen und Gruppen nach Tagname oder nach Name und Wert zu suchen.</span><span class="sxs-lookup"><span data-stu-id="4f169-147">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzResource and Get-AzResourceGroup to search for resources and groups by tag name or by name and value.</span></span> <span data-ttu-id="4f169-148">Sie können Kategorien verwenden, um Ihre Ressourcen zu kategorisieren, z. B. nach Abteilung oder Kostenstelle, oder um Notizen oder Kommentare zu den Ressourcen zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="4f169-148">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>
<span data-ttu-id="4f169-149">Um die vordefinierten Tags zu erhalten, verwenden Sie das Get-AzTag Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f169-149">To get your predefined tags, use the Get-AzTag cmdlet.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f169-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4f169-150">-Confirm</span></span>
<span data-ttu-id="4f169-151">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4f169-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f169-152">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4f169-152">-WhatIf</span></span>
<span data-ttu-id="4f169-153">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4f169-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f169-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4f169-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f169-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f169-155">CommonParameters</span></span>
<span data-ttu-id="4f169-156">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f169-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f169-157">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4f169-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f169-158">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4f169-158">INPUTS</span></span>

### <span data-ttu-id="4f169-159">System.String</span><span class="sxs-lookup"><span data-stu-id="4f169-159">System.String</span></span>

### <span data-ttu-id="4f169-160">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4f169-160">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4f169-161">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4f169-161">OUTPUTS</span></span>

### <span data-ttu-id="4f169-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4f169-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="4f169-163">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4f169-163">NOTES</span></span>

## <span data-ttu-id="4f169-164">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4f169-164">RELATED LINKS</span></span>

[<span data-ttu-id="4f169-165">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="4f169-165">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="4f169-166">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4f169-166">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="4f169-167">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="4f169-167">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="4f169-168">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4f169-168">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="4f169-169">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4f169-169">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)

[<span data-ttu-id="4f169-170">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4f169-170">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)
