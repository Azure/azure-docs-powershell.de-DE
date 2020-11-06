---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 67EE6EFB-3297-4D21-A6EC-B03F5FE82F84
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
ms.openlocfilehash: 4800d7d56d03071b57d25cdacfcf271defa9276f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496681"
---
# <span data-ttu-id="d7b2b-101">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d7b2b-101">Set-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="d7b2b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d7b2b-102">SYNOPSIS</span></span>
<span data-ttu-id="d7b2b-103">Legt die Details des API-Vorgangs fest.</span><span class="sxs-lookup"><span data-stu-id="d7b2b-103">Sets API operation details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7b2b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7b2b-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d7b2b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d7b2b-105">DESCRIPTION</span></span>
<span data-ttu-id="d7b2b-106">Das Cmdlet " **Set-AzureRmApiManagementOperation** " legt API-Vorgangsdetails fest.</span><span class="sxs-lookup"><span data-stu-id="d7b2b-106">The **Set-AzureRmApiManagementOperation** cmdlet sets API operation details.</span></span>

## <span data-ttu-id="d7b2b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d7b2b-107">EXAMPLES</span></span>

### <span data-ttu-id="d7b2b-108">Beispiel 1: Einrichten der Vorgangsdetails</span><span class="sxs-lookup"><span data-stu-id="d7b2b-108">Example 1: Set the operation details</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIID -OperationId $OperationId -Name "Get Resource" -Method GET -UrlTemplate "/newresource" -Description "Use this operation to get newresource"
```

<span data-ttu-id="d7b2b-109">Dieser Befehl legt die Vorgangsdetails für die API-Verwaltung fest.</span><span class="sxs-lookup"><span data-stu-id="d7b2b-109">This command sets the operation details for API management.</span></span>

## <span data-ttu-id="d7b2b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7b2b-110">PARAMETERS</span></span>

### <span data-ttu-id="d7b2b-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="d7b2b-111">-ApiId</span></span>
<span data-ttu-id="d7b2b-112">Gibt den Bezeichner der API an.</span><span class="sxs-lookup"><span data-stu-id="d7b2b-112">Specifies the identifier of the API.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7b2b-113">-Context</span><span class="sxs-lookup"><span data-stu-id="d7b2b-113">-Context</span></span>
<span data-ttu-id="d7b2b-114">Gibt eine Instanz von **PsApiManagementContext** an.</span><span class="sxs-lookup"><span data-stu-id="d7b2b-114">Specifies an instance of **PsApiManagementContext**.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7b2b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7b2b-115">-DefaultProfile</span></span>
<span data-ttu-id="d7b2b-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d7b2b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7b2b-117">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d7b2b-117">-Description</span></span>
<span data-ttu-id="d7b2b-118">Gibt die Beschreibung des neuen Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="d7b2b-118">Specifies the description of the new operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7b2b-119">-Methode</span><span class="sxs-lookup"><span data-stu-id="d7b2b-119">-Method</span></span>
<span data-ttu-id="d7b2b-120">Gibt die HTTP-Methode des neuen Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="d7b2b-120">Specifies the HTTP method of the new operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7b2b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d7b2b-121">-Name</span></span>
<span data-ttu-id="d7b2b-122">Gibt den Anzeigenamen des neuen Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="d7b2b-122">Specifies the display name of the new operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7b2b-123">-Vorgangs-Nr</span><span class="sxs-lookup"><span data-stu-id="d7b2b-123">-OperationId</span></span>
<span data-ttu-id="d7b2b-124">Gibt den Bezeichner des vorhandenen Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="d7b2b-124">Specifies the identifier of the existing operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7b2b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7b2b-125">-PassThru</span></span>
<span data-ttu-id="d7b2b-126">passthru</span><span class="sxs-lookup"><span data-stu-id="d7b2b-126">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7b2b-127">-Anfrage</span><span class="sxs-lookup"><span data-stu-id="d7b2b-127">-Request</span></span>
<span data-ttu-id="d7b2b-128">Gibt die Vorgangs Anforderungsdetails an.</span><span class="sxs-lookup"><span data-stu-id="d7b2b-128">Specifies the operation request details.</span></span>

```yaml
Type: PsApiManagementRequest
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7b2b-129">-Antworten</span><span class="sxs-lookup"><span data-stu-id="d7b2b-129">-Responses</span></span>
<span data-ttu-id="d7b2b-130">Gibt ein Array möglicher Vorgangsantworten an.</span><span class="sxs-lookup"><span data-stu-id="d7b2b-130">Specifies an array of possible operation responses.</span></span>

```yaml
Type: PsApiManagementResponse[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7b2b-131">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="d7b2b-131">-TemplateParameters</span></span>
<span data-ttu-id="d7b2b-132">Gibt ein Array oder Parameter an, die in Parameter *UrlTemplate* definiert sind.</span><span class="sxs-lookup"><span data-stu-id="d7b2b-132">Specifies an array or parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="d7b2b-133">Wenn Sie keinen Wert angeben, wird basierend auf dem UrlTemplate ein Standardwert generiert.</span><span class="sxs-lookup"><span data-stu-id="d7b2b-133">If you do not specify a value, a default value will be generated based on the UrlTemplate.</span></span>
<span data-ttu-id="d7b2b-134">Verwenden Sie den Parameter, um weitere Details zu Parametern wie Description, Type und anderen möglichen Werten anzugeben.</span><span class="sxs-lookup"><span data-stu-id="d7b2b-134">Use the parameter to give more details on parameters such as description, type, and other possible values.</span></span>

```yaml
Type: PsApiManagementParameter[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7b2b-135">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="d7b2b-135">-UrlTemplate</span></span>
<span data-ttu-id="d7b2b-136">Gibt die URL-Vorlage an.</span><span class="sxs-lookup"><span data-stu-id="d7b2b-136">Specifies the URL template.</span></span>
<span data-ttu-id="d7b2b-137">Beispiel: Kunden/{CID}/Orders/{OID}/? date = {date}.</span><span class="sxs-lookup"><span data-stu-id="d7b2b-137">For instance: customers/{cid}/orders/{oid}/?date={date}.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7b2b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7b2b-138">CommonParameters</span></span>
<span data-ttu-id="d7b2b-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7b2b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7b2b-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7b2b-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7b2b-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d7b2b-141">INPUTS</span></span>

### <span data-ttu-id="d7b2b-142">Keine</span><span class="sxs-lookup"><span data-stu-id="d7b2b-142">None</span></span>
<span data-ttu-id="d7b2b-143">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="d7b2b-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d7b2b-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d7b2b-144">OUTPUTS</span></span>

### <span data-ttu-id="d7b2b-145">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d7b2b-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="d7b2b-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="d7b2b-146">NOTES</span></span>

## <span data-ttu-id="d7b2b-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d7b2b-147">RELATED LINKS</span></span>

[<span data-ttu-id="d7b2b-148">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d7b2b-148">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="d7b2b-149">Neu – AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d7b2b-149">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="d7b2b-150">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d7b2b-150">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)


