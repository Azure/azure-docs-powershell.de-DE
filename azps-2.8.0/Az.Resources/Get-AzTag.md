---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: ce672284a3d9887fe52c33081f04a86e1e072405
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825024"
---
# <span data-ttu-id="5bf16-101">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="5bf16-101">Get-AzTag</span></span>

## <span data-ttu-id="5bf16-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5bf16-102">SYNOPSIS</span></span>
<span data-ttu-id="5bf16-103">Ruft vordefinierte Azure-Tags ab.</span><span class="sxs-lookup"><span data-stu-id="5bf16-103">Gets predefined Azure tags.</span></span>

## <span data-ttu-id="5bf16-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5bf16-104">SYNTAX</span></span>

```
Get-AzTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5bf16-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5bf16-105">DESCRIPTION</span></span>
<span data-ttu-id="5bf16-106">Das Cmdlet " **Get-AzTag** " ruft vordefinierte Azure-Tags in Ihrem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="5bf16-106">The **Get-AzTag** cmdlet gets predefined Azure tags in your subscription.</span></span>
<span data-ttu-id="5bf16-107">Dieses Cmdlet gibt grundlegende Informationen zu den Tags oder detaillierte Informationen zu Tags und deren Werten zurück.</span><span class="sxs-lookup"><span data-stu-id="5bf16-107">This cmdlet returns basic information about the tags or detailed information about tags and their values.</span></span>
<span data-ttu-id="5bf16-108">Alle Ausgabeobjekte enthalten eine Count-Eigenschaft, die die Anzahl der Ressourcen und Ressourcengruppen darstellt, auf die die Kategorien und Werte angewendet wurden.</span><span class="sxs-lookup"><span data-stu-id="5bf16-108">All output objects include a Count property that represents the number of resources and resource groups to which the tags and values have been applied.</span></span>
<span data-ttu-id="5bf16-109">Das Azure-Tags-Modul, in dem **Get-AzTag** enthalten ist, kann Ihnen helfen, vordefinierte Azure-Tags zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="5bf16-109">The Azure Tags module that **Get-AzTag** is a part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="5bf16-110">Bei einem Azure-Tag handelt es sich um ein Name-Wert-Paar, mit dem Sie Ihre Azure-Ressourcen und Ressourcengruppen kategorisieren können, beispielsweise nach Abteilung oder Kostenstelle, oder um Notizen oder Kommentare zu Ressourcen und Gruppen zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="5bf16-110">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="5bf16-111">Sie können Tags in einem einzigen Schritt definieren und anwenden, doch mit vordefinierten Tags können Sie standardmäßige, konsistente, vorhersagbare Namen und Werte für die Tags in Ihrem Abonnement einrichten.</span><span class="sxs-lookup"><span data-stu-id="5bf16-111">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="5bf16-112">Verwenden Sie das New-AzTag-Cmdlet, um eine vordefinierte Kategorie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5bf16-112">To create a predefined tag, use the New-AzTag cmdlet.</span></span>
<span data-ttu-id="5bf16-113">Wenn Sie eine vordefinierte Kategorie auf eine Ressourcengruppe anwenden möchten, verwenden Sie den *Tag* -Parameter des New-AzTag-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="5bf16-113">To apply a predefined tag to a resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="5bf16-114">Verwenden Sie den *Tag* -Parameter des Get-AzResourceGroup-Cmdlets, um Ressourcengruppen nach einem bestimmten Tag-Namen oder-Namen und-Wert zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="5bf16-114">To search resource groups for a specific tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>

## <span data-ttu-id="5bf16-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5bf16-115">EXAMPLES</span></span>

### <span data-ttu-id="5bf16-116">Beispiel 1: Abrufen aller vordefinierten Tags</span><span class="sxs-lookup"><span data-stu-id="5bf16-116">Example 1: Get all predefined tags</span></span>
```
PS C:\>Get-AzTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

<span data-ttu-id="5bf16-117">Dieser Befehl ruft alle vordefinierten Tags im Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="5bf16-117">This command gets all predefined tags in the subscription.</span></span>
<span data-ttu-id="5bf16-118">Die Count-Eigenschaft zeigt, wie oft das Tag auf Ressourcen und Ressourcengruppen im Abonnement angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="5bf16-118">The Count property shows how many times the tag has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="5bf16-119">Beispiel 2: Abrufen einer Kategorie nach Name</span><span class="sxs-lookup"><span data-stu-id="5bf16-119">Example 2: Get a tag by name</span></span>
```
PS C:\>Get-AzTag -Name "Department"

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3
```

<span data-ttu-id="5bf16-120">Dieser Befehl erhält detaillierte Informationen über das Department-Tag und seine Werte.</span><span class="sxs-lookup"><span data-stu-id="5bf16-120">This command gets detailed information about the Department tag and its values.</span></span>
<span data-ttu-id="5bf16-121">Die Count-Eigenschaft zeigt an, wie oft das Tag und jeder seiner Werte auf Ressourcen und Ressourcengruppen im Abonnement angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="5bf16-121">The Count property shows how many times the tag and each of its values has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="5bf16-122">Beispiel 3: Abrufen von Werten aller Tags</span><span class="sxs-lookup"><span data-stu-id="5bf16-122">Example 3: Get values of all tags</span></span>
```
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

<span data-ttu-id="5bf16-123">Dieser Befehl verwendet den *detaillierten* Parameter, um detaillierte Informationen zu allen vordefinierten Tags im Abonnement abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5bf16-123">This command uses the *Detailed* parameter to get detailed information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="5bf16-124">Die Verwendung des Parameters *detaillierte* entspricht der Verwendung des Parameters *Name* für jedes Tag.</span><span class="sxs-lookup"><span data-stu-id="5bf16-124">Using the *Detailed* parameter is the equivalent of using the *Name* parameter for every tag.</span></span>

## <span data-ttu-id="5bf16-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="5bf16-125">PARAMETERS</span></span>

### <span data-ttu-id="5bf16-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bf16-126">-DefaultProfile</span></span>
<span data-ttu-id="5bf16-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5bf16-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5bf16-128">-Detailliert</span><span class="sxs-lookup"><span data-stu-id="5bf16-128">-Detailed</span></span>
<span data-ttu-id="5bf16-129">Gibt an, dass dieser Vorgang der Ausgabe Informationen zu Transponder Werten hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="5bf16-129">Indicates that this operation adds information about tag values to the output.</span></span>

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

### <span data-ttu-id="5bf16-130">-Name</span><span class="sxs-lookup"><span data-stu-id="5bf16-130">-Name</span></span>
<span data-ttu-id="5bf16-131">Gibt den Namen des abzurufenden Transponders an.</span><span class="sxs-lookup"><span data-stu-id="5bf16-131">Specifies the name of the tag to get.</span></span>
<span data-ttu-id="5bf16-132">Standardmäßig ruft **Get-AzTag** grundlegende Informationen zu allen vordefinierten Tags im Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="5bf16-132">By default, **Get-AzTag** gets basic information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="5bf16-133">Wenn Sie den Parameter *Name* angeben, hat der *Detail* Parameter keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="5bf16-133">When you specify the *Name* parameter, the *Detailed* parameter has no effect.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bf16-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bf16-134">CommonParameters</span></span>
<span data-ttu-id="5bf16-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bf16-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bf16-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bf16-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bf16-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5bf16-137">INPUTS</span></span>

### <span data-ttu-id="5bf16-138">System. String</span><span class="sxs-lookup"><span data-stu-id="5bf16-138">System.String</span></span>

### <span data-ttu-id="5bf16-139">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="5bf16-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5bf16-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5bf16-140">OUTPUTS</span></span>

### <span data-ttu-id="5bf16-141">Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag</span><span class="sxs-lookup"><span data-stu-id="5bf16-141">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag</span></span>

## <span data-ttu-id="5bf16-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="5bf16-142">NOTES</span></span>

## <span data-ttu-id="5bf16-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5bf16-143">RELATED LINKS</span></span>

[<span data-ttu-id="5bf16-144">Neu – AzTag</span><span class="sxs-lookup"><span data-stu-id="5bf16-144">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="5bf16-145">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="5bf16-145">Remove-AzTag</span></span>](./Remove-AzTag.md)


