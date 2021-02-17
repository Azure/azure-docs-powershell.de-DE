---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
ms.openlocfilehash: 22a43739ec63f8287ce51c4c4f4a125b4e5b1c65
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156452"
---
# <span data-ttu-id="f4259-101">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="f4259-101">Remove-AzTag</span></span>

## <span data-ttu-id="f4259-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4259-102">SYNOPSIS</span></span>
<span data-ttu-id="f4259-103">Löscht vordefinierte Azure-Tags oder -| Löscht den gesamten Satz von Tags für eine Ressource oder ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f4259-103">Deletes predefined Azure tags or values | Deletes the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="f4259-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f4259-104">SYNTAX</span></span>

### <span data-ttu-id="f4259-105">RemovePredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4259-105">RemovePredefinedTagParameterSet</span></span>

```powershell
Remove-AzTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4259-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4259-106">RemoveByResourceIdParameterSet</span></span>

```powershell
Remove-AzTag
   -ResourceId <String>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="f4259-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f4259-107">DESCRIPTION</span></span>

<span data-ttu-id="f4259-108">**RemovePredefinedTagSet:** Das **Cmdlet "Remove-AzTag"** löscht vordefinierte #A0 und -Werte aus Ihrem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f4259-108">**RemovePredefinedTagSet**: The **Remove-AzTag** cmdlet deletes predefined Azure tags and values from your subscription.</span></span>
<span data-ttu-id="f4259-109">Verwenden Sie den Parameter *"Value",* um bestimmte Werte aus einem vordefinierten Tag zu löschen.</span><span class="sxs-lookup"><span data-stu-id="f4259-109">To delete particular values from a predefined tag, use the *Value* parameter.</span></span>
<span data-ttu-id="f4259-110">Standardmäßig löscht **"Remove-AzTag"** das angegebene Tag und alle werte. Sie können ein Tag oder einen Wert, der derzeit auf eine Ressource oder Ressourcengruppe angewendet wird, nicht löschen.</span><span class="sxs-lookup"><span data-stu-id="f4259-110">By default, **Remove-AzTag** deletes the specified tag and all of its values.You cannot delete a tag or value that is currently applied to a resource or resource group.</span></span>
<span data-ttu-id="f4259-111">Bevor Sie **"Remove-AzTag"** verwenden, verwenden Sie den Parameter *"Tag"* des cmdlets Set-AzResourceGroup, um das Tag oder die Werte aus der Ressourcengruppe zu löschen.</span><span class="sxs-lookup"><span data-stu-id="f4259-111">Before using **Remove-AzTag**, use the *Tag* parameter of the Set-AzResourceGroup cmdlet to delete the tag or values from the resource or resource group.</span></span>
<span data-ttu-id="f4259-112">Das Azure-Tags-Modul, zu dem **"Remove-AzTag"** gehört, kann Ihnen dabei helfen, Ihre vordefinierten #A0 zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="f4259-112">The Azure Tags module that **Remove-AzTag** is part of can help you manage your predefined Azure tags.</span></span>
<span data-ttu-id="f4259-113">Ein Azure-Tag ist ein Name-Wert-Paar, mit dem Sie Ihre Azure-Ressourcen und -Ressourcengruppen kategorisieren können, z. B. nach Abteilung oder Kostencenter, oder um Notizen oder Kommentare zu den Ressourcen und Gruppen nachverfolgt werden.</span><span class="sxs-lookup"><span data-stu-id="f4259-113">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="f4259-114">Sie können Tags in einem einzigen Schritt definieren und anwenden, aber mit vordefinierten Tags können Sie standardübliche, konsistente, vorhersehbare Namen und Werte für die Tags in Ihrem Abonnement festlegen.</span><span class="sxs-lookup"><span data-stu-id="f4259-114">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>

<span data-ttu-id="f4259-115">**RemoveByResourceIdParameterSet:** Das **Cmdlet "Remove-AzTag"** mit einer **ResourceId** löscht den gesamten Satz von Tags für eine Ressource oder ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f4259-115">**RemoveByResourceIdParameterSet**: The **Remove-AzTag** cmdlet with a **ResourceId** deletes the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="f4259-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f4259-116">EXAMPLES</span></span>

### <span data-ttu-id="f4259-117">Beispiel 1: Löschen eines vordefinierten Tags</span><span class="sxs-lookup"><span data-stu-id="f4259-117">Example 1: Delete a predefined tag</span></span>
```powershell
PS C:\>Remove-AzTag -Name "Department"
```

<span data-ttu-id="f4259-118">Mit diesem Befehl werden das vordefinierte Tag "Abteilung" und alle Werte gelöscht.</span><span class="sxs-lookup"><span data-stu-id="f4259-118">This command deletes the predefined tag named Department and all of its values.</span></span>
<span data-ttu-id="f4259-119">Wenn das Tag auf Ressourcen oder Ressourcengruppen angewendet wurde, schlägt der Befehl fehl.</span><span class="sxs-lookup"><span data-stu-id="f4259-119">If the tag has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="f4259-120">Beispiel 2: Löschen eines Werts aus einem vordefinierten Tag</span><span class="sxs-lookup"><span data-stu-id="f4259-120">Example 2: Delete a value from a predefined tag</span></span>
```powershell
PS C:\>Remove-AzTag -Name "Department" -Value "HumanResources" -PassThru
Name:   Department
Count:  14
Values: 

        Name        Count
        =========   =====

        Finance        2
        IT            12
```

<span data-ttu-id="f4259-121">Mit diesem Befehl wird der Wert "HumanResources" aus dem vordefinierten Tag "Department" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="f4259-121">This command deletes the HumanResources value from the predefined Department tag.</span></span>
<span data-ttu-id="f4259-122">Das Tag wird nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="f4259-122">It does not delete the tag.</span></span>
<span data-ttu-id="f4259-123">Wenn der Wert auf Ressourcen oder Ressourcengruppen angewendet wurde, schlägt der Befehl fehl.</span><span class="sxs-lookup"><span data-stu-id="f4259-123">If the value has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="f4259-124">Beispiel 3: Löscht die gesamte Gruppe von Kategorien in einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f4259-124">Example 3: Deletes the entire set of tags on a subscription</span></span>

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}
```

<span data-ttu-id="f4259-125">Mit diesem Befehl wird der gesamte Satz von Tags im Abonnement mit {subId} gelöscht.</span><span class="sxs-lookup"><span data-stu-id="f4259-125">This command deletes the entire set of tags on the subscription with {subId}.</span></span> <span data-ttu-id="f4259-126">Wenn "-PassThru" nicht übergeben wird, wird das gelöschte Objekt nicht zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f4259-126">It will not return the object deleted if not passing in "-PassThru".</span></span>

### <span data-ttu-id="f4259-127">Beispiel 4: Löscht den gesamten Satz von Tags für eine Ressource.</span><span class="sxs-lookup"><span data-stu-id="f4259-127">Example 4: Deletes the entire set of tags on a resource</span></span>

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1 -PassThru

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

<span data-ttu-id="f4259-128">Mit diesem Befehl wird der gesamte Satz von Markierungen für die Ressource mit {resourceId} gelöscht.</span><span class="sxs-lookup"><span data-stu-id="f4259-128">This command deletes the entire set of tags on the resource with {resourceId}.</span></span> <span data-ttu-id="f4259-129">Beim Übergeben von "-PassThru" wird das gelöschte Auswerfen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f4259-129">It returns the deleted oject when passing in "-PassThru".</span></span>

## <span data-ttu-id="f4259-130">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4259-130">PARAMETERS</span></span>

### <span data-ttu-id="f4259-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4259-131">-DefaultProfile</span></span>
<span data-ttu-id="f4259-132">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f4259-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4259-133">-Name</span><span class="sxs-lookup"><span data-stu-id="f4259-133">-Name</span></span>
<span data-ttu-id="f4259-134">Gibt den Namen des vordefinierten Tags an, das entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f4259-134">Specifies the Name of the predefined tag to remove.</span></span>
<span data-ttu-id="f4259-135">Standardmäßig entfernt **"Remove-AzTag"** das angegebene Tag und alle werte.</span><span class="sxs-lookup"><span data-stu-id="f4259-135">By default, **Remove-AzTag** removes the specified tag and all of its values.</span></span>
<span data-ttu-id="f4259-136">Verwenden Sie den Parameter *"Value",* um ausgewählte Werte zu löschen, das Tag aber nicht zu löschen.</span><span class="sxs-lookup"><span data-stu-id="f4259-136">To delete selected values, but not delete the tag, use the *Value* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: RemovePredefinedTagParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4259-137">-Value</span><span class="sxs-lookup"><span data-stu-id="f4259-137">-Value</span></span>
<span data-ttu-id="f4259-138">Löscht die angegebenen Werte aus dem vordefinierten Tag, aber nicht das Tag.</span><span class="sxs-lookup"><span data-stu-id="f4259-138">Deletes the specified values from the predefined tag, but does not delete the tag.</span></span>

```yaml
Type: System.String[]
Parameter Sets: RemovePredefinedTagParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4259-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4259-139">-ResourceId</span></span>
<span data-ttu-id="f4259-140">Der Ressourcenbezeichner für die markierte Entität.</span><span class="sxs-lookup"><span data-stu-id="f4259-140">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="f4259-141">Möglicherweise ist eine Ressource, eine Ressourcengruppe oder ein Abonnement markiert.</span><span class="sxs-lookup"><span data-stu-id="f4259-141">A resource, a resource group or a subscription may be tagged.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4259-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f4259-142">-PassThru</span></span>
<span data-ttu-id="f4259-143">Gibt ein Objekt zurück, das das gelöschte Tag oder das resultierende Tag mit einem gelöschten Wert darstellt.</span><span class="sxs-lookup"><span data-stu-id="f4259-143">Returns an object that represents the deleted tag or the resulting tag with deleted valued.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4259-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4259-144">-Confirm</span></span>
<span data-ttu-id="f4259-145">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f4259-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4259-146">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f4259-146">-WhatIf</span></span>
<span data-ttu-id="f4259-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f4259-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4259-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f4259-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4259-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4259-149">CommonParameters</span></span>
<span data-ttu-id="f4259-150">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4259-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4259-151">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f4259-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4259-152">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f4259-152">INPUTS</span></span>

### <span data-ttu-id="f4259-153">System.String</span><span class="sxs-lookup"><span data-stu-id="f4259-153">System.String</span></span>

### <span data-ttu-id="f4259-154">System.String[]</span><span class="sxs-lookup"><span data-stu-id="f4259-154">System.String[]</span></span>

### <span data-ttu-id="f4259-155">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f4259-155">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f4259-156">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f4259-156">OUTPUTS</span></span>

### <span data-ttu-id="f4259-157">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span><span class="sxs-lookup"><span data-stu-id="f4259-157">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="f4259-158">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f4259-158">NOTES</span></span>

## <span data-ttu-id="f4259-159">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f4259-159">RELATED LINKS</span></span>

[<span data-ttu-id="f4259-160">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="f4259-160">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="f4259-161">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="f4259-161">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="f4259-162">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="f4259-162">Update-AzTag</span></span>](./Update-AzTag.md)