---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementPolicy.md
ms.openlocfilehash: 0da4e2168ccc7f5a62aa4265af3b7823dd4cb050
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650380"
---
# <span data-ttu-id="6671e-101">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6671e-101">Get-AzApiManagementPolicy</span></span>

## <span data-ttu-id="6671e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6671e-102">SYNOPSIS</span></span>
<span data-ttu-id="6671e-103">Ruft die angegebene Bereichs Richtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="6671e-103">Gets the specified scope policy.</span></span>

## <span data-ttu-id="6671e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6671e-104">SYNTAX</span></span>

### <span data-ttu-id="6671e-105">GetTenantLevel (Standard)</span><span class="sxs-lookup"><span data-stu-id="6671e-105">GetTenantLevel (Default)</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6671e-106">GetProductLevel</span><span class="sxs-lookup"><span data-stu-id="6671e-106">GetProductLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6671e-107">GetApiLevel</span><span class="sxs-lookup"><span data-stu-id="6671e-107">GetApiLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6671e-108">GetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="6671e-108">GetOperationLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] -OperationId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6671e-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6671e-109">DESCRIPTION</span></span>
<span data-ttu-id="6671e-110">Das Cmdlet " **Get-AzApiManagementPolicy** " Ruft die angegebene Bereichs Richtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="6671e-110">The **Get-AzApiManagementPolicy** cmdlet gets the specified scope policy.</span></span>

## <span data-ttu-id="6671e-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6671e-111">EXAMPLES</span></span>

### <span data-ttu-id="6671e-112">Beispiel 1: Abrufen der Richtlinie für Mandantenebene</span><span class="sxs-lookup"><span data-stu-id="6671e-112">Example 1: Get the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="6671e-113">Dieser Befehl ruft die Richtlinie für Mandantenebene ab und speichert Sie in einer Datei mit dem Namen tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="6671e-113">This command gets tenant level policy and saves it to a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="6671e-114">Beispiel 2: Abrufen der Richtlinie für den Produktbereich</span><span class="sxs-lookup"><span data-stu-id="6671e-114">Example 2: Get the product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="6671e-115">Dieser Befehl ruft die Richtlinie für den Produktbereich ab</span><span class="sxs-lookup"><span data-stu-id="6671e-115">This command gets product-scope policy</span></span>

### <span data-ttu-id="6671e-116">Beispiel 3: Abrufen der API-Bereichs Richtlinie</span><span class="sxs-lookup"><span data-stu-id="6671e-116">Example 3: Get the API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="6671e-117">Dieser Befehl ruft eine Richtlinie für den API-Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="6671e-117">This command gets API-scope policy.</span></span>

### <span data-ttu-id="6671e-118">Beispiel 4: Abrufen der Richtlinie für den Vorgangsbereich</span><span class="sxs-lookup"><span data-stu-id="6671e-118">Example 4: Get the operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="6671e-119">Mit diesem Befehl wird die Richtlinie für den Vorgangsbereich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="6671e-119">This command gets the operation-scope policy.</span></span>

## <span data-ttu-id="6671e-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="6671e-120">PARAMETERS</span></span>

### <span data-ttu-id="6671e-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="6671e-121">-ApiId</span></span>
<span data-ttu-id="6671e-122">Gibt den Bezeichner der vorhandenen API an.</span><span class="sxs-lookup"><span data-stu-id="6671e-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="6671e-123">Wenn Sie diesen Parameter angeben, gibt das Cmdlet die Richtlinie für den API-Bereich zurück.</span><span class="sxs-lookup"><span data-stu-id="6671e-123">If you specify this parameter the cmdlet returns the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6671e-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="6671e-124">-ApiRevision</span></span>
<span data-ttu-id="6671e-125">Bezeichner der API-Überarbeitung.</span><span class="sxs-lookup"><span data-stu-id="6671e-125">Identifier of API Revision.</span></span> <span data-ttu-id="6671e-126">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="6671e-126">This parameter is optional.</span></span> <span data-ttu-id="6671e-127">Wenn Sie nicht angegeben wird, wird die Richtlinie aus der aktuell aktiven API-Revision abgerufen.</span><span class="sxs-lookup"><span data-stu-id="6671e-127">If not specified, the policy will be retrieved from the currently active api revision.</span></span>

```yaml
Type: System.String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6671e-128">-Context</span><span class="sxs-lookup"><span data-stu-id="6671e-128">-Context</span></span>
<span data-ttu-id="6671e-129">Gibt eine Instanz von **PsApiManagementContext** an.</span><span class="sxs-lookup"><span data-stu-id="6671e-129">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="6671e-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6671e-130">-DefaultProfile</span></span>
<span data-ttu-id="6671e-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6671e-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6671e-132">-Force</span><span class="sxs-lookup"><span data-stu-id="6671e-132">-Force</span></span>
<span data-ttu-id="6671e-133">ps_force</span><span class="sxs-lookup"><span data-stu-id="6671e-133">ps_force</span></span>

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

### <span data-ttu-id="6671e-134">-Format</span><span class="sxs-lookup"><span data-stu-id="6671e-134">-Format</span></span>
<span data-ttu-id="6671e-135">Gibt das Format der API-Verwaltungsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="6671e-135">Specifies the format of the API management policy.</span></span>
<span data-ttu-id="6671e-136">Der Standardwert für diesen Parameter ist "application/vnd. ms-AZ-APIM. Policy + XML".</span><span class="sxs-lookup"><span data-stu-id="6671e-136">The default value for this parameter is "application/vnd.ms-az-apim.policy+xml".</span></span>

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

### <span data-ttu-id="6671e-137">-Vorgangs-Nr</span><span class="sxs-lookup"><span data-stu-id="6671e-137">-OperationId</span></span>
<span data-ttu-id="6671e-138">Gibt den Bezeichner des vorhandenen API-Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="6671e-138">Specifies the identifier of the existing API operation.</span></span>
<span data-ttu-id="6671e-139">Wenn Sie diesen Parameter mit *ApiId* angeben, gibt das Cmdlet die Richtlinie für den Vorgangsbereich zurück.</span><span class="sxs-lookup"><span data-stu-id="6671e-139">If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6671e-140">-ProductID</span><span class="sxs-lookup"><span data-stu-id="6671e-140">-ProductId</span></span>
<span data-ttu-id="6671e-141">Gibt den Bezeichner eines vorhandenen Produkts an.</span><span class="sxs-lookup"><span data-stu-id="6671e-141">Specifies the identifier of an existing product.</span></span>
<span data-ttu-id="6671e-142">Wenn Sie diesen Parameter angeben, gibt das Cmdlet die Richtlinie für den Produktbereich zurück.</span><span class="sxs-lookup"><span data-stu-id="6671e-142">If you specify this parameter the cmdlet returns the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetProductLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6671e-143">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="6671e-143">-SaveAs</span></span>
<span data-ttu-id="6671e-144">Gibt den Dateipfad an, in dem das Ergebnis gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6671e-144">Specifies the file path to save the result to.</span></span>
<span data-ttu-id="6671e-145">Wenn Sie diesen Parameter nicht angeben, wird das Ergebnis als Stich Pipeline durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="6671e-145">If you do not specify this parameter the result is pipelined as a sting.</span></span>

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

### <span data-ttu-id="6671e-146">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6671e-146">-Confirm</span></span>
<span data-ttu-id="6671e-147">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6671e-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6671e-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6671e-148">-WhatIf</span></span>
<span data-ttu-id="6671e-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6671e-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6671e-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6671e-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6671e-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6671e-151">CommonParameters</span></span>
<span data-ttu-id="6671e-152">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6671e-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6671e-153">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6671e-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6671e-154">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6671e-154">INPUTS</span></span>

### <span data-ttu-id="6671e-155">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6671e-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6671e-156">System. String</span><span class="sxs-lookup"><span data-stu-id="6671e-156">System.String</span></span>

### <span data-ttu-id="6671e-157">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="6671e-157">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6671e-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6671e-158">OUTPUTS</span></span>

### <span data-ttu-id="6671e-159">System. String</span><span class="sxs-lookup"><span data-stu-id="6671e-159">System.String</span></span>

## <span data-ttu-id="6671e-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="6671e-160">NOTES</span></span>

## <span data-ttu-id="6671e-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6671e-161">RELATED LINKS</span></span>

[<span data-ttu-id="6671e-162">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6671e-162">Remove-AzApiManagementPolicy</span></span>](./Remove-AzApiManagementPolicy.md)

[<span data-ttu-id="6671e-163">Satz-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6671e-163">Set-AzApiManagementPolicy</span></span>](./Set-AzApiManagementPolicy.md)


