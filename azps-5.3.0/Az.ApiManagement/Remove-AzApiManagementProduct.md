---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
ms.openlocfilehash: 33b00df9e0c9c5b5e0ef04d22b745942535effcb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381981"
---
# <span data-ttu-id="b01fd-101">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="b01fd-101">Remove-AzApiManagementProduct</span></span>

## <span data-ttu-id="b01fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b01fd-102">SYNOPSIS</span></span>
<span data-ttu-id="b01fd-103">Entfernt ein vorhandenes API-Verwaltungsprodukt.</span><span class="sxs-lookup"><span data-stu-id="b01fd-103">Removes an existing API Management product.</span></span>

## <span data-ttu-id="b01fd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b01fd-104">SYNTAX</span></span>

```
Remove-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b01fd-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b01fd-105">DESCRIPTION</span></span>
<span data-ttu-id="b01fd-106">Das **Cmdlet "Remove-AzApiManagementProduct"** entfernt ein vorhandenes API-Verwaltungsprodukt.</span><span class="sxs-lookup"><span data-stu-id="b01fd-106">The **Remove-AzApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="b01fd-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b01fd-107">EXAMPLES</span></span>

### <span data-ttu-id="b01fd-108">Beispiel 1: Entfernen eines vorhandenen Produkts und aller Abonnements</span><span class="sxs-lookup"><span data-stu-id="b01fd-108">Example 1: Remove an existing product and all subscriptions</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -DeleteSubscriptions
```

<span data-ttu-id="b01fd-109">Mit diesem Befehl werden ein vorhandenes Produkt und alle Abonnements entfernt.</span><span class="sxs-lookup"><span data-stu-id="b01fd-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="b01fd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b01fd-110">PARAMETERS</span></span>

### <span data-ttu-id="b01fd-111">-Context</span><span class="sxs-lookup"><span data-stu-id="b01fd-111">-Context</span></span>
<span data-ttu-id="b01fd-112">Gibt eine Instanz des **PsApiManagementContext-Objekts** an.</span><span class="sxs-lookup"><span data-stu-id="b01fd-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b01fd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b01fd-113">-DefaultProfile</span></span>
<span data-ttu-id="b01fd-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b01fd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b01fd-115">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="b01fd-115">-DeleteSubscriptions</span></span>
<span data-ttu-id="b01fd-116">Gibt an, ob Abonnements für das Produkt gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="b01fd-116">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="b01fd-117">Wenn Sie diesen Parameter nicht festlegen und Abonnements vorhanden sind, wird eine Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="b01fd-117">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

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

### <span data-ttu-id="b01fd-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b01fd-118">-PassThru</span></span>
<span data-ttu-id="b01fd-119">Gibt an, dass dieses Cmdlet bei einem Fehler den Wert "$True" oder den Wert "$False" zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="b01fd-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

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

### <span data-ttu-id="b01fd-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="b01fd-120">-ProductId</span></span>
<span data-ttu-id="b01fd-121">Gibt den Bezeichner des vorhandenen Produkts an.</span><span class="sxs-lookup"><span data-stu-id="b01fd-121">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="b01fd-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b01fd-122">-Confirm</span></span>
<span data-ttu-id="b01fd-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b01fd-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b01fd-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b01fd-124">-WhatIf</span></span>
<span data-ttu-id="b01fd-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b01fd-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b01fd-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b01fd-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b01fd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b01fd-127">CommonParameters</span></span>
<span data-ttu-id="b01fd-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b01fd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b01fd-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b01fd-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b01fd-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b01fd-130">INPUTS</span></span>

### <span data-ttu-id="b01fd-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b01fd-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b01fd-132">System.String</span><span class="sxs-lookup"><span data-stu-id="b01fd-132">System.String</span></span>

### <span data-ttu-id="b01fd-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b01fd-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b01fd-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b01fd-134">OUTPUTS</span></span>

### <span data-ttu-id="b01fd-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b01fd-135">System.Boolean</span></span>

## <span data-ttu-id="b01fd-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b01fd-136">NOTES</span></span>

## <span data-ttu-id="b01fd-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b01fd-137">RELATED LINKS</span></span>

[<span data-ttu-id="b01fd-138">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="b01fd-138">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="b01fd-139">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="b01fd-139">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="b01fd-140">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="b01fd-140">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


