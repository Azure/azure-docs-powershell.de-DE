---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 223FBBA6-4405-4B7A-BA63-5F2434A2A50D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
ms.openlocfilehash: 9bee67dd299163b8e660b0e17c4e3bc11da5b40e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004377"
---
# <span data-ttu-id="80859-101">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="80859-101">Set-AzApiManagementProduct</span></span>

## <span data-ttu-id="80859-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="80859-102">SYNOPSIS</span></span>
<span data-ttu-id="80859-103">Legt die API-Verwaltungsprodukt Details fest.</span><span class="sxs-lookup"><span data-stu-id="80859-103">Sets the API Management product details.</span></span>

## <span data-ttu-id="80859-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="80859-104">SYNTAX</span></span>

```
Set-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-Title <String>]
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80859-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="80859-105">DESCRIPTION</span></span>
<span data-ttu-id="80859-106">Das Cmdlet " **Set-AzApiManagementProduct** " legt die API-Verwaltungsprodukt Details fest.</span><span class="sxs-lookup"><span data-stu-id="80859-106">The **Set-AzApiManagementProduct** cmdlet sets the API Management product details.</span></span>

## <span data-ttu-id="80859-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="80859-107">EXAMPLES</span></span>

### <span data-ttu-id="80859-108">Beispiel 1: Aktualisieren der Produkt Details</span><span class="sxs-lookup"><span data-stu-id="80859-108">Example 1: Update the product details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $True -State "NotPublished"
```

<span data-ttu-id="80859-109">Dieser Befehl aktualisiert die API-Verwaltungsprodukt Details, erfordert ein Abonnement und dann die Veröffentlichung.</span><span class="sxs-lookup"><span data-stu-id="80859-109">This command updates the API Management product details, requires a subscription, and then unpublishes.</span></span>

## <span data-ttu-id="80859-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="80859-110">PARAMETERS</span></span>

### <span data-ttu-id="80859-111">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="80859-111">-ApprovalRequired</span></span>
<span data-ttu-id="80859-112">Gibt an, ob das Abonnement für das Produkt genehmigt werden muss.</span><span class="sxs-lookup"><span data-stu-id="80859-112">Indicates whether the subscription to the product requires approval.</span></span>
<span data-ttu-id="80859-113">Der Standardwert ist **$false**.</span><span class="sxs-lookup"><span data-stu-id="80859-113">The default value is **$False**.</span></span>

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

### <span data-ttu-id="80859-114">-Context</span><span class="sxs-lookup"><span data-stu-id="80859-114">-Context</span></span>
<span data-ttu-id="80859-115">Gibt eine Instanz des **PsApiManagementContext** -Objekts an.</span><span class="sxs-lookup"><span data-stu-id="80859-115">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="80859-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80859-116">-DefaultProfile</span></span>
<span data-ttu-id="80859-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="80859-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80859-118">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="80859-118">-Description</span></span>
<span data-ttu-id="80859-119">Gibt die Produktbeschreibung an.</span><span class="sxs-lookup"><span data-stu-id="80859-119">Specifies the product description.</span></span>

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

### <span data-ttu-id="80859-120">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="80859-120">-LegalTerms</span></span>
<span data-ttu-id="80859-121">Gibt die rechtlichen Nutzungsbestimmungen des Produkts an.</span><span class="sxs-lookup"><span data-stu-id="80859-121">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="80859-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="80859-122">-PassThru</span></span>
<span data-ttu-id="80859-123">passthru</span><span class="sxs-lookup"><span data-stu-id="80859-123">passthru</span></span>

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

### <span data-ttu-id="80859-124">-ProductID</span><span class="sxs-lookup"><span data-stu-id="80859-124">-ProductId</span></span>
<span data-ttu-id="80859-125">Gibt den Bezeichner des vorhandenen Produkts an.</span><span class="sxs-lookup"><span data-stu-id="80859-125">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="80859-126">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="80859-126">-State</span></span>
<span data-ttu-id="80859-127">Gibt den Produktstatus an.</span><span class="sxs-lookup"><span data-stu-id="80859-127">Specifies the product state.</span></span>
<span data-ttu-id="80859-128">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="80859-128">psdx_paramvalues</span></span>
- <span data-ttu-id="80859-129">NotPublished</span><span class="sxs-lookup"><span data-stu-id="80859-129">NotPublished</span></span>
- <span data-ttu-id="80859-130">Veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="80859-130">Published</span></span>

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

### <span data-ttu-id="80859-131">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="80859-131">-SubscriptionRequired</span></span>
<span data-ttu-id="80859-132">Gibt an, ob für das Produkt ein Abonnement erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="80859-132">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="80859-133">Der Standardwert für diesen Parameter ist **$true**.</span><span class="sxs-lookup"><span data-stu-id="80859-133">The default value for this parameter is **$True**.</span></span>

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

### <span data-ttu-id="80859-134">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="80859-134">-SubscriptionsLimit</span></span>
<span data-ttu-id="80859-135">Gibt die maximale Anzahl gleichzeitiger Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="80859-135">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="80859-136">Der Standardwert für diesen Parameter ist None.</span><span class="sxs-lookup"><span data-stu-id="80859-136">The default value for this parameter is None.</span></span>

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

### <span data-ttu-id="80859-137">-Title</span><span class="sxs-lookup"><span data-stu-id="80859-137">-Title</span></span>
<span data-ttu-id="80859-138">Gibt den Produkttitel an, der vom Cmdlet festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="80859-138">Specifies the product title this cmdlet sets.</span></span>

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

### <span data-ttu-id="80859-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="80859-139">-Confirm</span></span>
<span data-ttu-id="80859-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="80859-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80859-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80859-141">-WhatIf</span></span>
<span data-ttu-id="80859-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="80859-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="80859-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="80859-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80859-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80859-144">CommonParameters</span></span>
<span data-ttu-id="80859-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80859-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80859-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80859-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80859-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="80859-147">INPUTS</span></span>

### <span data-ttu-id="80859-148">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="80859-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="80859-149">System. String</span><span class="sxs-lookup"><span data-stu-id="80859-149">System.String</span></span>

### <span data-ttu-id="80859-150">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="80859-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="80859-151">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="80859-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="80859-152">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementProductState, Microsoft. Azure. PowerShell. Cmdlets. ApiManagement. Servicemanagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="80859-152">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="80859-153">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="80859-153">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="80859-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="80859-154">OUTPUTS</span></span>

### <span data-ttu-id="80859-155">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="80859-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="80859-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="80859-156">NOTES</span></span>

## <span data-ttu-id="80859-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="80859-157">RELATED LINKS</span></span>

[<span data-ttu-id="80859-158">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="80859-158">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="80859-159">Neu – AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="80859-159">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="80859-160">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="80859-160">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)


