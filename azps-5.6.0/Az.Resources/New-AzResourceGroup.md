---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceGroup.md
ms.openlocfilehash: e32d5f53b13b26a93f23e4e557c6bad20911a776
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946920"
---
# <span data-ttu-id="ddfed-101">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ddfed-101">New-AzResourceGroup</span></span>

## <span data-ttu-id="ddfed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddfed-102">SYNOPSIS</span></span>
<span data-ttu-id="ddfed-103">Erstellt eine Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ddfed-103">Creates an Azure resource group.</span></span>

## <span data-ttu-id="ddfed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ddfed-104">SYNTAX</span></span>

```
New-AzResourceGroup [-Name] <String> [-Location] <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddfed-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ddfed-105">DESCRIPTION</span></span>
<span data-ttu-id="ddfed-106">Das **Cmdlet New-AzResourceGroup** erstellt eine Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ddfed-106">The **New-AzResourceGroup** cmdlet creates an Azure resource group.</span></span>
<span data-ttu-id="ddfed-107">Sie können eine Ressourcengruppe erstellen, indem Sie nur einen Namen und einen Speicherort verwenden und dann das cmdlet New-AzResource verwenden, um Ressourcen zu erstellen, die der Ressourcengruppe hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="ddfed-107">You can create a resource group by using just a name and location, and then use the New-AzResource cmdlet to create resources to add to the resource group.</span></span>
<span data-ttu-id="ddfed-108">Zum Hinzufügen einer Bereitstellung zu einer vorhandenen Ressourcengruppe verwenden Sie das New-AzResourceGroupDeployment Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddfed-108">To add a deployment to an existing resource group, use the New-AzResourceGroupDeployment cmdlet.</span></span> <span data-ttu-id="ddfed-109">Wenn Sie einer vorhandenen Ressourcengruppe eine Ressource hinzufügen möchten, verwenden Sie das **Cmdlet New-AzResource.**</span><span class="sxs-lookup"><span data-stu-id="ddfed-109">To add a resource to an existing resource group, use the **New-AzResource** cmdlet.</span></span> <span data-ttu-id="ddfed-110">Eine Azure-Ressource ist eine vom Benutzer verwaltete Azure-Entität, z. B. ein Datenbankserver, eine Datenbank oder eine Website.</span><span class="sxs-lookup"><span data-stu-id="ddfed-110">An Azure resource is a user-managed Azure entity, such as a database server, database, or website.</span></span> <span data-ttu-id="ddfed-111">Eine Azure-Ressourcengruppe ist eine Sammlung von Azure-Ressourcen, die als Einheit bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="ddfed-111">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>

## <span data-ttu-id="ddfed-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ddfed-112">EXAMPLES</span></span>

### <span data-ttu-id="ddfed-113">Beispiel 1: Erstellen einer leeren Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="ddfed-113">Example 1: Create an empty resource group</span></span>
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US"
```

<span data-ttu-id="ddfed-114">Mit diesem Befehl wird eine Ressourcengruppe ohne Ressourcen erstellt.</span><span class="sxs-lookup"><span data-stu-id="ddfed-114">This command creates a resource group that has no resources.</span></span> <span data-ttu-id="ddfed-115">Sie können die **Cmdlets New-AzResource** oder **New-AzResourceGroupDeployment** verwenden, um dieser Ressourcengruppe Ressourcen und Bereitstellungen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="ddfed-115">You can use the **New-AzResource** or **New-AzResourceGroupDeployment** cmdlets to add resources and deployments to this resource group.</span></span>

### <span data-ttu-id="ddfed-116">Beispiel 2: Erstellen einer leeren Ressourcengruppe mit Positionsparametern</span><span class="sxs-lookup"><span data-stu-id="ddfed-116">Example 2: Create an empty resource group using positional parameters</span></span>
```
PS> New-AzResourceGroup RG01 "South Central US"
```

<span data-ttu-id="ddfed-117">Mit diesem Befehl wird eine Ressourcengruppe ohne Ressourcen erstellt.</span><span class="sxs-lookup"><span data-stu-id="ddfed-117">This command creates a resource group that has no resources.</span></span>

### <span data-ttu-id="ddfed-118">Beispiel 3: Erstellen einer Ressourcengruppe mit Tags</span><span class="sxs-lookup"><span data-stu-id="ddfed-118">Example 3: Create a resource group with tags</span></span>
```
PS> New-AzResourceGroup -Name RG01 -Location "South Central US" -Tag @{Empty=$null; Department="Marketing"}
```

<span data-ttu-id="ddfed-119">Mit diesem Befehl wird eine leere Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="ddfed-119">This command creates an empty resource group.</span></span> <span data-ttu-id="ddfed-120">Dieser Befehl ist mit dem Befehl in Beispiel 1 identisch, mit der Ausnahme, dass er der Ressourcengruppe Tags zu weist.</span><span class="sxs-lookup"><span data-stu-id="ddfed-120">This command is the same as the command in Example 1, except that it assigns tags to the resource group.</span></span> <span data-ttu-id="ddfed-121">Das erste Tag mit dem Namen Leer kann verwendet werden, um Ressourcengruppen zu identifizieren, die keine Ressourcen haben.</span><span class="sxs-lookup"><span data-stu-id="ddfed-121">The first tag, named Empty, can be used to identify resource groups that have no resources.</span></span> <span data-ttu-id="ddfed-122">Das zweite Tag trägt den Namen "Abteilung" und hat den Wert "Marketing".</span><span class="sxs-lookup"><span data-stu-id="ddfed-122">The second tag is named Department and has a value of Marketing.</span></span> <span data-ttu-id="ddfed-123">Sie können ein Tag wie dieses verwenden, um Ressourcengruppen für die Verwaltung oder Budgetierung zu kategorisieren.</span><span class="sxs-lookup"><span data-stu-id="ddfed-123">You can use a tag such as this one to categorize resource groups for administration or budgeting.</span></span>

## <span data-ttu-id="ddfed-124">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ddfed-124">PARAMETERS</span></span>

### <span data-ttu-id="ddfed-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ddfed-125">-ApiVersion</span></span>
<span data-ttu-id="ddfed-126">Gibt die vom Ressourcenanbieter unterstützte API-Version an.</span><span class="sxs-lookup"><span data-stu-id="ddfed-126">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="ddfed-127">Sie können eine andere Version als die Standardversion angeben.</span><span class="sxs-lookup"><span data-stu-id="ddfed-127">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="ddfed-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddfed-128">-DefaultProfile</span></span>
<span data-ttu-id="ddfed-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="ddfed-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ddfed-130">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="ddfed-130">-Force</span></span>
<span data-ttu-id="ddfed-131">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="ddfed-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ddfed-132">-Location</span><span class="sxs-lookup"><span data-stu-id="ddfed-132">-Location</span></span>
<span data-ttu-id="ddfed-133">Gibt den Speicherort der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ddfed-133">Specifies the location of the resource group.</span></span> <span data-ttu-id="ddfed-134">Geben Sie einen Azure-Rechenzentrumsspeicherort an, z. B. West-USA oder Südostasien.</span><span class="sxs-lookup"><span data-stu-id="ddfed-134">Specify an Azure data center location, such as West US or Southeast Asia.</span></span> <span data-ttu-id="ddfed-135">Sie können eine Ressourcengruppe an einem beliebigen Speicherort platzieren.</span><span class="sxs-lookup"><span data-stu-id="ddfed-135">You can place a resource group in any location.</span></span> <span data-ttu-id="ddfed-136">Die Ressourcengruppe muss sich nicht an demselben Speicherort wie Ihr Azure-Abonnement oder an demselben Speicherort wie die Ressourcen befinden.</span><span class="sxs-lookup"><span data-stu-id="ddfed-136">The resource group does not have to be in the same location your Azure subscription or in the same location as its resources.</span></span>
<span data-ttu-id="ddfed-137">Um zu ermitteln, welcher Speicherort die einzelnen Ressourcentypen unterstützt, verwenden Get-AzResourceProvider cmdlet mit dem *Parameter ProviderNamespace.*</span><span class="sxs-lookup"><span data-stu-id="ddfed-137">To determine which location supports each resource type, use the Get-AzResourceProvider cmdlet with the *ProviderNamespace* parameter.</span></span>

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

### <span data-ttu-id="ddfed-138">-Name</span><span class="sxs-lookup"><span data-stu-id="ddfed-138">-Name</span></span>
<span data-ttu-id="ddfed-139">Gibt einen Namen für die Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ddfed-139">Specifies a name for the resource group.</span></span> <span data-ttu-id="ddfed-140">Der Ressourcenname muss im Abonnement eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="ddfed-140">The resource name must be unique in the subscription.</span></span> <span data-ttu-id="ddfed-141">Wenn eine Ressourcengruppe mit diesem Namen bereits vorhanden ist, werden Sie mit dem Befehl zur Bestätigung aufgefordert, bevor Sie die vorhandene Ressourcengruppe ersetzen.</span><span class="sxs-lookup"><span data-stu-id="ddfed-141">If a resource group that has that name already exists, the command prompts you for confirmation before replacing the existing resource group.</span></span>

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

### <span data-ttu-id="ddfed-142">-Pre</span><span class="sxs-lookup"><span data-stu-id="ddfed-142">-Pre</span></span>
<span data-ttu-id="ddfed-143">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ddfed-143">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ddfed-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="ddfed-144">-Tag</span></span>
<span data-ttu-id="ddfed-145">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="ddfed-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ddfed-146">Beispiel: @{key0="value0";key1=$null;key2="value2"} Zum Hinzufügen oder Ändern eines Tags müssen Sie die Sammlung von Tags für die Ressourcengruppe ersetzen.</span><span class="sxs-lookup"><span data-stu-id="ddfed-146">For example: @{key0="value0";key1=$null;key2="value2"} To add or change a tag, you must replace the collection of tags for the resource group.</span></span>
<span data-ttu-id="ddfed-147">Nachdem Sie Ressourcen und Gruppen Tags zugewiesen  haben, können Sie den Parameter Tag von Get-AzResource und Get-AzResourceGroup verwenden, um nach Ressourcen und Gruppen nach Dem Tagnamen oder nach Name und Wert zu suchen.</span><span class="sxs-lookup"><span data-stu-id="ddfed-147">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzResource and Get-AzResourceGroup to search for resources and groups by tag name or by name and value.</span></span> <span data-ttu-id="ddfed-148">Sie können Kategorien verwenden, um Ihre Ressourcen zu kategorisieren, z. B. nach Abteilung oder Kostenstelle, oder um Notizen oder Kommentare zu den Ressourcen nachverfolgt zu werden.</span><span class="sxs-lookup"><span data-stu-id="ddfed-148">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>
<span data-ttu-id="ddfed-149">Verwenden Sie das cmdlet Get-AzTag, um ihre vordefinierten Tags zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ddfed-149">To get your predefined tags, use the Get-AzTag cmdlet.</span></span>

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

### <span data-ttu-id="ddfed-150">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ddfed-150">-Confirm</span></span>
<span data-ttu-id="ddfed-151">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ddfed-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddfed-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddfed-152">-WhatIf</span></span>
<span data-ttu-id="ddfed-153">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ddfed-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddfed-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ddfed-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddfed-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddfed-155">CommonParameters</span></span>
<span data-ttu-id="ddfed-156">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddfed-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddfed-157">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ddfed-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddfed-158">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ddfed-158">INPUTS</span></span>

### <span data-ttu-id="ddfed-159">System.String</span><span class="sxs-lookup"><span data-stu-id="ddfed-159">System.String</span></span>

### <span data-ttu-id="ddfed-160">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="ddfed-160">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ddfed-161">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ddfed-161">OUTPUTS</span></span>

### <span data-ttu-id="ddfed-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ddfed-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="ddfed-163">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ddfed-163">NOTES</span></span>

## <span data-ttu-id="ddfed-164">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ddfed-164">RELATED LINKS</span></span>

[<span data-ttu-id="ddfed-165">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="ddfed-165">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="ddfed-166">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ddfed-166">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="ddfed-167">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="ddfed-167">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="ddfed-168">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ddfed-168">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="ddfed-169">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ddfed-169">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)

[<span data-ttu-id="ddfed-170">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ddfed-170">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)
