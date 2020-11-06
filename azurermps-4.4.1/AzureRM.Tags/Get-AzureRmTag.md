---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM.Tags
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Get-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Get-AzureRmTag.md
ms.openlocfilehash: 5e0766039a9becb65aaec13d08e46f751893b8dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499921"
---
# <span data-ttu-id="931df-101">Get-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="931df-101">Get-AzureRmTag</span></span>

## <span data-ttu-id="931df-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="931df-102">SYNOPSIS</span></span>
<span data-ttu-id="931df-103">Ruft vordefinierte Azure-Tags ab.</span><span class="sxs-lookup"><span data-stu-id="931df-103">Gets predefined Azure tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="931df-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="931df-104">SYNTAX</span></span>

```
Get-AzureRmTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="931df-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="931df-105">DESCRIPTION</span></span>
<span data-ttu-id="931df-106">Das Cmdlet " **Get-AzureRmTag** " ruft vordefinierte Azure-Tags in Ihrem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="931df-106">The **Get-AzureRmTag** cmdlet gets predefined Azure tags in your subscription.</span></span>
<span data-ttu-id="931df-107">Dieses Cmdlet gibt grundlegende Informationen zu den Tags oder detaillierte Informationen zu Tags und deren Werten zurück.</span><span class="sxs-lookup"><span data-stu-id="931df-107">This cmdlet returns basic information about the tags or detailed information about tags and their values.</span></span>
<span data-ttu-id="931df-108">Alle Ausgabeobjekte enthalten eine Count-Eigenschaft, die die Anzahl der Ressourcen und Ressourcengruppen darstellt, auf die die Kategorien und Werte angewendet wurden.</span><span class="sxs-lookup"><span data-stu-id="931df-108">All output objects include a Count property that represents the number of resources and resource groups to which the tags and values have been applied.</span></span>

<span data-ttu-id="931df-109">Das Azure-Tags-Modul, in dem **Get-AzureRMTag** enthalten ist, kann Ihnen helfen, vordefinierte Azure-Tags zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="931df-109">The Azure Tags module that **Get-AzureRMTag** is a part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="931df-110">Bei einem Azure-Tag handelt es sich um ein Name-Wert-Paar, mit dem Sie Ihre Azure-Ressourcen und Ressourcengruppen kategorisieren können, beispielsweise nach Abteilung oder Kostenstelle, oder um Notizen oder Kommentare zu Ressourcen und Gruppen zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="931df-110">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>

<span data-ttu-id="931df-111">Sie können Tags in einem einzigen Schritt definieren und anwenden, doch mit vordefinierten Tags können Sie standardmäßige, konsistente, vorhersagbare Namen und Werte für die Tags in Ihrem Abonnement einrichten.</span><span class="sxs-lookup"><span data-stu-id="931df-111">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="931df-112">Wenn das Abonnement vordefinierte Tags enthält, können Sie nicht definierte Tags oder Werte auf eine Ressource oder eine Ressourcengruppe im Abonnement anwenden.</span><span class="sxs-lookup"><span data-stu-id="931df-112">If the subscription includes any predefined tags, you cannot apply undefined tags or values to any resource or resource group in the subscription.</span></span>

<span data-ttu-id="931df-113">Verwenden Sie das New-AzureRmTag-Cmdlet, um eine vordefinierte Kategorie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="931df-113">To create a predefined tag, use the New-AzureRmTag cmdlet.</span></span>
<span data-ttu-id="931df-114">Wenn Sie eine vordefinierte Kategorie auf eine Ressourcengruppe anwenden möchten, verwenden Sie den *Tag* -Parameter des New-AzureRmTag-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="931df-114">To apply a predefined tag to a resource group, use the *Tag* parameter of the New-AzureRmTag cmdlet.</span></span>
<span data-ttu-id="931df-115">Verwenden Sie den *Tag* -Parameter des Get-AzureRMResourceGroup-Cmdlets, um Ressourcengruppen nach einem bestimmten Tag-Namen oder-Namen und-Wert zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="931df-115">To search resource groups for a specific tag name or name and value, use the *Tag* parameter of the Get-AzureRMResourceGroup cmdlet.</span></span>

## <span data-ttu-id="931df-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="931df-116">EXAMPLES</span></span>

### <span data-ttu-id="931df-117">Beispiel 1: Abrufen aller vordefinierten Tags</span><span class="sxs-lookup"><span data-stu-id="931df-117">Example 1: Get all predefined tags</span></span>
```
PS C:\>Get-AzureRmTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

<span data-ttu-id="931df-118">Dieser Befehl ruft alle vordefinierten Tags im Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="931df-118">This command gets all predefined tags in the subscription.</span></span>
<span data-ttu-id="931df-119">Die Count-Eigenschaft zeigt, wie oft das Tag auf Ressourcen und Ressourcengruppen im Abonnement angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="931df-119">The Count property shows how many times the tag has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="931df-120">Beispiel 2: Abrufen einer Kategorie nach Name</span><span class="sxs-lookup"><span data-stu-id="931df-120">Example 2: Get a tag by name</span></span>
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

<span data-ttu-id="931df-121">Dieser Befehl erhält detaillierte Informationen über das Department-Tag und seine Werte.</span><span class="sxs-lookup"><span data-stu-id="931df-121">This command gets detailed information about the Department tag and its values.</span></span>
<span data-ttu-id="931df-122">Die Count-Eigenschaft zeigt an, wie oft das Tag und jeder seiner Werte auf Ressourcen und Ressourcengruppen im Abonnement angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="931df-122">The Count property shows how many times the tag and each of its values has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="931df-123">Beispiel 3: Abrufen von Werten aller Tags</span><span class="sxs-lookup"><span data-stu-id="931df-123">Example 3: Get values of all tags</span></span>
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

<span data-ttu-id="931df-124">Dieser Befehl verwendet den *detaillierten* Parameter, um detaillierte Informationen zu allen vordefinierten Tags im Abonnement abzurufen.</span><span class="sxs-lookup"><span data-stu-id="931df-124">This command uses the *Detailed* parameter to get detailed information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="931df-125">Die Verwendung des Parameters *detaillierte* entspricht der Verwendung des Parameters *Name* für jedes Tag.</span><span class="sxs-lookup"><span data-stu-id="931df-125">Using the *Detailed* parameter is the equivalent of using the *Name* parameter for every tag.</span></span>

## <span data-ttu-id="931df-126">Parameter</span><span class="sxs-lookup"><span data-stu-id="931df-126">PARAMETERS</span></span>

### <span data-ttu-id="931df-127">-Detailliert</span><span class="sxs-lookup"><span data-stu-id="931df-127">-Detailed</span></span>
<span data-ttu-id="931df-128">Gibt an, dass dieser Vorgang der Ausgabe Informationen zu Transponder Werten hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="931df-128">Indicates that this operation adds information about tag values to the output.</span></span>

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

### <span data-ttu-id="931df-129">-Name</span><span class="sxs-lookup"><span data-stu-id="931df-129">-Name</span></span>
<span data-ttu-id="931df-130">Gibt den Namen des abzurufenden Transponders an.</span><span class="sxs-lookup"><span data-stu-id="931df-130">Specifies the name of the tag to get.</span></span>
<span data-ttu-id="931df-131">Standardmäßig ruft **Get-AzureRmTag** grundlegende Informationen zu allen vordefinierten Tags im Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="931df-131">By default, **Get-AzureRmTag** gets basic information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="931df-132">Wenn Sie den Parameter *Name* angeben, hat der *Detail* Parameter keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="931df-132">When you specify the *Name* parameter, the *Detailed* parameter has no effect.</span></span>

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

### <span data-ttu-id="931df-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="931df-133">-DefaultProfile</span></span>
<span data-ttu-id="931df-134">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="931df-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="931df-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="931df-135">CommonParameters</span></span>
<span data-ttu-id="931df-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="931df-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="931df-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="931df-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="931df-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="931df-138">INPUTS</span></span>

### <span data-ttu-id="931df-139">Keine</span><span class="sxs-lookup"><span data-stu-id="931df-139">None</span></span>

## <span data-ttu-id="931df-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="931df-140">OUTPUTS</span></span>

### <span data-ttu-id="931df-141">Microsoft. Azure. Commands. Tags. Model. PSTag, Microsoft. Azure. Commands. Tags</span><span class="sxs-lookup"><span data-stu-id="931df-141">Microsoft.Azure.Commands.Tags.Model.PSTag, Microsoft.Azure.Commands.Tags</span></span>

## <span data-ttu-id="931df-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="931df-142">NOTES</span></span>

## <span data-ttu-id="931df-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="931df-143">RELATED LINKS</span></span>

[<span data-ttu-id="931df-144">Neu – AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="931df-144">New-AzureRmTag</span></span>](./New-AzureRmTag.md)

[<span data-ttu-id="931df-145">Remove-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="931df-145">Remove-AzureRmTag</span></span>](./Remove-AzureRmTag.md)


