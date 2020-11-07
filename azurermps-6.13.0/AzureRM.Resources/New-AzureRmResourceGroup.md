---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroup.md
ms.openlocfilehash: 7264733055322c3d5886ff57f50d22e23f932a7c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662494"
---
# <span data-ttu-id="a4596-101">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a4596-101">New-AzureRmResourceGroup</span></span>

## <span data-ttu-id="a4596-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a4596-102">SYNOPSIS</span></span>
<span data-ttu-id="a4596-103">Erstellt eine Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a4596-103">Creates an Azure resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4596-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4596-104">SYNTAX</span></span>

```
New-AzureRmResourceGroup -Name <String> -Location <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4596-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a4596-105">DESCRIPTION</span></span>
<span data-ttu-id="a4596-106">Das Cmdlet **New-AzureRmResourceGroup** erstellt eine Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a4596-106">The **New-AzureRmResourceGroup** cmdlet creates an Azure resource group.</span></span>
<span data-ttu-id="a4596-107">Sie können eine Ressourcengruppe erstellen, indem Sie nur einen Namen und einen Speicherort verwenden, und dann mithilfe des New-AzureRmResource-Cmdlets Ressourcen erstellen, die der Ressourcengruppe hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a4596-107">You can create a resource group by using just a name and location, and then use the New-AzureRmResource cmdlet to create resources to add to the resource group.</span></span>
<span data-ttu-id="a4596-108">Wenn Sie eine Bereitstellung zu einer vorhandenen Ressourcengruppe hinzufügen möchten, verwenden Sie das New-AzureRmResourceGroupDeployment-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4596-108">To add a deployment to an existing resource group, use the New-AzureRmResourceGroupDeployment cmdlet.</span></span> <span data-ttu-id="a4596-109">Wenn Sie einer vorhandenen Ressourcengruppe eine Ressource hinzufügen möchten, verwenden Sie das Cmdlet **New-AzureRmResource** .</span><span class="sxs-lookup"><span data-stu-id="a4596-109">To add a resource to an existing resource group, use the **New-AzureRmResource** cmdlet.</span></span> <span data-ttu-id="a4596-110">Eine Azure-Ressource ist eine vom Benutzer verwaltete Azure-Entität, beispielsweise ein Datenbankserver, eine Datenbank oder eine Website.</span><span class="sxs-lookup"><span data-stu-id="a4596-110">An Azure resource is a user-managed Azure entity, such as a database server, database, or website.</span></span> <span data-ttu-id="a4596-111">Eine Azure-Ressourcengruppe ist eine Sammlung von Azure-Ressourcen, die als Einheit bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a4596-111">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>

## <span data-ttu-id="a4596-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a4596-112">EXAMPLES</span></span>

### <span data-ttu-id="a4596-113">Beispiel 1: Erstellen einer leeren Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="a4596-113">Example 1: Create an empty resource group</span></span>
```
PS> New-AzureRmResourceGroup -Name RG01 -Location "South Central US"
```

<span data-ttu-id="a4596-114">Mit diesem Befehl wird eine Ressourcengruppe erstellt, die keine Ressourcen aufweist.</span><span class="sxs-lookup"><span data-stu-id="a4596-114">This command creates a resource group that has no resources.</span></span> <span data-ttu-id="a4596-115">Sie können die Cmdlets **New-AzureRmResource** oder **New-AzureRmResourceGroupDeployment** verwenden, um dieser Ressourcengruppe Ressourcen und Bereitstellungen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="a4596-115">You can use the **New-AzureRmResource** or **New-AzureRmResourceGroupDeployment** cmdlets to add resources and deployments to this resource group.</span></span>

### <span data-ttu-id="a4596-116">Beispiel 2: Erstellen einer leeren Ressourcengruppe mithilfe von Positionsparametern</span><span class="sxs-lookup"><span data-stu-id="a4596-116">Example 2: Create an empty resource group using positional parameters</span></span>
```
PS> New-AzureRmResourceGroup RG01 "South Central US"
```

<span data-ttu-id="a4596-117">Mit diesem Befehl wird eine Ressourcengruppe erstellt, die keine Ressourcen aufweist.</span><span class="sxs-lookup"><span data-stu-id="a4596-117">This command creates a resource group that has no resources.</span></span>

### <span data-ttu-id="a4596-118">Beispiel 3: Erstellen einer Ressourcengruppe mit Tags</span><span class="sxs-lookup"><span data-stu-id="a4596-118">Example 3: Create a resource group with tags</span></span>
```
PS> New-AzureRmResourceGroup -Name RG01 -Location "South Central US" -Tag @{Empty=$null; Department="Marketing"}
```

<span data-ttu-id="a4596-119">Mit diesem Befehl wird eine leere Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="a4596-119">This command creates an empty resource group.</span></span> <span data-ttu-id="a4596-120">Dieser Befehl entspricht dem Befehl in Beispiel 1, mit der Ausnahme, dass er der Ressourcengruppe Tags zuweist.</span><span class="sxs-lookup"><span data-stu-id="a4596-120">This command is the same as the command in Example 1, except that it assigns tags to the resource group.</span></span> <span data-ttu-id="a4596-121">Mit dem ersten Tag mit dem Namen Empty können Ressourcengruppen identifiziert werden, die keine Ressourcen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a4596-121">The first tag, named Empty, can be used to identify resource groups that have no resources.</span></span> <span data-ttu-id="a4596-122">Das zweite Tag hat den Namen Department und hat einen Wert für Marketing.</span><span class="sxs-lookup"><span data-stu-id="a4596-122">The second tag is named Department and has a value of Marketing.</span></span> <span data-ttu-id="a4596-123">Sie können eine Kategorie wie diese verwenden, um Ressourcengruppen für die Verwaltung oder Budgetierung zu kategorisieren.</span><span class="sxs-lookup"><span data-stu-id="a4596-123">You can use a tag such as this one to categorize resource groups for administration or budgeting.</span></span>

## <span data-ttu-id="a4596-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4596-124">PARAMETERS</span></span>

### <span data-ttu-id="a4596-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a4596-125">-ApiVersion</span></span>
<span data-ttu-id="a4596-126">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="a4596-126">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="a4596-127">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="a4596-127">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="a4596-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4596-128">-DefaultProfile</span></span>
<span data-ttu-id="a4596-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a4596-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4596-130">-Force</span><span class="sxs-lookup"><span data-stu-id="a4596-130">-Force</span></span>
<span data-ttu-id="a4596-131">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="a4596-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a4596-132">-Standort</span><span class="sxs-lookup"><span data-stu-id="a4596-132">-Location</span></span>
<span data-ttu-id="a4596-133">Gibt den Speicherort der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="a4596-133">Specifies the location of the resource group.</span></span> <span data-ttu-id="a4596-134">Geben Sie einen Azure Data Center-Standort an, beispielsweise West-oder Südostasien.</span><span class="sxs-lookup"><span data-stu-id="a4596-134">Specify an Azure data center location, such as West US or Southeast Asia.</span></span> <span data-ttu-id="a4596-135">Sie können eine Ressourcengruppe an einem beliebigen Ort platzieren.</span><span class="sxs-lookup"><span data-stu-id="a4596-135">You can place a resource group in any location.</span></span> <span data-ttu-id="a4596-136">Die Ressourcengruppe muss sich nicht am gleichen Speicherort wie das Azure-Abonnement oder am gleichen Speicherort wie die Ressourcen befinden.</span><span class="sxs-lookup"><span data-stu-id="a4596-136">The resource group does not have to be in the same location your Azure subscription or in the same location as its resources.</span></span>
<span data-ttu-id="a4596-137">Verwenden Sie das Get-AzureRmResourceProvider-Cmdlet mit dem *ProviderNamespace* -Parameter, um zu bestimmen, welcher Speicherort die einzelnen Ressourcentypen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a4596-137">To determine which location supports each resource type, use the Get-AzureRmResourceProvider cmdlet with the *ProviderNamespace* parameter.</span></span>

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

### <span data-ttu-id="a4596-138">-Name</span><span class="sxs-lookup"><span data-stu-id="a4596-138">-Name</span></span>
<span data-ttu-id="a4596-139">Gibt einen Namen für die Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="a4596-139">Specifies a name for the resource group.</span></span> <span data-ttu-id="a4596-140">Der Ressourcenname muss im Abonnement eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="a4596-140">The resource name must be unique in the subscription.</span></span> <span data-ttu-id="a4596-141">Wenn bereits eine Ressourcengruppe mit diesem Namen vorhanden ist, werden Sie vom Befehl zur Bestätigung aufgefordert, bevor die vorhandene Ressourcengruppe ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="a4596-141">If a resource group that has that name already exists, the command prompts you for confirmation before replacing the existing resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4596-142">-Pre</span><span class="sxs-lookup"><span data-stu-id="a4596-142">-Pre</span></span>
<span data-ttu-id="a4596-143">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="a4596-143">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a4596-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="a4596-144">-Tag</span></span>
<span data-ttu-id="a4596-145">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="a4596-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a4596-146">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"} um eine Kategorie hinzuzufügen oder zu ändern, müssen Sie die Sammlung von Tags für die Ressourcengruppe ersetzen.</span><span class="sxs-lookup"><span data-stu-id="a4596-146">For example: @{key0="value0";key1=$null;key2="value2"} To add or change a tag, you must replace the collection of tags for the resource group.</span></span>
<span data-ttu-id="a4596-147">Nachdem Sie Ressourcen und Gruppen Kategorien zugewiesen haben, können Sie mit dem *Tag* -Parameter von Get-AzureRmResource und Get-AzureRmResourceGroup nach Ressourcen und Gruppen nach Tag-Name oder nach Name und Wert suchen.</span><span class="sxs-lookup"><span data-stu-id="a4596-147">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzureRmResource and Get-AzureRmResourceGroup to search for resources and groups by tag name or by name and value.</span></span> <span data-ttu-id="a4596-148">Sie können Kategorien verwenden, um Ihre Ressourcen zu kategorisieren, beispielsweise nach Abteilung oder Kostenstelle, oder um Notizen oder Kommentare zu den Ressourcen zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="a4596-148">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>
<span data-ttu-id="a4596-149">Verwenden Sie das Get-AzureRMTag-Cmdlet, um ihre vordefinierten Tags abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a4596-149">To get your predefined tags, use the Get-AzureRMTag cmdlet.</span></span>

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

### <span data-ttu-id="a4596-150">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a4596-150">-Confirm</span></span>
<span data-ttu-id="a4596-151">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a4596-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4596-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4596-152">-WhatIf</span></span>
<span data-ttu-id="a4596-153">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a4596-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4596-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a4596-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4596-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4596-155">CommonParameters</span></span>
<span data-ttu-id="a4596-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4596-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4596-157">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4596-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4596-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a4596-158">INPUTS</span></span>

### <span data-ttu-id="a4596-159">Keine</span><span class="sxs-lookup"><span data-stu-id="a4596-159">None</span></span>

## <span data-ttu-id="a4596-160">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a4596-160">OUTPUTS</span></span>

### <span data-ttu-id="a4596-161">Microsoft. Azure. Commands. ResourceManagement. Models. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a4596-161">Microsoft.Azure.Commands.ResourceManagement.Models.PSResourceGroup</span></span>

## <span data-ttu-id="a4596-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="a4596-162">NOTES</span></span>

## <span data-ttu-id="a4596-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a4596-163">RELATED LINKS</span></span>

[<span data-ttu-id="a4596-164">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="a4596-164">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="a4596-165">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a4596-165">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="a4596-166">Neu – AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="a4596-166">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="a4596-167">Neu – AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a4596-167">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="a4596-168">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a4596-168">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)

[<span data-ttu-id="a4596-169">Satz-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a4596-169">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)
