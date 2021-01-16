---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 223FBBA6-4405-4B7A-BA63-5F2434A2A50D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
ms.openlocfilehash: 9bee67dd299163b8e660b0e17c4e3bc11da5b40e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98308648"
---
# <span data-ttu-id="b007f-101">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="b007f-101">Set-AzApiManagementProduct</span></span>

## <span data-ttu-id="b007f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b007f-102">SYNOPSIS</span></span>
<span data-ttu-id="b007f-103">Legt die Produktdetails für die API-Verwaltung fest.</span><span class="sxs-lookup"><span data-stu-id="b007f-103">Sets the API Management product details.</span></span>

## <span data-ttu-id="b007f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b007f-104">SYNTAX</span></span>

```
Set-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-Title <String>]
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b007f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b007f-105">DESCRIPTION</span></span>
<span data-ttu-id="b007f-106">Das **Cmdlet "Set-AzApiManagementProduct"** legt die Produktdetails für die API-Verwaltung fest.</span><span class="sxs-lookup"><span data-stu-id="b007f-106">The **Set-AzApiManagementProduct** cmdlet sets the API Management product details.</span></span>

## <span data-ttu-id="b007f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b007f-107">EXAMPLES</span></span>

### <span data-ttu-id="b007f-108">Beispiel 1: Aktualisieren der Produktdetails</span><span class="sxs-lookup"><span data-stu-id="b007f-108">Example 1: Update the product details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $True -State "NotPublished"
```

<span data-ttu-id="b007f-109">Mit diesem Befehl werden die Produktdetails der API-Verwaltung aktualisiert, ein Abonnement erforderlich, und die Veröffentlichung wird dann wieder aufheben.</span><span class="sxs-lookup"><span data-stu-id="b007f-109">This command updates the API Management product details, requires a subscription, and then unpublishes.</span></span>

## <span data-ttu-id="b007f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b007f-110">PARAMETERS</span></span>

### <span data-ttu-id="b007f-111">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="b007f-111">-ApprovalRequired</span></span>
<span data-ttu-id="b007f-112">Gibt an, ob das Abonnement für das Produkt genehmigt werden muss.</span><span class="sxs-lookup"><span data-stu-id="b007f-112">Indicates whether the subscription to the product requires approval.</span></span>
<span data-ttu-id="b007f-113">Der Standardwert ist **$False.**</span><span class="sxs-lookup"><span data-stu-id="b007f-113">The default value is **$False**.</span></span>

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

### <span data-ttu-id="b007f-114">-Context</span><span class="sxs-lookup"><span data-stu-id="b007f-114">-Context</span></span>
<span data-ttu-id="b007f-115">Gibt eine Instanz des **"PsApiManagementContext"-Objekts** an.</span><span class="sxs-lookup"><span data-stu-id="b007f-115">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b007f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b007f-116">-DefaultProfile</span></span>
<span data-ttu-id="b007f-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b007f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b007f-118">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b007f-118">-Description</span></span>
<span data-ttu-id="b007f-119">Gibt die Produktbeschreibung an.</span><span class="sxs-lookup"><span data-stu-id="b007f-119">Specifies the product description.</span></span>

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

### <span data-ttu-id="b007f-120">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="b007f-120">-LegalTerms</span></span>
<span data-ttu-id="b007f-121">Gibt die rechtlichen Nutzungsbedingungen für das Produkt an.</span><span class="sxs-lookup"><span data-stu-id="b007f-121">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="b007f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b007f-122">-PassThru</span></span>
<span data-ttu-id="b007f-123">passthru</span><span class="sxs-lookup"><span data-stu-id="b007f-123">passthru</span></span>

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

### <span data-ttu-id="b007f-124">-ProductId</span><span class="sxs-lookup"><span data-stu-id="b007f-124">-ProductId</span></span>
<span data-ttu-id="b007f-125">Gibt den Bezeichner des vorhandenen Produkts an.</span><span class="sxs-lookup"><span data-stu-id="b007f-125">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="b007f-126">-State</span><span class="sxs-lookup"><span data-stu-id="b007f-126">-State</span></span>
<span data-ttu-id="b007f-127">Gibt den Produktstatus an.</span><span class="sxs-lookup"><span data-stu-id="b007f-127">Specifies the product state.</span></span>
<span data-ttu-id="b007f-128">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="b007f-128">psdx_paramvalues</span></span>
- <span data-ttu-id="b007f-129">NotPublished</span><span class="sxs-lookup"><span data-stu-id="b007f-129">NotPublished</span></span>
- <span data-ttu-id="b007f-130">Veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="b007f-130">Published</span></span>

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

### <span data-ttu-id="b007f-131">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="b007f-131">-SubscriptionRequired</span></span>
<span data-ttu-id="b007f-132">Gibt an, ob für das Produkt ein Abonnement erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="b007f-132">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="b007f-133">Der Standardwert für diesen Parameter ist **$True.**</span><span class="sxs-lookup"><span data-stu-id="b007f-133">The default value for this parameter is **$True**.</span></span>

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

### <span data-ttu-id="b007f-134">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="b007f-134">-SubscriptionsLimit</span></span>
<span data-ttu-id="b007f-135">Gibt die maximale Anzahl gleichzeitiger Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="b007f-135">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="b007f-136">Der Standardwert für diesen Parameter ist "None".</span><span class="sxs-lookup"><span data-stu-id="b007f-136">The default value for this parameter is None.</span></span>

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

### <span data-ttu-id="b007f-137">-Title</span><span class="sxs-lookup"><span data-stu-id="b007f-137">-Title</span></span>
<span data-ttu-id="b007f-138">Gibt den Produkttitel an, den dieses Cmdlet legt.</span><span class="sxs-lookup"><span data-stu-id="b007f-138">Specifies the product title this cmdlet sets.</span></span>

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

### <span data-ttu-id="b007f-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b007f-139">-Confirm</span></span>
<span data-ttu-id="b007f-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b007f-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b007f-141">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b007f-141">-WhatIf</span></span>
<span data-ttu-id="b007f-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b007f-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b007f-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b007f-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b007f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b007f-144">CommonParameters</span></span>
<span data-ttu-id="b007f-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b007f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b007f-146">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b007f-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b007f-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b007f-147">INPUTS</span></span>

### <span data-ttu-id="b007f-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b007f-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b007f-149">System.String</span><span class="sxs-lookup"><span data-stu-id="b007f-149">System.String</span></span>

### <span data-ttu-id="b007f-150">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b007f-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b007f-151">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b007f-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b007f-152">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="b007f-152">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="b007f-153">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b007f-153">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b007f-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b007f-154">OUTPUTS</span></span>

### <span data-ttu-id="b007f-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="b007f-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="b007f-156">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b007f-156">NOTES</span></span>

## <span data-ttu-id="b007f-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b007f-157">RELATED LINKS</span></span>

[<span data-ttu-id="b007f-158">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="b007f-158">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="b007f-159">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="b007f-159">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="b007f-160">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="b007f-160">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)


