---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementPolicy.md
ms.openlocfilehash: dbabc98a8221cc2b870368b2b9cdd55e81280863
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940651"
---
# <span data-ttu-id="a1df0-101">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a1df0-101">Get-AzApiManagementPolicy</span></span>

## <span data-ttu-id="a1df0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1df0-102">SYNOPSIS</span></span>
<span data-ttu-id="a1df0-103">Ruft die angegebene Bereichsrichtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="a1df0-103">Gets the specified scope policy.</span></span>

## <span data-ttu-id="a1df0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a1df0-104">SYNTAX</span></span>

### <span data-ttu-id="a1df0-105">GetTenantLevel (Standard)</span><span class="sxs-lookup"><span data-stu-id="a1df0-105">GetTenantLevel (Default)</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1df0-106">GetProductLevel</span><span class="sxs-lookup"><span data-stu-id="a1df0-106">GetProductLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a1df0-107">GetApiLevel</span><span class="sxs-lookup"><span data-stu-id="a1df0-107">GetApiLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1df0-108">GetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="a1df0-108">GetOperationLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] -OperationId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1df0-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a1df0-109">DESCRIPTION</span></span>
<span data-ttu-id="a1df0-110">Das **Get-AzApiManagementPolicy-Cmdlet** ruft die angegebene Bereichsrichtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="a1df0-110">The **Get-AzApiManagementPolicy** cmdlet gets the specified scope policy.</span></span>

## <span data-ttu-id="a1df0-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a1df0-111">EXAMPLES</span></span>

### <span data-ttu-id="a1df0-112">Beispiel 1: Erhalten der Richtlinie auf Mandantenebene</span><span class="sxs-lookup"><span data-stu-id="a1df0-112">Example 1: Get the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="a1df0-113">Dieser Befehl ruft die Richtlinie auf Mandantenebene ab und speichert sie in einer Datei namens tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="a1df0-113">This command gets tenant level policy and saves it to a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="a1df0-114">Beispiel 2: Erhalten der Richtlinie für den Produktbereich</span><span class="sxs-lookup"><span data-stu-id="a1df0-114">Example 2: Get the product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="a1df0-115">Dieser Befehl ruft eine Richtlinie für den Produktbereich ab.</span><span class="sxs-lookup"><span data-stu-id="a1df0-115">This command gets product-scope policy</span></span>

### <span data-ttu-id="a1df0-116">Beispiel 3: Abrufen der API-Scope-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="a1df0-116">Example 3: Get the API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="a1df0-117">Dieser Befehl ruft die API-Scope-Richtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="a1df0-117">This command gets API-scope policy.</span></span>

### <span data-ttu-id="a1df0-118">Beispiel 4: Erhalten der Richtlinie für den Vorgangsbereich</span><span class="sxs-lookup"><span data-stu-id="a1df0-118">Example 4: Get the operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="a1df0-119">Dieser Befehl ruft die Richtlinie für den Vorgangsbereich ab.</span><span class="sxs-lookup"><span data-stu-id="a1df0-119">This command gets the operation-scope policy.</span></span>

### <span data-ttu-id="a1df0-120">Beispiel 5: Herunterladen der Richtlinie für den Mandantenbereich im RawXml-Format</span><span class="sxs-lookup"><span data-stu-id="a1df0-120">Example 5: Get the Tenant scope policy in RawXml format</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS c:\> Get-AzApiManagementPolicy -Context $apimContext -Format rawxml

<policies>
        <inbound>
                <set-header name="correlationid" exists-action="skip">
                        <value>@{
                var guidBinary = new byte[16];
                Array.Copy(Guid.NewGuid().ToByteArray(), 0, guidBinary, 0, 10);
                long time = DateTime.Now.Ticks;
                byte[] bytes = new byte[6];
                unchecked
                {
                       bytes[5] = (byte)(time >> 40);
                       bytes[4] = (byte)(time >> 32);
                       bytes[3] = (byte)(time >> 24);
                       bytes[2] = (byte)(time >> 16);
                       bytes[1] = (byte)(time >> 8);
                       bytes[0] = (byte)(time);
                }
                Array.Copy(bytes, 0, guidBinary, 10, 6);
                return new Guid(guidBinary).ToString();
            }
            </value>
                </set-header>
        </inbound>
        <backend>
                <forward-request />
        </backend>
        <outbound />
        <on-error />
</policies>
```

<span data-ttu-id="a1df0-121">Dieser Befehl ruft die Richtlinie für den Mandantenbereich im Nicht-Xml-Escapeformat ab.</span><span class="sxs-lookup"><span data-stu-id="a1df0-121">This command gets the tenant-scope policy in Non-Xml escaped format.</span></span>

## <span data-ttu-id="a1df0-122">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a1df0-122">PARAMETERS</span></span>

### <span data-ttu-id="a1df0-123">-ApiId</span><span class="sxs-lookup"><span data-stu-id="a1df0-123">-ApiId</span></span>
<span data-ttu-id="a1df0-124">Gibt den Bezeichner der vorhandenen API an.</span><span class="sxs-lookup"><span data-stu-id="a1df0-124">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="a1df0-125">Wenn Sie diesen Parameter angeben, gibt das Cmdlet die API-Scope-Richtlinie zurück.</span><span class="sxs-lookup"><span data-stu-id="a1df0-125">If you specify this parameter the cmdlet returns the API-scope policy.</span></span>

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

### <span data-ttu-id="a1df0-126">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="a1df0-126">-ApiRevision</span></span>
<span data-ttu-id="a1df0-127">Bezeichner der API-Überarbeitung.</span><span class="sxs-lookup"><span data-stu-id="a1df0-127">Identifier of API Revision.</span></span> <span data-ttu-id="a1df0-128">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="a1df0-128">This parameter is optional.</span></span> <span data-ttu-id="a1df0-129">Wenn nicht angegeben, wird die Richtlinie aus der aktuell aktiven Api-Überarbeitung abgerufen.</span><span class="sxs-lookup"><span data-stu-id="a1df0-129">If not specified, the policy will be retrieved from the currently active api revision.</span></span>

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

### <span data-ttu-id="a1df0-130">-Context</span><span class="sxs-lookup"><span data-stu-id="a1df0-130">-Context</span></span>
<span data-ttu-id="a1df0-131">Gibt eine Instanz von **PsApiManagementContext an.**</span><span class="sxs-lookup"><span data-stu-id="a1df0-131">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="a1df0-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1df0-132">-DefaultProfile</span></span>
<span data-ttu-id="a1df0-133">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a1df0-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1df0-134">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="a1df0-134">-Force</span></span>
<span data-ttu-id="a1df0-135">ps_force</span><span class="sxs-lookup"><span data-stu-id="a1df0-135">ps_force</span></span>

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

### <span data-ttu-id="a1df0-136">-Format</span><span class="sxs-lookup"><span data-stu-id="a1df0-136">-Format</span></span>
<span data-ttu-id="a1df0-137">Gibt das Format der API-Verwaltungsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="a1df0-137">Specifies the format of the API management policy.</span></span>
<span data-ttu-id="a1df0-138">Der Standardwert für diesen Parameter ist "xml".</span><span class="sxs-lookup"><span data-stu-id="a1df0-138">The default value for this parameter is "xml".</span></span>

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

### <span data-ttu-id="a1df0-139">-OperationId</span><span class="sxs-lookup"><span data-stu-id="a1df0-139">-OperationId</span></span>
<span data-ttu-id="a1df0-140">Gibt den Bezeichner des vorhandenen API-Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="a1df0-140">Specifies the identifier of the existing API operation.</span></span>
<span data-ttu-id="a1df0-141">Wenn Sie diesen Parameter mit *ApiId angeben,* gibt das Cmdlet eine Richtlinie für den Vorgangsbereich zurück.</span><span class="sxs-lookup"><span data-stu-id="a1df0-141">If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.</span></span>

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

### <span data-ttu-id="a1df0-142">-ProductId</span><span class="sxs-lookup"><span data-stu-id="a1df0-142">-ProductId</span></span>
<span data-ttu-id="a1df0-143">Gibt den Bezeichner eines vorhandenen Produkts an.</span><span class="sxs-lookup"><span data-stu-id="a1df0-143">Specifies the identifier of an existing product.</span></span>
<span data-ttu-id="a1df0-144">Wenn Sie diesen Parameter angeben, gibt das Cmdlet die Richtlinie für den Produktbereich zurück.</span><span class="sxs-lookup"><span data-stu-id="a1df0-144">If you specify this parameter the cmdlet returns the product-scope policy.</span></span>

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

### <span data-ttu-id="a1df0-145">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="a1df0-145">-SaveAs</span></span>
<span data-ttu-id="a1df0-146">Gibt den Dateipfad an, in dem das Ergebnis gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a1df0-146">Specifies the file path to save the result to.</span></span>
<span data-ttu-id="a1df0-147">Wenn Sie diesen Parameter nicht angeben, wird das Ergebnis als Zierde pipelineiert.</span><span class="sxs-lookup"><span data-stu-id="a1df0-147">If you do not specify this parameter the result is pipelined as a sting.</span></span>

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

### <span data-ttu-id="a1df0-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a1df0-148">-Confirm</span></span>
<span data-ttu-id="a1df0-149">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a1df0-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1df0-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1df0-150">-WhatIf</span></span>
<span data-ttu-id="a1df0-151">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a1df0-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a1df0-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a1df0-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1df0-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1df0-153">CommonParameters</span></span>
<span data-ttu-id="a1df0-154">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1df0-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1df0-155">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1df0-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1df0-156">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a1df0-156">INPUTS</span></span>

### <span data-ttu-id="a1df0-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a1df0-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a1df0-158">System.String</span><span class="sxs-lookup"><span data-stu-id="a1df0-158">System.String</span></span>

### <span data-ttu-id="a1df0-159">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a1df0-159">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a1df0-160">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a1df0-160">OUTPUTS</span></span>

### <span data-ttu-id="a1df0-161">System.String</span><span class="sxs-lookup"><span data-stu-id="a1df0-161">System.String</span></span>

## <span data-ttu-id="a1df0-162">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a1df0-162">NOTES</span></span>

## <span data-ttu-id="a1df0-163">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a1df0-163">RELATED LINKS</span></span>

[<span data-ttu-id="a1df0-164">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a1df0-164">Remove-AzApiManagementPolicy</span></span>](./Remove-AzApiManagementPolicy.md)

[<span data-ttu-id="a1df0-165">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a1df0-165">Set-AzApiManagementPolicy</span></span>](./Set-AzApiManagementPolicy.md)


