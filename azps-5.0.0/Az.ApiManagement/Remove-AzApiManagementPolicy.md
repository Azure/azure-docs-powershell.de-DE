---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 466AFB8C-C272-4A4F-8E13-A4DBD6EE3A85
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementPolicy.md
ms.openlocfilehash: a51bd7aed5ca8793a921c2cde7729c5280df44b5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303238"
---
# <span data-ttu-id="0acb5-101">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0acb5-101">Remove-AzApiManagementPolicy</span></span>

## <span data-ttu-id="0acb5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0acb5-102">SYNOPSIS</span></span>
<span data-ttu-id="0acb5-103">Entfernt die API-Verwaltungsrichtlinie aus einem angegebenen Bereich.</span><span class="sxs-lookup"><span data-stu-id="0acb5-103">Removes the API Management policy from a specified scope.</span></span>

## <span data-ttu-id="0acb5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0acb5-104">SYNTAX</span></span>

### <span data-ttu-id="0acb5-105">RemoveTenantLevel (Standard)</span><span class="sxs-lookup"><span data-stu-id="0acb5-105">RemoveTenantLevel (Default)</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0acb5-106">RemoveProductLevel</span><span class="sxs-lookup"><span data-stu-id="0acb5-106">RemoveProductLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ProductId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0acb5-107">RemoveApiLevel</span><span class="sxs-lookup"><span data-stu-id="0acb5-107">RemoveApiLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0acb5-108">RemoveOperationLevel</span><span class="sxs-lookup"><span data-stu-id="0acb5-108">RemoveOperationLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0acb5-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0acb5-109">DESCRIPTION</span></span>
<span data-ttu-id="0acb5-110">Das Cmdlet **Remove-AzApiManagementPolicy** entfernt die API-Verwaltungsrichtlinie aus dem angegebenen Bereich.</span><span class="sxs-lookup"><span data-stu-id="0acb5-110">The **Remove-AzApiManagementPolicy** cmdlet removes the API Management policy from specified scope.</span></span>

## <span data-ttu-id="0acb5-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0acb5-111">EXAMPLES</span></span>

### <span data-ttu-id="0acb5-112">Beispiel 1: Entfernen der Richtlinie für Mandantenebene</span><span class="sxs-lookup"><span data-stu-id="0acb5-112">Example 1: Remove the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext
```

<span data-ttu-id="0acb5-113">Dieser Befehl entfernt die Richtlinie für Mandantenebene aus der API-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="0acb5-113">This command removes tenant level policy from API Management.</span></span>

### <span data-ttu-id="0acb5-114">Beispiel 2: Entfernen der Richtlinie für den Produktbereich</span><span class="sxs-lookup"><span data-stu-id="0acb5-114">Example 2: Remove the product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="0acb5-115">Dieser Befehl entfernt die Richtlinie für den Produktbereich aus der API-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="0acb5-115">This command removes product-scope policy from API Management.</span></span>

### <span data-ttu-id="0acb5-116">Beispiel 3: Entfernen der API-Bereichs Richtlinie</span><span class="sxs-lookup"><span data-stu-id="0acb5-116">Example 3: Remove the API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="0acb5-117">Dieser Befehl entfernt API-Bereichs Richtlinien aus der API-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="0acb5-117">This command removes API-scope policy from API Management.</span></span>

### <span data-ttu-id="0acb5-118">Beispiel 4: Entfernen der Richtlinie für den Vorgangsbereich</span><span class="sxs-lookup"><span data-stu-id="0acb5-118">Example 4: Remove the operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="0acb5-119">Dieser Befehl entfernt die Richtlinie für den Vorgangsbereich aus der API-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="0acb5-119">This command removes operation-scope policy from API Management.</span></span>

## <span data-ttu-id="0acb5-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="0acb5-120">PARAMETERS</span></span>

### <span data-ttu-id="0acb5-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="0acb5-121">-ApiId</span></span>
<span data-ttu-id="0acb5-122">Gibt den Bezeichner einer vorhandenen API an.</span><span class="sxs-lookup"><span data-stu-id="0acb5-122">Specifies the identifier of an existing API.</span></span>
<span data-ttu-id="0acb5-123">Wenn Sie diesen Parameter angeben, entfernt das Cmdlet die Richtlinie für den API-Bereich.</span><span class="sxs-lookup"><span data-stu-id="0acb5-123">If you specify this parameter, the cmdlet removes the API-scope policy.</span></span>

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

### <span data-ttu-id="0acb5-124">-Context</span><span class="sxs-lookup"><span data-stu-id="0acb5-124">-Context</span></span>
<span data-ttu-id="0acb5-125">Gibt die Instanz des **PsApiManagementContext** -Objekts an.</span><span class="sxs-lookup"><span data-stu-id="0acb5-125">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0acb5-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0acb5-126">-DefaultProfile</span></span>
<span data-ttu-id="0acb5-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0acb5-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0acb5-128">-Vorgangs-Nr</span><span class="sxs-lookup"><span data-stu-id="0acb5-128">-OperationId</span></span>
<span data-ttu-id="0acb5-129">Gibt den Bezeichner eines vorhandenen Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="0acb5-129">Specifies the identifier of an existing operation.</span></span>
<span data-ttu-id="0acb5-130">Wenn Sie diesen Parameter mit dem *ApiId* -Parameter angeben, entfernt dieses Cmdlet die Richtlinie für den Vorgangsbereich.</span><span class="sxs-lookup"><span data-stu-id="0acb5-130">If you specify this parameter with the *ApiId* parameter, this cmdlet removes the operation-scope policy.</span></span>

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

### <span data-ttu-id="0acb5-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0acb5-131">-PassThru</span></span>
<span data-ttu-id="0acb5-132">Gibt an, dass dieses Cmdlet einen Wert von $true zurückgibt, wenn dies erfolgreich ist, oder einen Wert von $false, andernfalls.</span><span class="sxs-lookup"><span data-stu-id="0acb5-132">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="0acb5-133">-ProductID</span><span class="sxs-lookup"><span data-stu-id="0acb5-133">-ProductId</span></span>
<span data-ttu-id="0acb5-134">Gibt den Bezeichner des vorhandenen Produkts an.</span><span class="sxs-lookup"><span data-stu-id="0acb5-134">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="0acb5-135">Wenn Sie diesen Parameter angeben, entfernt das Cmdlet die Richtlinie für den Produktbereich.</span><span class="sxs-lookup"><span data-stu-id="0acb5-135">If you specify this parameter, the cmdlet removes the product-scope policy.</span></span>

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

### <span data-ttu-id="0acb5-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0acb5-136">-Confirm</span></span>
<span data-ttu-id="0acb5-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0acb5-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0acb5-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0acb5-138">-WhatIf</span></span>
<span data-ttu-id="0acb5-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0acb5-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0acb5-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0acb5-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0acb5-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0acb5-141">CommonParameters</span></span>
<span data-ttu-id="0acb5-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0acb5-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0acb5-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0acb5-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0acb5-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0acb5-144">INPUTS</span></span>

### <span data-ttu-id="0acb5-145">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0acb5-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0acb5-146">System. String</span><span class="sxs-lookup"><span data-stu-id="0acb5-146">System.String</span></span>

### <span data-ttu-id="0acb5-147">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="0acb5-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0acb5-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0acb5-148">OUTPUTS</span></span>

### <span data-ttu-id="0acb5-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0acb5-149">System.Boolean</span></span>

## <span data-ttu-id="0acb5-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="0acb5-150">NOTES</span></span>

## <span data-ttu-id="0acb5-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0acb5-151">RELATED LINKS</span></span>

[<span data-ttu-id="0acb5-152">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0acb5-152">Get-AzApiManagementPolicy</span></span>](./Get-AzApiManagementPolicy.md)

[<span data-ttu-id="0acb5-153">Satz-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0acb5-153">Set-AzApiManagementPolicy</span></span>](./Set-AzApiManagementPolicy.md)


