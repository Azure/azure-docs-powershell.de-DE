---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 223FBBA6-4405-4B7A-BA63-5F2434A2A50D
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
ms.openlocfilehash: e827fcf43c151f0812d96456de430f57686d4562
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922531"
---
# <span data-ttu-id="821ff-101">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="821ff-101">Set-AzApiManagementProduct</span></span>

## <span data-ttu-id="821ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="821ff-102">SYNOPSIS</span></span>
<span data-ttu-id="821ff-103">Legt die Produktdetails für die API-Verwaltung fest.</span><span class="sxs-lookup"><span data-stu-id="821ff-103">Sets the API Management product details.</span></span>

## <span data-ttu-id="821ff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="821ff-104">SYNTAX</span></span>

```
Set-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-Title <String>]
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="821ff-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="821ff-105">DESCRIPTION</span></span>
<span data-ttu-id="821ff-106">Das **Cmdlet Set-AzApiManagementProduct** legt die Produktdetails für die API-Verwaltung fest.</span><span class="sxs-lookup"><span data-stu-id="821ff-106">The **Set-AzApiManagementProduct** cmdlet sets the API Management product details.</span></span>

## <span data-ttu-id="821ff-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="821ff-107">EXAMPLES</span></span>

### <span data-ttu-id="821ff-108">Beispiel 1: Aktualisieren der Produktdetails</span><span class="sxs-lookup"><span data-stu-id="821ff-108">Example 1: Update the product details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $True -State "NotPublished"
```

<span data-ttu-id="821ff-109">Mit diesem Befehl werden die Produktdetails der API-Verwaltung aktualisiert, ein Abonnement erforderlich und die Veröffentlichung wird dann aufheben.</span><span class="sxs-lookup"><span data-stu-id="821ff-109">This command updates the API Management product details, requires a subscription, and then unpublishes.</span></span>

## <span data-ttu-id="821ff-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="821ff-110">PARAMETERS</span></span>

### <span data-ttu-id="821ff-111">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="821ff-111">-ApprovalRequired</span></span>
<span data-ttu-id="821ff-112">Gibt an, ob für das Abonnement des Produkts eine Genehmigung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="821ff-112">Indicates whether the subscription to the product requires approval.</span></span>
<span data-ttu-id="821ff-113">Der Standardwert ist **$False**.</span><span class="sxs-lookup"><span data-stu-id="821ff-113">The default value is **$False**.</span></span>

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

### <span data-ttu-id="821ff-114">-Context</span><span class="sxs-lookup"><span data-stu-id="821ff-114">-Context</span></span>
<span data-ttu-id="821ff-115">Gibt eine Instanz des **PsApiManagementContext-Objekts** an.</span><span class="sxs-lookup"><span data-stu-id="821ff-115">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="821ff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="821ff-116">-DefaultProfile</span></span>
<span data-ttu-id="821ff-117">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="821ff-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="821ff-118">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="821ff-118">-Description</span></span>
<span data-ttu-id="821ff-119">Gibt die Produktbeschreibung an.</span><span class="sxs-lookup"><span data-stu-id="821ff-119">Specifies the product description.</span></span>

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

### <span data-ttu-id="821ff-120">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="821ff-120">-LegalTerms</span></span>
<span data-ttu-id="821ff-121">Gibt die gesetzlichen Nutzungsbedingungen für das Produkt an.</span><span class="sxs-lookup"><span data-stu-id="821ff-121">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="821ff-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="821ff-122">-PassThru</span></span>
<span data-ttu-id="821ff-123">passthru</span><span class="sxs-lookup"><span data-stu-id="821ff-123">passthru</span></span>

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

### <span data-ttu-id="821ff-124">-ProductId</span><span class="sxs-lookup"><span data-stu-id="821ff-124">-ProductId</span></span>
<span data-ttu-id="821ff-125">Gibt den Bezeichner des vorhandenen Produkts an.</span><span class="sxs-lookup"><span data-stu-id="821ff-125">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="821ff-126">-State</span><span class="sxs-lookup"><span data-stu-id="821ff-126">-State</span></span>
<span data-ttu-id="821ff-127">Gibt den Produktzustand an.</span><span class="sxs-lookup"><span data-stu-id="821ff-127">Specifies the product state.</span></span>
<span data-ttu-id="821ff-128">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="821ff-128">psdx_paramvalues</span></span>
- <span data-ttu-id="821ff-129">NotPublished</span><span class="sxs-lookup"><span data-stu-id="821ff-129">NotPublished</span></span>
- <span data-ttu-id="821ff-130">Veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="821ff-130">Published</span></span>

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

### <span data-ttu-id="821ff-131">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="821ff-131">-SubscriptionRequired</span></span>
<span data-ttu-id="821ff-132">Gibt an, ob für das Produkt ein Abonnement erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="821ff-132">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="821ff-133">Der Standardwert für diesen Parameter ist **$True**.</span><span class="sxs-lookup"><span data-stu-id="821ff-133">The default value for this parameter is **$True**.</span></span>

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

### <span data-ttu-id="821ff-134">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="821ff-134">-SubscriptionsLimit</span></span>
<span data-ttu-id="821ff-135">Gibt die maximale Anzahl gleichzeitiger Abonnements an.</span><span class="sxs-lookup"><span data-stu-id="821ff-135">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="821ff-136">Der Standardwert für diesen Parameter ist None.</span><span class="sxs-lookup"><span data-stu-id="821ff-136">The default value for this parameter is None.</span></span>

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

### <span data-ttu-id="821ff-137">-Title</span><span class="sxs-lookup"><span data-stu-id="821ff-137">-Title</span></span>
<span data-ttu-id="821ff-138">Gibt den Produkttitel an, den dieses Cmdlet setzt.</span><span class="sxs-lookup"><span data-stu-id="821ff-138">Specifies the product title this cmdlet sets.</span></span>

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

### <span data-ttu-id="821ff-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="821ff-139">-Confirm</span></span>
<span data-ttu-id="821ff-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="821ff-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="821ff-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="821ff-141">-WhatIf</span></span>
<span data-ttu-id="821ff-142">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="821ff-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="821ff-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="821ff-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="821ff-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="821ff-144">CommonParameters</span></span>
<span data-ttu-id="821ff-145">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="821ff-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="821ff-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="821ff-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="821ff-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="821ff-147">INPUTS</span></span>

### <span data-ttu-id="821ff-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="821ff-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="821ff-149">System.String</span><span class="sxs-lookup"><span data-stu-id="821ff-149">System.String</span></span>

### <span data-ttu-id="821ff-150">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="821ff-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="821ff-151">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="821ff-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="821ff-152">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="821ff-152">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="821ff-153">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="821ff-153">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="821ff-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="821ff-154">OUTPUTS</span></span>

### <span data-ttu-id="821ff-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="821ff-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="821ff-156">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="821ff-156">NOTES</span></span>

## <span data-ttu-id="821ff-157">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="821ff-157">RELATED LINKS</span></span>

[<span data-ttu-id="821ff-158">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="821ff-158">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="821ff-159">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="821ff-159">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="821ff-160">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="821ff-160">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)


