---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 223FBBA6-4405-4B7A-BA63-5F2434A2A50D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
ms.openlocfilehash: f60bf40cd6226979955f71e413be3914fc05c417
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820972"
---
# <span data-ttu-id="069cd-101">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="069cd-101">Set-AzApiManagementProduct</span></span>

## <span data-ttu-id="069cd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="069cd-102">SYNOPSIS</span></span>
<span data-ttu-id="069cd-103">Legt die API-Verwaltungsprodukt Details fest.</span><span class="sxs-lookup"><span data-stu-id="069cd-103">Sets the API Management product details.</span></span>

## <span data-ttu-id="069cd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="069cd-104">SYNTAX</span></span>

```
Set-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-Title <String>]
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="069cd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="069cd-105">DESCRIPTION</span></span>
<span data-ttu-id="069cd-106">Das Cmdlet " **Set-AzApiManagementProduct** " legt die API-Verwaltungsprodukt Details fest.</span><span class="sxs-lookup"><span data-stu-id="069cd-106">The **Set-AzApiManagementProduct** cmdlet sets the API Management product details.</span></span>

## <span data-ttu-id="069cd-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="069cd-107">EXAMPLES</span></span>

### <span data-ttu-id="069cd-108">Beispiel 1: Aktualisieren der Produkt Details</span><span class="sxs-lookup"><span data-stu-id="069cd-108">Example 1: Update the product details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $True -State "NotPublished"
```

<span data-ttu-id="069cd-109">Dieser Befehl aktualisiert die API-Verwaltungsprodukt Details, erfordert ein Abonnement und dann die Veröffentlichung.</span><span class="sxs-lookup"><span data-stu-id="069cd-109">This command updates the API Management product details, requires a subscription, and then unpublishes.</span></span>

## <span data-ttu-id="069cd-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="069cd-110">PARAMETERS</span></span>

### <span data-ttu-id="069cd-111">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="069cd-111">-ApprovalRequired</span></span>
<span data-ttu-id="069cd-112">Gibt an, ob das Abonnement für das Produkt genehmigt werden muss.</span><span class="sxs-lookup"><span data-stu-id="069cd-112">Indicates whether the subscription to the product requires approval.</span></span>
<span data-ttu-id="069cd-113">Der Standardwert ist **$false**.</span><span class="sxs-lookup"><span data-stu-id="069cd-113">The default value is **$False**.</span></span>

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

### <span data-ttu-id="069cd-114">-Context</span><span class="sxs-lookup"><span data-stu-id="069cd-114">-Context</span></span>
<span data-ttu-id="069cd-115">Gibt eine Instanz des **PsApiManagementContext** -Objekts an.</span><span class="sxs-lookup"><span data-stu-id="069cd-115">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="069cd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="069cd-116">-DefaultProfile</span></span>
<span data-ttu-id="069cd-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="069cd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="069cd-118">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="069cd-118">-Description</span></span>
<span data-ttu-id="069cd-119">Gibt die Produktbeschreibung an.</span><span class="sxs-lookup"><span data-stu-id="069cd-119">Specifies the product description.</span></span>

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

### <span data-ttu-id="069cd-120">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="069cd-120">-LegalTerms</span></span>
<span data-ttu-id="069cd-121">Gibt die rechtlichen Nutzungsbestimmungen des Produkts an.</span><span class="sxs-lookup"><span data-stu-id="069cd-121">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="069cd-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="069cd-122">-PassThru</span></span>
<span data-ttu-id="069cd-123">passthru</span><span class="sxs-lookup"><span data-stu-id="069cd-123">passthru</span></span>

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

### <span data-ttu-id="069cd-124">-ProductID</span><span class="sxs-lookup"><span data-stu-id="069cd-124">-ProductId</span></span>
<span data-ttu-id="069cd-125">Gibt den Bezeichner des vorhandenen Produkts an.</span><span class="sxs-lookup"><span data-stu-id="069cd-125">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="069cd-126">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="069cd-126">-State</span></span>
<span data-ttu-id="069cd-127">Gibt den Produktstatus an.</span><span class="sxs-lookup"><span data-stu-id="069cd-127">Specifies the product state.</span></span>
<span data-ttu-id="069cd-128">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="069cd-128">psdx_paramvalues</span></span>
- <span data-ttu-id="069cd-129">NotPublished</span><span class="sxs-lookup"><span data-stu-id="069cd-129">NotPublished</span></span>
- <span data-ttu-id="069cd-130">Veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="069cd-130">Published</span></span>

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

### <span data-ttu-id="069cd-131">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="069cd-131">-SubscriptionRequired</span></span>
<span data-ttu-id="069cd-132">Gibt an, ob für das Produkt ein Abonnement erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="069cd-132">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="069cd-133">Der Standardwert für diesen Parameter ist **$true**.</span><span class="sxs-lookup"><span data-stu-id="069cd-133">The default value for this parameter is **$True**.</span></span>

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

### <span data-ttu-id="069cd-134">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="069cd-134">-SubscriptionsLimit</span></span>
<span data-ttu-id="069cd-135">Gibt die maximale Anzahl gleichzeitiger Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="069cd-135">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="069cd-136">Der Standardwert für diesen Parameter ist 1.</span><span class="sxs-lookup"><span data-stu-id="069cd-136">The default value for this parameter is 1.</span></span>

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

### <span data-ttu-id="069cd-137">-Title</span><span class="sxs-lookup"><span data-stu-id="069cd-137">-Title</span></span>
<span data-ttu-id="069cd-138">Gibt den Produkttitel an, der vom Cmdlet festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="069cd-138">Specifies the product title this cmdlet sets.</span></span>

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

### <span data-ttu-id="069cd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="069cd-139">CommonParameters</span></span>
<span data-ttu-id="069cd-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="069cd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="069cd-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="069cd-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="069cd-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="069cd-142">INPUTS</span></span>

### <span data-ttu-id="069cd-143">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="069cd-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="069cd-144">System. String</span><span class="sxs-lookup"><span data-stu-id="069cd-144">System.String</span></span>

### <span data-ttu-id="069cd-145">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="069cd-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="069cd-146">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="069cd-146">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="069cd-147">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementProductState, Microsoft. Azure. PowerShell. Cmdlets. ApiManagement. Servicemanagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="069cd-147">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="069cd-148">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="069cd-148">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="069cd-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="069cd-149">OUTPUTS</span></span>

### <span data-ttu-id="069cd-150">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="069cd-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="069cd-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="069cd-151">NOTES</span></span>

## <span data-ttu-id="069cd-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="069cd-152">RELATED LINKS</span></span>

[<span data-ttu-id="069cd-153">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="069cd-153">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="069cd-154">Neu – AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="069cd-154">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="069cd-155">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="069cd-155">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)


