---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzTag.md
ms.openlocfilehash: 242f207faa98c6165e4c64f095f9b171f1d72d5c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843316"
---
# <span data-ttu-id="133fd-101">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="133fd-101">New-AzTag</span></span>

## <span data-ttu-id="133fd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="133fd-102">SYNOPSIS</span></span>
<span data-ttu-id="133fd-103">Erstellt eine vordefinierte Azure-Kategorie oder fügt Werte zu einem vorhandenen Tag hinzu.</span><span class="sxs-lookup"><span data-stu-id="133fd-103">Creates a predefined Azure tag or adds values to an existing tag.</span></span>

## <span data-ttu-id="133fd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="133fd-104">SYNTAX</span></span>

```
New-AzTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="133fd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="133fd-105">DESCRIPTION</span></span>
<span data-ttu-id="133fd-106">Das Cmdlet **New-AzTag** erstellt ein vordefiniertes Azure-Tag mit einem optionalen vordefinierten Wert.</span><span class="sxs-lookup"><span data-stu-id="133fd-106">The **New-AzTag** cmdlet creates a predefined Azure tag with an optional predefined value.</span></span>
<span data-ttu-id="133fd-107">Sie können es auch verwenden, um zusätzliche Werte zu vorhandenen vordefinierten Tags hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="133fd-107">You can also use it to add additional values to existing predefined tags.</span></span>
<span data-ttu-id="133fd-108">Wenn Sie ein vordefiniertes Tag erstellen möchten, geben Sie einen eindeutigen Tag-Namen ein.</span><span class="sxs-lookup"><span data-stu-id="133fd-108">To create a predefined tag, enter a unique tag name.</span></span>
<span data-ttu-id="133fd-109">Wenn Sie einen Wert zu einem vorhandenen vordefinierten Tag hinzufügen möchten, geben Sie den Namen des vorhandenen Tags und den neuen Wert an.</span><span class="sxs-lookup"><span data-stu-id="133fd-109">To add a value to an existing predefined tag, specify the name of the existing tag and the new value.</span></span>
<span data-ttu-id="133fd-110">Dieses Cmdlet gibt ein Objekt zurück, das das neue oder geänderte Tag mit seinen Werten und der Anzahl der Ressourcen darstellt, auf die es angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="133fd-110">This cmdlet returns an object that represents the new or modified tag with its values and the number of resources to which it has been applied.</span></span>
<span data-ttu-id="133fd-111">Das Azure-Tags-Modul, in dem **New-AzTag** enthalten ist, kann Ihnen dabei helfen, vordefinierte Azure-Tags zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="133fd-111">The Azure Tags module that **New-AzTag** is part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="133fd-112">Bei einem Azure-Tag handelt es sich um ein Name-Wert-Paar, mit dem Sie Ihre Azure-Ressourcen und Ressourcengruppen kategorisieren können, beispielsweise nach Abteilung oder Kostenstelle, oder um Notizen oder Kommentare zu Ressourcen und Gruppen zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="133fd-112">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="133fd-113">Sie können Tags in einem einzigen Schritt definieren und anwenden, doch mit vordefinierten Tags können Sie standardmäßige, konsistente, vorhersagbare Namen und Werte für die Tags in Ihrem Abonnement einrichten.</span><span class="sxs-lookup"><span data-stu-id="133fd-113">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="133fd-114">Wenn Sie eine vordefinierte Kategorie auf eine Ressource oder eine Ressourcengruppe anwenden möchten, verwenden Sie den *Tag* -Parameter des New-AzTag-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="133fd-114">To apply a predefined tag to a resource or resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="133fd-115">Verwenden Sie den *Tag* -Parameter des Get-AzResourceGroup-Cmdlets, um nach Ressourcengruppen mit einem angegebenen Tag-Namen oder-Namen und-Wert zu suchen.</span><span class="sxs-lookup"><span data-stu-id="133fd-115">To search for resource groups with a specified tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="133fd-116">Jedes Tag hat einen Namen.</span><span class="sxs-lookup"><span data-stu-id="133fd-116">Every tag has a name.</span></span>
<span data-ttu-id="133fd-117">Die Werte sind optional.</span><span class="sxs-lookup"><span data-stu-id="133fd-117">The values are optional.</span></span>
<span data-ttu-id="133fd-118">Ein vordefiniertes Azure-Tag kann mehrere Werte aufweisen, doch wenn Sie das Tag auf eine Ressource oder eine Ressourcengruppe anwenden, wenden Sie den Tagnamen und nur einen seiner Werte an.</span><span class="sxs-lookup"><span data-stu-id="133fd-118">A predefined Azure tag can have multiple values, but when you apply the tag to a resource or resource group, you apply the tag name and only one of its values.</span></span>
<span data-ttu-id="133fd-119">So können Sie beispielsweise eine vordefinierte Abteilungs Kategorie mit einem Wert für jede Abteilung erstellen, beispielsweise Finance, Personalwesen und IT.</span><span class="sxs-lookup"><span data-stu-id="133fd-119">For example, you can create a predefined Department tag with a value for each department, such as Finance, Human Resources, and IT.</span></span>
<span data-ttu-id="133fd-120">Wenn Sie die Kategorie "Abteilung" auf eine Ressource anwenden, wenden Sie nur einen vordefinierten Wert wie "Finance" an.</span><span class="sxs-lookup"><span data-stu-id="133fd-120">When you apply the Department tag to a resource, you apply only one predefined value, such as Finance.</span></span>

## <span data-ttu-id="133fd-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="133fd-121">EXAMPLES</span></span>

### <span data-ttu-id="133fd-122">Beispiel 1: Erstellen eines vordefinierten Tags</span><span class="sxs-lookup"><span data-stu-id="133fd-122">Example 1: Create a predefined tag</span></span>
```
PS C:\>New-AzTag -Name "FY2015"
                                
Name   ValuesTable Count Values 
----   ----------- ----- ------
FY2015             0     {}
```

<span data-ttu-id="133fd-123">Dieser Befehl erstellt ein vordefiniertes Tag mit dem Namen FY2015.</span><span class="sxs-lookup"><span data-stu-id="133fd-123">This command creates a predefined tag named FY2015.</span></span>
<span data-ttu-id="133fd-124">Dieses Tag hat keine Werte.</span><span class="sxs-lookup"><span data-stu-id="133fd-124">This tag has no values.</span></span>
<span data-ttu-id="133fd-125">Sie können eine Kategorie ohne Werte auf eine Ressource oder eine Ressourcengruppe anwenden oder mithilfe von **New-AzTag** dem Tag Werte hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="133fd-125">You can apply a tag with no values to a resource or resource group, or use **New-AzTag** to add values to the tag.</span></span>
<span data-ttu-id="133fd-126">Sie können auch einen Wert angeben, wenn Sie die Kategorie auf die Ressourcen-oder Ressourcengruppe anwenden.</span><span class="sxs-lookup"><span data-stu-id="133fd-126">You can also specify a value when you apply the tag to the resource or resource group.</span></span>

### <span data-ttu-id="133fd-127">Beispiel 2: Erstellen eines vordefinierten Tags mit einem Wert</span><span class="sxs-lookup"><span data-stu-id="133fd-127">Example 2: Create a predefined tag with a value</span></span>
```
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

<span data-ttu-id="133fd-128">Mit diesem Befehl wird eine vordefinierte Kategorie mit dem Namen "Department" mit dem Wert "Finance" erstellt.</span><span class="sxs-lookup"><span data-stu-id="133fd-128">This command creates a predefined tag named Department with a value of Finance.</span></span>

### <span data-ttu-id="133fd-129">Beispiel 3: Hinzufügen eines Werts zu einem vordefinierten Tag</span><span class="sxs-lookup"><span data-stu-id="133fd-129">Example 3: Add a value to a predefined tag</span></span>
```
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

<span data-ttu-id="133fd-130">Mit diesen Befehlen wird ein vordefiniertes Tag mit dem Namen Department mit zwei Werten erstellt.</span><span class="sxs-lookup"><span data-stu-id="133fd-130">These commands create a predefined tag named Department with two values.</span></span>
<span data-ttu-id="133fd-131">Wenn der Tag-Name vorhanden ist, fügt **New-AzTag** den Wert dem vorhandenen Tag hinzu, anstatt eine neue zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="133fd-131">If the tag name exists, **New-AzTag** adds the value to the existing tag instead of creating a new one.</span></span>

### <span data-ttu-id="133fd-132">Beispiel 4: Verwenden eines vordefinierten Tags</span><span class="sxs-lookup"><span data-stu-id="133fd-132">Example 4: Use a predefined tag</span></span>
```
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

<span data-ttu-id="133fd-133">Mit den Befehlen in diesem Beispiel wird ein vordefiniertes Tag erstellt und verwendet.</span><span class="sxs-lookup"><span data-stu-id="133fd-133">The commands in this example create and use a predefined tag.</span></span>

## <span data-ttu-id="133fd-134">Parameter</span><span class="sxs-lookup"><span data-stu-id="133fd-134">PARAMETERS</span></span>

### <span data-ttu-id="133fd-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="133fd-135">-DefaultProfile</span></span>
<span data-ttu-id="133fd-136">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="133fd-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="133fd-137">-Name</span><span class="sxs-lookup"><span data-stu-id="133fd-137">-Name</span></span>
<span data-ttu-id="133fd-138">Gibt den Namen der Kategorie an.</span><span class="sxs-lookup"><span data-stu-id="133fd-138">Specifies the tag name.</span></span>
<span data-ttu-id="133fd-139">Wenn Sie ein neues vordefiniertes Tag erstellen möchten, geben Sie einen eindeutigen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="133fd-139">To create a new predefined tag, enter a unique name.</span></span>
<span data-ttu-id="133fd-140">Wenn Sie einen Wert zu einer vorhandenen Kategorie hinzufügen möchten, geben Sie den Namen des vorhandenen Tags ein.</span><span class="sxs-lookup"><span data-stu-id="133fd-140">To add a value to an existing tag, enter the name of the existing tag.</span></span>
<span data-ttu-id="133fd-141">Wenn ein vorhandenes vordefiniertes Tag den angegebenen Namen aufweist, fügt **New-AzTag** den angegebenen Wert, falls vorhanden, dem Tag mit diesem Namen hinzu, anstatt eine neue Kategorie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="133fd-141">If an existing predefined tag has the specified name, **New-AzTag** adds the specified value, if any, to the tag with that name instead of creating a new tag.</span></span>

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

### <span data-ttu-id="133fd-142">-Wert</span><span class="sxs-lookup"><span data-stu-id="133fd-142">-Value</span></span>
<span data-ttu-id="133fd-143">Gibt einen Tag-Wert an.</span><span class="sxs-lookup"><span data-stu-id="133fd-143">Specifies a tag value.</span></span>
<span data-ttu-id="133fd-144">Vordefinierte Tags können mehrere Werte haben, aber Sie können in jedem Befehl nur einen Wert eingeben.</span><span class="sxs-lookup"><span data-stu-id="133fd-144">Predefined tags can have multiple values, but you can enter only one value in each command.</span></span>
<span data-ttu-id="133fd-145">Dieser Parameter ist optional, da Tags Namen ohne Werte enthalten können.</span><span class="sxs-lookup"><span data-stu-id="133fd-145">This parameter is optional, because tags can have names without values.</span></span>

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

### <span data-ttu-id="133fd-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="133fd-146">CommonParameters</span></span>
<span data-ttu-id="133fd-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="133fd-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="133fd-148">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="133fd-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="133fd-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="133fd-149">INPUTS</span></span>

### <span data-ttu-id="133fd-150">System. String</span><span class="sxs-lookup"><span data-stu-id="133fd-150">System.String</span></span>

## <span data-ttu-id="133fd-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="133fd-151">OUTPUTS</span></span>

### <span data-ttu-id="133fd-152">Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag</span><span class="sxs-lookup"><span data-stu-id="133fd-152">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag</span></span>

## <span data-ttu-id="133fd-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="133fd-153">NOTES</span></span>

## <span data-ttu-id="133fd-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="133fd-154">RELATED LINKS</span></span>

[<span data-ttu-id="133fd-155">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="133fd-155">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="133fd-156">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="133fd-156">Remove-AzTag</span></span>](./Remove-AzTag.md)

