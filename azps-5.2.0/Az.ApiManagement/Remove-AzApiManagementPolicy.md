---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 466AFB8C-C272-4A4F-8E13-A4DBD6EE3A85
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementPolicy.md
ms.openlocfilehash: a51bd7aed5ca8793a921c2cde7729c5280df44b5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98305291"
---
# <span data-ttu-id="76001-101">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="76001-101">Remove-AzApiManagementPolicy</span></span>

## <span data-ttu-id="76001-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76001-102">SYNOPSIS</span></span>
<span data-ttu-id="76001-103">Entfernt die API-Verwaltungsrichtlinie aus einem angegebenen Bereich.</span><span class="sxs-lookup"><span data-stu-id="76001-103">Removes the API Management policy from a specified scope.</span></span>

## <span data-ttu-id="76001-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76001-104">SYNTAX</span></span>

### <span data-ttu-id="76001-105">RemoveTenantLevel (Standard)</span><span class="sxs-lookup"><span data-stu-id="76001-105">RemoveTenantLevel (Default)</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76001-106">RemoveProductLevel</span><span class="sxs-lookup"><span data-stu-id="76001-106">RemoveProductLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ProductId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76001-107">RemoveApiLevel</span><span class="sxs-lookup"><span data-stu-id="76001-107">RemoveApiLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76001-108">RemoveOperationLevel</span><span class="sxs-lookup"><span data-stu-id="76001-108">RemoveOperationLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76001-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="76001-109">DESCRIPTION</span></span>
<span data-ttu-id="76001-110">Das **Cmdlet "Remove-AzApiManagementPolicy"** entfernt die API-Verwaltungsrichtlinie aus dem angegebenen Bereich.</span><span class="sxs-lookup"><span data-stu-id="76001-110">The **Remove-AzApiManagementPolicy** cmdlet removes the API Management policy from specified scope.</span></span>

## <span data-ttu-id="76001-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="76001-111">EXAMPLES</span></span>

### <span data-ttu-id="76001-112">Beispiel 1: Entfernen der Richtlinie auf Mandantenebene</span><span class="sxs-lookup"><span data-stu-id="76001-112">Example 1: Remove the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext
```

<span data-ttu-id="76001-113">Mit diesem Befehl wird die Richtlinie auf Mandantenebene aus der API-Verwaltung entfernt.</span><span class="sxs-lookup"><span data-stu-id="76001-113">This command removes tenant level policy from API Management.</span></span>

### <span data-ttu-id="76001-114">Beispiel 2: Entfernen der Produktbereichsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="76001-114">Example 2: Remove the product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="76001-115">Mit diesem Befehl wird die Produktbereichsrichtlinie aus der API-Verwaltung entfernt.</span><span class="sxs-lookup"><span data-stu-id="76001-115">This command removes product-scope policy from API Management.</span></span>

### <span data-ttu-id="76001-116">Beispiel 3: Entfernen der API-Bereichsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="76001-116">Example 3: Remove the API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="76001-117">Mit diesem Befehl wird die API-Bereichsrichtlinie aus der API-Verwaltung entfernt.</span><span class="sxs-lookup"><span data-stu-id="76001-117">This command removes API-scope policy from API Management.</span></span>

### <span data-ttu-id="76001-118">Beispiel 4: Entfernen der Vorgangsbereichsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="76001-118">Example 4: Remove the operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="76001-119">Mit diesem Befehl wird die Vorgangsbereichsrichtlinie aus der API-Verwaltung entfernt.</span><span class="sxs-lookup"><span data-stu-id="76001-119">This command removes operation-scope policy from API Management.</span></span>

## <span data-ttu-id="76001-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76001-120">PARAMETERS</span></span>

### <span data-ttu-id="76001-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="76001-121">-ApiId</span></span>
<span data-ttu-id="76001-122">Gibt den Bezeichner einer vorhandenen API an.</span><span class="sxs-lookup"><span data-stu-id="76001-122">Specifies the identifier of an existing API.</span></span>
<span data-ttu-id="76001-123">Wenn Sie diesen Parameter angeben, entfernt das Cmdlet die API-Bereichsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="76001-123">If you specify this parameter, the cmdlet removes the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveApiLevel, RemoveOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76001-124">-Context</span><span class="sxs-lookup"><span data-stu-id="76001-124">-Context</span></span>
<span data-ttu-id="76001-125">Gibt die Instanz des **"PsApiManagementContext"-Objekts** an.</span><span class="sxs-lookup"><span data-stu-id="76001-125">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="76001-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76001-126">-DefaultProfile</span></span>
<span data-ttu-id="76001-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="76001-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76001-128">-OperationId</span><span class="sxs-lookup"><span data-stu-id="76001-128">-OperationId</span></span>
<span data-ttu-id="76001-129">Gibt den Bezeichner eines vorhandenen Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="76001-129">Specifies the identifier of an existing operation.</span></span>
<span data-ttu-id="76001-130">Wenn Sie diesen Parameter mit dem Parameter *"ApiId"* angeben, entfernt dieses Cmdlet die Richtlinie für den Vorgangsbereich.</span><span class="sxs-lookup"><span data-stu-id="76001-130">If you specify this parameter with the *ApiId* parameter, this cmdlet removes the operation-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76001-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76001-131">-PassThru</span></span>
<span data-ttu-id="76001-132">Gibt an, dass dieses Cmdlet den Wert "$True" zurückgibt, wenn es erfolgreich ist, oder den Wert "$False" zurück.</span><span class="sxs-lookup"><span data-stu-id="76001-132">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="76001-133">-ProductId</span><span class="sxs-lookup"><span data-stu-id="76001-133">-ProductId</span></span>
<span data-ttu-id="76001-134">Gibt den Bezeichner des vorhandenen Produkts an.</span><span class="sxs-lookup"><span data-stu-id="76001-134">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="76001-135">Wenn Sie diesen Parameter angeben, entfernt das Cmdlet die Richtlinie für den Produktbereich.</span><span class="sxs-lookup"><span data-stu-id="76001-135">If you specify this parameter, the cmdlet removes the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveProductLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76001-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76001-136">-Confirm</span></span>
<span data-ttu-id="76001-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="76001-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76001-138">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="76001-138">-WhatIf</span></span>
<span data-ttu-id="76001-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="76001-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76001-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="76001-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76001-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76001-141">CommonParameters</span></span>
<span data-ttu-id="76001-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76001-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76001-143">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76001-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76001-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="76001-144">INPUTS</span></span>

### <span data-ttu-id="76001-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="76001-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="76001-146">System.String</span><span class="sxs-lookup"><span data-stu-id="76001-146">System.String</span></span>

### <span data-ttu-id="76001-147">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="76001-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="76001-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="76001-148">OUTPUTS</span></span>

### <span data-ttu-id="76001-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="76001-149">System.Boolean</span></span>

## <span data-ttu-id="76001-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="76001-150">NOTES</span></span>

## <span data-ttu-id="76001-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="76001-151">RELATED LINKS</span></span>

[<span data-ttu-id="76001-152">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="76001-152">Get-AzApiManagementPolicy</span></span>](./Get-AzApiManagementPolicy.md)

[<span data-ttu-id="76001-153">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="76001-153">Set-AzApiManagementPolicy</span></span>](./Set-AzApiManagementPolicy.md)


