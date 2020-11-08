---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 67EE6EFB-3297-4D21-A6EC-B03F5FE82F84
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOperation.md
ms.openlocfilehash: 92848cb2daa0976d8206549fc16d1a6f039199a6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004384"
---
# <span data-ttu-id="ac672-101">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ac672-101">Set-AzApiManagementOperation</span></span>

## <span data-ttu-id="ac672-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ac672-102">SYNOPSIS</span></span>
<span data-ttu-id="ac672-103">Legt die Details des API-Vorgangs fest.</span><span class="sxs-lookup"><span data-stu-id="ac672-103">Sets API operation details.</span></span>

## <span data-ttu-id="ac672-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac672-104">SYNTAX</span></span>

```
Set-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac672-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ac672-105">DESCRIPTION</span></span>
<span data-ttu-id="ac672-106">Das Cmdlet " **Set-AzApiManagementOperation** " legt API-Vorgangsdetails fest.</span><span class="sxs-lookup"><span data-stu-id="ac672-106">The **Set-AzApiManagementOperation** cmdlet sets API operation details.</span></span>

## <span data-ttu-id="ac672-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ac672-107">EXAMPLES</span></span>

### <span data-ttu-id="ac672-108">Beispiel 1: Einrichten der Vorgangsdetails</span><span class="sxs-lookup"><span data-stu-id="ac672-108">Example 1: Set the operation details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementOperation -Context $apimContext -ApiId $APIID -OperationId $OperationId -Name "Get Resource" -Method GET -UrlTemplate "/newresource" -Description "Use this operation to get newresource"
```

<span data-ttu-id="ac672-109">Dieser Befehl legt die Vorgangsdetails für die API-Verwaltung fest.</span><span class="sxs-lookup"><span data-stu-id="ac672-109">This command sets the operation details for API management.</span></span>

## <span data-ttu-id="ac672-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac672-110">PARAMETERS</span></span>

### <span data-ttu-id="ac672-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="ac672-111">-ApiId</span></span>
<span data-ttu-id="ac672-112">Gibt den Bezeichner der API an.</span><span class="sxs-lookup"><span data-stu-id="ac672-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="ac672-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="ac672-113">-ApiRevision</span></span>
<span data-ttu-id="ac672-114">Bezeichner der API-Überarbeitung.</span><span class="sxs-lookup"><span data-stu-id="ac672-114">Identifier of API Revision.</span></span> <span data-ttu-id="ac672-115">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="ac672-115">This parameter is optional.</span></span> <span data-ttu-id="ac672-116">Wenn Sie nicht angegeben wird, wird der Vorgang in der aktuell aktiven API-Revision aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="ac672-116">If not specified, the operation will be updated in the currently active api revision.</span></span>

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

### <span data-ttu-id="ac672-117">-Context</span><span class="sxs-lookup"><span data-stu-id="ac672-117">-Context</span></span>
<span data-ttu-id="ac672-118">Gibt eine Instanz von **PsApiManagementContext** an.</span><span class="sxs-lookup"><span data-stu-id="ac672-118">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="ac672-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac672-119">-DefaultProfile</span></span>
<span data-ttu-id="ac672-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ac672-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac672-121">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ac672-121">-Description</span></span>
<span data-ttu-id="ac672-122">Gibt die Beschreibung des neuen Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="ac672-122">Specifies the description of the new operation.</span></span>

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

### <span data-ttu-id="ac672-123">-Methode</span><span class="sxs-lookup"><span data-stu-id="ac672-123">-Method</span></span>
<span data-ttu-id="ac672-124">Gibt die HTTP-Methode des neuen Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="ac672-124">Specifies the HTTP method of the new operation.</span></span>

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

### <span data-ttu-id="ac672-125">-Name</span><span class="sxs-lookup"><span data-stu-id="ac672-125">-Name</span></span>
<span data-ttu-id="ac672-126">Gibt den Anzeigenamen des neuen Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="ac672-126">Specifies the display name of the new operation.</span></span>

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

### <span data-ttu-id="ac672-127">-Vorgangs-Nr</span><span class="sxs-lookup"><span data-stu-id="ac672-127">-OperationId</span></span>
<span data-ttu-id="ac672-128">Gibt den Bezeichner des vorhandenen Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="ac672-128">Specifies the identifier of the existing operation.</span></span>

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

### <span data-ttu-id="ac672-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac672-129">-PassThru</span></span>
<span data-ttu-id="ac672-130">passthru</span><span class="sxs-lookup"><span data-stu-id="ac672-130">passthru</span></span>

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

### <span data-ttu-id="ac672-131">-Anfrage</span><span class="sxs-lookup"><span data-stu-id="ac672-131">-Request</span></span>
<span data-ttu-id="ac672-132">Gibt die Vorgangs Anforderungsdetails an.</span><span class="sxs-lookup"><span data-stu-id="ac672-132">Specifies the operation request details.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac672-133">-Antworten</span><span class="sxs-lookup"><span data-stu-id="ac672-133">-Responses</span></span>
<span data-ttu-id="ac672-134">Gibt ein Array möglicher Vorgangsantworten an.</span><span class="sxs-lookup"><span data-stu-id="ac672-134">Specifies an array of possible operation responses.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac672-135">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="ac672-135">-TemplateParameters</span></span>
<span data-ttu-id="ac672-136">Gibt ein Array oder Parameter an, die in Parameter *UrlTemplate* definiert sind.</span><span class="sxs-lookup"><span data-stu-id="ac672-136">Specifies an array or parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="ac672-137">Wenn Sie keinen Wert angeben, wird basierend auf dem UrlTemplate ein Standardwert generiert.</span><span class="sxs-lookup"><span data-stu-id="ac672-137">If you do not specify a value, a default value will be generated based on the UrlTemplate.</span></span>
<span data-ttu-id="ac672-138">Verwenden Sie den Parameter, um weitere Details zu Parametern wie Description, Type und anderen möglichen Werten anzugeben.</span><span class="sxs-lookup"><span data-stu-id="ac672-138">Use the parameter to give more details on parameters such as description, type, and other possible values.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac672-139">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="ac672-139">-UrlTemplate</span></span>
<span data-ttu-id="ac672-140">Gibt die URL-Vorlage an.</span><span class="sxs-lookup"><span data-stu-id="ac672-140">Specifies the URL template.</span></span>
<span data-ttu-id="ac672-141">Beispiel: Kunden/{CID}/Orders/{OID}/? date = {date}.</span><span class="sxs-lookup"><span data-stu-id="ac672-141">For instance: customers/{cid}/orders/{oid}/?date={date}.</span></span>

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

### <span data-ttu-id="ac672-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ac672-142">-Confirm</span></span>
<span data-ttu-id="ac672-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ac672-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac672-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac672-144">-WhatIf</span></span>
<span data-ttu-id="ac672-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ac672-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ac672-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ac672-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac672-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac672-147">CommonParameters</span></span>
<span data-ttu-id="ac672-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac672-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac672-149">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac672-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac672-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ac672-150">INPUTS</span></span>

### <span data-ttu-id="ac672-151">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ac672-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ac672-152">System. String</span><span class="sxs-lookup"><span data-stu-id="ac672-152">System.String</span></span>

### <span data-ttu-id="ac672-153">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementParameter []</span><span class="sxs-lookup"><span data-stu-id="ac672-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span></span>

### <span data-ttu-id="ac672-154">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementRequest</span><span class="sxs-lookup"><span data-stu-id="ac672-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span></span>

### <span data-ttu-id="ac672-155">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementResponse []</span><span class="sxs-lookup"><span data-stu-id="ac672-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span></span>

### <span data-ttu-id="ac672-156">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="ac672-156">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ac672-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ac672-157">OUTPUTS</span></span>

### <span data-ttu-id="ac672-158">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ac672-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="ac672-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="ac672-159">NOTES</span></span>

## <span data-ttu-id="ac672-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ac672-160">RELATED LINKS</span></span>

[<span data-ttu-id="ac672-161">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ac672-161">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="ac672-162">Neu – AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ac672-162">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="ac672-163">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ac672-163">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)


