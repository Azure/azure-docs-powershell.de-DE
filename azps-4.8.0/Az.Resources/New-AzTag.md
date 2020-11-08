---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
ms.openlocfilehash: 176328452c123c3d3cada88940efcdadf88943e0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165666"
---
# <span data-ttu-id="dae46-101">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="dae46-101">New-AzTag</span></span>

## <span data-ttu-id="dae46-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dae46-102">SYNOPSIS</span></span>
<span data-ttu-id="dae46-103">Erstellt eine vordefinierte Azure-Kategorie oder addiert Werte zu einem vorhandenen Tag | Erstellt oder aktualisiert den gesamten Satz von Tags für eine Ressource oder ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dae46-103">Creates a predefined Azure tag or adds values to an existing tag | Creates or updates the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="dae46-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dae46-104">SYNTAX</span></span>

### <span data-ttu-id="dae46-105">CreatePredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="dae46-105">CreatePredefinedTagParameterSet</span></span>

```powershell
New-AzTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dae46-106">CreateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dae46-106">CreateByResourceIdParameterSet</span></span>

```powershell
New-AzTag
   -ResourceId <String>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="dae46-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dae46-107">DESCRIPTION</span></span>

<span data-ttu-id="dae46-108">**CreatePredefinedTagSet** : das Cmdlet **New-AzTag** erstellt ein vordefiniertes Azure-Tag mit einem optionalen vordefinierten Wert.</span><span class="sxs-lookup"><span data-stu-id="dae46-108">**CreatePredefinedTagSet** : The **New-AzTag** cmdlet creates a predefined Azure tag with an optional predefined value.</span></span>
<span data-ttu-id="dae46-109">Sie können es auch verwenden, um zusätzliche Werte zu vorhandenen vordefinierten Tags hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="dae46-109">You can also use it to add additional values to existing predefined tags.</span></span>
<span data-ttu-id="dae46-110">Wenn Sie ein vordefiniertes Tag erstellen möchten, geben Sie einen eindeutigen Tag-Namen ein.</span><span class="sxs-lookup"><span data-stu-id="dae46-110">To create a predefined tag, enter a unique tag name.</span></span>
<span data-ttu-id="dae46-111">Wenn Sie einen Wert zu einem vorhandenen vordefinierten Tag hinzufügen möchten, geben Sie den Namen des vorhandenen Tags und den neuen Wert an.</span><span class="sxs-lookup"><span data-stu-id="dae46-111">To add a value to an existing predefined tag, specify the name of the existing tag and the new value.</span></span>
<span data-ttu-id="dae46-112">Dieses Cmdlet gibt ein Objekt zurück, das das neue oder geänderte Tag mit seinen Werten und der Anzahl der Ressourcen darstellt, auf die es angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="dae46-112">This cmdlet returns an object that represents the new or modified tag with its values and the number of resources to which it has been applied.</span></span>
<span data-ttu-id="dae46-113">Das Azure-Tags-Modul, in dem **New-AzTag** enthalten ist, kann Ihnen dabei helfen, vordefinierte Azure-Tags zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="dae46-113">The Azure Tags module that **New-AzTag** is part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="dae46-114">Bei einem Azure-Tag handelt es sich um ein Name-Wert-Paar, mit dem Sie Ihre Azure-Ressourcen und Ressourcengruppen kategorisieren können, beispielsweise nach Abteilung oder Kostenstelle, oder um Notizen oder Kommentare zu Ressourcen und Gruppen zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="dae46-114">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="dae46-115">Sie können Tags in einem einzigen Schritt definieren und anwenden, doch mit vordefinierten Tags können Sie standardmäßige, konsistente, vorhersagbare Namen und Werte für die Tags in Ihrem Abonnement einrichten.</span><span class="sxs-lookup"><span data-stu-id="dae46-115">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="dae46-116">Wenn Sie eine vordefinierte Kategorie auf eine Ressource oder eine Ressourcengruppe anwenden möchten, verwenden Sie den *Tag* -Parameter des New-AzTag-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="dae46-116">To apply a predefined tag to a resource or resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="dae46-117">Verwenden Sie den *Tag* -Parameter des Get-AzResourceGroup-Cmdlets, um nach Ressourcengruppen mit einem angegebenen Tag-Namen oder-Namen und-Wert zu suchen.</span><span class="sxs-lookup"><span data-stu-id="dae46-117">To search for resource groups with a specified tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="dae46-118">Jedes Tag hat einen Namen.</span><span class="sxs-lookup"><span data-stu-id="dae46-118">Every tag has a name.</span></span>
<span data-ttu-id="dae46-119">Die Werte sind optional.</span><span class="sxs-lookup"><span data-stu-id="dae46-119">The values are optional.</span></span>
<span data-ttu-id="dae46-120">Ein vordefiniertes Azure-Tag kann mehrere Werte aufweisen, doch wenn Sie das Tag auf eine Ressource oder eine Ressourcengruppe anwenden, wenden Sie den Tagnamen und nur einen seiner Werte an.</span><span class="sxs-lookup"><span data-stu-id="dae46-120">A predefined Azure tag can have multiple values, but when you apply the tag to a resource or resource group, you apply the tag name and only one of its values.</span></span>
<span data-ttu-id="dae46-121">So können Sie beispielsweise eine vordefinierte Abteilungs Kategorie mit einem Wert für jede Abteilung erstellen, beispielsweise Finance, Personalwesen und IT.</span><span class="sxs-lookup"><span data-stu-id="dae46-121">For example, you can create a predefined Department tag with a value for each department, such as Finance, Human Resources, and IT.</span></span>
<span data-ttu-id="dae46-122">Wenn Sie die Kategorie "Abteilung" auf eine Ressource anwenden, wenden Sie nur einen vordefinierten Wert wie "Finance" an.</span><span class="sxs-lookup"><span data-stu-id="dae46-122">When you apply the Department tag to a resource, you apply only one predefined value, such as Finance.</span></span>

<span data-ttu-id="dae46-123">**CreateByResourceIdParameterSet** : das Cmdlet **New-AzTag** mit einer **Resourcen** -Kennung erstellt oder aktualisiert den gesamten Satz von Tags für eine Ressource oder ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dae46-123">**CreateByResourceIdParameterSet** : The **New-AzTag** cmdlet with a **ResourceId** creates or updates the entire set of tags on a resource or subscription.</span></span>
<span data-ttu-id="dae46-124">Dieser Vorgang ermöglicht das Hinzufügen oder Ersetzen der gesamten Gruppe von Tags für die angegebene Ressource oder das angegebene Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dae46-124">This operation allows adding or replacing the entire set of tags on the specified resource or subscription.</span></span> <span data-ttu-id="dae46-125">Die angegebene Entität kann maximal 50-Tags enthalten.</span><span class="sxs-lookup"><span data-stu-id="dae46-125">The specified entity can have a maximum of 50 tags.</span></span>

## <span data-ttu-id="dae46-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dae46-126">EXAMPLES</span></span>

### <span data-ttu-id="dae46-127">Beispiel 1: Erstellen eines vordefinierten Tags</span><span class="sxs-lookup"><span data-stu-id="dae46-127">Example 1: Create a predefined tag</span></span>
```powershell
PS C:\>New-AzTag -Name "FY2015"
                                
Name   ValuesTable Count Values 
----   ----------- ----- ------
FY2015             0     {}
```

<span data-ttu-id="dae46-128">Dieser Befehl erstellt ein vordefiniertes Tag mit dem Namen FY2015.</span><span class="sxs-lookup"><span data-stu-id="dae46-128">This command creates a predefined tag named FY2015.</span></span>
<span data-ttu-id="dae46-129">Dieses Tag hat keine Werte.</span><span class="sxs-lookup"><span data-stu-id="dae46-129">This tag has no values.</span></span>
<span data-ttu-id="dae46-130">Sie können eine Kategorie ohne Werte auf eine Ressource oder eine Ressourcengruppe anwenden oder mithilfe von **New-AzTag** dem Tag Werte hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="dae46-130">You can apply a tag with no values to a resource or resource group, or use **New-AzTag** to add values to the tag.</span></span>
<span data-ttu-id="dae46-131">Sie können auch einen Wert angeben, wenn Sie die Kategorie auf die Ressourcen-oder Ressourcengruppe anwenden.</span><span class="sxs-lookup"><span data-stu-id="dae46-131">You can also specify a value when you apply the tag to the resource or resource group.</span></span>

### <span data-ttu-id="dae46-132">Beispiel 2: Erstellen eines vordefinierten Tags mit einem Wert</span><span class="sxs-lookup"><span data-stu-id="dae46-132">Example 2: Create a predefined tag with a value</span></span>
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

<span data-ttu-id="dae46-133">Mit diesem Befehl wird eine vordefinierte Kategorie mit dem Namen "Department" mit dem Wert "Finance" erstellt.</span><span class="sxs-lookup"><span data-stu-id="dae46-133">This command creates a predefined tag named Department with a value of Finance.</span></span>

### <span data-ttu-id="dae46-134">Beispiel 3: Hinzufügen eines Werts zu einem vordefinierten Tag</span><span class="sxs-lookup"><span data-stu-id="dae46-134">Example 3: Add a value to a predefined tag</span></span>
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

<span data-ttu-id="dae46-135">Mit diesen Befehlen wird ein vordefiniertes Tag mit dem Namen Department mit zwei Werten erstellt.</span><span class="sxs-lookup"><span data-stu-id="dae46-135">These commands create a predefined tag named Department with two values.</span></span>
<span data-ttu-id="dae46-136">Wenn der Tag-Name vorhanden ist, fügt **New-AzTag** den Wert dem vorhandenen Tag hinzu, anstatt eine neue zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="dae46-136">If the tag name exists, **New-AzTag** adds the value to the existing tag instead of creating a new one.</span></span>

### <span data-ttu-id="dae46-137">Beispiel 4: Verwenden eines vordefinierten Tags</span><span class="sxs-lookup"><span data-stu-id="dae46-137">Example 4: Use a predefined tag</span></span>
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

<span data-ttu-id="dae46-138">Mit den Befehlen in diesem Beispiel wird ein vordefiniertes Tag erstellt und verwendet.</span><span class="sxs-lookup"><span data-stu-id="dae46-138">The commands in this example create and use a predefined tag.</span></span>

### <span data-ttu-id="dae46-139">Beispiel 5: Erstellen oder Aktualisieren der gesamten Gruppe von Tags in einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="dae46-139">Example 5: Creates or updates the entire set of tags on a subscription</span></span>

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

<span data-ttu-id="dae46-140">Mit diesem Befehl wird der gesamte Satz von Tags im Abonnement mit {subId} erstellt oder aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="dae46-140">This command creates or updates the entire set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="dae46-141">Beispiel 6: Erstellen oder Aktualisieren der gesamten Gruppe von Tags für eine Ressource</span><span class="sxs-lookup"><span data-stu-id="dae46-141">Example 6: Creates or updates the entire set of tags on a resource</span></span>

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

<span data-ttu-id="dae46-142">Mit diesem Befehl wird der gesamte Satz von Tags für die Ressource mit {Ressourcenkennung} erstellt oder aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="dae46-142">This command creates or updates the entire set of tags on the resource with {resourceId}.</span></span>

## <span data-ttu-id="dae46-143">Parameter</span><span class="sxs-lookup"><span data-stu-id="dae46-143">PARAMETERS</span></span>

### <span data-ttu-id="dae46-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dae46-144">-DefaultProfile</span></span>
<span data-ttu-id="dae46-145">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dae46-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dae46-146">-Name</span><span class="sxs-lookup"><span data-stu-id="dae46-146">-Name</span></span>
<span data-ttu-id="dae46-147">Gibt den vordefinierten Tagnamen an.</span><span class="sxs-lookup"><span data-stu-id="dae46-147">Specifies the predefined tag name.</span></span>
<span data-ttu-id="dae46-148">Wenn Sie ein neues vordefiniertes Tag erstellen möchten, geben Sie einen eindeutigen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="dae46-148">To create a new predefined tag, enter a unique name.</span></span>
<span data-ttu-id="dae46-149">Wenn Sie einen Wert zu einer vorhandenen Kategorie hinzufügen möchten, geben Sie den Namen des vorhandenen Tags ein.</span><span class="sxs-lookup"><span data-stu-id="dae46-149">To add a value to an existing tag, enter the name of the existing tag.</span></span>
<span data-ttu-id="dae46-150">Wenn ein vorhandenes vordefiniertes Tag den angegebenen Namen aufweist, fügt **New-AzTag** den angegebenen Wert, falls vorhanden, dem Tag mit diesem Namen hinzu, anstatt eine neue Kategorie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="dae46-150">If an existing predefined tag has the specified name, **New-AzTag** adds the specified value, if any, to the tag with that name instead of creating a new tag.</span></span>

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

### <span data-ttu-id="dae46-151">-Wert</span><span class="sxs-lookup"><span data-stu-id="dae46-151">-Value</span></span>
<span data-ttu-id="dae46-152">Gibt einen vordefinierten Tag-Wert an.</span><span class="sxs-lookup"><span data-stu-id="dae46-152">Specifies a predefined tag value.</span></span>
<span data-ttu-id="dae46-153">Vordefinierte Tags können mehrere Werte haben, aber Sie können in jedem Befehl nur einen Wert eingeben.</span><span class="sxs-lookup"><span data-stu-id="dae46-153">Predefined tags can have multiple values, but you can enter only one value in each command.</span></span>
<span data-ttu-id="dae46-154">Dieser Parameter ist optional, da Tags Namen ohne Werte enthalten können.</span><span class="sxs-lookup"><span data-stu-id="dae46-154">This parameter is optional, because tags can have names without values.</span></span>

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

### <span data-ttu-id="dae46-155">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="dae46-155">-ResourceId</span></span>
<span data-ttu-id="dae46-156">Der Ressourcenbezeichner für die Entität, die markiert wird.</span><span class="sxs-lookup"><span data-stu-id="dae46-156">The resource identifier for the entity being tagged.</span></span> <span data-ttu-id="dae46-157">Eine Ressource, eine Ressourcengruppe oder ein Abonnement können markiert sein.</span><span class="sxs-lookup"><span data-stu-id="dae46-157">A resource, a resource group or a subscription may be tagged.</span></span>

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

### <span data-ttu-id="dae46-158">-Tag</span><span class="sxs-lookup"><span data-stu-id="dae46-158">-Tag</span></span>
<span data-ttu-id="dae46-159">Die Tags, die auf die Ressource gesetzt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dae46-159">The tags to put on the resource.</span></span>

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

### <span data-ttu-id="dae46-160">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dae46-160">-Confirm</span></span>
<span data-ttu-id="dae46-161">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dae46-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dae46-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dae46-162">-WhatIf</span></span>
<span data-ttu-id="dae46-163">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dae46-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dae46-164">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dae46-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dae46-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dae46-165">CommonParameters</span></span>
<span data-ttu-id="dae46-166">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dae46-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dae46-167">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dae46-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dae46-168">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dae46-168">INPUTS</span></span>

### <span data-ttu-id="dae46-169">System. String</span><span class="sxs-lookup"><span data-stu-id="dae46-169">System.String</span></span>

### <span data-ttu-id="dae46-170">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="dae46-170">System.Collections.Hashtable</span></span>

## <span data-ttu-id="dae46-171">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dae46-171">OUTPUTS</span></span>

### <span data-ttu-id="dae46-172">Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag | Microsoft. Azure. Commands. Tags. Model. PSTagResource</span><span class="sxs-lookup"><span data-stu-id="dae46-172">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="dae46-173">Notizen</span><span class="sxs-lookup"><span data-stu-id="dae46-173">NOTES</span></span>

## <span data-ttu-id="dae46-174">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dae46-174">RELATED LINKS</span></span>

[<span data-ttu-id="dae46-175">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="dae46-175">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="dae46-176">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="dae46-176">Remove-AzTag</span></span>](./Remove-AzTag.md)

[<span data-ttu-id="dae46-177">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="dae46-177">Update-AzTag</span></span>](./Update-AzTag.md)
