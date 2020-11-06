---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: E94B88AA-B8B0-49F0-AD36-6707E17B40AD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProduct.md
ms.openlocfilehash: 636a969f6aef013ee947afbb43d398871848818a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500310"
---
# <span data-ttu-id="38d3b-101">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="38d3b-101">New-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="38d3b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="38d3b-102">SYNOPSIS</span></span>
<span data-ttu-id="38d3b-103">Erstellt ein API-Verwaltungsprodukt.</span><span class="sxs-lookup"><span data-stu-id="38d3b-103">Creates an API Management product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38d3b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="38d3b-104">SYNTAX</span></span>

```
New-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-ProductId <String>] -Title <String>
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38d3b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="38d3b-105">DESCRIPTION</span></span>
<span data-ttu-id="38d3b-106">Das Cmdlet **New-AzureRmApiManagementProduct** erstellt ein API-Verwaltungsprodukt.</span><span class="sxs-lookup"><span data-stu-id="38d3b-106">The **New-AzureRmApiManagementProduct** cmdlet creates an API Management product.</span></span>

## <span data-ttu-id="38d3b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="38d3b-107">EXAMPLES</span></span>

### <span data-ttu-id="38d3b-108">Beispiel 1: Erstellen eines Produkts, für das kein Abonnement erforderlich ist</span><span class="sxs-lookup"><span data-stu-id="38d3b-108">Example 1: Create a product that does not require a subscription</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $False -State "Published"
```

<span data-ttu-id="38d3b-109">Dieser Befehl erstellt ein API-Verwaltungsprodukt.</span><span class="sxs-lookup"><span data-stu-id="38d3b-109">This command creates an API Management product.</span></span>
<span data-ttu-id="38d3b-110">Es ist kein Abonnement erforderlich.</span><span class="sxs-lookup"><span data-stu-id="38d3b-110">No subscription is required.</span></span>

### <span data-ttu-id="38d3b-111">Beispiel 2: Erstellen eines Produkts, das ein Abonnement und eine Genehmigung erfordert</span><span class="sxs-lookup"><span data-stu-id="38d3b-111">Example 2: Create a product that requires a subscription and approval</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementProduct -Context $apimContext -ProductId "9876543210" -Title "Unlimited" -Description "Subscribers have completely unlimited access to the API. Administrator approval is required." -LegalTerms "Free for all" -ApprovalRequired $True -State "Published" -NotificationPeriod "D10" -SubscriptionPeriod "Y1"
```

<span data-ttu-id="38d3b-112">Mit diesem Befehl wird ein Produkt erstellt.</span><span class="sxs-lookup"><span data-stu-id="38d3b-112">This command creates a product.</span></span>
<span data-ttu-id="38d3b-113">Ein Abonnement und eine Genehmigung sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="38d3b-113">A subscription and approval are required.</span></span>
<span data-ttu-id="38d3b-114">Dieser Befehl legt den Benachrichtigungszeitraum auf 10 Tage fest.</span><span class="sxs-lookup"><span data-stu-id="38d3b-114">This command sets the notification period to 10 days.</span></span>
<span data-ttu-id="38d3b-115">Die Dauer des Abonnements ist auf ein Jahr eingestellt.</span><span class="sxs-lookup"><span data-stu-id="38d3b-115">The subscription duration is set to one year.</span></span>

## <span data-ttu-id="38d3b-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="38d3b-116">PARAMETERS</span></span>

### <span data-ttu-id="38d3b-117">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="38d3b-117">-ApprovalRequired</span></span>
<span data-ttu-id="38d3b-118">Gibt an, ob das Abonnement für das Produkt genehmigt werden muss.</span><span class="sxs-lookup"><span data-stu-id="38d3b-118">Indicates whether the subscription to the product requires approval or not.</span></span>
<span data-ttu-id="38d3b-119">Standardmäßig ist dieser Parameter **$false**.</span><span class="sxs-lookup"><span data-stu-id="38d3b-119">By default, this parameter is **$False**.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38d3b-120">-Context</span><span class="sxs-lookup"><span data-stu-id="38d3b-120">-Context</span></span>
<span data-ttu-id="38d3b-121">Gibt eine Instanz eines **PsApiManagementContext** -Objekts an.</span><span class="sxs-lookup"><span data-stu-id="38d3b-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38d3b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38d3b-122">-DefaultProfile</span></span>
<span data-ttu-id="38d3b-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="38d3b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38d3b-124">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="38d3b-124">-Description</span></span>
<span data-ttu-id="38d3b-125">Gibt die Produktbeschreibung an.</span><span class="sxs-lookup"><span data-stu-id="38d3b-125">Specifies the product description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38d3b-126">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="38d3b-126">-LegalTerms</span></span>
<span data-ttu-id="38d3b-127">Gibt die rechtlichen Nutzungsbestimmungen des Produkts an.</span><span class="sxs-lookup"><span data-stu-id="38d3b-127">Specifies the legal terms of use of the product.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38d3b-128">-ProductID</span><span class="sxs-lookup"><span data-stu-id="38d3b-128">-ProductId</span></span>
<span data-ttu-id="38d3b-129">Gibt den Bezeichner des neuen Produkts an.</span><span class="sxs-lookup"><span data-stu-id="38d3b-129">Specifies the identifier of new product.</span></span>
<span data-ttu-id="38d3b-130">Wenn Sie diesen Parameter nicht angeben, wird ein neues Produkt generiert.</span><span class="sxs-lookup"><span data-stu-id="38d3b-130">If you do not specify this parameter, a new product is generated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38d3b-131">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="38d3b-131">-State</span></span>
<span data-ttu-id="38d3b-132">Gibt den Produktstatus an.</span><span class="sxs-lookup"><span data-stu-id="38d3b-132">Specifies the product state.</span></span>
<span data-ttu-id="38d3b-133">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="38d3b-133">psdx_paramvalues</span></span>
- <span data-ttu-id="38d3b-134">NotPublished</span><span class="sxs-lookup"><span data-stu-id="38d3b-134">NotPublished</span></span>
- <span data-ttu-id="38d3b-135">Veröffentlicht der Standardwert ist NotPublished.</span><span class="sxs-lookup"><span data-stu-id="38d3b-135">Published The default value is NotPublished.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState]
Parameter Sets: (All)
Aliases:
Accepted values: NotPublished, Published

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38d3b-136">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="38d3b-136">-SubscriptionRequired</span></span>
<span data-ttu-id="38d3b-137">Gibt an, ob für das Produkt ein Abonnement erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="38d3b-137">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="38d3b-138">Der Standardwert ist **$true**.</span><span class="sxs-lookup"><span data-stu-id="38d3b-138">The default value is **$True**.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38d3b-139">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="38d3b-139">-SubscriptionsLimit</span></span>
<span data-ttu-id="38d3b-140">Gibt die maximale Anzahl gleichzeitiger Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="38d3b-140">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="38d3b-141">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="38d3b-141">The default value is 1.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38d3b-142">-Title</span><span class="sxs-lookup"><span data-stu-id="38d3b-142">-Title</span></span>
<span data-ttu-id="38d3b-143">Gibt den Produkttitel an.</span><span class="sxs-lookup"><span data-stu-id="38d3b-143">Specifies the product title.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38d3b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38d3b-144">CommonParameters</span></span>
<span data-ttu-id="38d3b-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38d3b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38d3b-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38d3b-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38d3b-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="38d3b-147">INPUTS</span></span>

### <span data-ttu-id="38d3b-148">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="38d3b-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="38d3b-149">System. String</span><span class="sxs-lookup"><span data-stu-id="38d3b-149">System.String</span></span>

### <span data-ttu-id="38d3b-150">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="38d3b-150">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="38d3b-151">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="38d3b-151">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="38d3b-152">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementProductState, Microsoft. Azure. Commands. ApiManagement. Servicemanagement, Version = 6.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="38d3b-152">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.Commands.ApiManagement.ServiceManagement, Version=6.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="38d3b-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="38d3b-153">OUTPUTS</span></span>

### <span data-ttu-id="38d3b-154">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="38d3b-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="38d3b-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="38d3b-155">NOTES</span></span>

## <span data-ttu-id="38d3b-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="38d3b-156">RELATED LINKS</span></span>

[<span data-ttu-id="38d3b-157">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="38d3b-157">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="38d3b-158">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="38d3b-158">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)

[<span data-ttu-id="38d3b-159">Satz-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="38d3b-159">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


