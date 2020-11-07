---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceGroup.md
ms.openlocfilehash: a6fa8a27bacf5504564703d8669616f748aa95d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664439"
---
# <span data-ttu-id="ea0b2-101">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ea0b2-101">Set-AzureRmResourceGroup</span></span>

## <span data-ttu-id="ea0b2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ea0b2-102">SYNOPSIS</span></span>
<span data-ttu-id="ea0b2-103">Ändert eine Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ea0b2-103">Modifies a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea0b2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea0b2-104">SYNTAX</span></span>

### <span data-ttu-id="ea0b2-105">Listet die Ressourcengruppe auf, die auf dem Namen basiert.</span><span class="sxs-lookup"><span data-stu-id="ea0b2-105">Lists the resource group based in the name.</span></span> <span data-ttu-id="ea0b2-106">Standard</span><span class="sxs-lookup"><span data-stu-id="ea0b2-106">(Default)</span></span>
```
Set-AzureRmResourceGroup [-Name] <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea0b2-107">Listet die Ressourcengruppe auf, die in der ID basiert.</span><span class="sxs-lookup"><span data-stu-id="ea0b2-107">Lists the resource group based in the Id.</span></span>
```
Set-AzureRmResourceGroup [-Tag] <Hashtable> [-Id] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea0b2-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ea0b2-108">DESCRIPTION</span></span>
<span data-ttu-id="ea0b2-109">Das Cmdlet " **Satz-AzureRmResourceGroup** " ändert die Eigenschaften einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ea0b2-109">The **Set-AzureRmResourceGroup** cmdlet modifies the properties of a resource group.</span></span>
<span data-ttu-id="ea0b2-110">Mit diesem Cmdlet können Sie die auf eine Ressourcengruppe angewendeten Azure-Tags hinzufügen, ändern oder löschen.</span><span class="sxs-lookup"><span data-stu-id="ea0b2-110">You can use this cmdlet to add, change, or delete the Azure tags applied to a resource group.</span></span>
<span data-ttu-id="ea0b2-111">Geben Sie den Parameter *Name* an, um die Ressourcengruppe zu identifizieren, und den *Tag* -Parameter, um die Kategorien zu ändern.</span><span class="sxs-lookup"><span data-stu-id="ea0b2-111">Specify the *Name* parameter to identify the resource group and the *Tag* parameter to modify the tags.</span></span>

<span data-ttu-id="ea0b2-112">Sie können dieses Cmdlet nicht verwenden, um den Namen einer Ressourcengruppe zu ändern.</span><span class="sxs-lookup"><span data-stu-id="ea0b2-112">You cannot use this cmdlet to change the name of a resource group.</span></span>

## <span data-ttu-id="ea0b2-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ea0b2-113">EXAMPLES</span></span>

### <span data-ttu-id="ea0b2-114">Beispiel 1: Anwenden einer Kategorie auf eine Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="ea0b2-114">Example 1: Apply a tag to a resource group</span></span>
```
PS C:\>Set-AzureRmResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

<span data-ttu-id="ea0b2-115">Mit diesem Befehl wird eine Abteilungs Kategorie mit einem Wert auf eine Ressourcengruppe angewendet, die über keine vorhandenen Kategorien verfügt.</span><span class="sxs-lookup"><span data-stu-id="ea0b2-115">This command applies a Department tag with a value of IT to a resource group that has no existing tags.</span></span>

### <span data-ttu-id="ea0b2-116">Beispiel 2: Hinzufügen von Kategorien zu einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="ea0b2-116">Example 2: Add tags to a resource group</span></span>
```
PS C:\>$Tags = (Get-AzureRmResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzureRmResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzureRmResourceGroup -Name "ContosoRG").Tags
```

<span data-ttu-id="ea0b2-117">In diesem Beispiel wird ein statustag mit dem Wert Approved und einem FY2016-Tag zu einer Ressourcengruppe hinzugefügt, die über vorhandene Tags verfügt.</span><span class="sxs-lookup"><span data-stu-id="ea0b2-117">This example adds a Status tag with a value of Approved and an FY2016 tag to a resource group that has existing tags.</span></span> <span data-ttu-id="ea0b2-118">Da die von Ihnen angegebenen Tags die vorhandenen Tags ersetzen, müssen Sie die vorhandenen Tags in die neue Tag-Sammlung einbeziehen, oder Sie werden verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="ea0b2-118">Because the tags you specify replace the existing tags, you must include the existing tags in the new tag collection or you will lose them.</span></span>

<span data-ttu-id="ea0b2-119">Der erste Befehl ruft die ContosoRG-Ressourcengruppe ab und verwendet die dot-Methode, um den Wert ihrer Tags-Eigenschaft abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ea0b2-119">The first command gets the ContosoRG resource group and uses the dot method to get the value of its Tags property.</span></span> <span data-ttu-id="ea0b2-120">Der Befehl speichert die Tags in der $Tags-Variablen.</span><span class="sxs-lookup"><span data-stu-id="ea0b2-120">The command stores the tags in the $Tags variable.</span></span>

<span data-ttu-id="ea0b2-121">Der zweite Befehl ruft die Tags in der $Tags Variablen ab.</span><span class="sxs-lookup"><span data-stu-id="ea0b2-121">The second command gets the tags in the $Tags variable.</span></span>

<span data-ttu-id="ea0b2-122">Der dritte Befehl verwendet den + = Zuweisungsoperator, um dem Array von Tags in der $Tags Variablen die Tags "Status" und "FY2016" hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="ea0b2-122">The third command uses the += assignment operator to add the Status and FY2016 tags to the array of tags in the $Tags variable.</span></span>

<span data-ttu-id="ea0b2-123">Der vierte Befehl verwendet den *Tag* -Parameter von "AzureRmResourceGroup", um die Tags in der $Tags-Variablen auf die ContosoRG **-** Ressourcengruppe anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="ea0b2-123">The fourth command uses the *Tag* parameter of **Set-AzureRmResourceGroup** to apply the tags in the $Tags variable to the ContosoRG resource group.</span></span>

<span data-ttu-id="ea0b2-124">Der fünfte Befehl ruft alle auf die ContosoRG-Ressourcengruppe angewendeten Tags ab.</span><span class="sxs-lookup"><span data-stu-id="ea0b2-124">The fifth command gets all of the tags applied to the ContosoRG resource group.</span></span> <span data-ttu-id="ea0b2-125">Die Ausgabe zeigt, dass die Ressourcengruppe die Kategorie "Abteilung" und die beiden neuen Kategorien "Status" und "FY2015" enthält.</span><span class="sxs-lookup"><span data-stu-id="ea0b2-125">The output shows that the resource group has the Department tag and the two new tags, Status and FY2015.</span></span>

### <span data-ttu-id="ea0b2-126">Beispiel 3: Löschen aller Tags für eine Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="ea0b2-126">Example 3: Delete all tags for a resource group</span></span>
```
PS C:\>Set-AzureRmResourceGroup -Name "ContosoRG" -Tag @{}
```

<span data-ttu-id="ea0b2-127">Dieser Befehl gibt den *Tag* -Parameter mit einem leeren Hashtabellenwert an, um alle Tags aus der ContosoRG-Ressourcengruppe zu löschen.</span><span class="sxs-lookup"><span data-stu-id="ea0b2-127">This command specifies the *Tag* parameter with an empty hash table value to delete all tags from the ContosoRG resource group.</span></span>

## <span data-ttu-id="ea0b2-128">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea0b2-128">PARAMETERS</span></span>

### <span data-ttu-id="ea0b2-129">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ea0b2-129">-ApiVersion</span></span>
<span data-ttu-id="ea0b2-130">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="ea0b2-130">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="ea0b2-131">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="ea0b2-131">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="ea0b2-132">-ID</span><span class="sxs-lookup"><span data-stu-id="ea0b2-132">-Id</span></span>
<span data-ttu-id="ea0b2-133">Gibt die ID der zu ändernden Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ea0b2-133">Specifies the ID of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based in the Id.
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea0b2-134">-Name</span><span class="sxs-lookup"><span data-stu-id="ea0b2-134">-Name</span></span>
<span data-ttu-id="ea0b2-135">Gibt den Namen der zu ändernden Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ea0b2-135">Specifies the name of the resource group to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based in the name.
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea0b2-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="ea0b2-136">-Pre</span></span>
<span data-ttu-id="ea0b2-137">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="ea0b2-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ea0b2-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="ea0b2-138">-Tag</span></span>
<span data-ttu-id="ea0b2-139">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="ea0b2-139">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ea0b2-140">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="ea0b2-140">For example:</span></span>

<span data-ttu-id="ea0b2-141">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="ea0b2-141">@{key0="value0";key1=$null;key2="value2"}</span></span>

<span data-ttu-id="ea0b2-142">Bei einem Tag handelt es sich um ein Name-Wert-Paar, das Sie erstellen und auf Ressourcen und Ressourcengruppen anwenden können.</span><span class="sxs-lookup"><span data-stu-id="ea0b2-142">A tag is a name-value pair that you can create and apply to resources and resource groups.</span></span> <span data-ttu-id="ea0b2-143">Nachdem Sie Ressourcen und Gruppen Kategorien zugewiesen haben, können Sie den *Tag* -Parameter von Get-AzureRmResource und Get-AzureRmResourceGroup verwenden, um nach Ressourcen und Gruppen nach Tag-Name oder Name und Wert zu suchen.</span><span class="sxs-lookup"><span data-stu-id="ea0b2-143">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzureRmResource and Get-AzureRmResourceGroup to search for resources and groups by tag name or name and value.</span></span> <span data-ttu-id="ea0b2-144">Sie können Kategorien verwenden, um Ihre Ressourcen zu kategorisieren, beispielsweise nach Abteilung oder Kostenstelle, oder um Notizen oder Kommentare zu den Ressourcen zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="ea0b2-144">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>

<span data-ttu-id="ea0b2-145">Wenn Sie ein Tag hinzufügen oder ändern möchten, müssen Sie die Sammlung von Tags für die Ressourcengruppe ersetzen.</span><span class="sxs-lookup"><span data-stu-id="ea0b2-145">To add or change a tag, you must replace the collection of tags for the resource group.</span></span> <span data-ttu-id="ea0b2-146">Wenn Sie eine Kategorie löschen möchten, geben Sie eine Hashtabelle mit allen Tags, die aktuell auf die Ressourcengruppe angewendet werden, in " **Get-AzureRmResourceGroup** " ein, mit Ausnahme der Kategorie, die Sie löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="ea0b2-146">To delete a tag, enter a hash table with all tags currently applied to the resource group, from **Get-AzureRmResourceGroup** , except for the tag you want to delete.</span></span> <span data-ttu-id="ea0b2-147">Wenn Sie alle Kategorien aus einer Ressourcengruppe löschen möchten, geben Sie eine leere Hashtabelle an: `@{}` .</span><span class="sxs-lookup"><span data-stu-id="ea0b2-147">To delete all tags from a resource group, specify an empty hash table: `@{}`.</span></span>

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

### <span data-ttu-id="ea0b2-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea0b2-148">-DefaultProfile</span></span>
<span data-ttu-id="ea0b2-149">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ea0b2-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea0b2-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea0b2-150">CommonParameters</span></span>
<span data-ttu-id="ea0b2-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea0b2-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea0b2-152">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea0b2-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea0b2-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ea0b2-153">INPUTS</span></span>

### <span data-ttu-id="ea0b2-154">Keine</span><span class="sxs-lookup"><span data-stu-id="ea0b2-154">None</span></span>

## <span data-ttu-id="ea0b2-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ea0b2-155">OUTPUTS</span></span>

### <span data-ttu-id="ea0b2-156">Microsoft. Azure. Commands. resources. Models. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ea0b2-156">Microsoft.Azure.Commands.Resources.Models.PSResourceGroup</span></span>

## <span data-ttu-id="ea0b2-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="ea0b2-157">NOTES</span></span>

## <span data-ttu-id="ea0b2-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ea0b2-158">RELATED LINKS</span></span>

[<span data-ttu-id="ea0b2-159">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ea0b2-159">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="ea0b2-160">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ea0b2-160">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="ea0b2-161">Neu – AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ea0b2-161">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="ea0b2-162">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ea0b2-162">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)
