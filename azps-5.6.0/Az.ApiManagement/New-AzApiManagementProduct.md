---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: E94B88AA-B8B0-49F0-AD36-6707E17B40AD
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProduct.md
ms.openlocfilehash: 12de4862e91555b90a4168ac7ac5908b897d6e49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937176"
---
# <span data-ttu-id="253d4-101">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="253d4-101">New-AzApiManagementProduct</span></span>

## <span data-ttu-id="253d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="253d4-102">SYNOPSIS</span></span>
<span data-ttu-id="253d4-103">Erstellt ein API-Verwaltungsprodukt.</span><span class="sxs-lookup"><span data-stu-id="253d4-103">Creates an API Management product.</span></span>

## <span data-ttu-id="253d4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="253d4-104">SYNTAX</span></span>

```
New-AzApiManagementProduct -Context <PsApiManagementContext> [-ProductId <String>] -Title <String>
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="253d4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="253d4-105">DESCRIPTION</span></span>
<span data-ttu-id="253d4-106">Das **Cmdlet New-AzApiManagementProduct** erstellt ein API-Verwaltungsprodukt.</span><span class="sxs-lookup"><span data-stu-id="253d4-106">The **New-AzApiManagementProduct** cmdlet creates an API Management product.</span></span>

## <span data-ttu-id="253d4-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="253d4-107">EXAMPLES</span></span>

### <span data-ttu-id="253d4-108">Beispiel 1: Erstellen eines Produkts, für das kein Abonnement erforderlich ist</span><span class="sxs-lookup"><span data-stu-id="253d4-108">Example 1: Create a product that does not require a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $False -State "Published"
```

<span data-ttu-id="253d4-109">Mit diesem Befehl wird ein API-Verwaltungsprodukt erstellt.</span><span class="sxs-lookup"><span data-stu-id="253d4-109">This command creates an API Management product.</span></span>
<span data-ttu-id="253d4-110">Es ist kein Abonnement erforderlich.</span><span class="sxs-lookup"><span data-stu-id="253d4-110">No subscription is required.</span></span>

### <span data-ttu-id="253d4-111">Beispiel 2: Erstellen eines Produkts, das ein Abonnement und eine Genehmigung erfordert</span><span class="sxs-lookup"><span data-stu-id="253d4-111">Example 2: Create a product that requires a subscription and approval</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProduct -Context $apimContext -ProductId "9876543210" -Title "Unlimited" -Description "Subscribers have completely unlimited access to the API. Administrator approval is required." -LegalTerms "Free for all" -ApprovalRequired $True -State "Published" -NotificationPeriod "D10" -SubscriptionPeriod "Y1"
```

<span data-ttu-id="253d4-112">Mit diesem Befehl wird ein Produkt erstellt.</span><span class="sxs-lookup"><span data-stu-id="253d4-112">This command creates a product.</span></span>
<span data-ttu-id="253d4-113">Ein Abonnement und eine Genehmigung sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="253d4-113">A subscription and approval are required.</span></span>
<span data-ttu-id="253d4-114">Mit diesem Befehl wird der Benachrichtigungszeitraum auf 10 Tage fest.</span><span class="sxs-lookup"><span data-stu-id="253d4-114">This command sets the notification period to 10 days.</span></span>
<span data-ttu-id="253d4-115">Die Abonnementdauer ist auf ein Jahr festgelegt.</span><span class="sxs-lookup"><span data-stu-id="253d4-115">The subscription duration is set to one year.</span></span>

## <span data-ttu-id="253d4-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="253d4-116">PARAMETERS</span></span>

### <span data-ttu-id="253d4-117">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="253d4-117">-ApprovalRequired</span></span>
<span data-ttu-id="253d4-118">Gibt an, ob für das Abonnement des Produkts eine Genehmigung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="253d4-118">Indicates whether the subscription to the product requires approval or not.</span></span>
<span data-ttu-id="253d4-119">Dieser Parameter ist standardmäßig **$False**.</span><span class="sxs-lookup"><span data-stu-id="253d4-119">By default, this parameter is **$False**.</span></span>

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

### <span data-ttu-id="253d4-120">-Context</span><span class="sxs-lookup"><span data-stu-id="253d4-120">-Context</span></span>
<span data-ttu-id="253d4-121">Gibt eine Instanz eines **PsApiManagementContext-Objekts** an.</span><span class="sxs-lookup"><span data-stu-id="253d4-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="253d4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="253d4-122">-DefaultProfile</span></span>
<span data-ttu-id="253d4-123">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="253d4-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="253d4-124">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="253d4-124">-Description</span></span>
<span data-ttu-id="253d4-125">Gibt die Produktbeschreibung an.</span><span class="sxs-lookup"><span data-stu-id="253d4-125">Specifies the product description.</span></span>

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

### <span data-ttu-id="253d4-126">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="253d4-126">-LegalTerms</span></span>
<span data-ttu-id="253d4-127">Gibt die gesetzlichen Nutzungsbedingungen für das Produkt an.</span><span class="sxs-lookup"><span data-stu-id="253d4-127">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="253d4-128">-ProductId</span><span class="sxs-lookup"><span data-stu-id="253d4-128">-ProductId</span></span>
<span data-ttu-id="253d4-129">Gibt den Bezeichner des neuen Produkts an.</span><span class="sxs-lookup"><span data-stu-id="253d4-129">Specifies the identifier of new product.</span></span>
<span data-ttu-id="253d4-130">Wenn Sie diesen Parameter nicht angeben, wird ein neues Produkt generiert.</span><span class="sxs-lookup"><span data-stu-id="253d4-130">If you do not specify this parameter, a new product is generated.</span></span>

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

### <span data-ttu-id="253d4-131">-State</span><span class="sxs-lookup"><span data-stu-id="253d4-131">-State</span></span>
<span data-ttu-id="253d4-132">Gibt den Produktzustand an.</span><span class="sxs-lookup"><span data-stu-id="253d4-132">Specifies the product state.</span></span>
<span data-ttu-id="253d4-133">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="253d4-133">psdx_paramvalues</span></span>
- <span data-ttu-id="253d4-134">NotPublished</span><span class="sxs-lookup"><span data-stu-id="253d4-134">NotPublished</span></span>
- <span data-ttu-id="253d4-135">Veröffentlicht Der Standardwert ist "NotPublished".</span><span class="sxs-lookup"><span data-stu-id="253d4-135">Published The default value is NotPublished.</span></span>

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

### <span data-ttu-id="253d4-136">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="253d4-136">-SubscriptionRequired</span></span>
<span data-ttu-id="253d4-137">Gibt an, ob für das Produkt ein Abonnement erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="253d4-137">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="253d4-138">Der Standardwert ist **$True**.</span><span class="sxs-lookup"><span data-stu-id="253d4-138">The default value is **$True**.</span></span>

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

### <span data-ttu-id="253d4-139">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="253d4-139">-SubscriptionsLimit</span></span>
<span data-ttu-id="253d4-140">Gibt die maximale Anzahl gleichzeitiger Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="253d4-140">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="253d4-141">Der Standardwert ist Keine.</span><span class="sxs-lookup"><span data-stu-id="253d4-141">The default value is None.</span></span>

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

### <span data-ttu-id="253d4-142">-Title</span><span class="sxs-lookup"><span data-stu-id="253d4-142">-Title</span></span>
<span data-ttu-id="253d4-143">Gibt den Produkttitel an.</span><span class="sxs-lookup"><span data-stu-id="253d4-143">Specifies the product title.</span></span>

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

### <span data-ttu-id="253d4-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="253d4-144">CommonParameters</span></span>
<span data-ttu-id="253d4-145">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="253d4-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="253d4-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="253d4-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="253d4-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="253d4-147">INPUTS</span></span>

### <span data-ttu-id="253d4-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="253d4-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="253d4-149">System.String</span><span class="sxs-lookup"><span data-stu-id="253d4-149">System.String</span></span>

### <span data-ttu-id="253d4-150">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="253d4-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="253d4-151">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="253d4-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="253d4-152">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="253d4-152">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="253d4-153">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="253d4-153">OUTPUTS</span></span>

### <span data-ttu-id="253d4-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="253d4-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="253d4-155">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="253d4-155">NOTES</span></span>

## <span data-ttu-id="253d4-156">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="253d4-156">RELATED LINKS</span></span>

[<span data-ttu-id="253d4-157">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="253d4-157">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="253d4-158">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="253d4-158">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)

[<span data-ttu-id="253d4-159">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="253d4-159">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


