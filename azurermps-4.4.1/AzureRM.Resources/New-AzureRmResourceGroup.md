---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroup.md
ms.openlocfilehash: ccb0b4afdf39510461dd0f6627748492ba22818f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496933"
---
# <span data-ttu-id="f0959-101">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f0959-101">New-AzureRmResourceGroup</span></span>

## <span data-ttu-id="f0959-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f0959-102">SYNOPSIS</span></span>
<span data-ttu-id="f0959-103">Erstellt eine Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f0959-103">Creates an Azure resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0959-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0959-104">SYNTAX</span></span>

```
New-AzureRmResourceGroup -Name <String> -Location <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0959-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f0959-105">DESCRIPTION</span></span>
<span data-ttu-id="f0959-106">Das Cmdlet **New-AzureRmResourceGroup** erstellt eine Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f0959-106">The **New-AzureRmResourceGroup** cmdlet creates an Azure resource group.</span></span>

<span data-ttu-id="f0959-107">Sie können eine Ressourcengruppe erstellen, indem Sie nur einen Namen und einen Speicherort verwenden, und dann mithilfe des New-AzureRmResource-Cmdlets Ressourcen erstellen, die der Ressourcengruppe hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f0959-107">You can create a resource group by using just a name and location, and then use the New-AzureRmResource cmdlet to create resources to add to the resource group.</span></span>

<span data-ttu-id="f0959-108">Wenn Sie eine Bereitstellung zu einer vorhandenen Ressourcengruppe hinzufügen möchten, verwenden Sie das New-AzureRmResourceGroupDeployment-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0959-108">To add a deployment to an existing resource group, use the New-AzureRmResourceGroupDeployment cmdlet.</span></span> <span data-ttu-id="f0959-109">Wenn Sie einer vorhandenen Ressourcengruppe eine Ressource hinzufügen möchten, verwenden Sie das Cmdlet **New-AzureRmResource** .</span><span class="sxs-lookup"><span data-stu-id="f0959-109">To add a resource to an existing resource group, use the **New-AzureRmResource** cmdlet.</span></span> <span data-ttu-id="f0959-110">Eine Azure-Ressource ist eine vom Benutzer verwaltete Azure-Entität, beispielsweise ein Datenbankserver, eine Datenbank oder eine Website.</span><span class="sxs-lookup"><span data-stu-id="f0959-110">An Azure resource is a user-managed Azure entity, such as a database server, database, or website.</span></span> <span data-ttu-id="f0959-111">Eine Azure-Ressourcengruppe ist eine Sammlung von Azure-Ressourcen, die als Einheit bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="f0959-111">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>

## <span data-ttu-id="f0959-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f0959-112">EXAMPLES</span></span>

### <span data-ttu-id="f0959-113">Beispiel 1: Erstellen einer leeren Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="f0959-113">Example 1: Create an empty resource group</span></span>
```
PS C:\>New-AzureRmResourceGroup -Name "RG01" -Location "South Central US"
```

<span data-ttu-id="f0959-114">Mit diesem Befehl wird eine Ressourcengruppe erstellt, die keine Ressourcen aufweist.</span><span class="sxs-lookup"><span data-stu-id="f0959-114">This command creates a resource group that has no resources.</span></span> <span data-ttu-id="f0959-115">Sie können die Cmdlets **New-AzureRmResource** oder **New-AzureRmResourceGroupDeployment** verwenden, um dieser Ressourcengruppe Ressourcen und Bereitstellungen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="f0959-115">You can use the **New-AzureRmResource** or **New-AzureRmResourceGroupDeployment** cmdlets to add resources and deployments to this resource group.</span></span>

### <span data-ttu-id="f0959-116">Beispiel 2: Erstellen einer Ressourcengruppe mit Tags</span><span class="sxs-lookup"><span data-stu-id="f0959-116">Example 2: Create a resource group with tags</span></span>
```
PS C:\>New-AzureRmResourceGroup -Name "RG01" -Location "South Central US" -Tag @{"Empty"=$null; "Department"="Marketing"}
```

<span data-ttu-id="f0959-117">Mit diesem Befehl wird eine leere Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="f0959-117">This command creates an empty resource group.</span></span> <span data-ttu-id="f0959-118">Dieser Befehl entspricht dem Befehl in Beispiel 1, mit der Ausnahme, dass er der Ressourcengruppe Tags zuweist.</span><span class="sxs-lookup"><span data-stu-id="f0959-118">This command is the same as the command in Example 1, except that it assigns tags to the resource group.</span></span> <span data-ttu-id="f0959-119">Mit dem ersten Tag mit dem Namen Empty können Ressourcengruppen identifiziert werden, die keine Ressourcen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="f0959-119">The first tag, named Empty, can be used to identify resource groups that have no resources.</span></span> <span data-ttu-id="f0959-120">Das zweite Tag hat den Namen Department und hat einen Wert für Marketing.</span><span class="sxs-lookup"><span data-stu-id="f0959-120">The second tag is named Department and has a value of Marketing.</span></span> <span data-ttu-id="f0959-121">Sie können eine Kategorie wie diese verwenden, um Ressourcengruppen für die Verwaltung oder Budgetierung zu kategorisieren.</span><span class="sxs-lookup"><span data-stu-id="f0959-121">You can use a tag such as this one to categorize resource groups for administration or budgeting.</span></span>

## <span data-ttu-id="f0959-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0959-122">PARAMETERS</span></span>

### <span data-ttu-id="f0959-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f0959-123">-ApiVersion</span></span>
<span data-ttu-id="f0959-124">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="f0959-124">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="f0959-125">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="f0959-125">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="f0959-126">-Force</span><span class="sxs-lookup"><span data-stu-id="f0959-126">-Force</span></span>
<span data-ttu-id="f0959-127">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="f0959-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f0959-128">-Standort</span><span class="sxs-lookup"><span data-stu-id="f0959-128">-Location</span></span>
<span data-ttu-id="f0959-129">Gibt den Speicherort der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="f0959-129">Specifies the location of the resource group.</span></span> <span data-ttu-id="f0959-130">Geben Sie einen Azure Data Center-Standort an, beispielsweise West-oder Südostasien.</span><span class="sxs-lookup"><span data-stu-id="f0959-130">Specify an Azure data center location, such as West US or Southeast Asia.</span></span> <span data-ttu-id="f0959-131">Sie können eine Ressourcengruppe an einem beliebigen Ort platzieren.</span><span class="sxs-lookup"><span data-stu-id="f0959-131">You can place a resource group in any location.</span></span> <span data-ttu-id="f0959-132">Die Ressourcengruppe muss sich nicht am gleichen Speicherort wie das Azure-Abonnement oder am gleichen Speicherort wie die Ressourcen befinden.</span><span class="sxs-lookup"><span data-stu-id="f0959-132">The resource group does not have to be in the same location your Azure subscription or in the same location as its resources.</span></span>

<span data-ttu-id="f0959-133">Verwenden Sie das Get-AzureRmResourceProvider-Cmdlet mit dem *ProviderNamespace* -Parameter, um zu bestimmen, welcher Speicherort die einzelnen Ressourcentypen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f0959-133">To determine which location supports each resource type, use the Get-AzureRmResourceProvider cmdlet with the *ProviderNamespace* parameter.</span></span>

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

### <span data-ttu-id="f0959-134">-Name</span><span class="sxs-lookup"><span data-stu-id="f0959-134">-Name</span></span>
<span data-ttu-id="f0959-135">Gibt einen Namen für die Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="f0959-135">Specifies a name for the resource group.</span></span> <span data-ttu-id="f0959-136">Der Ressourcenname muss im Abonnement eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="f0959-136">The resource name must be unique in the subscription.</span></span> <span data-ttu-id="f0959-137">Wenn bereits eine Ressourcengruppe mit diesem Namen vorhanden ist, werden Sie vom Befehl zur Bestätigung aufgefordert, bevor die vorhandene Ressourcengruppe ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="f0959-137">If a resource group that has that name already exists, the command prompts you for confirmation before replacing the existing resource group.</span></span>

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

### <span data-ttu-id="f0959-138">-Pre</span><span class="sxs-lookup"><span data-stu-id="f0959-138">-Pre</span></span>
<span data-ttu-id="f0959-139">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="f0959-139">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f0959-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="f0959-140">-Tag</span></span>
<span data-ttu-id="f0959-141">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="f0959-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f0959-142">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="f0959-142">For example:</span></span>

<span data-ttu-id="f0959-143">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="f0959-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

<span data-ttu-id="f0959-144">Wenn Sie ein Tag hinzufügen oder ändern möchten, müssen Sie die Sammlung von Tags für die Ressourcengruppe ersetzen.</span><span class="sxs-lookup"><span data-stu-id="f0959-144">To add or change a tag, you must replace the collection of tags for the resource group.</span></span>

<span data-ttu-id="f0959-145">Nachdem Sie Ressourcen und Gruppen Kategorien zugewiesen haben, können Sie mit dem *Tag* -Parameter von Get-AzureRmResource und Get-AzureRmResourceGroup nach Ressourcen und Gruppen nach Tag-Name oder nach Name und Wert suchen.</span><span class="sxs-lookup"><span data-stu-id="f0959-145">After you assign tags to resources and groups, you can use the *Tag* parameter of Get-AzureRmResource and Get-AzureRmResourceGroup to search for resources and groups by tag name or by name and value.</span></span> <span data-ttu-id="f0959-146">Sie können Kategorien verwenden, um Ihre Ressourcen zu kategorisieren, beispielsweise nach Abteilung oder Kostenstelle, oder um Notizen oder Kommentare zu den Ressourcen zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="f0959-146">You can use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span>

<span data-ttu-id="f0959-147">Verwenden Sie das Get-AzureRMTag-Cmdlet, um ihre vordefinierten Tags abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f0959-147">To get your predefined tags, use the Get-AzureRMTag cmdlet.</span></span>

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

### <span data-ttu-id="f0959-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f0959-148">-Confirm</span></span>
<span data-ttu-id="f0959-149">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f0959-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0959-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0959-150">-WhatIf</span></span>
<span data-ttu-id="f0959-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f0959-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0959-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f0959-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0959-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0959-153">-DefaultProfile</span></span>
<span data-ttu-id="f0959-154">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f0959-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0959-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0959-155">CommonParameters</span></span>
<span data-ttu-id="f0959-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0959-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0959-157">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0959-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0959-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f0959-158">INPUTS</span></span>

### <span data-ttu-id="f0959-159">Keine</span><span class="sxs-lookup"><span data-stu-id="f0959-159">None</span></span>

## <span data-ttu-id="f0959-160">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f0959-160">OUTPUTS</span></span>

### <span data-ttu-id="f0959-161">Microsoft. Azure. Commands. ResourceManagement. Models. PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f0959-161">Microsoft.Azure.Commands.ResourceManagement.Models.PSResourceGroup</span></span>

## <span data-ttu-id="f0959-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="f0959-162">NOTES</span></span>

## <span data-ttu-id="f0959-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f0959-163">RELATED LINKS</span></span>

[<span data-ttu-id="f0959-164">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="f0959-164">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="f0959-165">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f0959-165">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="f0959-166">Neu – AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="f0959-166">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="f0959-167">Neu – AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="f0959-167">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="f0959-168">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f0959-168">Remove-AzureRmResourceGroup</span></span>](./Remove-AzureRmResourceGroup.md)

[<span data-ttu-id="f0959-169">Satz-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f0959-169">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)
