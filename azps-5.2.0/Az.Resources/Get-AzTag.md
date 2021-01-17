---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: 058f4a61f1e7ff2fe7f416ea0e4ada098c9efe51
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365278"
---
# <span data-ttu-id="37d63-101">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="37d63-101">Get-AzTag</span></span>

## <span data-ttu-id="37d63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37d63-102">SYNOPSIS</span></span>
<span data-ttu-id="37d63-103">Ruft vordefinierte Azure-Tags | Ruft die gesamte Gruppe von Tags für eine Ressource oder ein Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="37d63-103">Gets predefined Azure tags | Gets the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="37d63-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="37d63-104">SYNTAX</span></span>

### <span data-ttu-id="37d63-105">GetPredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="37d63-105">GetPredefinedTagParameterSet</span></span>
```
Get-AzTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="37d63-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="37d63-106">GetByResourceIdParameterSet</span></span>
```
Get-AzTag -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37d63-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="37d63-107">DESCRIPTION</span></span>

<span data-ttu-id="37d63-108">**GetPredefinedTagSet**: Das **Cmdlet "Get-AzTag"** ruft vordefinierte #A0 in Ihrem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="37d63-108">**GetPredefinedTagSet**: The **Get-AzTag** cmdlet gets predefined Azure tags in your subscription.</span></span>
<span data-ttu-id="37d63-109">Dieses Cmdlet gibt grundlegende Informationen zu den Kategorien oder detaillierte Informationen zu Tags und deren Werten zurück.</span><span class="sxs-lookup"><span data-stu-id="37d63-109">This cmdlet returns basic information about the tags or detailed information about tags and their values.</span></span>
<span data-ttu-id="37d63-110">Alle Ausgabeobjekte enthalten eine Count-Eigenschaft, die die Anzahl der Ressourcen und Ressourcengruppen darstellt, auf die die Tags und Werte angewendet wurden.</span><span class="sxs-lookup"><span data-stu-id="37d63-110">All output objects include a Count property that represents the number of resources and resource groups to which the tags and values have been applied.</span></span>
<span data-ttu-id="37d63-111">Das Azure-Tags-Modul, **zu dem "Get-AzTag"** gehört, kann Sie bei der Verwaltung vordefinierter #A0 unterstützen.</span><span class="sxs-lookup"><span data-stu-id="37d63-111">The Azure Tags module that **Get-AzTag** is a part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="37d63-112">Ein Azure-Tag ist ein Name-Wert-Paar, mit dem Sie Ihre Azure-Ressourcen und -Ressourcengruppen kategorisieren können, z. B. nach Abteilung oder Kostencenter, oder um Notizen oder Kommentare zu den Ressourcen und Gruppen nachverfolgt werden.</span><span class="sxs-lookup"><span data-stu-id="37d63-112">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="37d63-113">Sie können Tags in einem einzigen Schritt definieren und anwenden, aber mit vordefinierten Tags können Sie standardübliche, konsistente, vorhersehbare Namen und Werte für die Tags in Ihrem Abonnement festlegen.</span><span class="sxs-lookup"><span data-stu-id="37d63-113">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="37d63-114">Verwenden Sie zum Erstellen eines vordefinierten Tags das cmdlet New-AzTag-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37d63-114">To create a predefined tag, use the New-AzTag cmdlet.</span></span>
<span data-ttu-id="37d63-115">Wenn Sie eine vordefinierte Markierung auf eine Ressourcengruppe anwenden möchten, verwenden Sie den *Parameter "Tag"* des New-AzTag Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="37d63-115">To apply a predefined tag to a resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="37d63-116">Um Ressourcengruppen nach einem bestimmten Tagnamen oder -namen und Wert zu durchsuchen, verwenden Sie den *Parameter "Tag"* des Get-AzResourceGroup Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="37d63-116">To search resource groups for a specific tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>

<span data-ttu-id="37d63-117">**GetByResourceIdParameterSet**: Das **Cmdlet "Get-AzTag"** mit einer **ResourceId** ruft den gesamten Satz von Tags für eine Ressource oder ein Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="37d63-117">**GetByResourceIdParameterSet**: The **Get-AzTag** cmdlet with a **ResourceId** gets the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="37d63-118">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="37d63-118">EXAMPLES</span></span>

### <span data-ttu-id="37d63-119">Beispiel 1: Alle vordefinierten Tags erhalten</span><span class="sxs-lookup"><span data-stu-id="37d63-119">Example 1: Get all predefined tags</span></span>
```powershell
PS C:\>Get-AzTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

<span data-ttu-id="37d63-120">Dieser Befehl ruft alle vordefinierten Tags im Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="37d63-120">This command gets all predefined tags in the subscription.</span></span>
<span data-ttu-id="37d63-121">Die Eigenschaft "Anzahl" zeigt an, wie oft das Tag auf Ressourcen und Ressourcengruppen im Abonnement angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="37d63-121">The Count property shows how many times the tag has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="37d63-122">Beispiel 2: Erhalten eines Tags nach Name</span><span class="sxs-lookup"><span data-stu-id="37d63-122">Example 2: Get a tag by name</span></span>
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

<span data-ttu-id="37d63-123">Dieser Befehl ruft detaillierte Informationen über das Tag "Department" und dessen Werte ab.</span><span class="sxs-lookup"><span data-stu-id="37d63-123">This command gets detailed information about the Department tag and its values.</span></span>
<span data-ttu-id="37d63-124">Die Eigenschaft "Anzahl" zeigt an, wie oft das Tag und die einzelnen Werte auf Ressourcen und Ressourcengruppen im Abonnement angewendet wurden.</span><span class="sxs-lookup"><span data-stu-id="37d63-124">The Count property shows how many times the tag and each of its values has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="37d63-125">Beispiel 3: Erhalten von Werten aller Tags</span><span class="sxs-lookup"><span data-stu-id="37d63-125">Example 3: Get values of all tags</span></span>
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

<span data-ttu-id="37d63-126">Dieser Befehl verwendet den *Parameter "Detailed",* um detaillierte Informationen zu allen vordefinierten Tags im Abonnement zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="37d63-126">This command uses the *Detailed* parameter to get detailed information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="37d63-127">Die Verwendung *des Parameters "Detailed"* entspricht der Verwendung des *Namensparameters* für jedes Tag.</span><span class="sxs-lookup"><span data-stu-id="37d63-127">Using the *Detailed* parameter is the equivalent of using the *Name* parameter for every tag.</span></span>

### <span data-ttu-id="37d63-128">Beispiel 4: Den gesamten Satz markierungen für ein Abonnement erhalten</span><span class="sxs-lookup"><span data-stu-id="37d63-128">Example 4: Get the entire set of tags on a subscription</span></span>

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

<span data-ttu-id="37d63-129">Dieser Befehl ruft die gesamte Gruppe von Tags für das Abonnement mit {subId} ab.</span><span class="sxs-lookup"><span data-stu-id="37d63-129">This command gets the entire set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="37d63-130">Beispiel 5: Den gesamten Satz von Tags für eine Ressource erhalten</span><span class="sxs-lookup"><span data-stu-id="37d63-130">Example 5: Get the entire set of tags on a resource</span></span>

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

<span data-ttu-id="37d63-131">Dieser Befehl ruft die gesamte Gruppe von Tags für die Ressource mit {resourceId} ab.</span><span class="sxs-lookup"><span data-stu-id="37d63-131">This command gets the entire set of tags on the resource with {resourceId}.</span></span>

## <span data-ttu-id="37d63-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37d63-132">PARAMETERS</span></span>

### <span data-ttu-id="37d63-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37d63-133">-DefaultProfile</span></span>
<span data-ttu-id="37d63-134">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="37d63-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37d63-135">-Detailliert</span><span class="sxs-lookup"><span data-stu-id="37d63-135">-Detailed</span></span>
<span data-ttu-id="37d63-136">Gibt an, dass dieser Vorgang der Ausgabe Informationen zu Tagwerten hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="37d63-136">Indicates that this operation adds information about tag values to the output.</span></span>

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

### <span data-ttu-id="37d63-137">-Name</span><span class="sxs-lookup"><span data-stu-id="37d63-137">-Name</span></span>
<span data-ttu-id="37d63-138">Name des vordefinierten Tags.</span><span class="sxs-lookup"><span data-stu-id="37d63-138">Name of the predefined tag.</span></span>
<span data-ttu-id="37d63-139">Standardmäßig ruft **Get-AzTag** grundlegende Informationen zu allen vordefinierten Tags im Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="37d63-139">By default, **Get-AzTag** gets basic information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="37d63-140">Wenn Sie den Parameter *"Name"* angeben, hat der *Parameter "Detailed"* keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="37d63-140">When you specify the *Name* parameter, the *Detailed* parameter has no effect.</span></span>

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

### <span data-ttu-id="37d63-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="37d63-141">-ResourceId</span></span>
<span data-ttu-id="37d63-142">Der Ressourcenbezeichner für die markierte Entität.</span><span class="sxs-lookup"><span data-stu-id="37d63-142">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="37d63-143">Möglicherweise ist eine Ressource, eine Ressourcengruppe oder ein Abonnement markiert.</span><span class="sxs-lookup"><span data-stu-id="37d63-143">A resource, a resource group or a subscription may be tagged.</span></span>

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

### <span data-ttu-id="37d63-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37d63-144">CommonParameters</span></span>
<span data-ttu-id="37d63-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37d63-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37d63-146">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37d63-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37d63-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="37d63-147">INPUTS</span></span>

### <span data-ttu-id="37d63-148">System.String</span><span class="sxs-lookup"><span data-stu-id="37d63-148">System.String</span></span>

### <span data-ttu-id="37d63-149">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="37d63-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="37d63-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="37d63-150">OUTPUTS</span></span>

### <span data-ttu-id="37d63-151">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span><span class="sxs-lookup"><span data-stu-id="37d63-151">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="37d63-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="37d63-152">NOTES</span></span>

## <span data-ttu-id="37d63-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="37d63-153">RELATED LINKS</span></span>

[<span data-ttu-id="37d63-154">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="37d63-154">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="37d63-155">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="37d63-155">Remove-AzTag</span></span>](./Remove-AzTag.md)

[<span data-ttu-id="37d63-156">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="37d63-156">Update-AzTag</span></span>](./Update-AzTag.md)
