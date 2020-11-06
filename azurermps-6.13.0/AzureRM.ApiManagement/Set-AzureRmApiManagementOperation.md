---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 67EE6EFB-3297-4D21-A6EC-B03F5FE82F84
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
ms.openlocfilehash: e50e912c55a09ef5d036bee668bc45f58fc42c19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478046"
---
# <span data-ttu-id="bd4c5-101">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="bd4c5-101">Set-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="bd4c5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bd4c5-102">SYNOPSIS</span></span>
<span data-ttu-id="bd4c5-103">Legt die Details des API-Vorgangs fest.</span><span class="sxs-lookup"><span data-stu-id="bd4c5-103">Sets API operation details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd4c5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd4c5-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bd4c5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bd4c5-105">DESCRIPTION</span></span>
<span data-ttu-id="bd4c5-106">Das Cmdlet " **Set-AzureRmApiManagementOperation** " legt API-Vorgangsdetails fest.</span><span class="sxs-lookup"><span data-stu-id="bd4c5-106">The **Set-AzureRmApiManagementOperation** cmdlet sets API operation details.</span></span>

## <span data-ttu-id="bd4c5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bd4c5-107">EXAMPLES</span></span>

### <span data-ttu-id="bd4c5-108">Beispiel 1: Einrichten der Vorgangsdetails</span><span class="sxs-lookup"><span data-stu-id="bd4c5-108">Example 1: Set the operation details</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIID -OperationId $OperationId -Name "Get Resource" -Method GET -UrlTemplate "/newresource" -Description "Use this operation to get newresource"
```

<span data-ttu-id="bd4c5-109">Dieser Befehl legt die Vorgangsdetails für die API-Verwaltung fest.</span><span class="sxs-lookup"><span data-stu-id="bd4c5-109">This command sets the operation details for API management.</span></span>

## <span data-ttu-id="bd4c5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd4c5-110">PARAMETERS</span></span>

### <span data-ttu-id="bd4c5-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="bd4c5-111">-ApiId</span></span>
<span data-ttu-id="bd4c5-112">Gibt den Bezeichner der API an.</span><span class="sxs-lookup"><span data-stu-id="bd4c5-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="bd4c5-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="bd4c5-113">-ApiRevision</span></span>
<span data-ttu-id="bd4c5-114">Bezeichner der API-Überarbeitung.</span><span class="sxs-lookup"><span data-stu-id="bd4c5-114">Identifier of API Revision.</span></span> <span data-ttu-id="bd4c5-115">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="bd4c5-115">This parameter is optional.</span></span> <span data-ttu-id="bd4c5-116">Wenn Sie nicht angegeben wird, wird der Vorgang in der aktuell aktiven API-Revision aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="bd4c5-116">If not specified, the operation will be updated in the currently active api revision.</span></span>

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

### <span data-ttu-id="bd4c5-117">-Context</span><span class="sxs-lookup"><span data-stu-id="bd4c5-117">-Context</span></span>
<span data-ttu-id="bd4c5-118">Gibt eine Instanz von **PsApiManagementContext** an.</span><span class="sxs-lookup"><span data-stu-id="bd4c5-118">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="bd4c5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd4c5-119">-DefaultProfile</span></span>
<span data-ttu-id="bd4c5-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bd4c5-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd4c5-121">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bd4c5-121">-Description</span></span>
<span data-ttu-id="bd4c5-122">Gibt die Beschreibung des neuen Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="bd4c5-122">Specifies the description of the new operation.</span></span>

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

### <span data-ttu-id="bd4c5-123">-Methode</span><span class="sxs-lookup"><span data-stu-id="bd4c5-123">-Method</span></span>
<span data-ttu-id="bd4c5-124">Gibt die HTTP-Methode des neuen Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="bd4c5-124">Specifies the HTTP method of the new operation.</span></span>

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

### <span data-ttu-id="bd4c5-125">-Name</span><span class="sxs-lookup"><span data-stu-id="bd4c5-125">-Name</span></span>
<span data-ttu-id="bd4c5-126">Gibt den Anzeigenamen des neuen Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="bd4c5-126">Specifies the display name of the new operation.</span></span>

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

### <span data-ttu-id="bd4c5-127">-Vorgangs-Nr</span><span class="sxs-lookup"><span data-stu-id="bd4c5-127">-OperationId</span></span>
<span data-ttu-id="bd4c5-128">Gibt den Bezeichner des vorhandenen Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="bd4c5-128">Specifies the identifier of the existing operation.</span></span>

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

### <span data-ttu-id="bd4c5-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bd4c5-129">-PassThru</span></span>
<span data-ttu-id="bd4c5-130">passthru</span><span class="sxs-lookup"><span data-stu-id="bd4c5-130">passthru</span></span>

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

### <span data-ttu-id="bd4c5-131">-Anfrage</span><span class="sxs-lookup"><span data-stu-id="bd4c5-131">-Request</span></span>
<span data-ttu-id="bd4c5-132">Gibt die Vorgangs Anforderungsdetails an.</span><span class="sxs-lookup"><span data-stu-id="bd4c5-132">Specifies the operation request details.</span></span>

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

### <span data-ttu-id="bd4c5-133">-Antworten</span><span class="sxs-lookup"><span data-stu-id="bd4c5-133">-Responses</span></span>
<span data-ttu-id="bd4c5-134">Gibt ein Array möglicher Vorgangsantworten an.</span><span class="sxs-lookup"><span data-stu-id="bd4c5-134">Specifies an array of possible operation responses.</span></span>

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

### <span data-ttu-id="bd4c5-135">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="bd4c5-135">-TemplateParameters</span></span>
<span data-ttu-id="bd4c5-136">Gibt ein Array oder Parameter an, die in Parameter *UrlTemplate* definiert sind.</span><span class="sxs-lookup"><span data-stu-id="bd4c5-136">Specifies an array or parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="bd4c5-137">Wenn Sie keinen Wert angeben, wird basierend auf dem UrlTemplate ein Standardwert generiert.</span><span class="sxs-lookup"><span data-stu-id="bd4c5-137">If you do not specify a value, a default value will be generated based on the UrlTemplate.</span></span>
<span data-ttu-id="bd4c5-138">Verwenden Sie den Parameter, um weitere Details zu Parametern wie Description, Type und anderen möglichen Werten anzugeben.</span><span class="sxs-lookup"><span data-stu-id="bd4c5-138">Use the parameter to give more details on parameters such as description, type, and other possible values.</span></span>

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

### <span data-ttu-id="bd4c5-139">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="bd4c5-139">-UrlTemplate</span></span>
<span data-ttu-id="bd4c5-140">Gibt die URL-Vorlage an.</span><span class="sxs-lookup"><span data-stu-id="bd4c5-140">Specifies the URL template.</span></span>
<span data-ttu-id="bd4c5-141">Beispiel: Kunden/{CID}/Orders/{OID}/? date = {date}.</span><span class="sxs-lookup"><span data-stu-id="bd4c5-141">For instance: customers/{cid}/orders/{oid}/?date={date}.</span></span>

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

### <span data-ttu-id="bd4c5-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd4c5-142">CommonParameters</span></span>
<span data-ttu-id="bd4c5-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd4c5-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd4c5-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd4c5-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd4c5-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bd4c5-145">INPUTS</span></span>

### <span data-ttu-id="bd4c5-146">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bd4c5-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bd4c5-147">System. String</span><span class="sxs-lookup"><span data-stu-id="bd4c5-147">System.String</span></span>

### <span data-ttu-id="bd4c5-148">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementParameter []</span><span class="sxs-lookup"><span data-stu-id="bd4c5-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span></span>

### <span data-ttu-id="bd4c5-149">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementRequest</span><span class="sxs-lookup"><span data-stu-id="bd4c5-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span></span>

### <span data-ttu-id="bd4c5-150">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementResponse []</span><span class="sxs-lookup"><span data-stu-id="bd4c5-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span></span>

### <span data-ttu-id="bd4c5-151">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="bd4c5-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bd4c5-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bd4c5-152">OUTPUTS</span></span>

### <span data-ttu-id="bd4c5-153">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="bd4c5-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="bd4c5-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="bd4c5-154">NOTES</span></span>

## <span data-ttu-id="bd4c5-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bd4c5-155">RELATED LINKS</span></span>

[<span data-ttu-id="bd4c5-156">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="bd4c5-156">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="bd4c5-157">Neu – AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="bd4c5-157">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="bd4c5-158">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="bd4c5-158">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)


