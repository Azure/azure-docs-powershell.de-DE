---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM.Tags
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.tags/remove-azurermtag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Remove-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Remove-AzureRmTag.md
ms.openlocfilehash: 1c7f55bb3f84051326cd102c1c12a2d978a79f71
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664790"
---
# <span data-ttu-id="e75bf-101">Remove-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="e75bf-101">Remove-AzureRmTag</span></span>

## <span data-ttu-id="e75bf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e75bf-102">SYNOPSIS</span></span>
<span data-ttu-id="e75bf-103">Löscht vordefinierte Azure-Tags oder-Werte.</span><span class="sxs-lookup"><span data-stu-id="e75bf-103">Deletes predefined Azure tags or values.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e75bf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e75bf-104">SYNTAX</span></span>

```
Remove-AzureRmTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e75bf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e75bf-105">DESCRIPTION</span></span>
<span data-ttu-id="e75bf-106">Das Cmdlet **Remove-AzureRmTag** löscht vordefinierte Azure-Tags und-Werte aus Ihrem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e75bf-106">The **Remove-AzureRmTag** cmdlet deletes predefined Azure tags and values from your subscription.</span></span>
<span data-ttu-id="e75bf-107">Verwenden Sie den *value* -Parameter, um bestimmte Werte aus einem vordefinierten Tag zu löschen.</span><span class="sxs-lookup"><span data-stu-id="e75bf-107">To delete particular values from a predefined tag, use the *Value* parameter.</span></span>
<span data-ttu-id="e75bf-108">Standardmäßig löscht **Remove-AzureRmTag** das angegebene Tag und alle seine Werte. Sie können eine Kategorie oder einen Wert, der aktuell auf eine Ressource oder eine Ressourcengruppe angewendet wird, nicht löschen.</span><span class="sxs-lookup"><span data-stu-id="e75bf-108">By default, **Remove-AzureRmTag** deletes the specified tag and all of its values.You cannot delete a tag or value that is currently applied to a resource or resource group.</span></span>
<span data-ttu-id="e75bf-109">Verwenden Sie vor der Verwendung von **Remove-AzureRmTag** den *Tag* -Parameter des Set-AzureRMResourceGroup-Cmdlets, um das Tag oder die Werte aus der Ressourcen-oder Ressourcengruppe zu löschen.</span><span class="sxs-lookup"><span data-stu-id="e75bf-109">Before using **Remove-AzureRmTag** , use the *Tag* parameter of the Set-AzureRMResourceGroup cmdlet to delete the tag or values from the resource or resource group.</span></span>
<span data-ttu-id="e75bf-110">Das Azure-Tags-Modul, in dem **Remove-AzureRmTag** enthalten ist, kann Ihnen bei der Verwaltung Ihrer vordefinierten Azure-Tags helfen.</span><span class="sxs-lookup"><span data-stu-id="e75bf-110">The Azure Tags module that **Remove-AzureRmTag** is part of can help you manage your predefined Azure tags.</span></span>
<span data-ttu-id="e75bf-111">Bei einem Azure-Tag handelt es sich um ein Name-Wert-Paar, mit dem Sie Ihre Azure-Ressourcen und Ressourcengruppen kategorisieren können, beispielsweise nach Abteilung oder Kostenstelle, oder um Notizen oder Kommentare zu Ressourcen und Gruppen zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="e75bf-111">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="e75bf-112">Sie können Tags in einem einzigen Schritt definieren und anwenden, doch mit vordefinierten Tags können Sie standardmäßige, konsistente, vorhersagbare Namen und Werte für die Tags in Ihrem Abonnement einrichten.</span><span class="sxs-lookup"><span data-stu-id="e75bf-112">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>

## <span data-ttu-id="e75bf-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e75bf-113">EXAMPLES</span></span>

### <span data-ttu-id="e75bf-114">Beispiel 1: Löschen eines vordefinierten Tags</span><span class="sxs-lookup"><span data-stu-id="e75bf-114">Example 1: Delete a predefined tag</span></span>
```
PS C:\>Remove-AzureRmTag -Name "Department"
```

<span data-ttu-id="e75bf-115">Mit diesem Befehl wird das vordefinierte Tag "Department" und alle zugehörigen Ressourcen gelöscht.</span><span class="sxs-lookup"><span data-stu-id="e75bf-115">This command deletes the predefined tag named Department and all of its resources.</span></span>
<span data-ttu-id="e75bf-116">Wenn das Tag auf Ressourcen oder Ressourcengruppen angewendet wurde, schlägt der Befehl fehl.</span><span class="sxs-lookup"><span data-stu-id="e75bf-116">If the tag has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="e75bf-117">Beispiel 2: Löschen eines Werts aus einem vordefinierten Tag</span><span class="sxs-lookup"><span data-stu-id="e75bf-117">Example 2: Delete a value from a predefined tag</span></span>
```
PS C:\>Remove-AzureRmTag -Name "Department" -Value "HumanResources" -PassThru
Name:   Department
Count:  14
Values: 

        Name        Count
        =========   =====

        Finance        2
        IT            12
```

<span data-ttu-id="e75bf-118">Dieser Befehl löscht den HumanResources-Wert aus dem vordefinierten Department-Tag.</span><span class="sxs-lookup"><span data-stu-id="e75bf-118">This command deletes the HumanResources value from the predefined Department tag.</span></span>
<span data-ttu-id="e75bf-119">Die Kategorie wird nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="e75bf-119">It does not delete the tag.</span></span>
<span data-ttu-id="e75bf-120">Wenn der Wert auf Ressourcen oder Ressourcengruppen angewendet wurde, schlägt der Befehl fehl.</span><span class="sxs-lookup"><span data-stu-id="e75bf-120">If the value has been applied to any resources or resource groups, the command fails.</span></span>

## <span data-ttu-id="e75bf-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="e75bf-121">PARAMETERS</span></span>

### <span data-ttu-id="e75bf-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e75bf-122">-DefaultProfile</span></span>
<span data-ttu-id="e75bf-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e75bf-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e75bf-124">-Name</span><span class="sxs-lookup"><span data-stu-id="e75bf-124">-Name</span></span>
<span data-ttu-id="e75bf-125">Gibt den Namen der zu löschenden Kategorie an.</span><span class="sxs-lookup"><span data-stu-id="e75bf-125">Specifies the name of the tag to be deleted.</span></span>
<span data-ttu-id="e75bf-126">Standardmäßig entfernt **Remove-AzureRmTag** das angegebene Tag und alle seine Werte.</span><span class="sxs-lookup"><span data-stu-id="e75bf-126">By default, **Remove-AzureRmTag** removes the specified tag and all of its values.</span></span>
<span data-ttu-id="e75bf-127">Verwenden Sie den *Wert* -Parameter, um ausgewählte Werte zu löschen, aber die Kategorie nicht zu löschen.</span><span class="sxs-lookup"><span data-stu-id="e75bf-127">To delete selected values, but not delete the tag, use the *Value* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e75bf-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e75bf-128">-PassThru</span></span>
<span data-ttu-id="e75bf-129">Gibt ein Objekt zurück, das das gelöschte Tag oder das resultierende Tag mit gelöschten Werten darstellt.</span><span class="sxs-lookup"><span data-stu-id="e75bf-129">Returns an object that represents the deleted tag or the resulting tag with deleted valued.</span></span>

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

### <span data-ttu-id="e75bf-130">-Wert</span><span class="sxs-lookup"><span data-stu-id="e75bf-130">-Value</span></span>
<span data-ttu-id="e75bf-131">Löscht die angegebenen Werte aus dem vordefinierten Tag, löscht das Tag aber nicht.</span><span class="sxs-lookup"><span data-stu-id="e75bf-131">Deletes the specified values from the predefined tag, but does not delete the tag.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e75bf-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e75bf-132">-Confirm</span></span>
<span data-ttu-id="e75bf-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e75bf-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e75bf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e75bf-134">-WhatIf</span></span>
<span data-ttu-id="e75bf-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e75bf-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e75bf-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e75bf-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e75bf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e75bf-137">CommonParameters</span></span>
<span data-ttu-id="e75bf-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e75bf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e75bf-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e75bf-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e75bf-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e75bf-140">INPUTS</span></span>

### <span data-ttu-id="e75bf-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e75bf-141">System.String</span></span>

### <span data-ttu-id="e75bf-142">System. String []</span><span class="sxs-lookup"><span data-stu-id="e75bf-142">System.String[]</span></span>

### <span data-ttu-id="e75bf-143">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="e75bf-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e75bf-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e75bf-144">OUTPUTS</span></span>

### <span data-ttu-id="e75bf-145">Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag</span><span class="sxs-lookup"><span data-stu-id="e75bf-145">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag</span></span>

## <span data-ttu-id="e75bf-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="e75bf-146">NOTES</span></span>

## <span data-ttu-id="e75bf-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e75bf-147">RELATED LINKS</span></span>

[<span data-ttu-id="e75bf-148">Get-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="e75bf-148">Get-AzureRmTag</span></span>](./Get-AzureRmTag.md)

[<span data-ttu-id="e75bf-149">Neu – AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="e75bf-149">New-AzureRmTag</span></span>](./New-AzureRmTag.md)


