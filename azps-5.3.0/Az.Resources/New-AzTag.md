---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
ms.openlocfilehash: 937ac50ac34f8b04912a0d500dedb5b490806b1a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459268"
---
# <span data-ttu-id="c86a5-101">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="c86a5-101">New-AzTag</span></span>

## <span data-ttu-id="c86a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c86a5-102">SYNOPSIS</span></span>
<span data-ttu-id="c86a5-103">Erstellt ein vordefiniertes Azure-Tag oder fügt einem vorhandenen Tag Werte hinzu | Erstellt oder aktualisiert den gesamten Satz von Tags für eine Ressource oder ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c86a5-103">Creates a predefined Azure tag or adds values to an existing tag | Creates or updates the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="c86a5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c86a5-104">SYNTAX</span></span>

### <span data-ttu-id="c86a5-105">CreatePredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="c86a5-105">CreatePredefinedTagParameterSet</span></span>

```powershell
New-AzTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c86a5-106">CreateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c86a5-106">CreateByResourceIdParameterSet</span></span>

```powershell
New-AzTag
   -ResourceId <String>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="c86a5-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c86a5-107">DESCRIPTION</span></span>

<span data-ttu-id="c86a5-108">**CreatePredefinedTagSet**: Das **Cmdlet "New-AzTag"** erstellt ein vordefiniertes #A0 mit einem optionalen vordefinierten Wert.</span><span class="sxs-lookup"><span data-stu-id="c86a5-108">**CreatePredefinedTagSet**: The **New-AzTag** cmdlet creates a predefined Azure tag with an optional predefined value.</span></span>
<span data-ttu-id="c86a5-109">Sie können es auch verwenden, um vorhandenen vordefinierten Tags zusätzliche Werte hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="c86a5-109">You can also use it to add additional values to existing predefined tags.</span></span>
<span data-ttu-id="c86a5-110">Um ein vordefiniertes Tag zu erstellen, geben Sie einen eindeutigen Tagnamen ein.</span><span class="sxs-lookup"><span data-stu-id="c86a5-110">To create a predefined tag, enter a unique tag name.</span></span>
<span data-ttu-id="c86a5-111">Wenn Sie einem vorhandenen vordefinierten Tag einen Wert hinzufügen möchten, geben Sie den Namen des vorhandenen Tags und den neuen Wert an.</span><span class="sxs-lookup"><span data-stu-id="c86a5-111">To add a value to an existing predefined tag, specify the name of the existing tag and the new value.</span></span>
<span data-ttu-id="c86a5-112">Dieses Cmdlet gibt ein Objekt zurück, das das neue oder geänderte Tag mit seinen Werten und der Anzahl der Ressourcen darstellt, auf die es angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c86a5-112">This cmdlet returns an object that represents the new or modified tag with its values and the number of resources to which it has been applied.</span></span>
<span data-ttu-id="c86a5-113">Das Azure-Tags-Modul, zu dem **"New-AzTag"** gehört, kann Sie bei der Verwaltung vordefinierter #A0 unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c86a5-113">The Azure Tags module that **New-AzTag** is part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="c86a5-114">Ein Azure-Tag ist ein Name-Wert-Paar, mit dem Sie Ihre Azure-Ressourcen und -Ressourcengruppen kategorisieren können, z. B. nach Abteilung oder Kostencenter, oder um Notizen oder Kommentare zu den Ressourcen und Gruppen nachverfolgt werden.</span><span class="sxs-lookup"><span data-stu-id="c86a5-114">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="c86a5-115">Sie können Tags in einem einzigen Schritt definieren und anwenden, aber mit vordefinierten Tags können Sie standardübliche, konsistente, vorhersehbare Namen und Werte für die Tags in Ihrem Abonnement festlegen.</span><span class="sxs-lookup"><span data-stu-id="c86a5-115">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="c86a5-116">Wenn Sie eine vordefinierte Markierung auf eine Ressource oder Ressourcengruppe anwenden möchten, verwenden Sie den *Parameter "Tag"* des New-AzTag Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="c86a5-116">To apply a predefined tag to a resource or resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="c86a5-117">Um nach Ressourcengruppen mit einem angegebenen Tagnamen oder -namen und Wert zu suchen, verwenden Sie den *Parameter "Tag"* des Get-AzResourceGroup Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="c86a5-117">To search for resource groups with a specified tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="c86a5-118">Jedes Tag hat einen Namen.</span><span class="sxs-lookup"><span data-stu-id="c86a5-118">Every tag has a name.</span></span>
<span data-ttu-id="c86a5-119">Die Werte sind optional.</span><span class="sxs-lookup"><span data-stu-id="c86a5-119">The values are optional.</span></span>
<span data-ttu-id="c86a5-120">Ein vordefiniertes Azure-Tag kann mehrere Werte enthalten, aber wenn Sie das Tag auf eine Ressource oder Ressourcengruppe anwenden, wenden Sie den Tagnamen und nur einen der Werte an.</span><span class="sxs-lookup"><span data-stu-id="c86a5-120">A predefined Azure tag can have multiple values, but when you apply the tag to a resource or resource group, you apply the tag name and only one of its values.</span></span>
<span data-ttu-id="c86a5-121">Sie können z. B. ein vordefiniertes Abteilungstag mit einem Wert für jede Abteilung erstellen, z. B. "Finanzen", "Personalwesen" und "IT".</span><span class="sxs-lookup"><span data-stu-id="c86a5-121">For example, you can create a predefined Department tag with a value for each department, such as Finance, Human Resources, and IT.</span></span>
<span data-ttu-id="c86a5-122">Wenn Sie die Tag "Department" auf eine Ressource anwenden, wenden Sie nur einen vordefinierten Wert an, z. B. "Finanzen".</span><span class="sxs-lookup"><span data-stu-id="c86a5-122">When you apply the Department tag to a resource, you apply only one predefined value, such as Finance.</span></span>

<span data-ttu-id="c86a5-123">**CreateByResourceIdParameterSet:** Das **Cmdlet "New-AzTag"** mit einer **ResourceId** erstellt oder aktualisiert den gesamten Satz von Tags für eine Ressource oder ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c86a5-123">**CreateByResourceIdParameterSet**: The **New-AzTag** cmdlet with a **ResourceId** creates or updates the entire set of tags on a resource or subscription.</span></span>
<span data-ttu-id="c86a5-124">Dieser Vorgang ermöglicht das Hinzufügen oder Ersetzen aller Markierungen für die angegebene Ressource oder das angegebene Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c86a5-124">This operation allows adding or replacing the entire set of tags on the specified resource or subscription.</span></span> <span data-ttu-id="c86a5-125">Die angegebene Entität kann maximal 50 Tags enthalten.</span><span class="sxs-lookup"><span data-stu-id="c86a5-125">The specified entity can have a maximum of 50 tags.</span></span>

## <span data-ttu-id="c86a5-126">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c86a5-126">EXAMPLES</span></span>

### <span data-ttu-id="c86a5-127">Beispiel 1: Erstellen eines vordefinierten Tags</span><span class="sxs-lookup"><span data-stu-id="c86a5-127">Example 1: Create a predefined tag</span></span>
```powershell
PS C:\>New-AzTag -Name "FY2015"
                                
Name   ValuesTable Count Values 
----   ----------- ----- ------
FY2015             0     {}
```

<span data-ttu-id="c86a5-128">Mit diesem Befehl wird ein vordefiniertes Tag namens "Y2015" erstellt.</span><span class="sxs-lookup"><span data-stu-id="c86a5-128">This command creates a predefined tag named FY2015.</span></span>
<span data-ttu-id="c86a5-129">Dieses Tag enthält keine Werte.</span><span class="sxs-lookup"><span data-stu-id="c86a5-129">This tag has no values.</span></span>
<span data-ttu-id="c86a5-130">Sie können eine Markierung ohne Werte auf eine Ressource oder Ressourcengruppe anwenden oder **"Neues-AzTag"** verwenden, um dem Tag Werte hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="c86a5-130">You can apply a tag with no values to a resource or resource group, or use **New-AzTag** to add values to the tag.</span></span>
<span data-ttu-id="c86a5-131">Sie können auch einen Wert angeben, wenn Sie die Markierung auf die Ressource oder Ressourcengruppe anwenden.</span><span class="sxs-lookup"><span data-stu-id="c86a5-131">You can also specify a value when you apply the tag to the resource or resource group.</span></span>

### <span data-ttu-id="c86a5-132">Beispiel 2: Erstellen eines vordefinierten Tags mit einem Wert</span><span class="sxs-lookup"><span data-stu-id="c86a5-132">Example 2: Create a predefined tag with a value</span></span>
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

<span data-ttu-id="c86a5-133">Mit diesem Befehl wird ein vordefiniertes Tag namens "Abteilung" mit dem Wert "Finanzen" erstellt.</span><span class="sxs-lookup"><span data-stu-id="c86a5-133">This command creates a predefined tag named Department with a value of Finance.</span></span>

### <span data-ttu-id="c86a5-134">Beispiel 3: Hinzufügen eines Werts zu einem vordefinierten Tag</span><span class="sxs-lookup"><span data-stu-id="c86a5-134">Example 3: Add a value to a predefined tag</span></span>
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0 
PS C:\>New-AzTag -Name "Department" -Value "IT"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0
        IT          0
```

<span data-ttu-id="c86a5-135">Mit diesen Befehlen wird ein vordefiniertes Tag namens "Abteilung" mit zwei Werten erstellt.</span><span class="sxs-lookup"><span data-stu-id="c86a5-135">These commands create a predefined tag named Department with two values.</span></span>
<span data-ttu-id="c86a5-136">Wenn der Tagname vorhanden ist, wird der Wert von **"Neu-AzTag"** zum vorhandenen Tag addiert, statt ein neues Tag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c86a5-136">If the tag name exists, **New-AzTag** adds the value to the existing tag instead of creating a new one.</span></span>

### <span data-ttu-id="c86a5-137">Beispiel 4: Verwenden eines vordefinierten Tags</span><span class="sxs-lookup"><span data-stu-id="c86a5-137">Example 4: Use a predefined tag</span></span>
```powershell
PS C:\>New-AzTag -Name "CostCenter" -Value "0001"
Name:   CostCenter
Count:  0
Values: 
        Name        Count
        =========   =====
        0001        0 
PS C:\>Set-AzResourceGroup -Name "EngineerBlog" -Tag @{Name="CostCenter";Value="0001"}
Name:      EngineerBlog
Location:  East US
Resources: 
            
  Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US
    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001 
PS C:\>Get-AzTag -Name "CostCenter"
Name:   CostCenter
Count:  1
Values: 
        Name        Count
        =========   =====
        0001        1 
PS C:\>Get-AzResourceGroup -Tag @{Name="CostCenter"}
Name:      EngineerBlog
Location:  East US
Resources: 
     Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US

    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001
```

<span data-ttu-id="c86a5-138">Mit den Befehlen in diesem Beispiel wird ein vordefiniertes Tag erstellt und verwendet.</span><span class="sxs-lookup"><span data-stu-id="c86a5-138">The commands in this example create and use a predefined tag.</span></span>

### <span data-ttu-id="c86a5-139">Beispiel 5: Erstellt oder aktualisiert die gesamte Gruppe von Tags in einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c86a5-139">Example 5: Creates or updates the entire set of tags on a subscription</span></span>

```powershell
PS C:\>$Tags = @{"tagKey1"="tagValue1"; "tagKey2"="tagValue2"}
PS C:\>New-AzTag -ResourceId /subscriptions/{subId} -Tag $Tags

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             tagKey1  tagValue1
             tagKey2  tagValue2
```

<span data-ttu-id="c86a5-140">Mit diesem Befehl wird die gesamte Gruppe von Tags für das Abonnement mit {subId} erstellt oder aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="c86a5-140">This command creates or updates the entire set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="c86a5-141">Beispiel 6: Erstellt oder aktualisiert den gesamten Satz von Tags für eine Ressource.</span><span class="sxs-lookup"><span data-stu-id="c86a5-141">Example 6: Creates or updates the entire set of tags on a resource</span></span>

```powershell
PS C:\>$Tags = @{"Dept"="Finance"; "Status"="Normal"}
PS C:\>New-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1 -Tag $Tags

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

<span data-ttu-id="c86a5-142">Mit diesem Befehl wird der gesamte Satz von Tags für die Ressource mit {resourceId} erstellt oder aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="c86a5-142">This command creates or updates the entire set of tags on the resource with {resourceId}.</span></span>

## <span data-ttu-id="c86a5-143">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c86a5-143">PARAMETERS</span></span>

### <span data-ttu-id="c86a5-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c86a5-144">-DefaultProfile</span></span>
<span data-ttu-id="c86a5-145">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c86a5-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c86a5-146">-Name</span><span class="sxs-lookup"><span data-stu-id="c86a5-146">-Name</span></span>
<span data-ttu-id="c86a5-147">Gibt den vordefinierten Tagnamen an.</span><span class="sxs-lookup"><span data-stu-id="c86a5-147">Specifies the predefined tag name.</span></span>
<span data-ttu-id="c86a5-148">Wenn Sie ein neues vordefiniertes Tag erstellen möchten, geben Sie einen eindeutigen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="c86a5-148">To create a new predefined tag, enter a unique name.</span></span>
<span data-ttu-id="c86a5-149">Wenn Sie einem vorhandenen Tag einen Wert hinzufügen möchten, geben Sie den Namen des vorhandenen Tags ein.</span><span class="sxs-lookup"><span data-stu-id="c86a5-149">To add a value to an existing tag, enter the name of the existing tag.</span></span>
<span data-ttu-id="c86a5-150">Wenn ein vorhandenes vordefiniertes Tag den angegebenen Namen enthält, fügt **"New-AzTag"** den angegebenen Wert (sofern vorhanden) zum Tag mit diesem Namen hinzu, statt ein neues Tag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c86a5-150">If an existing predefined tag has the specified name, **New-AzTag** adds the specified value, if any, to the tag with that name instead of creating a new tag.</span></span>

```yaml
Type: System.String
Parameter Sets: CreatePredefinedTagParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c86a5-151">-Value</span><span class="sxs-lookup"><span data-stu-id="c86a5-151">-Value</span></span>
<span data-ttu-id="c86a5-152">Gibt einen vordefinierten Tagwert an.</span><span class="sxs-lookup"><span data-stu-id="c86a5-152">Specifies a predefined tag value.</span></span>
<span data-ttu-id="c86a5-153">Vordefinierte Tags können mehrere Werte enthalten, Sie können aber nur einen Wert in jeden Befehl eingeben.</span><span class="sxs-lookup"><span data-stu-id="c86a5-153">Predefined tags can have multiple values, but you can enter only one value in each command.</span></span>
<span data-ttu-id="c86a5-154">Dieser Parameter ist optional, da Tags Namen ohne Werte enthalten können.</span><span class="sxs-lookup"><span data-stu-id="c86a5-154">This parameter is optional, because tags can have names without values.</span></span>

```yaml
Type: System.String
Parameter Sets: CreatePredefinedTagParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c86a5-155">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c86a5-155">-ResourceId</span></span>
<span data-ttu-id="c86a5-156">Der Ressourcenbezeichner für die entität, die markiert wird.</span><span class="sxs-lookup"><span data-stu-id="c86a5-156">The resource identifier for the entity being tagged.</span></span> <span data-ttu-id="c86a5-157">Möglicherweise ist eine Ressource, eine Ressourcengruppe oder ein Abonnement markiert.</span><span class="sxs-lookup"><span data-stu-id="c86a5-157">A resource, a resource group or a subscription may be tagged.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c86a5-158">-Tag</span><span class="sxs-lookup"><span data-stu-id="c86a5-158">-Tag</span></span>
<span data-ttu-id="c86a5-159">Die Tags, die der Ressource zugeordnet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="c86a5-159">The tags to put on the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c86a5-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c86a5-160">-Confirm</span></span>
<span data-ttu-id="c86a5-161">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c86a5-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c86a5-162">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c86a5-162">-WhatIf</span></span>
<span data-ttu-id="c86a5-163">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c86a5-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c86a5-164">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c86a5-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c86a5-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c86a5-165">CommonParameters</span></span>
<span data-ttu-id="c86a5-166">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c86a5-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c86a5-167">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c86a5-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c86a5-168">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c86a5-168">INPUTS</span></span>

### <span data-ttu-id="c86a5-169">System.String</span><span class="sxs-lookup"><span data-stu-id="c86a5-169">System.String</span></span>

### <span data-ttu-id="c86a5-170">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c86a5-170">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c86a5-171">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c86a5-171">OUTPUTS</span></span>

### <span data-ttu-id="c86a5-172">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span><span class="sxs-lookup"><span data-stu-id="c86a5-172">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="c86a5-173">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c86a5-173">NOTES</span></span>

## <span data-ttu-id="c86a5-174">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c86a5-174">RELATED LINKS</span></span>

[<span data-ttu-id="c86a5-175">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="c86a5-175">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="c86a5-176">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="c86a5-176">Remove-AzTag</span></span>](./Remove-AzTag.md)

[<span data-ttu-id="c86a5-177">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="c86a5-177">Update-AzTag</span></span>](./Update-AzTag.md)