---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: b44c861e06c1043fd53e470cfba1e322ce1f1f48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939416"
---
# <span data-ttu-id="39214-101">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="39214-101">Get-AzTag</span></span>

## <span data-ttu-id="39214-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39214-102">SYNOPSIS</span></span>
<span data-ttu-id="39214-103">Ruft vordefinierte Azure-Tags | Ruft den gesamten Satz von Tags für eine Ressource oder ein Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="39214-103">Gets predefined Azure tags | Gets the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="39214-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="39214-104">SYNTAX</span></span>

### <span data-ttu-id="39214-105">GetPredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="39214-105">GetPredefinedTagParameterSet</span></span>
```
Get-AzTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39214-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="39214-106">GetByResourceIdParameterSet</span></span>
```
Get-AzTag -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39214-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="39214-107">DESCRIPTION</span></span>

<span data-ttu-id="39214-108">**GetPredefinedTagSet:** Das **Get-AzTag-Cmdlet** ruft vordefinierte #A0 in Ihrem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="39214-108">**GetPredefinedTagSet**: The **Get-AzTag** cmdlet gets predefined Azure tags in your subscription.</span></span>
<span data-ttu-id="39214-109">Dieses Cmdlet gibt grundlegende Informationen zu den Tags oder detaillierte Informationen zu Tags und deren Werten zurück.</span><span class="sxs-lookup"><span data-stu-id="39214-109">This cmdlet returns basic information about the tags or detailed information about tags and their values.</span></span>
<span data-ttu-id="39214-110">Alle Ausgabeobjekte enthalten eine Count-Eigenschaft, die die Anzahl der Ressourcen und Ressourcengruppen darstellt, auf die die Tags und Werte angewendet wurden.</span><span class="sxs-lookup"><span data-stu-id="39214-110">All output objects include a Count property that represents the number of resources and resource groups to which the tags and values have been applied.</span></span>
<span data-ttu-id="39214-111">Das Azure-Tags-Modul, zu dem **Get-AzTag** gehört, kann Ihnen bei der Verwaltung vordefinierter #A0 helfen.</span><span class="sxs-lookup"><span data-stu-id="39214-111">The Azure Tags module that **Get-AzTag** is a part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="39214-112">Ein Azure-Tag ist ein Namen-Wert-Paar, das Sie verwenden können, um Ihre Azure-Ressourcen und Ressourcengruppen zu kategorisieren, z. B. nach Abteilung oder Kostenstelle, oder um Notizen oder Kommentare zu den Ressourcen und Gruppen nachverfolgt zu werden.</span><span class="sxs-lookup"><span data-stu-id="39214-112">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="39214-113">Sie können Tags in einem einzigen Schritt definieren und anwenden, aber mit vordefinierten Tags können Sie standardmäßige, konsistente, vorhersagbare Namen und Werte für die Tags in Ihrem Abonnement festlegen.</span><span class="sxs-lookup"><span data-stu-id="39214-113">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="39214-114">Zum Erstellen eines vordefinierten Tags verwenden Sie das New-AzTag Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39214-114">To create a predefined tag, use the New-AzTag cmdlet.</span></span>
<span data-ttu-id="39214-115">Verwenden Sie zum Anwenden eines vordefinierten Tags auf eine Ressourcengruppe den *Parameter Tag* des New-AzTag Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="39214-115">To apply a predefined tag to a resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="39214-116">Wenn Sie Ressourcengruppen nach einem bestimmten Tagnamen oder -namen und -wert durchsuchen möchten, verwenden Sie den *Parameter Tag* des cmdlets Get-AzResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39214-116">To search resource groups for a specific tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>

<span data-ttu-id="39214-117">**GetByResourceIdParameterSet**: Das **Get-AzTag-Cmdlet** mit **einer ResourceId** ruft den gesamten Satz von Tags für eine Ressource oder ein Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="39214-117">**GetByResourceIdParameterSet**: The **Get-AzTag** cmdlet with a **ResourceId** gets the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="39214-118">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="39214-118">EXAMPLES</span></span>

### <span data-ttu-id="39214-119">Beispiel 1: Alle vordefinierten Tags erhalten</span><span class="sxs-lookup"><span data-stu-id="39214-119">Example 1: Get all predefined tags</span></span>
```powershell
PS C:\>Get-AzTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

<span data-ttu-id="39214-120">Dieser Befehl ruft alle vordefinierten Tags im Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="39214-120">This command gets all predefined tags in the subscription.</span></span>
<span data-ttu-id="39214-121">Die Count-Eigenschaft zeigt an, wie oft das Tag auf Ressourcen und Ressourcengruppen im Abonnement angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="39214-121">The Count property shows how many times the tag has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="39214-122">Beispiel 2: Erhalten eines Tags nach Name</span><span class="sxs-lookup"><span data-stu-id="39214-122">Example 2: Get a tag by name</span></span>
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

<span data-ttu-id="39214-123">Dieser Befehl ruft detaillierte Informationen zum Tag "Department" und deren Werten ab.</span><span class="sxs-lookup"><span data-stu-id="39214-123">This command gets detailed information about the Department tag and its values.</span></span>
<span data-ttu-id="39214-124">Die Count-Eigenschaft zeigt an, wie oft das Tag und jeder seiner Werte auf Ressourcen und Ressourcengruppen im Abonnement angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="39214-124">The Count property shows how many times the tag and each of its values has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="39214-125">Beispiel 3: Erhalten von Werten aller Tags</span><span class="sxs-lookup"><span data-stu-id="39214-125">Example 3: Get values of all tags</span></span>
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

<span data-ttu-id="39214-126">Dieser Befehl verwendet den *Parameter Detail,* um detaillierte Informationen zu allen vordefinierten Tags im Abonnement zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="39214-126">This command uses the *Detailed* parameter to get detailed information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="39214-127">Die Verwendung *des Parameters* Detail entspricht der Verwendung des *Parameters Name* für jedes Tag.</span><span class="sxs-lookup"><span data-stu-id="39214-127">Using the *Detailed* parameter is the equivalent of using the *Name* parameter for every tag.</span></span>

### <span data-ttu-id="39214-128">Beispiel 4: Erhalten der gesamten Gruppe von Tags für ein Abonnement</span><span class="sxs-lookup"><span data-stu-id="39214-128">Example 4: Get the entire set of tags on a subscription</span></span>

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

<span data-ttu-id="39214-129">Mit diesem Befehl wird der gesamte Satz von Tags für das Abonnement mit {subId} abgerufen.</span><span class="sxs-lookup"><span data-stu-id="39214-129">This command gets the entire set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="39214-130">Beispiel 5: Gesamte Gruppe von Tags für eine Ressource</span><span class="sxs-lookup"><span data-stu-id="39214-130">Example 5: Get the entire set of tags on a resource</span></span>

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

<span data-ttu-id="39214-131">Mit diesem Befehl wird der gesamte Satz von Tags für die Ressource mit {resourceId} abgerufen.</span><span class="sxs-lookup"><span data-stu-id="39214-131">This command gets the entire set of tags on the resource with {resourceId}.</span></span>

## <span data-ttu-id="39214-132">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="39214-132">PARAMETERS</span></span>

### <span data-ttu-id="39214-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39214-133">-DefaultProfile</span></span>
<span data-ttu-id="39214-134">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39214-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39214-135">-Detailliert</span><span class="sxs-lookup"><span data-stu-id="39214-135">-Detailed</span></span>
<span data-ttu-id="39214-136">Gibt an, dass mit diesem Vorgang Informationen zu Tagwerten zur Ausgabe addiert werden.</span><span class="sxs-lookup"><span data-stu-id="39214-136">Indicates that this operation adds information about tag values to the output.</span></span>

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

### <span data-ttu-id="39214-137">-Name</span><span class="sxs-lookup"><span data-stu-id="39214-137">-Name</span></span>
<span data-ttu-id="39214-138">Name des vordefinierten Tags.</span><span class="sxs-lookup"><span data-stu-id="39214-138">Name of the predefined tag.</span></span>
<span data-ttu-id="39214-139">Standardmäßig ruft **Get-AzTag** grundlegende Informationen zu allen vordefinierten Tags im Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="39214-139">By default, **Get-AzTag** gets basic information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="39214-140">Wenn Sie den *Parameter Name angeben,* hat der *Parameter Detail* keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="39214-140">When you specify the *Name* parameter, the *Detailed* parameter has no effect.</span></span>

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

### <span data-ttu-id="39214-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39214-141">-ResourceId</span></span>
<span data-ttu-id="39214-142">Der Ressourcenbezeichner für die markierte Entität.</span><span class="sxs-lookup"><span data-stu-id="39214-142">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="39214-143">Eine Ressource, eine Ressourcengruppe oder ein Abonnement kann markiert werden.</span><span class="sxs-lookup"><span data-stu-id="39214-143">A resource, a resource group or a subscription may be tagged.</span></span>

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

### <span data-ttu-id="39214-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39214-144">CommonParameters</span></span>
<span data-ttu-id="39214-145">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39214-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39214-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="39214-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39214-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="39214-147">INPUTS</span></span>

### <span data-ttu-id="39214-148">System.String</span><span class="sxs-lookup"><span data-stu-id="39214-148">System.String</span></span>

### <span data-ttu-id="39214-149">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="39214-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="39214-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="39214-150">OUTPUTS</span></span>

### <span data-ttu-id="39214-151">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span><span class="sxs-lookup"><span data-stu-id="39214-151">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="39214-152">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="39214-152">NOTES</span></span>

## <span data-ttu-id="39214-153">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="39214-153">RELATED LINKS</span></span>

[<span data-ttu-id="39214-154">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="39214-154">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="39214-155">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="39214-155">Remove-AzTag</span></span>](./Remove-AzTag.md)

[<span data-ttu-id="39214-156">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="39214-156">Update-AzTag</span></span>](./Update-AzTag.md)
