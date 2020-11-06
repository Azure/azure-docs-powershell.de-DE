---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM.Tags
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.tags/get-azurermtag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Get-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Get-AzureRmTag.md
ms.openlocfilehash: 945af88df11e210c3af3a11bd69123dd32befe4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504246"
---
# <span data-ttu-id="8d88c-101">Get-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="8d88c-101">Get-AzureRmTag</span></span>

## <span data-ttu-id="8d88c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8d88c-102">SYNOPSIS</span></span>
<span data-ttu-id="8d88c-103">Ruft vordefinierte Azure-Tags ab.</span><span class="sxs-lookup"><span data-stu-id="8d88c-103">Gets predefined Azure tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d88c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d88c-104">SYNTAX</span></span>

```
Get-AzureRmTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d88c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8d88c-105">DESCRIPTION</span></span>
<span data-ttu-id="8d88c-106">Das Cmdlet " **Get-AzureRmTag** " ruft vordefinierte Azure-Tags in Ihrem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="8d88c-106">The **Get-AzureRmTag** cmdlet gets predefined Azure tags in your subscription.</span></span>
<span data-ttu-id="8d88c-107">Dieses Cmdlet gibt grundlegende Informationen zu den Tags oder detaillierte Informationen zu Tags und deren Werten zurück.</span><span class="sxs-lookup"><span data-stu-id="8d88c-107">This cmdlet returns basic information about the tags or detailed information about tags and their values.</span></span>
<span data-ttu-id="8d88c-108">Alle Ausgabeobjekte enthalten eine Count-Eigenschaft, die die Anzahl der Ressourcen und Ressourcengruppen darstellt, auf die die Kategorien und Werte angewendet wurden.</span><span class="sxs-lookup"><span data-stu-id="8d88c-108">All output objects include a Count property that represents the number of resources and resource groups to which the tags and values have been applied.</span></span>
<span data-ttu-id="8d88c-109">Das Azure-Tags-Modul, in dem **Get-AzureRMTag** enthalten ist, kann Ihnen helfen, vordefinierte Azure-Tags zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="8d88c-109">The Azure Tags module that **Get-AzureRMTag** is a part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="8d88c-110">Bei einem Azure-Tag handelt es sich um ein Name-Wert-Paar, mit dem Sie Ihre Azure-Ressourcen und Ressourcengruppen kategorisieren können, beispielsweise nach Abteilung oder Kostenstelle, oder um Notizen oder Kommentare zu Ressourcen und Gruppen zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="8d88c-110">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="8d88c-111">Sie können Tags in einem einzigen Schritt definieren und anwenden, doch mit vordefinierten Tags können Sie standardmäßige, konsistente, vorhersagbare Namen und Werte für die Tags in Ihrem Abonnement einrichten.</span><span class="sxs-lookup"><span data-stu-id="8d88c-111">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="8d88c-112">Verwenden Sie das New-AzureRmTag-Cmdlet, um eine vordefinierte Kategorie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8d88c-112">To create a predefined tag, use the New-AzureRmTag cmdlet.</span></span>
<span data-ttu-id="8d88c-113">Wenn Sie eine vordefinierte Kategorie auf eine Ressourcengruppe anwenden möchten, verwenden Sie den *Tag* -Parameter des New-AzureRmTag-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="8d88c-113">To apply a predefined tag to a resource group, use the *Tag* parameter of the New-AzureRmTag cmdlet.</span></span>
<span data-ttu-id="8d88c-114">Verwenden Sie den *Tag* -Parameter des Get-AzureRMResourceGroup-Cmdlets, um Ressourcengruppen nach einem bestimmten Tag-Namen oder-Namen und-Wert zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="8d88c-114">To search resource groups for a specific tag name or name and value, use the *Tag* parameter of the Get-AzureRMResourceGroup cmdlet.</span></span>

## <span data-ttu-id="8d88c-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8d88c-115">EXAMPLES</span></span>

### <span data-ttu-id="8d88c-116">Beispiel 1: Abrufen aller vordefinierten Tags</span><span class="sxs-lookup"><span data-stu-id="8d88c-116">Example 1: Get all predefined tags</span></span>
```
PS C:\>Get-AzureRmTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

<span data-ttu-id="8d88c-117">Dieser Befehl ruft alle vordefinierten Tags im Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="8d88c-117">This command gets all predefined tags in the subscription.</span></span>
<span data-ttu-id="8d88c-118">Die Count-Eigenschaft zeigt, wie oft das Tag auf Ressourcen und Ressourcengruppen im Abonnement angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="8d88c-118">The Count property shows how many times the tag has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="8d88c-119">Beispiel 2: Abrufen einer Kategorie nach Name</span><span class="sxs-lookup"><span data-stu-id="8d88c-119">Example 2: Get a tag by name</span></span>
```
PS C:\>Get-AzureRmTag -Name "Department"

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3
```

<span data-ttu-id="8d88c-120">Dieser Befehl erhält detaillierte Informationen über das Department-Tag und seine Werte.</span><span class="sxs-lookup"><span data-stu-id="8d88c-120">This command gets detailed information about the Department tag and its values.</span></span>
<span data-ttu-id="8d88c-121">Die Count-Eigenschaft zeigt an, wie oft das Tag und jeder seiner Werte auf Ressourcen und Ressourcengruppen im Abonnement angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="8d88c-121">The Count property shows how many times the tag and each of its values has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="8d88c-122">Beispiel 3: Abrufen von Werten aller Tags</span><span class="sxs-lookup"><span data-stu-id="8d88c-122">Example 3: Get values of all tags</span></span>
```
PS C:\>Get-AzureRmTag -Detailed

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

<span data-ttu-id="8d88c-123">Dieser Befehl verwendet den *detaillierten* Parameter, um detaillierte Informationen zu allen vordefinierten Tags im Abonnement abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8d88c-123">This command uses the *Detailed* parameter to get detailed information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="8d88c-124">Die Verwendung des Parameters *detaillierte* entspricht der Verwendung des Parameters *Name* für jedes Tag.</span><span class="sxs-lookup"><span data-stu-id="8d88c-124">Using the *Detailed* parameter is the equivalent of using the *Name* parameter for every tag.</span></span>

## <span data-ttu-id="8d88c-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d88c-125">PARAMETERS</span></span>

### <span data-ttu-id="8d88c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d88c-126">-DefaultProfile</span></span>
<span data-ttu-id="8d88c-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8d88c-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d88c-128">-Detailliert</span><span class="sxs-lookup"><span data-stu-id="8d88c-128">-Detailed</span></span>
<span data-ttu-id="8d88c-129">Gibt an, dass dieser Vorgang der Ausgabe Informationen zu Transponder Werten hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="8d88c-129">Indicates that this operation adds information about tag values to the output.</span></span>

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

### <span data-ttu-id="8d88c-130">-Name</span><span class="sxs-lookup"><span data-stu-id="8d88c-130">-Name</span></span>
<span data-ttu-id="8d88c-131">Gibt den Namen des abzurufenden Transponders an.</span><span class="sxs-lookup"><span data-stu-id="8d88c-131">Specifies the name of the tag to get.</span></span>
<span data-ttu-id="8d88c-132">Standardmäßig ruft **Get-AzureRmTag** grundlegende Informationen zu allen vordefinierten Tags im Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="8d88c-132">By default, **Get-AzureRmTag** gets basic information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="8d88c-133">Wenn Sie den Parameter *Name* angeben, hat der *Detail* Parameter keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="8d88c-133">When you specify the *Name* parameter, the *Detailed* parameter has no effect.</span></span>

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

### <span data-ttu-id="8d88c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d88c-134">CommonParameters</span></span>
<span data-ttu-id="8d88c-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d88c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d88c-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d88c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d88c-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8d88c-137">INPUTS</span></span>

### <span data-ttu-id="8d88c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="8d88c-138">System.String</span></span>

### <span data-ttu-id="8d88c-139">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="8d88c-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8d88c-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8d88c-140">OUTPUTS</span></span>

### <span data-ttu-id="8d88c-141">Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag</span><span class="sxs-lookup"><span data-stu-id="8d88c-141">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag</span></span>

## <span data-ttu-id="8d88c-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="8d88c-142">NOTES</span></span>

## <span data-ttu-id="8d88c-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8d88c-143">RELATED LINKS</span></span>

[<span data-ttu-id="8d88c-144">Neu – AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="8d88c-144">New-AzureRmTag</span></span>](./New-AzureRmTag.md)

[<span data-ttu-id="8d88c-145">Remove-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="8d88c-145">Remove-AzureRmTag</span></span>](./Remove-AzureRmTag.md)


