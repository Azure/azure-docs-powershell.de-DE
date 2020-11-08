---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
ms.openlocfilehash: 33b00df9e0c9c5b5e0ef04d22b745942535effcb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996843"
---
# <span data-ttu-id="00167-101">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="00167-101">Remove-AzApiManagementProduct</span></span>

## <span data-ttu-id="00167-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="00167-102">SYNOPSIS</span></span>
<span data-ttu-id="00167-103">Entfernt ein vorhandenes API-Verwaltungsprodukt.</span><span class="sxs-lookup"><span data-stu-id="00167-103">Removes an existing API Management product.</span></span>

## <span data-ttu-id="00167-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="00167-104">SYNTAX</span></span>

```
Remove-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00167-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="00167-105">DESCRIPTION</span></span>
<span data-ttu-id="00167-106">Das Cmdlet **Remove-AzApiManagementProduct** entfernt ein vorhandenes API-Verwaltungsprodukt.</span><span class="sxs-lookup"><span data-stu-id="00167-106">The **Remove-AzApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="00167-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="00167-107">EXAMPLES</span></span>

### <span data-ttu-id="00167-108">Beispiel 1: Entfernen eines vorhandenen Produkts und aller Abonnements</span><span class="sxs-lookup"><span data-stu-id="00167-108">Example 1: Remove an existing product and all subscriptions</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -DeleteSubscriptions
```

<span data-ttu-id="00167-109">Mit diesem Befehl werden ein vorhandenes Produkt und alle Abonnements entfernt.</span><span class="sxs-lookup"><span data-stu-id="00167-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="00167-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="00167-110">PARAMETERS</span></span>

### <span data-ttu-id="00167-111">-Context</span><span class="sxs-lookup"><span data-stu-id="00167-111">-Context</span></span>
<span data-ttu-id="00167-112">Gibt eine Instanz des **PsApiManagementContext** -Objekts an.</span><span class="sxs-lookup"><span data-stu-id="00167-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="00167-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00167-113">-DefaultProfile</span></span>
<span data-ttu-id="00167-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="00167-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00167-115">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="00167-115">-DeleteSubscriptions</span></span>
<span data-ttu-id="00167-116">Gibt an, ob Abonnements für das Produkt gelöscht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="00167-116">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="00167-117">Wenn Sie diesen Parameter nicht setzen und Abonnements vorhanden sind, wird eine Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="00167-117">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

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

### <span data-ttu-id="00167-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="00167-118">-PassThru</span></span>
<span data-ttu-id="00167-119">Gibt an, dass dieses Cmdlet einen Wert von $true zurückgibt, wenn es erfolgreich ist, oder einen Wert von $false, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="00167-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

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

### <span data-ttu-id="00167-120">-ProductID</span><span class="sxs-lookup"><span data-stu-id="00167-120">-ProductId</span></span>
<span data-ttu-id="00167-121">Gibt den Bezeichner des vorhandenen Produkts an.</span><span class="sxs-lookup"><span data-stu-id="00167-121">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="00167-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="00167-122">-Confirm</span></span>
<span data-ttu-id="00167-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="00167-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00167-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00167-124">-WhatIf</span></span>
<span data-ttu-id="00167-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="00167-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00167-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="00167-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00167-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00167-127">CommonParameters</span></span>
<span data-ttu-id="00167-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00167-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00167-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="00167-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00167-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="00167-130">INPUTS</span></span>

### <span data-ttu-id="00167-131">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="00167-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="00167-132">System. String</span><span class="sxs-lookup"><span data-stu-id="00167-132">System.String</span></span>

### <span data-ttu-id="00167-133">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="00167-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="00167-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="00167-134">OUTPUTS</span></span>

### <span data-ttu-id="00167-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="00167-135">System.Boolean</span></span>

## <span data-ttu-id="00167-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="00167-136">NOTES</span></span>

## <span data-ttu-id="00167-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="00167-137">RELATED LINKS</span></span>

[<span data-ttu-id="00167-138">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="00167-138">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="00167-139">Neu – AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="00167-139">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="00167-140">Satz-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="00167-140">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


