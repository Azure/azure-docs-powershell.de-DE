---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: 058f4a61f1e7ff2fe7f416ea0e4ada098c9efe51
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301066"
---
# <span data-ttu-id="15e68-101">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="15e68-101">Get-AzTag</span></span>

## <span data-ttu-id="15e68-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="15e68-102">SYNOPSIS</span></span>
<span data-ttu-id="15e68-103">Ruft vordefinierte Azure-Tags ab | Ruft den gesamten Satz von Tags für eine Ressource oder ein Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="15e68-103">Gets predefined Azure tags | Gets the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="15e68-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="15e68-104">SYNTAX</span></span>

### <span data-ttu-id="15e68-105">GetPredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="15e68-105">GetPredefinedTagParameterSet</span></span>
```
Get-AzTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15e68-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="15e68-106">GetByResourceIdParameterSet</span></span>
```
Get-AzTag -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15e68-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="15e68-107">DESCRIPTION</span></span>

<span data-ttu-id="15e68-108">**GetPredefinedTagSet** : mit dem Cmdlet **Get-AzTag werden** in Ihrem Abonnement vordefinierte Azure-Tags abgerufen.</span><span class="sxs-lookup"><span data-stu-id="15e68-108">**GetPredefinedTagSet** : The **Get-AzTag** cmdlet gets predefined Azure tags in your subscription.</span></span>
<span data-ttu-id="15e68-109">Dieses Cmdlet gibt grundlegende Informationen zu den Tags oder detaillierte Informationen zu Tags und deren Werten zurück.</span><span class="sxs-lookup"><span data-stu-id="15e68-109">This cmdlet returns basic information about the tags or detailed information about tags and their values.</span></span>
<span data-ttu-id="15e68-110">Alle Ausgabeobjekte enthalten eine Count-Eigenschaft, die die Anzahl der Ressourcen und Ressourcengruppen darstellt, auf die die Kategorien und Werte angewendet wurden.</span><span class="sxs-lookup"><span data-stu-id="15e68-110">All output objects include a Count property that represents the number of resources and resource groups to which the tags and values have been applied.</span></span>
<span data-ttu-id="15e68-111">Das Azure-Tags-Modul, in dem **Get-AzTag** enthalten ist, kann Ihnen helfen, vordefinierte Azure-Tags zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="15e68-111">The Azure Tags module that **Get-AzTag** is a part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="15e68-112">Bei einem Azure-Tag handelt es sich um ein Name-Wert-Paar, mit dem Sie Ihre Azure-Ressourcen und Ressourcengruppen kategorisieren können, beispielsweise nach Abteilung oder Kostenstelle, oder um Notizen oder Kommentare zu Ressourcen und Gruppen zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="15e68-112">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="15e68-113">Sie können Tags in einem einzigen Schritt definieren und anwenden, doch mit vordefinierten Tags können Sie standardmäßige, konsistente, vorhersagbare Namen und Werte für die Tags in Ihrem Abonnement einrichten.</span><span class="sxs-lookup"><span data-stu-id="15e68-113">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="15e68-114">Verwenden Sie das New-AzTag-Cmdlet, um eine vordefinierte Kategorie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="15e68-114">To create a predefined tag, use the New-AzTag cmdlet.</span></span>
<span data-ttu-id="15e68-115">Wenn Sie eine vordefinierte Kategorie auf eine Ressourcengruppe anwenden möchten, verwenden Sie den *Tag* -Parameter des New-AzTag-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="15e68-115">To apply a predefined tag to a resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="15e68-116">Verwenden Sie den *Tag* -Parameter des Get-AzResourceGroup-Cmdlets, um Ressourcengruppen nach einem bestimmten Tag-Namen oder-Namen und-Wert zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="15e68-116">To search resource groups for a specific tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>

<span data-ttu-id="15e68-117">**GetByResourceIdParameterSet** : das Cmdlet " **Get-AzTag** " mit einer Ressourcen **Quelle** Ruft den gesamten Satz von Tags für eine Ressource oder ein Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="15e68-117">**GetByResourceIdParameterSet** : The **Get-AzTag** cmdlet with a **ResourceId** gets the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="15e68-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="15e68-118">EXAMPLES</span></span>

### <span data-ttu-id="15e68-119">Beispiel 1: Abrufen aller vordefinierten Tags</span><span class="sxs-lookup"><span data-stu-id="15e68-119">Example 1: Get all predefined tags</span></span>
```powershell
PS C:\>Get-AzTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

<span data-ttu-id="15e68-120">Dieser Befehl ruft alle vordefinierten Tags im Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="15e68-120">This command gets all predefined tags in the subscription.</span></span>
<span data-ttu-id="15e68-121">Die Count-Eigenschaft zeigt, wie oft das Tag auf Ressourcen und Ressourcengruppen im Abonnement angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="15e68-121">The Count property shows how many times the tag has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="15e68-122">Beispiel 2: Abrufen einer Kategorie nach Name</span><span class="sxs-lookup"><span data-stu-id="15e68-122">Example 2: Get a tag by name</span></span>
```powershell
PS C:\>Get-AzTag -Name "Department"

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3
```

<span data-ttu-id="15e68-123">Dieser Befehl erhält detaillierte Informationen über das Department-Tag und seine Werte.</span><span class="sxs-lookup"><span data-stu-id="15e68-123">This command gets detailed information about the Department tag and its values.</span></span>
<span data-ttu-id="15e68-124">Die Count-Eigenschaft zeigt an, wie oft das Tag und jeder seiner Werte auf Ressourcen und Ressourcengruppen im Abonnement angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="15e68-124">The Count property shows how many times the tag and each of its values has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="15e68-125">Beispiel 3: Abrufen von Werten aller Tags</span><span class="sxs-lookup"><span data-stu-id="15e68-125">Example 3: Get values of all tags</span></span>
```powershell
PS C:\>Get-AzTag -Detailed

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3


Name:   FY2015
Count:  2


Name:   CostCenter
Count:  20
Values: 

        Name        Count
        ==========  =====

        0001          5
        0002         10
        0003          5
```

<span data-ttu-id="15e68-126">Dieser Befehl verwendet den *detaillierten* Parameter, um detaillierte Informationen zu allen vordefinierten Tags im Abonnement abzurufen.</span><span class="sxs-lookup"><span data-stu-id="15e68-126">This command uses the *Detailed* parameter to get detailed information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="15e68-127">Die Verwendung des Parameters *detaillierte* entspricht der Verwendung des Parameters *Name* für jedes Tag.</span><span class="sxs-lookup"><span data-stu-id="15e68-127">Using the *Detailed* parameter is the equivalent of using the *Name* parameter for every tag.</span></span>

### <span data-ttu-id="15e68-128">Beispiel 4: Abrufen der gesamten Gruppe von Transpondern in einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="15e68-128">Example 4: Get the entire set of tags on a subscription</span></span>

```powershell
PS C:\>Get-AzTag -ResourceId /subscriptions/{subId}

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             tagKey1  tagValue1
             tagKey2  tagValue2
```

<span data-ttu-id="15e68-129">Mit diesem Befehl wird der gesamte Satz von Tags für das Abonnement mit {subId} abgerufen.</span><span class="sxs-lookup"><span data-stu-id="15e68-129">This command gets the entire set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="15e68-130">Beispiel 5: Abrufen der gesamten Gruppe von Tags für eine Ressource</span><span class="sxs-lookup"><span data-stu-id="15e68-130">Example 5: Get the entire set of tags on a resource</span></span>

```powershell
PS C:\>Get-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

<span data-ttu-id="15e68-131">Mit diesem Befehl wird der gesamte Satz von Tags für die Ressource mit {Ressourcenkennung} abgerufen.</span><span class="sxs-lookup"><span data-stu-id="15e68-131">This command gets the entire set of tags on the resource with {resourceId}.</span></span>

## <span data-ttu-id="15e68-132">Parameter</span><span class="sxs-lookup"><span data-stu-id="15e68-132">PARAMETERS</span></span>

### <span data-ttu-id="15e68-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15e68-133">-DefaultProfile</span></span>
<span data-ttu-id="15e68-134">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="15e68-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15e68-135">-Detailliert</span><span class="sxs-lookup"><span data-stu-id="15e68-135">-Detailed</span></span>
<span data-ttu-id="15e68-136">Gibt an, dass dieser Vorgang der Ausgabe Informationen zu Transponder Werten hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="15e68-136">Indicates that this operation adds information about tag values to the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetPredefinedTagParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15e68-137">-Name</span><span class="sxs-lookup"><span data-stu-id="15e68-137">-Name</span></span>
<span data-ttu-id="15e68-138">Der Name des vordefinierten Tags.</span><span class="sxs-lookup"><span data-stu-id="15e68-138">Name of the predefined tag.</span></span>
<span data-ttu-id="15e68-139">Standardmäßig ruft **Get-AzTag** grundlegende Informationen zu allen vordefinierten Tags im Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="15e68-139">By default, **Get-AzTag** gets basic information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="15e68-140">Wenn Sie den Parameter *Name* angeben, hat der *Detail* Parameter keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="15e68-140">When you specify the *Name* parameter, the *Detailed* parameter has no effect.</span></span>

```yaml
Type: System.String
Parameter Sets: GetPredefinedTagParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15e68-141">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="15e68-141">-ResourceId</span></span>
<span data-ttu-id="15e68-142">Der Ressourcenbezeichner für die markierte Entität.</span><span class="sxs-lookup"><span data-stu-id="15e68-142">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="15e68-143">Eine Ressource, eine Ressourcengruppe oder ein Abonnement können markiert sein.</span><span class="sxs-lookup"><span data-stu-id="15e68-143">A resource, a resource group or a subscription may be tagged.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15e68-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15e68-144">CommonParameters</span></span>
<span data-ttu-id="15e68-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15e68-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15e68-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15e68-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15e68-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="15e68-147">INPUTS</span></span>

### <span data-ttu-id="15e68-148">System. String</span><span class="sxs-lookup"><span data-stu-id="15e68-148">System.String</span></span>

### <span data-ttu-id="15e68-149">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="15e68-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="15e68-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="15e68-150">OUTPUTS</span></span>

### <span data-ttu-id="15e68-151">Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag | Microsoft. Azure. Commands. Tags. Model. PSTagResource</span><span class="sxs-lookup"><span data-stu-id="15e68-151">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="15e68-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="15e68-152">NOTES</span></span>

## <span data-ttu-id="15e68-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="15e68-153">RELATED LINKS</span></span>

[<span data-ttu-id="15e68-154">Neu – AzTag</span><span class="sxs-lookup"><span data-stu-id="15e68-154">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="15e68-155">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="15e68-155">Remove-AzTag</span></span>](./Remove-AzTag.md)

[<span data-ttu-id="15e68-156">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="15e68-156">Update-AzTag</span></span>](./Update-AzTag.md)
