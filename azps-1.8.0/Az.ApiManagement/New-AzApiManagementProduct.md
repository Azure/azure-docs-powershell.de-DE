---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: E94B88AA-B8B0-49F0-AD36-6707E17B40AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProduct.md
ms.openlocfilehash: 1eef13c2227a2cc4da50f63b9ad3cc11b6969a1e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821151"
---
# <span data-ttu-id="04af7-101">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="04af7-101">New-AzApiManagementProduct</span></span>

## <span data-ttu-id="04af7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="04af7-102">SYNOPSIS</span></span>
<span data-ttu-id="04af7-103">Erstellt ein API-Verwaltungsprodukt.</span><span class="sxs-lookup"><span data-stu-id="04af7-103">Creates an API Management product.</span></span>

## <span data-ttu-id="04af7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="04af7-104">SYNTAX</span></span>

```
New-AzApiManagementProduct -Context <PsApiManagementContext> [-ProductId <String>] -Title <String>
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04af7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="04af7-105">DESCRIPTION</span></span>
<span data-ttu-id="04af7-106">Das Cmdlet **New-AzApiManagementProduct** erstellt ein API-Verwaltungsprodukt.</span><span class="sxs-lookup"><span data-stu-id="04af7-106">The **New-AzApiManagementProduct** cmdlet creates an API Management product.</span></span>

## <span data-ttu-id="04af7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="04af7-107">EXAMPLES</span></span>

### <span data-ttu-id="04af7-108">Beispiel 1: Erstellen eines Produkts, für das kein Abonnement erforderlich ist</span><span class="sxs-lookup"><span data-stu-id="04af7-108">Example 1: Create a product that does not require a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $False -State "Published"
```

<span data-ttu-id="04af7-109">Dieser Befehl erstellt ein API-Verwaltungsprodukt.</span><span class="sxs-lookup"><span data-stu-id="04af7-109">This command creates an API Management product.</span></span>
<span data-ttu-id="04af7-110">Es ist kein Abonnement erforderlich.</span><span class="sxs-lookup"><span data-stu-id="04af7-110">No subscription is required.</span></span>

### <span data-ttu-id="04af7-111">Beispiel 2: Erstellen eines Produkts, das ein Abonnement und eine Genehmigung erfordert</span><span class="sxs-lookup"><span data-stu-id="04af7-111">Example 2: Create a product that requires a subscription and approval</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProduct -Context $apimContext -ProductId "9876543210" -Title "Unlimited" -Description "Subscribers have completely unlimited access to the API. Administrator approval is required." -LegalTerms "Free for all" -ApprovalRequired $True -State "Published" -NotificationPeriod "D10" -SubscriptionPeriod "Y1"
```

<span data-ttu-id="04af7-112">Mit diesem Befehl wird ein Produkt erstellt.</span><span class="sxs-lookup"><span data-stu-id="04af7-112">This command creates a product.</span></span>
<span data-ttu-id="04af7-113">Ein Abonnement und eine Genehmigung sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="04af7-113">A subscription and approval are required.</span></span>
<span data-ttu-id="04af7-114">Dieser Befehl legt den Benachrichtigungszeitraum auf 10 Tage fest.</span><span class="sxs-lookup"><span data-stu-id="04af7-114">This command sets the notification period to 10 days.</span></span>
<span data-ttu-id="04af7-115">Die Dauer des Abonnements ist auf ein Jahr eingestellt.</span><span class="sxs-lookup"><span data-stu-id="04af7-115">The subscription duration is set to one year.</span></span>

## <span data-ttu-id="04af7-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="04af7-116">PARAMETERS</span></span>

### <span data-ttu-id="04af7-117">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="04af7-117">-ApprovalRequired</span></span>
<span data-ttu-id="04af7-118">Gibt an, ob das Abonnement für das Produkt genehmigt werden muss.</span><span class="sxs-lookup"><span data-stu-id="04af7-118">Indicates whether the subscription to the product requires approval or not.</span></span>
<span data-ttu-id="04af7-119">Standardmäßig ist dieser Parameter **$false**.</span><span class="sxs-lookup"><span data-stu-id="04af7-119">By default, this parameter is **$False**.</span></span>

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

### <span data-ttu-id="04af7-120">-Context</span><span class="sxs-lookup"><span data-stu-id="04af7-120">-Context</span></span>
<span data-ttu-id="04af7-121">Gibt eine Instanz eines **PsApiManagementContext** -Objekts an.</span><span class="sxs-lookup"><span data-stu-id="04af7-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="04af7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04af7-122">-DefaultProfile</span></span>
<span data-ttu-id="04af7-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="04af7-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04af7-124">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="04af7-124">-Description</span></span>
<span data-ttu-id="04af7-125">Gibt die Produktbeschreibung an.</span><span class="sxs-lookup"><span data-stu-id="04af7-125">Specifies the product description.</span></span>

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

### <span data-ttu-id="04af7-126">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="04af7-126">-LegalTerms</span></span>
<span data-ttu-id="04af7-127">Gibt die rechtlichen Nutzungsbestimmungen des Produkts an.</span><span class="sxs-lookup"><span data-stu-id="04af7-127">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="04af7-128">-ProductID</span><span class="sxs-lookup"><span data-stu-id="04af7-128">-ProductId</span></span>
<span data-ttu-id="04af7-129">Gibt den Bezeichner des neuen Produkts an.</span><span class="sxs-lookup"><span data-stu-id="04af7-129">Specifies the identifier of new product.</span></span>
<span data-ttu-id="04af7-130">Wenn Sie diesen Parameter nicht angeben, wird ein neues Produkt generiert.</span><span class="sxs-lookup"><span data-stu-id="04af7-130">If you do not specify this parameter, a new product is generated.</span></span>

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

### <span data-ttu-id="04af7-131">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="04af7-131">-State</span></span>
<span data-ttu-id="04af7-132">Gibt den Produktstatus an.</span><span class="sxs-lookup"><span data-stu-id="04af7-132">Specifies the product state.</span></span>
<span data-ttu-id="04af7-133">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="04af7-133">psdx_paramvalues</span></span>
- <span data-ttu-id="04af7-134">NotPublished</span><span class="sxs-lookup"><span data-stu-id="04af7-134">NotPublished</span></span>
- <span data-ttu-id="04af7-135">Veröffentlicht der Standardwert ist NotPublished.</span><span class="sxs-lookup"><span data-stu-id="04af7-135">Published The default value is NotPublished.</span></span>

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

### <span data-ttu-id="04af7-136">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="04af7-136">-SubscriptionRequired</span></span>
<span data-ttu-id="04af7-137">Gibt an, ob für das Produkt ein Abonnement erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="04af7-137">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="04af7-138">Der Standardwert ist **$true**.</span><span class="sxs-lookup"><span data-stu-id="04af7-138">The default value is **$True**.</span></span>

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

### <span data-ttu-id="04af7-139">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="04af7-139">-SubscriptionsLimit</span></span>
<span data-ttu-id="04af7-140">Gibt die maximale Anzahl gleichzeitiger Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="04af7-140">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="04af7-141">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="04af7-141">The default value is 1.</span></span>

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

### <span data-ttu-id="04af7-142">-Title</span><span class="sxs-lookup"><span data-stu-id="04af7-142">-Title</span></span>
<span data-ttu-id="04af7-143">Gibt den Produkttitel an.</span><span class="sxs-lookup"><span data-stu-id="04af7-143">Specifies the product title.</span></span>

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

### <span data-ttu-id="04af7-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04af7-144">CommonParameters</span></span>
<span data-ttu-id="04af7-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04af7-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04af7-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04af7-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04af7-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="04af7-147">INPUTS</span></span>

### <span data-ttu-id="04af7-148">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="04af7-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="04af7-149">System. String</span><span class="sxs-lookup"><span data-stu-id="04af7-149">System.String</span></span>

### <span data-ttu-id="04af7-150">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="04af7-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="04af7-151">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="04af7-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="04af7-152">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementProductState, Microsoft. Azure. PowerShell. Cmdlets. ApiManagement. Servicemanagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="04af7-152">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="04af7-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="04af7-153">OUTPUTS</span></span>

### <span data-ttu-id="04af7-154">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="04af7-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="04af7-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="04af7-155">NOTES</span></span>

## <span data-ttu-id="04af7-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="04af7-156">RELATED LINKS</span></span>

[<span data-ttu-id="04af7-157">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="04af7-157">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="04af7-158">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="04af7-158">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)

[<span data-ttu-id="04af7-159">Satz-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="04af7-159">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


