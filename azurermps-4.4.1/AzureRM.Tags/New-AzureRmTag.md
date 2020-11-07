---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM.Tags
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/New-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/New-AzureRmTag.md
ms.openlocfilehash: b5b7356a2cda001bb615700b38657cc0d3249ec5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663802"
---
# <span data-ttu-id="6bf0e-101">New-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="6bf0e-101">New-AzureRmTag</span></span>

## <span data-ttu-id="6bf0e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6bf0e-102">SYNOPSIS</span></span>
<span data-ttu-id="6bf0e-103">Erstellt eine vordefinierte Azure-Kategorie oder fügt Werte zu einem vorhandenen Tag hinzu.</span><span class="sxs-lookup"><span data-stu-id="6bf0e-103">Creates a predefined Azure tag or adds values to an existing tag.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6bf0e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6bf0e-104">SYNTAX</span></span>

```
New-AzureRmTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6bf0e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6bf0e-105">DESCRIPTION</span></span>
<span data-ttu-id="6bf0e-106">Das Cmdlet **New-AzureRmTag** erstellt ein vordefiniertes Azure-Tag mit einem optionalen vordefinierten Wert.</span><span class="sxs-lookup"><span data-stu-id="6bf0e-106">The **New-AzureRmTag** cmdlet creates a predefined Azure tag with an optional predefined value.</span></span>
<span data-ttu-id="6bf0e-107">Sie können es auch verwenden, um zusätzliche Werte zu vorhandenen vordefinierten Tags hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="6bf0e-107">You can also use it to add additional values to existing predefined tags.</span></span>
<span data-ttu-id="6bf0e-108">Wenn Sie ein vordefiniertes Tag erstellen möchten, geben Sie einen eindeutigen Tag-Namen ein.</span><span class="sxs-lookup"><span data-stu-id="6bf0e-108">To create a predefined tag, enter a unique tag name.</span></span>
<span data-ttu-id="6bf0e-109">Wenn Sie einen Wert zu einem vorhandenen vordefinierten Tag hinzufügen möchten, geben Sie den Namen des vorhandenen Tags und den neuen Wert an.</span><span class="sxs-lookup"><span data-stu-id="6bf0e-109">To add a value to an existing predefined tag, specify the name of the existing tag and the new value.</span></span>

<span data-ttu-id="6bf0e-110">Dieses Cmdlet gibt ein Objekt zurück, das das neue oder geänderte Tag mit seinen Werten und der Anzahl der Ressourcen darstellt, auf die es angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="6bf0e-110">This cmdlet returns an object that represents the new or modified tag with its values and the number of resources to which it has been applied.</span></span>

<span data-ttu-id="6bf0e-111">Das Azure-Tags-Modul, in dem **New-AzureRmTag** enthalten ist, kann Ihnen dabei helfen, vordefinierte Azure-Tags zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="6bf0e-111">The Azure Tags module that **New-AzureRmTag** is part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="6bf0e-112">Bei einem Azure-Tag handelt es sich um ein Name-Wert-Paar, mit dem Sie Ihre Azure-Ressourcen und Ressourcengruppen kategorisieren können, beispielsweise nach Abteilung oder Kostenstelle, oder um Notizen oder Kommentare zu Ressourcen und Gruppen zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="6bf0e-112">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>

<span data-ttu-id="6bf0e-113">Sie können Tags in einem einzigen Schritt definieren und anwenden, doch mit vordefinierten Tags können Sie standardmäßige, konsistente, vorhersagbare Namen und Werte für die Tags in Ihrem Abonnement einrichten.</span><span class="sxs-lookup"><span data-stu-id="6bf0e-113">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="6bf0e-114">Wenn das Abonnement vordefinierte Tags enthält, können Sie nicht definierte Tags oder Werte auf eine Ressource oder eine Ressourcengruppe im Abonnement anwenden.</span><span class="sxs-lookup"><span data-stu-id="6bf0e-114">If the subscription includes any predefined tags, you cannot apply undefined tags or values to any resource or resource group in the subscription.</span></span>

<span data-ttu-id="6bf0e-115">Wenn Sie eine vordefinierte Kategorie auf eine Ressource oder eine Ressourcengruppe anwenden möchten, verwenden Sie den *Tag* -Parameter des New-AzureRmTag-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="6bf0e-115">To apply a predefined tag to a resource or resource group, use the *Tag* parameter of the New-AzureRmTag cmdlet.</span></span>
<span data-ttu-id="6bf0e-116">Verwenden Sie den *Tag* -Parameter des Get-AzureRMResourceGroup-Cmdlets, um nach Ressourcengruppen mit einem angegebenen Tag-Namen oder-Namen und-Wert zu suchen.</span><span class="sxs-lookup"><span data-stu-id="6bf0e-116">To search for resource groups with a specified tag name or name and value, use the *Tag* parameter of the Get-AzureRMResourceGroup cmdlet.</span></span>

<span data-ttu-id="6bf0e-117">Jedes Tag hat einen Namen.</span><span class="sxs-lookup"><span data-stu-id="6bf0e-117">Every tag has a name.</span></span>
<span data-ttu-id="6bf0e-118">Die Werte sind optional.</span><span class="sxs-lookup"><span data-stu-id="6bf0e-118">The values are optional.</span></span>
<span data-ttu-id="6bf0e-119">Ein vordefiniertes Azure-Tag kann mehrere Werte aufweisen, doch wenn Sie das Tag auf eine Ressource oder eine Ressourcengruppe anwenden, wenden Sie den Tagnamen und nur einen seiner Werte an.</span><span class="sxs-lookup"><span data-stu-id="6bf0e-119">A predefined Azure tag can have multiple values, but when you apply the tag to a resource or resource group, you apply the tag name and only one of its values.</span></span>
<span data-ttu-id="6bf0e-120">So können Sie beispielsweise eine vordefinierte Abteilungs Kategorie mit einem Wert für jede Abteilung erstellen, beispielsweise Finance, Personalwesen und IT.</span><span class="sxs-lookup"><span data-stu-id="6bf0e-120">For example, you can create a predefined Department tag with a value for each department, such as Finance, Human Resources, and IT.</span></span>
<span data-ttu-id="6bf0e-121">Wenn Sie die Kategorie "Abteilung" auf eine Ressource anwenden, wenden Sie nur einen vordefinierten Wert wie "Finance" an.</span><span class="sxs-lookup"><span data-stu-id="6bf0e-121">When you apply the Department tag to a resource, you apply only one predefined value, such as Finance.</span></span>

## <span data-ttu-id="6bf0e-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6bf0e-122">EXAMPLES</span></span>

### <span data-ttu-id="6bf0e-123">Beispiel 1: Erstellen eines vordefinierten Tags</span><span class="sxs-lookup"><span data-stu-id="6bf0e-123">Example 1: Create a predefined tag</span></span>
```
PS C:\>New-AzureRmTag -Name "FY2015"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====

        Finance     0
```

<span data-ttu-id="6bf0e-124">Dieser Befehl erstellt ein vordefiniertes Tag mit dem Namen FY2015.</span><span class="sxs-lookup"><span data-stu-id="6bf0e-124">This command creates a predefined tag named FY2015.</span></span>
<span data-ttu-id="6bf0e-125">Dieses Tag hat keine Werte.</span><span class="sxs-lookup"><span data-stu-id="6bf0e-125">This tag has no values.</span></span>
<span data-ttu-id="6bf0e-126">Sie können eine Kategorie ohne Werte auf eine Ressource oder eine Ressourcengruppe anwenden oder mithilfe von **New-AzureRmTag** dem Tag Werte hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6bf0e-126">You can apply a tag with no values to a resource or resource group, or use **New-AzureRmTag** to add values to the tag.</span></span>
<span data-ttu-id="6bf0e-127">Sie können auch einen Wert angeben, wenn Sie die Kategorie auf die Ressourcen-oder Ressourcengruppe anwenden.</span><span class="sxs-lookup"><span data-stu-id="6bf0e-127">You can also specify a value when you apply the tag to the resource or resource group.</span></span>

### <span data-ttu-id="6bf0e-128">Beispiel 2: Erstellen eines vordefinierten Tags mit einem Wert</span><span class="sxs-lookup"><span data-stu-id="6bf0e-128">Example 2: Create a predefined tag with a value</span></span>
```
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

<span data-ttu-id="6bf0e-129">Mit diesem Befehl wird eine vordefinierte Kategorie mit dem Namen "Department" mit dem Wert "Finance" erstellt.</span><span class="sxs-lookup"><span data-stu-id="6bf0e-129">This command creates a predefined tag named Department with a value of Finance.</span></span>

### <span data-ttu-id="6bf0e-130">Beispiel 3: Hinzufügen eines Werts zu einem vordefinierten Tag</span><span class="sxs-lookup"><span data-stu-id="6bf0e-130">Example 3: Add a value to a predefined tag</span></span>
```
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0 PS C:\>New-AzureRmTag -Name "Department" -Value "IT"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0
        IT          0
```

<span data-ttu-id="6bf0e-131">Mit diesen Befehlen wird ein vordefiniertes Tag mit dem Namen Department mit zwei Werten erstellt.</span><span class="sxs-lookup"><span data-stu-id="6bf0e-131">These commands create a predefined tag named Department with two values.</span></span>
<span data-ttu-id="6bf0e-132">Wenn der Tag-Name vorhanden ist, fügt **New-AzureRmTag** den Wert dem vorhandenen Tag hinzu, anstatt eine neue zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6bf0e-132">If the tag name exists, **New-AzureRmTag** adds the value to the existing tag instead of creating a new one.</span></span>

### <span data-ttu-id="6bf0e-133">Beispiel 4: Verwenden eines vordefinierten Tags</span><span class="sxs-lookup"><span data-stu-id="6bf0e-133">Example 4: Use a predefined tag</span></span>
```
PS C:\>New-AzureRmTag -Name "CostCenter" -Value "0001"
Name:   CostCenter
Count:  0
Values: 
        Name        Count
        =========   =====
        0001        0 PS C:\>Set-AzureRmResourceGroup -Name "EngineerBlog" -Tag @{Name="CostCenter";Value="0001"}
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
    CostCenter   0001 PS C:\>Get-AzureRmTag -Name "CostCenter"
Name:   CostCenter
Count:  1
Values: 
        Name        Count
        =========   =====
        0001        1 PS C:\>Get-AzureRmResourceGroup -Tag @{Name="CostCenter"}
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

<span data-ttu-id="6bf0e-134">Mit den Befehlen in diesem Beispiel wird ein vordefiniertes Tag erstellt und verwendet.</span><span class="sxs-lookup"><span data-stu-id="6bf0e-134">The commands in this example create and use a predefined tag.</span></span>

## <span data-ttu-id="6bf0e-135">Parameter</span><span class="sxs-lookup"><span data-stu-id="6bf0e-135">PARAMETERS</span></span>

### <span data-ttu-id="6bf0e-136">-Name</span><span class="sxs-lookup"><span data-stu-id="6bf0e-136">-Name</span></span>
<span data-ttu-id="6bf0e-137">Gibt den Namen der Kategorie an.</span><span class="sxs-lookup"><span data-stu-id="6bf0e-137">Specifies the tag name.</span></span>
<span data-ttu-id="6bf0e-138">Wenn Sie ein neues vordefiniertes Tag erstellen möchten, geben Sie einen eindeutigen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="6bf0e-138">To create a new predefined tag, enter a unique name.</span></span>

<span data-ttu-id="6bf0e-139">Wenn Sie einen Wert zu einer vorhandenen Kategorie hinzufügen möchten, geben Sie den Namen des vorhandenen Tags ein.</span><span class="sxs-lookup"><span data-stu-id="6bf0e-139">To add a value to an existing tag, enter the name of the existing tag.</span></span>
<span data-ttu-id="6bf0e-140">Wenn ein vorhandenes vordefiniertes Tag den angegebenen Namen aufweist, fügt **New-AzureRmTag** den angegebenen Wert, falls vorhanden, dem Tag mit diesem Namen hinzu, anstatt eine neue Kategorie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6bf0e-140">If an existing predefined tag has the specified name, **New-AzureRmTag** adds the specified value, if any, to the tag with that name instead of creating a new tag.</span></span>

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

### <span data-ttu-id="6bf0e-141">-Wert</span><span class="sxs-lookup"><span data-stu-id="6bf0e-141">-Value</span></span>
<span data-ttu-id="6bf0e-142">Gibt einen Tag-Wert an.</span><span class="sxs-lookup"><span data-stu-id="6bf0e-142">Specifies a tag value.</span></span>
<span data-ttu-id="6bf0e-143">Vordefinierte Tags können mehrere Werte haben, aber Sie können in jedem Befehl nur einen Wert eingeben.</span><span class="sxs-lookup"><span data-stu-id="6bf0e-143">Predefined tags can have multiple values, but you can enter only one value in each command.</span></span>
<span data-ttu-id="6bf0e-144">Dieser Parameter ist optional, da Tags Namen ohne Werte enthalten können.</span><span class="sxs-lookup"><span data-stu-id="6bf0e-144">This parameter is optional, because tags can have names without values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bf0e-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bf0e-145">-DefaultProfile</span></span>
<span data-ttu-id="6bf0e-146">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6bf0e-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6bf0e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bf0e-147">CommonParameters</span></span>
<span data-ttu-id="6bf0e-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bf0e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bf0e-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bf0e-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bf0e-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6bf0e-150">INPUTS</span></span>

### <span data-ttu-id="6bf0e-151">Keine</span><span class="sxs-lookup"><span data-stu-id="6bf0e-151">None</span></span>

## <span data-ttu-id="6bf0e-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6bf0e-152">OUTPUTS</span></span>

### <span data-ttu-id="6bf0e-153">Microsoft. Azure. Commands. Tags. Model. PSTag</span><span class="sxs-lookup"><span data-stu-id="6bf0e-153">Microsoft.Azure.Commands.Tags.Model.PSTag</span></span>

## <span data-ttu-id="6bf0e-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="6bf0e-154">NOTES</span></span>

## <span data-ttu-id="6bf0e-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6bf0e-155">RELATED LINKS</span></span>

[<span data-ttu-id="6bf0e-156">Get-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="6bf0e-156">Get-AzureRmTag</span></span>](./Get-AzureRmTag.md)

[<span data-ttu-id="6bf0e-157">Remove-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="6bf0e-157">Remove-AzureRmTag</span></span>](./Remove-AzureRmTag.md)


