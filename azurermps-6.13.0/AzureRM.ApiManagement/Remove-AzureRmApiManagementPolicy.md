---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 466AFB8C-C272-4A4F-8E13-A4DBD6EE3A85
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 1066598a9e255cecbf7238208b5f06f74d88511e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482597"
---
# <span data-ttu-id="19ac2-101">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="19ac2-101">Remove-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="19ac2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="19ac2-102">SYNOPSIS</span></span>
<span data-ttu-id="19ac2-103">Entfernt die API-Verwaltungsrichtlinie aus einem angegebenen Bereich.</span><span class="sxs-lookup"><span data-stu-id="19ac2-103">Removes the API Management policy from a specified scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19ac2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="19ac2-104">SYNTAX</span></span>

### <span data-ttu-id="19ac2-105">RemoveTenantLevel (Standard)</span><span class="sxs-lookup"><span data-stu-id="19ac2-105">RemoveTenantLevel (Default)</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19ac2-106">RemoveProductLevel</span><span class="sxs-lookup"><span data-stu-id="19ac2-106">RemoveProductLevel</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ProductId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19ac2-107">RemoveApiLevel</span><span class="sxs-lookup"><span data-stu-id="19ac2-107">RemoveApiLevel</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19ac2-108">RemoveOperationLevel</span><span class="sxs-lookup"><span data-stu-id="19ac2-108">RemoveOperationLevel</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19ac2-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="19ac2-109">DESCRIPTION</span></span>
<span data-ttu-id="19ac2-110">Das Cmdlet **Remove-AzureRmApiManagementPolicy** entfernt die API-Verwaltungsrichtlinie aus dem angegebenen Bereich.</span><span class="sxs-lookup"><span data-stu-id="19ac2-110">The **Remove-AzureRmApiManagementPolicy** cmdlet removes the API Management policy from specified scope.</span></span>

## <span data-ttu-id="19ac2-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="19ac2-111">EXAMPLES</span></span>

### <span data-ttu-id="19ac2-112">Beispiel 1: Entfernen der Richtlinie für Mandantenebene</span><span class="sxs-lookup"><span data-stu-id="19ac2-112">Example 1: Remove the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementPolicy -Context $apimContext
```

<span data-ttu-id="19ac2-113">Dieser Befehl entfernt die Richtlinie für Mandantenebene aus der API-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="19ac2-113">This command removes tenant level policy from API Management.</span></span>

### <span data-ttu-id="19ac2-114">Beispiel 2: Entfernen der Richtlinie für den Produktbereich</span><span class="sxs-lookup"><span data-stu-id="19ac2-114">Example 2: Remove the product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="19ac2-115">Dieser Befehl entfernt die Richtlinie für den Produktbereich aus der API-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="19ac2-115">This command removes product-scope policy from API Management.</span></span>

### <span data-ttu-id="19ac2-116">Beispiel 3: Entfernen der API-Bereichs Richtlinie</span><span class="sxs-lookup"><span data-stu-id="19ac2-116">Example 3: Remove the API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="19ac2-117">Dieser Befehl entfernt API-Bereichs Richtlinien aus der API-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="19ac2-117">This command removes API-scope policy from API Management.</span></span>

### <span data-ttu-id="19ac2-118">Beispiel 4: Entfernen der Richtlinie für den Vorgangsbereich</span><span class="sxs-lookup"><span data-stu-id="19ac2-118">Example 4: Remove the operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="19ac2-119">Dieser Befehl entfernt die Richtlinie für den Vorgangsbereich aus der API-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="19ac2-119">This command removes operation-scope policy from API Management.</span></span>

## <span data-ttu-id="19ac2-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="19ac2-120">PARAMETERS</span></span>

### <span data-ttu-id="19ac2-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="19ac2-121">-ApiId</span></span>
<span data-ttu-id="19ac2-122">Gibt den Bezeichner einer vorhandenen API an.</span><span class="sxs-lookup"><span data-stu-id="19ac2-122">Specifies the identifier of an existing API.</span></span>
<span data-ttu-id="19ac2-123">Wenn Sie diesen Parameter angeben, entfernt das Cmdlet die Richtlinie für den API-Bereich.</span><span class="sxs-lookup"><span data-stu-id="19ac2-123">If you specify this parameter, the cmdlet removes the API-scope policy.</span></span>

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

### <span data-ttu-id="19ac2-124">-Context</span><span class="sxs-lookup"><span data-stu-id="19ac2-124">-Context</span></span>
<span data-ttu-id="19ac2-125">Gibt die Instanz des **PsApiManagementContext** -Objekts an.</span><span class="sxs-lookup"><span data-stu-id="19ac2-125">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="19ac2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19ac2-126">-DefaultProfile</span></span>
<span data-ttu-id="19ac2-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="19ac2-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19ac2-128">-Vorgangs-Nr</span><span class="sxs-lookup"><span data-stu-id="19ac2-128">-OperationId</span></span>
<span data-ttu-id="19ac2-129">Gibt den Bezeichner eines vorhandenen Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="19ac2-129">Specifies the identifier of an existing operation.</span></span>
<span data-ttu-id="19ac2-130">Wenn Sie diesen Parameter mit dem *ApiId* -Parameter angeben, entfernt dieses Cmdlet die Richtlinie für den Vorgangsbereich.</span><span class="sxs-lookup"><span data-stu-id="19ac2-130">If you specify this parameter with the *ApiId* parameter, this cmdlet removes the operation-scope policy.</span></span>

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

### <span data-ttu-id="19ac2-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19ac2-131">-PassThru</span></span>
<span data-ttu-id="19ac2-132">Gibt an, dass dieses Cmdlet einen Wert von $true zurückgibt, wenn dies erfolgreich ist, oder einen Wert von $false, andernfalls.</span><span class="sxs-lookup"><span data-stu-id="19ac2-132">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="19ac2-133">-ProductID</span><span class="sxs-lookup"><span data-stu-id="19ac2-133">-ProductId</span></span>
<span data-ttu-id="19ac2-134">Gibt den Bezeichner des vorhandenen Produkts an.</span><span class="sxs-lookup"><span data-stu-id="19ac2-134">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="19ac2-135">Wenn Sie diesen Parameter angeben, entfernt das Cmdlet die Richtlinie für den Produktbereich.</span><span class="sxs-lookup"><span data-stu-id="19ac2-135">If you specify this parameter, the cmdlet removes the product-scope policy.</span></span>

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

### <span data-ttu-id="19ac2-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="19ac2-136">-Confirm</span></span>
<span data-ttu-id="19ac2-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="19ac2-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19ac2-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19ac2-138">-WhatIf</span></span>
<span data-ttu-id="19ac2-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="19ac2-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19ac2-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="19ac2-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19ac2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19ac2-141">CommonParameters</span></span>
<span data-ttu-id="19ac2-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19ac2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19ac2-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19ac2-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19ac2-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="19ac2-144">INPUTS</span></span>

### <span data-ttu-id="19ac2-145">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="19ac2-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="19ac2-146">System. String</span><span class="sxs-lookup"><span data-stu-id="19ac2-146">System.String</span></span>

### <span data-ttu-id="19ac2-147">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="19ac2-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="19ac2-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="19ac2-148">OUTPUTS</span></span>

### <span data-ttu-id="19ac2-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="19ac2-149">System.Boolean</span></span>

## <span data-ttu-id="19ac2-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="19ac2-150">NOTES</span></span>

## <span data-ttu-id="19ac2-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="19ac2-151">RELATED LINKS</span></span>

[<span data-ttu-id="19ac2-152">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="19ac2-152">Get-AzureRmApiManagementPolicy</span></span>](./Get-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="19ac2-153">Satz-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="19ac2-153">Set-AzureRmApiManagementPolicy</span></span>](./Set-AzureRmApiManagementPolicy.md)


