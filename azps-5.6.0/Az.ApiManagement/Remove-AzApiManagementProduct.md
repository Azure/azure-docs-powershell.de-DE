---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
ms.openlocfilehash: 9ad08f867bf78dc4a6bc2df5c4dd3086c3cea33c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932128"
---
# <span data-ttu-id="1a4fe-101">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="1a4fe-101">Remove-AzApiManagementProduct</span></span>

## <span data-ttu-id="1a4fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a4fe-102">SYNOPSIS</span></span>
<span data-ttu-id="1a4fe-103">Entfernt ein vorhandenes API-Verwaltungsprodukt.</span><span class="sxs-lookup"><span data-stu-id="1a4fe-103">Removes an existing API Management product.</span></span>

## <span data-ttu-id="1a4fe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1a4fe-104">SYNTAX</span></span>

```
Remove-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a4fe-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1a4fe-105">DESCRIPTION</span></span>
<span data-ttu-id="1a4fe-106">Das **Cmdlet Remove-AzApiManagementProduct** entfernt ein vorhandenes API-Verwaltungsprodukt.</span><span class="sxs-lookup"><span data-stu-id="1a4fe-106">The **Remove-AzApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="1a4fe-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1a4fe-107">EXAMPLES</span></span>

### <span data-ttu-id="1a4fe-108">Beispiel 1: Entfernen eines vorhandenen Produkts und aller Abonnements</span><span class="sxs-lookup"><span data-stu-id="1a4fe-108">Example 1: Remove an existing product and all subscriptions</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -DeleteSubscriptions
```

<span data-ttu-id="1a4fe-109">Mit diesem Befehl werden ein vorhandenes Produkt und alle Abonnements entfernt.</span><span class="sxs-lookup"><span data-stu-id="1a4fe-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="1a4fe-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1a4fe-110">PARAMETERS</span></span>

### <span data-ttu-id="1a4fe-111">-Context</span><span class="sxs-lookup"><span data-stu-id="1a4fe-111">-Context</span></span>
<span data-ttu-id="1a4fe-112">Gibt eine Instanz des **PsApiManagementContext-Objekts** an.</span><span class="sxs-lookup"><span data-stu-id="1a4fe-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1a4fe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a4fe-113">-DefaultProfile</span></span>
<span data-ttu-id="1a4fe-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1a4fe-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a4fe-115">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="1a4fe-115">-DeleteSubscriptions</span></span>
<span data-ttu-id="1a4fe-116">Gibt an, ob Abonnements für das Produkt gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="1a4fe-116">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="1a4fe-117">Wenn Sie diesen Parameter nicht festlegen und Abonnements vorhanden sind, wird eine Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="1a4fe-117">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

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

### <span data-ttu-id="1a4fe-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1a4fe-118">-PassThru</span></span>
<span data-ttu-id="1a4fe-119">Gibt an, dass dieses Cmdlet einen Wert von $True , wenn es erfolgreich ist, oder einen Wert von $False zurückgibt, wenn es fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="1a4fe-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

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

### <span data-ttu-id="1a4fe-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="1a4fe-120">-ProductId</span></span>
<span data-ttu-id="1a4fe-121">Gibt den Bezeichner des vorhandenen Produkts an.</span><span class="sxs-lookup"><span data-stu-id="1a4fe-121">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="1a4fe-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1a4fe-122">-Confirm</span></span>
<span data-ttu-id="1a4fe-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1a4fe-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a4fe-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a4fe-124">-WhatIf</span></span>
<span data-ttu-id="1a4fe-125">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1a4fe-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a4fe-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1a4fe-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a4fe-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a4fe-127">CommonParameters</span></span>
<span data-ttu-id="1a4fe-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a4fe-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a4fe-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1a4fe-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a4fe-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1a4fe-130">INPUTS</span></span>

### <span data-ttu-id="1a4fe-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1a4fe-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1a4fe-132">System.String</span><span class="sxs-lookup"><span data-stu-id="1a4fe-132">System.String</span></span>

### <span data-ttu-id="1a4fe-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1a4fe-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1a4fe-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1a4fe-134">OUTPUTS</span></span>

### <span data-ttu-id="1a4fe-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1a4fe-135">System.Boolean</span></span>

## <span data-ttu-id="1a4fe-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1a4fe-136">NOTES</span></span>

## <span data-ttu-id="1a4fe-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1a4fe-137">RELATED LINKS</span></span>

[<span data-ttu-id="1a4fe-138">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="1a4fe-138">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="1a4fe-139">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="1a4fe-139">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="1a4fe-140">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="1a4fe-140">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


