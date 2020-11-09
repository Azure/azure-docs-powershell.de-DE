---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementPolicy.md
ms.openlocfilehash: 24af453d6605bc42e8c504cef26d368369753d9d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302846"
---
# <span data-ttu-id="f1897-101">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f1897-101">Get-AzApiManagementPolicy</span></span>

## <span data-ttu-id="f1897-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f1897-102">SYNOPSIS</span></span>
<span data-ttu-id="f1897-103">Ruft die angegebene Bereichs Richtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="f1897-103">Gets the specified scope policy.</span></span>

## <span data-ttu-id="f1897-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1897-104">SYNTAX</span></span>

### <span data-ttu-id="f1897-105">GetTenantLevel (Standard)</span><span class="sxs-lookup"><span data-stu-id="f1897-105">GetTenantLevel (Default)</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1897-106">GetProductLevel</span><span class="sxs-lookup"><span data-stu-id="f1897-106">GetProductLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f1897-107">GetApiLevel</span><span class="sxs-lookup"><span data-stu-id="f1897-107">GetApiLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1897-108">GetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="f1897-108">GetOperationLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] -OperationId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1897-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f1897-109">DESCRIPTION</span></span>
<span data-ttu-id="f1897-110">Das Cmdlet " **Get-AzApiManagementPolicy** " Ruft die angegebene Bereichs Richtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="f1897-110">The **Get-AzApiManagementPolicy** cmdlet gets the specified scope policy.</span></span>

## <span data-ttu-id="f1897-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f1897-111">EXAMPLES</span></span>

### <span data-ttu-id="f1897-112">Beispiel 1: Abrufen der Richtlinie für Mandantenebene</span><span class="sxs-lookup"><span data-stu-id="f1897-112">Example 1: Get the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="f1897-113">Dieser Befehl ruft die Richtlinie für Mandantenebene ab und speichert Sie in einer Datei mit dem Namen tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="f1897-113">This command gets tenant level policy and saves it to a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="f1897-114">Beispiel 2: Abrufen der Richtlinie für den Produktbereich</span><span class="sxs-lookup"><span data-stu-id="f1897-114">Example 2: Get the product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="f1897-115">Dieser Befehl ruft die Richtlinie für den Produktbereich ab</span><span class="sxs-lookup"><span data-stu-id="f1897-115">This command gets product-scope policy</span></span>

### <span data-ttu-id="f1897-116">Beispiel 3: Abrufen der API-Bereichs Richtlinie</span><span class="sxs-lookup"><span data-stu-id="f1897-116">Example 3: Get the API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="f1897-117">Dieser Befehl ruft eine Richtlinie für den API-Bereich ab.</span><span class="sxs-lookup"><span data-stu-id="f1897-117">This command gets API-scope policy.</span></span>

### <span data-ttu-id="f1897-118">Beispiel 4: Abrufen der Richtlinie für den Vorgangsbereich</span><span class="sxs-lookup"><span data-stu-id="f1897-118">Example 4: Get the operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="f1897-119">Mit diesem Befehl wird die Richtlinie für den Vorgangsbereich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="f1897-119">This command gets the operation-scope policy.</span></span>

### <span data-ttu-id="f1897-120">Beispiel 5: Abrufen der Mandanten Bereichs Richtlinie im RawXml-Format</span><span class="sxs-lookup"><span data-stu-id="f1897-120">Example 5: Get the Tenant scope policy in RawXml format</span></span>
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

<span data-ttu-id="f1897-121">Dieser Befehl ruft die Richtlinie für den MANDANTENBEREICH im nicht-XML-Escapezeichen-Format ab.</span><span class="sxs-lookup"><span data-stu-id="f1897-121">This command gets the tenant-scope policy in Non-Xml escaped format.</span></span>

## <span data-ttu-id="f1897-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1897-122">PARAMETERS</span></span>

### <span data-ttu-id="f1897-123">-ApiId</span><span class="sxs-lookup"><span data-stu-id="f1897-123">-ApiId</span></span>
<span data-ttu-id="f1897-124">Gibt den Bezeichner der vorhandenen API an.</span><span class="sxs-lookup"><span data-stu-id="f1897-124">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="f1897-125">Wenn Sie diesen Parameter angeben, gibt das Cmdlet die Richtlinie für den API-Bereich zurück.</span><span class="sxs-lookup"><span data-stu-id="f1897-125">If you specify this parameter the cmdlet returns the API-scope policy.</span></span>

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

### <span data-ttu-id="f1897-126">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="f1897-126">-ApiRevision</span></span>
<span data-ttu-id="f1897-127">Bezeichner der API-Überarbeitung.</span><span class="sxs-lookup"><span data-stu-id="f1897-127">Identifier of API Revision.</span></span> <span data-ttu-id="f1897-128">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="f1897-128">This parameter is optional.</span></span> <span data-ttu-id="f1897-129">Wenn Sie nicht angegeben wird, wird die Richtlinie aus der aktuell aktiven API-Revision abgerufen.</span><span class="sxs-lookup"><span data-stu-id="f1897-129">If not specified, the policy will be retrieved from the currently active api revision.</span></span>

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

### <span data-ttu-id="f1897-130">-Context</span><span class="sxs-lookup"><span data-stu-id="f1897-130">-Context</span></span>
<span data-ttu-id="f1897-131">Gibt eine Instanz von **PsApiManagementContext** an.</span><span class="sxs-lookup"><span data-stu-id="f1897-131">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="f1897-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1897-132">-DefaultProfile</span></span>
<span data-ttu-id="f1897-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f1897-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1897-134">-Force</span><span class="sxs-lookup"><span data-stu-id="f1897-134">-Force</span></span>
<span data-ttu-id="f1897-135">ps_force</span><span class="sxs-lookup"><span data-stu-id="f1897-135">ps_force</span></span>

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

### <span data-ttu-id="f1897-136">-Format</span><span class="sxs-lookup"><span data-stu-id="f1897-136">-Format</span></span>
<span data-ttu-id="f1897-137">Gibt das Format der API-Verwaltungsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="f1897-137">Specifies the format of the API management policy.</span></span>
<span data-ttu-id="f1897-138">Der Standardwert für diesen Parameter ist "XML".</span><span class="sxs-lookup"><span data-stu-id="f1897-138">The default value for this parameter is "xml".</span></span>

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

### <span data-ttu-id="f1897-139">-Vorgangs-Nr</span><span class="sxs-lookup"><span data-stu-id="f1897-139">-OperationId</span></span>
<span data-ttu-id="f1897-140">Gibt den Bezeichner des vorhandenen API-Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="f1897-140">Specifies the identifier of the existing API operation.</span></span>
<span data-ttu-id="f1897-141">Wenn Sie diesen Parameter mit *ApiId* angeben, gibt das Cmdlet die Richtlinie für den Vorgangsbereich zurück.</span><span class="sxs-lookup"><span data-stu-id="f1897-141">If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.</span></span>

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

### <span data-ttu-id="f1897-142">-ProductID</span><span class="sxs-lookup"><span data-stu-id="f1897-142">-ProductId</span></span>
<span data-ttu-id="f1897-143">Gibt den Bezeichner eines vorhandenen Produkts an.</span><span class="sxs-lookup"><span data-stu-id="f1897-143">Specifies the identifier of an existing product.</span></span>
<span data-ttu-id="f1897-144">Wenn Sie diesen Parameter angeben, gibt das Cmdlet die Richtlinie für den Produktbereich zurück.</span><span class="sxs-lookup"><span data-stu-id="f1897-144">If you specify this parameter the cmdlet returns the product-scope policy.</span></span>

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

### <span data-ttu-id="f1897-145">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="f1897-145">-SaveAs</span></span>
<span data-ttu-id="f1897-146">Gibt den Dateipfad an, in dem das Ergebnis gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f1897-146">Specifies the file path to save the result to.</span></span>
<span data-ttu-id="f1897-147">Wenn Sie diesen Parameter nicht angeben, wird das Ergebnis als Stich Pipeline durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="f1897-147">If you do not specify this parameter the result is pipelined as a sting.</span></span>

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

### <span data-ttu-id="f1897-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f1897-148">-Confirm</span></span>
<span data-ttu-id="f1897-149">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f1897-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1897-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1897-150">-WhatIf</span></span>
<span data-ttu-id="f1897-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f1897-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f1897-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f1897-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1897-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1897-153">CommonParameters</span></span>
<span data-ttu-id="f1897-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1897-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1897-155">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1897-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1897-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f1897-156">INPUTS</span></span>

### <span data-ttu-id="f1897-157">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f1897-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f1897-158">System. String</span><span class="sxs-lookup"><span data-stu-id="f1897-158">System.String</span></span>

### <span data-ttu-id="f1897-159">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="f1897-159">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f1897-160">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f1897-160">OUTPUTS</span></span>

### <span data-ttu-id="f1897-161">System. String</span><span class="sxs-lookup"><span data-stu-id="f1897-161">System.String</span></span>

## <span data-ttu-id="f1897-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="f1897-162">NOTES</span></span>

## <span data-ttu-id="f1897-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f1897-163">RELATED LINKS</span></span>

[<span data-ttu-id="f1897-164">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f1897-164">Remove-AzApiManagementPolicy</span></span>](./Remove-AzApiManagementPolicy.md)

[<span data-ttu-id="f1897-165">Satz-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f1897-165">Set-AzApiManagementPolicy</span></span>](./Set-AzApiManagementPolicy.md)


