---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
ms.openlocfilehash: 0523041357becb38475bb496c94ba1fd48c5acaf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150873"
---
# <span data-ttu-id="cd001-101">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cd001-101">Set-AzResourceGroup</span></span>

## <span data-ttu-id="cd001-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd001-102">SYNOPSIS</span></span>
<span data-ttu-id="cd001-103">Ändert eine Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cd001-103">Modifies a resource group.</span></span>

## <span data-ttu-id="cd001-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cd001-104">SYNTAX</span></span>

### <span data-ttu-id="cd001-105">SetByResourceGroupName (Standard)</span><span class="sxs-lookup"><span data-stu-id="cd001-105">SetByResourceGroupName (Default)</span></span>
```
Set-AzResourceGroup -Name <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd001-106">SetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="cd001-106">SetByResourceGroupId</span></span>
```
Set-AzResourceGroup [-Tag] <Hashtable> -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd001-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cd001-107">DESCRIPTION</span></span>
<span data-ttu-id="cd001-108">Das **Cmdlet "Set-AzResourceGroup"** ändert die Eigenschaften einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cd001-108">The **Set-AzResourceGroup** cmdlet modifies the properties of a resource group.</span></span>
<span data-ttu-id="cd001-109">Sie können dieses Cmdlet verwenden, um die einer Ressourcengruppe zugeordneten Azure-Tags hinzuzufügen, zu ändern oder zu löschen.</span><span class="sxs-lookup"><span data-stu-id="cd001-109">You can use this cmdlet to add, change, or delete the Azure tags applied to a resource group.</span></span>
<span data-ttu-id="cd001-110">Geben Sie den *Parameter "Name"* an, um die Ressourcengruppe zu identifizieren, und den *Parameter "Tag",* um die Tags zu ändern.</span><span class="sxs-lookup"><span data-stu-id="cd001-110">Specify the *Name* parameter to identify the resource group and the *Tag* parameter to modify the tags.</span></span>
<span data-ttu-id="cd001-111">Sie können dieses Cmdlet nicht verwenden, um den Namen einer Ressourcengruppe zu ändern.</span><span class="sxs-lookup"><span data-stu-id="cd001-111">You cannot use this cmdlet to change the name of a resource group.</span></span>

## <span data-ttu-id="cd001-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cd001-112">EXAMPLES</span></span>

### <span data-ttu-id="cd001-113">Beispiel 1: Anwenden einer Markierung auf eine Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="cd001-113">Example 1: Apply a tag to a resource group</span></span>
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

<span data-ttu-id="cd001-114">Dieser Befehl wendet ein Tag "Department" mit dem Wert "IT" auf eine Ressourcengruppe an, die keine Tags enthält.</span><span class="sxs-lookup"><span data-stu-id="cd001-114">This command applies a Department tag with a value of IT to a resource group that has no existing tags.</span></span>

### <span data-ttu-id="cd001-115">Beispiel 2: Hinzufügen von Tags zu einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="cd001-115">Example 2: Add tags to a resource group</span></span>
```
PS C:\>$Tags = (Get-AzResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="cd001-116">In diesem Beispiel wird einer Ressourcengruppe, die vorhandene Tags enthält, ein Statustag mit dem Wert "Genehmigt" und ein "FY2016"-Tag hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="cd001-116">This example adds a Status tag with a value of Approved and an FY2016 tag to a resource group that has existing tags.</span></span> <span data-ttu-id="cd001-117">Da die von Ihnen angegebenen Tags die vorhandenen Tags ersetzen, müssen Sie die vorhandenen Tags in die neue Tagsammlung hinzufügen, da sie verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="cd001-117">Because the tags you specify replace the existing tags, you must include the existing tags in the new tag collection or you will lose them.</span></span>
<span data-ttu-id="cd001-118">Der erste Befehl ruft die Ressourcengruppe "ContosoRG" ab und verwendet die dot-Methode, um den Wert der Eigenschaft "Tags" zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="cd001-118">The first command gets the ContosoRG resource group and uses the dot method to get the value of its Tags property.</span></span> <span data-ttu-id="cd001-119">Der Befehl speichert die Tags in der $Tags Variable.</span><span class="sxs-lookup"><span data-stu-id="cd001-119">The command stores the tags in the $Tags variable.</span></span>
<span data-ttu-id="cd001-120">Der zweite Befehl ruft die Tags in der Variablen $Tags ab.</span><span class="sxs-lookup"><span data-stu-id="cd001-120">The second command gets the tags in the $Tags variable.</span></span>
<span data-ttu-id="cd001-121">Der dritte Befehl verwendet den Zuordnungsoperator += zum Hinzufügen der Tags "Status" und "FY2016" zum Array von Tags in der $Tags Variable.</span><span class="sxs-lookup"><span data-stu-id="cd001-121">The third command uses the += assignment operator to add the Status and FY2016 tags to the array of tags in the $Tags variable.</span></span>
<span data-ttu-id="cd001-122">Der vierte Befehl verwendet den *Parameter "Tag"* von **"Set-AzResourceGroup",** um die Tags in der Variablen "$Tags" auf die Ressourcengruppe "ContosoRG" anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="cd001-122">The fourth command uses the *Tag* parameter of **Set-AzResourceGroup** to apply the tags in the $Tags variable to the ContosoRG resource group.</span></span>
<span data-ttu-id="cd001-123">Der fünfte Befehl ruft alle Tags ab, die der Ressourcengruppe "ContosoRG" zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="cd001-123">The fifth command gets all of the tags applied to the ContosoRG resource group.</span></span> <span data-ttu-id="cd001-124">Die Ausgabe zeigt, dass die Ressourcengruppe das Tag "Department" und die beiden neuen Tags "Status" und "FY2015" enthält.</span><span class="sxs-lookup"><span data-stu-id="cd001-124">The output shows that the resource group has the Department tag and the two new tags, Status and FY2015.</span></span>

### <span data-ttu-id="cd001-125">Beispiel 3: Löschen aller Tags für eine Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="cd001-125">Example 3: Delete all tags for a resource group</span></span>
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{}
```

<span data-ttu-id="cd001-126">Dieser Befehl gibt den *Parameter "Tag"* mit einem leeren Hashtabellenwert an, um alle Tags aus der Ressourcengruppe "ContosoRG" zu löschen.</span><span class="sxs-lookup"><span data-stu-id="cd001-126">This command specifies the *Tag* parameter with an empty hash table value to delete all tags from the ContosoRG resource group.</span></span>

## <span data-ttu-id="cd001-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd001-127">PARAMETERS</span></span>

### <span data-ttu-id="cd001-128">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="cd001-128">-ApiVersion</span></span>
<span data-ttu-id="cd001-129">Gibt die vom Ressourcenanbieter unterstützte API-Version an.</span><span class="sxs-lookup"><span data-stu-id="cd001-129">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="cd001-130">Sie können eine andere Version als die Standardversion angeben.</span><span class="sxs-lookup"><span data-stu-id="cd001-130">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="cd001-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd001-131">-DefaultProfile</span></span>
<span data-ttu-id="cd001-132">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="cd001-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd001-133">-ID</span><span class="sxs-lookup"><span data-stu-id="cd001-133">-Id</span></span>
<span data-ttu-id="cd001-134">Gibt die ID der zu ändernden Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="cd001-134">Specifies the ID of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd001-135">-Name</span><span class="sxs-lookup"><span data-stu-id="cd001-135">-Name</span></span>
<span data-ttu-id="cd001-136">Gibt den Namen der zu ändernden Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="cd001-136">Specifies the name of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd001-137">-Pre</span><span class="sxs-lookup"><span data-stu-id="cd001-137">-Pre</span></span>
<span data-ttu-id="cd001-138">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cd001-138">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="cd001-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="cd001-139">-Tag</span></span>
<span data-ttu-id="cd001-140">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="cd001-140">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="cd001-141">Beispiel: @{key0="value0";key1=$null;key2="value2"} Ein Tag ist ein Name-Wert-Paar, das Sie erstellen und auf Ressourcen- und Ressourcengruppen anwenden können.</span><span class="sxs-lookup"><span data-stu-id="cd001-141">For example: @{key0="value0";key1=$null;key2="value2"} A tag is a name-value pair that you can create and apply to resources and resource groups.</span></span> <span data-ttu-id="cd001-142">Nachdem Sie Ressourcen und Gruppen Tags zugewiesen haben, können Sie den Parameter *"Tag"* von Get-AzResource und Get-AzResourceGroup verwenden, um nach Ressourcen und Gruppen nach Tagname oder Name und Wert zu suchen.</span><span class="sxs-lookup"><span data-stu-id="cd001-142">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzResource and Get-AzResourceGroup to search for resources and groups by tag name or name and value.</span></span> <span data-ttu-id="cd001-143">Mithilfe von Kategorien können Sie Ressourcen kategorisieren, z. B. nach Abteilung oder Kostenstelle, oder Sie können Notizen oder Kommentare zu den Ressourcen nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="cd001-143">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>
<span data-ttu-id="cd001-144">Zum Hinzufügen oder Ändern eines Tags müssen Sie die Sammlung von Tags für die Ressourcengruppe ersetzen.</span><span class="sxs-lookup"><span data-stu-id="cd001-144">To add or change a tag, you must replace the collection of tags for the resource group.</span></span> <span data-ttu-id="cd001-145">Wenn Sie ein Tag löschen möchten, geben Sie in **"Get-AzResourceGroup"** eine Hashtabelle mit allen aktuell auf die Ressourcengruppe angewendeten Tags ein, mit Ausnahme des tags, das Sie löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="cd001-145">To delete a tag, enter a hash table with all tags currently applied to the resource group, from **Get-AzResourceGroup**, except for the tag you want to delete.</span></span> <span data-ttu-id="cd001-146">Um alle Tags aus einer Ressourcengruppe zu löschen, geben Sie eine leere Hashtabelle `@{}` an:</span><span class="sxs-lookup"><span data-stu-id="cd001-146">To delete all tags from a resource group, specify an empty hash table: `@{}`.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd001-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd001-147">CommonParameters</span></span>
<span data-ttu-id="cd001-148">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd001-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd001-149">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd001-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd001-150">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cd001-150">INPUTS</span></span>

### <span data-ttu-id="cd001-151">System.String</span><span class="sxs-lookup"><span data-stu-id="cd001-151">System.String</span></span>

### <span data-ttu-id="cd001-152">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="cd001-152">System.Collections.Hashtable</span></span>

## <span data-ttu-id="cd001-153">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cd001-153">OUTPUTS</span></span>

### <span data-ttu-id="cd001-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cd001-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup</span></span>

## <span data-ttu-id="cd001-155">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cd001-155">NOTES</span></span>

## <span data-ttu-id="cd001-156">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cd001-156">RELATED LINKS</span></span>

[<span data-ttu-id="cd001-157">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="cd001-157">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="cd001-158">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cd001-158">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="cd001-159">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cd001-159">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="cd001-160">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cd001-160">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)
