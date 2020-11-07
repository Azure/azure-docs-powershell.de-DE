---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 223FBBA6-4405-4B7A-BA63-5F2434A2A50D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProduct.md
ms.openlocfilehash: b050b55c978313cf038e8a27d5be0f7ad722905b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664939"
---
# <span data-ttu-id="c7d7e-101">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="c7d7e-101">Set-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="c7d7e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c7d7e-102">SYNOPSIS</span></span>
<span data-ttu-id="c7d7e-103">Legt die API-Verwaltungsprodukt Details fest.</span><span class="sxs-lookup"><span data-stu-id="c7d7e-103">Sets the API Management product details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7d7e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7d7e-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-Title <String>]
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7d7e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c7d7e-105">DESCRIPTION</span></span>
<span data-ttu-id="c7d7e-106">Das Cmdlet " **Set-AzureRmApiManagementProduct** " legt die API-Verwaltungsprodukt Details fest.</span><span class="sxs-lookup"><span data-stu-id="c7d7e-106">The **Set-AzureRmApiManagementProduct** cmdlet sets the API Management product details.</span></span>

## <span data-ttu-id="c7d7e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c7d7e-107">EXAMPLES</span></span>

### <span data-ttu-id="c7d7e-108">Beispiel 1: Aktualisieren der Produkt Details</span><span class="sxs-lookup"><span data-stu-id="c7d7e-108">Example 1: Update the product details</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $True -State "NotPublished"
```

<span data-ttu-id="c7d7e-109">Dieser Befehl aktualisiert die API-Verwaltungsprodukt Details, erfordert ein Abonnement und dann die Veröffentlichung.</span><span class="sxs-lookup"><span data-stu-id="c7d7e-109">This command updates the API Management product details, requires a subscription, and then unpublishes.</span></span>

## <span data-ttu-id="c7d7e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7d7e-110">PARAMETERS</span></span>

### <span data-ttu-id="c7d7e-111">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="c7d7e-111">-ApprovalRequired</span></span>
<span data-ttu-id="c7d7e-112">Gibt an, ob das Abonnement für das Produkt genehmigt werden muss.</span><span class="sxs-lookup"><span data-stu-id="c7d7e-112">Indicates whether the subscription to the product requires approval.</span></span>
<span data-ttu-id="c7d7e-113">Der Standardwert ist **$false**.</span><span class="sxs-lookup"><span data-stu-id="c7d7e-113">The default value is **$False**.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7d7e-114">-Context</span><span class="sxs-lookup"><span data-stu-id="c7d7e-114">-Context</span></span>
<span data-ttu-id="c7d7e-115">Gibt eine Instanz des **PsApiManagementContext** -Objekts an.</span><span class="sxs-lookup"><span data-stu-id="c7d7e-115">Specifies an instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7d7e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7d7e-116">-DefaultProfile</span></span>
<span data-ttu-id="c7d7e-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c7d7e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d7e-118">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c7d7e-118">-Description</span></span>
<span data-ttu-id="c7d7e-119">Gibt die Produktbeschreibung an.</span><span class="sxs-lookup"><span data-stu-id="c7d7e-119">Specifies the product description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7d7e-120">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="c7d7e-120">-LegalTerms</span></span>
<span data-ttu-id="c7d7e-121">Gibt die rechtlichen Nutzungsbestimmungen des Produkts an.</span><span class="sxs-lookup"><span data-stu-id="c7d7e-121">Specifies the legal terms of use of the product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7d7e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c7d7e-122">-PassThru</span></span>
<span data-ttu-id="c7d7e-123">passthru</span><span class="sxs-lookup"><span data-stu-id="c7d7e-123">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7d7e-124">-ProductID</span><span class="sxs-lookup"><span data-stu-id="c7d7e-124">-ProductId</span></span>
<span data-ttu-id="c7d7e-125">Gibt den Bezeichner des vorhandenen Produkts an.</span><span class="sxs-lookup"><span data-stu-id="c7d7e-125">Specifies the identifier of the existing product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7d7e-126">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="c7d7e-126">-State</span></span>
<span data-ttu-id="c7d7e-127">Gibt den Produktstatus an.</span><span class="sxs-lookup"><span data-stu-id="c7d7e-127">Specifies the product state.</span></span>
<span data-ttu-id="c7d7e-128">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="c7d7e-128">psdx_paramvalues</span></span>

- <span data-ttu-id="c7d7e-129">NotPublished</span><span class="sxs-lookup"><span data-stu-id="c7d7e-129">NotPublished</span></span>
- <span data-ttu-id="c7d7e-130">Veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="c7d7e-130">Published</span></span>

```yaml
Type: PsApiManagementProductState
Parameter Sets: (All)
Aliases: 
Accepted values: NotPublished, Published

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7d7e-131">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="c7d7e-131">-SubscriptionRequired</span></span>
<span data-ttu-id="c7d7e-132">Gibt an, ob für das Produkt ein Abonnement erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c7d7e-132">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="c7d7e-133">Der Standardwert für diesen Parameter ist **$true**.</span><span class="sxs-lookup"><span data-stu-id="c7d7e-133">The default value for this parameter is **$True**.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7d7e-134">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="c7d7e-134">-SubscriptionsLimit</span></span>
<span data-ttu-id="c7d7e-135">Gibt die maximale Anzahl gleichzeitiger Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="c7d7e-135">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="c7d7e-136">Der Standardwert für diesen Parameter ist 1.</span><span class="sxs-lookup"><span data-stu-id="c7d7e-136">The default value for this parameter is 1.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7d7e-137">-Title</span><span class="sxs-lookup"><span data-stu-id="c7d7e-137">-Title</span></span>
<span data-ttu-id="c7d7e-138">Gibt den Produkttitel an, der vom Cmdlet festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="c7d7e-138">Specifies the product title this cmdlet sets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7d7e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7d7e-139">CommonParameters</span></span>
<span data-ttu-id="c7d7e-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7d7e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7d7e-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7d7e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7d7e-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c7d7e-142">INPUTS</span></span>

### <span data-ttu-id="c7d7e-143">Keine</span><span class="sxs-lookup"><span data-stu-id="c7d7e-143">None</span></span>
<span data-ttu-id="c7d7e-144">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="c7d7e-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c7d7e-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c7d7e-145">OUTPUTS</span></span>

### <span data-ttu-id="c7d7e-146">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="c7d7e-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="c7d7e-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="c7d7e-147">NOTES</span></span>

## <span data-ttu-id="c7d7e-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c7d7e-148">RELATED LINKS</span></span>

[<span data-ttu-id="c7d7e-149">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="c7d7e-149">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="c7d7e-150">Neu – AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="c7d7e-150">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="c7d7e-151">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="c7d7e-151">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)


