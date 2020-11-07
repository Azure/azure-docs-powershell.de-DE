---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-Azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzResourceGroup.md
ms.openlocfilehash: d645f430c21a1e9675a0f356cffacbad6a7b5740
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843183"
---
# <span data-ttu-id="023be-101">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="023be-101">Set-AzResourceGroup</span></span>

## <span data-ttu-id="023be-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="023be-102">SYNOPSIS</span></span>
<span data-ttu-id="023be-103">Ändert eine Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="023be-103">Modifies a resource group.</span></span>

## <span data-ttu-id="023be-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="023be-104">SYNTAX</span></span>

### <span data-ttu-id="023be-105">SetByResourceGroupName (Standard)</span><span class="sxs-lookup"><span data-stu-id="023be-105">SetByResourceGroupName (Default)</span></span>
```
Set-AzResourceGroup [-Name] <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="023be-106">SetByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="023be-106">SetByResourceGroupId</span></span>
```
Set-AzResourceGroup [-Tag] <Hashtable> [-Id] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="023be-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="023be-107">DESCRIPTION</span></span>
<span data-ttu-id="023be-108">Das Cmdlet " **Satz-AzResourceGroup** " ändert die Eigenschaften einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="023be-108">The **Set-AzResourceGroup** cmdlet modifies the properties of a resource group.</span></span>
<span data-ttu-id="023be-109">Mit diesem Cmdlet können Sie die auf eine Ressourcengruppe angewendeten Azure-Tags hinzufügen, ändern oder löschen.</span><span class="sxs-lookup"><span data-stu-id="023be-109">You can use this cmdlet to add, change, or delete the Azure tags applied to a resource group.</span></span>
<span data-ttu-id="023be-110">Geben Sie den Parameter *Name* an, um die Ressourcengruppe zu identifizieren, und den *Tag* -Parameter, um die Kategorien zu ändern.</span><span class="sxs-lookup"><span data-stu-id="023be-110">Specify the *Name* parameter to identify the resource group and the *Tag* parameter to modify the tags.</span></span>
<span data-ttu-id="023be-111">Sie können dieses Cmdlet nicht verwenden, um den Namen einer Ressourcengruppe zu ändern.</span><span class="sxs-lookup"><span data-stu-id="023be-111">You cannot use this cmdlet to change the name of a resource group.</span></span>

## <span data-ttu-id="023be-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="023be-112">EXAMPLES</span></span>

### <span data-ttu-id="023be-113">Beispiel 1: Anwenden einer Kategorie auf eine Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="023be-113">Example 1: Apply a tag to a resource group</span></span>
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

<span data-ttu-id="023be-114">Mit diesem Befehl wird eine Abteilungs Kategorie mit einem Wert auf eine Ressourcengruppe angewendet, die über keine vorhandenen Kategorien verfügt.</span><span class="sxs-lookup"><span data-stu-id="023be-114">This command applies a Department tag with a value of IT to a resource group that has no existing tags.</span></span>

### <span data-ttu-id="023be-115">Beispiel 2: Hinzufügen von Kategorien zu einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="023be-115">Example 2: Add tags to a resource group</span></span>
```
PS C:\>$Tags = (Get-AzResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="023be-116">In diesem Beispiel wird ein statustag mit dem Wert Approved und einem FY2016-Tag zu einer Ressourcengruppe hinzugefügt, die über vorhandene Tags verfügt.</span><span class="sxs-lookup"><span data-stu-id="023be-116">This example adds a Status tag with a value of Approved and an FY2016 tag to a resource group that has existing tags.</span></span> <span data-ttu-id="023be-117">Da die von Ihnen angegebenen Tags die vorhandenen Tags ersetzen, müssen Sie die vorhandenen Tags in die neue Tag-Sammlung einbeziehen, oder Sie werden verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="023be-117">Because the tags you specify replace the existing tags, you must include the existing tags in the new tag collection or you will lose them.</span></span>
<span data-ttu-id="023be-118">Der erste Befehl ruft die ContosoRG-Ressourcengruppe ab und verwendet die dot-Methode, um den Wert ihrer Tags-Eigenschaft abzurufen.</span><span class="sxs-lookup"><span data-stu-id="023be-118">The first command gets the ContosoRG resource group and uses the dot method to get the value of its Tags property.</span></span> <span data-ttu-id="023be-119">Der Befehl speichert die Tags in der $Tags-Variablen.</span><span class="sxs-lookup"><span data-stu-id="023be-119">The command stores the tags in the $Tags variable.</span></span>
<span data-ttu-id="023be-120">Der zweite Befehl ruft die Tags in der $Tags Variablen ab.</span><span class="sxs-lookup"><span data-stu-id="023be-120">The second command gets the tags in the $Tags variable.</span></span>
<span data-ttu-id="023be-121">Der dritte Befehl verwendet den + = Zuweisungsoperator, um dem Array von Tags in der $Tags Variablen die Tags "Status" und "FY2016" hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="023be-121">The third command uses the += assignment operator to add the Status and FY2016 tags to the array of tags in the $Tags variable.</span></span>
<span data-ttu-id="023be-122">Der vierte Befehl verwendet den *Tag* -Parameter von "AzResourceGroup", um die Tags in der $Tags-Variablen auf die ContosoRG **-** Ressourcengruppe anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="023be-122">The fourth command uses the *Tag* parameter of **Set-AzResourceGroup** to apply the tags in the $Tags variable to the ContosoRG resource group.</span></span>
<span data-ttu-id="023be-123">Der fünfte Befehl ruft alle auf die ContosoRG-Ressourcengruppe angewendeten Tags ab.</span><span class="sxs-lookup"><span data-stu-id="023be-123">The fifth command gets all of the tags applied to the ContosoRG resource group.</span></span> <span data-ttu-id="023be-124">Die Ausgabe zeigt, dass die Ressourcengruppe die Kategorie "Abteilung" und die beiden neuen Kategorien "Status" und "FY2015" enthält.</span><span class="sxs-lookup"><span data-stu-id="023be-124">The output shows that the resource group has the Department tag and the two new tags, Status and FY2015.</span></span>

### <span data-ttu-id="023be-125">Beispiel 3: Löschen aller Tags für eine Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="023be-125">Example 3: Delete all tags for a resource group</span></span>
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{}
```

<span data-ttu-id="023be-126">Dieser Befehl gibt den *Tag* -Parameter mit einem leeren Hashtabellenwert an, um alle Tags aus der ContosoRG-Ressourcengruppe zu löschen.</span><span class="sxs-lookup"><span data-stu-id="023be-126">This command specifies the *Tag* parameter with an empty hash table value to delete all tags from the ContosoRG resource group.</span></span>

## <span data-ttu-id="023be-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="023be-127">PARAMETERS</span></span>

### <span data-ttu-id="023be-128">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="023be-128">-ApiVersion</span></span>
<span data-ttu-id="023be-129">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="023be-129">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="023be-130">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="023be-130">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="023be-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="023be-131">-DefaultProfile</span></span>
<span data-ttu-id="023be-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="023be-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="023be-133">-ID</span><span class="sxs-lookup"><span data-stu-id="023be-133">-Id</span></span>
<span data-ttu-id="023be-134">Gibt die ID der zu ändernden Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="023be-134">Specifies the ID of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="023be-135">-Name</span><span class="sxs-lookup"><span data-stu-id="023be-135">-Name</span></span>
<span data-ttu-id="023be-136">Gibt den Namen der zu ändernden Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="023be-136">Specifies the name of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="023be-137">-Pre</span><span class="sxs-lookup"><span data-stu-id="023be-137">-Pre</span></span>
<span data-ttu-id="023be-138">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="023be-138">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="023be-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="023be-139">-Tag</span></span>
<span data-ttu-id="023be-140">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="023be-140">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="023be-141">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"} ein Tag ist ein Name-Wert-Paar, das Sie erstellen und auf Ressourcen und Ressourcengruppen anwenden können.</span><span class="sxs-lookup"><span data-stu-id="023be-141">For example: @{key0="value0";key1=$null;key2="value2"} A tag is a name-value pair that you can create and apply to resources and resource groups.</span></span> <span data-ttu-id="023be-142">Nachdem Sie Ressourcen und Gruppen Kategorien zugewiesen haben, können Sie den *Tag* -Parameter von Get-AzResource und Get-AzResourceGroup verwenden, um nach Ressourcen und Gruppen nach Tag-Name oder Name und Wert zu suchen.</span><span class="sxs-lookup"><span data-stu-id="023be-142">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzResource and Get-AzResourceGroup to search for resources and groups by tag name or name and value.</span></span> <span data-ttu-id="023be-143">Sie können Kategorien verwenden, um Ihre Ressourcen zu kategorisieren, beispielsweise nach Abteilung oder Kostenstelle, oder um Notizen oder Kommentare zu den Ressourcen zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="023be-143">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>
<span data-ttu-id="023be-144">Wenn Sie ein Tag hinzufügen oder ändern möchten, müssen Sie die Sammlung von Tags für die Ressourcengruppe ersetzen.</span><span class="sxs-lookup"><span data-stu-id="023be-144">To add or change a tag, you must replace the collection of tags for the resource group.</span></span> <span data-ttu-id="023be-145">Wenn Sie eine Kategorie löschen möchten, geben Sie eine Hashtabelle mit allen Tags, die aktuell auf die Ressourcengruppe angewendet werden, in " **Get-AzResourceGroup** " ein, mit Ausnahme der Kategorie, die Sie löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="023be-145">To delete a tag, enter a hash table with all tags currently applied to the resource group, from **Get-AzResourceGroup** , except for the tag you want to delete.</span></span> <span data-ttu-id="023be-146">Wenn Sie alle Kategorien aus einer Ressourcengruppe löschen möchten, geben Sie eine leere Hashtabelle an: `@{}` .</span><span class="sxs-lookup"><span data-stu-id="023be-146">To delete all tags from a resource group, specify an empty hash table: `@{}`.</span></span>

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

### <span data-ttu-id="023be-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="023be-147">CommonParameters</span></span>
<span data-ttu-id="023be-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="023be-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="023be-149">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="023be-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="023be-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="023be-150">INPUTS</span></span>

### <span data-ttu-id="023be-151">Keine</span><span class="sxs-lookup"><span data-stu-id="023be-151">None</span></span>

## <span data-ttu-id="023be-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="023be-152">OUTPUTS</span></span>

### <span data-ttu-id="023be-153">Microsoft. Azure. Commands. resources. Models. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="023be-153">Microsoft.Azure.Commands.Resources.Models.PSResourceGroup</span></span>

## <span data-ttu-id="023be-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="023be-154">NOTES</span></span>

## <span data-ttu-id="023be-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="023be-155">RELATED LINKS</span></span>

[<span data-ttu-id="023be-156">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="023be-156">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="023be-157">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="023be-157">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="023be-158">Neu – AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="023be-158">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="023be-159">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="023be-159">Remove-AzResourceGroup</span></span>](./Remove-AzResourceGroup.md)
