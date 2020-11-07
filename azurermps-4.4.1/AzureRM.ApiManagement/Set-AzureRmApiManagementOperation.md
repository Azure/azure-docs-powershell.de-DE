---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 67EE6EFB-3297-4D21-A6EC-B03F5FE82F84
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
ms.openlocfilehash: 28bbc9158639faf066fa9a623f5dfacd6566d236
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664482"
---
# <span data-ttu-id="ca951-101">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ca951-101">Set-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="ca951-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ca951-102">SYNOPSIS</span></span>
<span data-ttu-id="ca951-103">Legt die Details des API-Vorgangs fest.</span><span class="sxs-lookup"><span data-stu-id="ca951-103">Sets API operation details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca951-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca951-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ca951-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ca951-105">DESCRIPTION</span></span>
<span data-ttu-id="ca951-106">Das Cmdlet " **Set-AzureRmApiManagementOperation** " legt API-Vorgangsdetails fest.</span><span class="sxs-lookup"><span data-stu-id="ca951-106">The **Set-AzureRmApiManagementOperation** cmdlet sets API operation details.</span></span>

## <span data-ttu-id="ca951-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ca951-107">EXAMPLES</span></span>

### <span data-ttu-id="ca951-108">Beispiel 1: Einrichten der Vorgangsdetails</span><span class="sxs-lookup"><span data-stu-id="ca951-108">Example 1: Set the operation details</span></span>
```
PS C:\>New-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIID -OperationId $OperationId -Name "Get Resource" -Method GET -UrlTemplate "/newresource" -Description "Use this operation to get newresource"
```

<span data-ttu-id="ca951-109">Dieser Befehl legt die Vorgangsdetails für die API-Verwaltung fest.</span><span class="sxs-lookup"><span data-stu-id="ca951-109">This command sets the operation details for API management.</span></span>

## <span data-ttu-id="ca951-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca951-110">PARAMETERS</span></span>

### <span data-ttu-id="ca951-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="ca951-111">-ApiId</span></span>
<span data-ttu-id="ca951-112">Gibt den Bezeichner der API an.</span><span class="sxs-lookup"><span data-stu-id="ca951-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="ca951-113">-Context</span><span class="sxs-lookup"><span data-stu-id="ca951-113">-Context</span></span>
<span data-ttu-id="ca951-114">Gibt eine Instanz von **PsApiManagementContext** an.</span><span class="sxs-lookup"><span data-stu-id="ca951-114">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="ca951-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ca951-115">-Description</span></span>
<span data-ttu-id="ca951-116">Gibt die Beschreibung des neuen Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="ca951-116">Specifies the description of the new operation.</span></span>

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

### <span data-ttu-id="ca951-117">-Methode</span><span class="sxs-lookup"><span data-stu-id="ca951-117">-Method</span></span>
<span data-ttu-id="ca951-118">Gibt die HTTP-Methode des neuen Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="ca951-118">Specifies the HTTP method of the new operation.</span></span>

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

### <span data-ttu-id="ca951-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ca951-119">-Name</span></span>
<span data-ttu-id="ca951-120">Gibt den Anzeigenamen des neuen Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="ca951-120">Specifies the display name of the new operation.</span></span>

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

### <span data-ttu-id="ca951-121">-Vorgangs-Nr</span><span class="sxs-lookup"><span data-stu-id="ca951-121">-OperationId</span></span>
<span data-ttu-id="ca951-122">Gibt den Bezeichner des vorhandenen Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="ca951-122">Specifies the identifier of the existing operation.</span></span>

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

### <span data-ttu-id="ca951-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca951-123">-PassThru</span></span>
<span data-ttu-id="ca951-124">passthru</span><span class="sxs-lookup"><span data-stu-id="ca951-124">passthru</span></span>

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

### <span data-ttu-id="ca951-125">-Anfrage</span><span class="sxs-lookup"><span data-stu-id="ca951-125">-Request</span></span>
<span data-ttu-id="ca951-126">Gibt die Vorgangs Anforderungsdetails an.</span><span class="sxs-lookup"><span data-stu-id="ca951-126">Specifies the operation request details.</span></span>

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

### <span data-ttu-id="ca951-127">-Antworten</span><span class="sxs-lookup"><span data-stu-id="ca951-127">-Responses</span></span>
<span data-ttu-id="ca951-128">Gibt ein Array möglicher Vorgangsantworten an.</span><span class="sxs-lookup"><span data-stu-id="ca951-128">Specifies an array of possible operation responses.</span></span>

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

### <span data-ttu-id="ca951-129">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="ca951-129">-TemplateParameters</span></span>
<span data-ttu-id="ca951-130">Gibt ein Array oder Parameter an, die in Parameter *UrlTemplate* definiert sind.</span><span class="sxs-lookup"><span data-stu-id="ca951-130">Specifies an array or parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="ca951-131">Wenn Sie keinen Wert angeben, wird basierend auf dem UrlTemplate ein Standardwert generiert.</span><span class="sxs-lookup"><span data-stu-id="ca951-131">If you do not specify a value, a default value will be generated based on the UrlTemplate.</span></span>
<span data-ttu-id="ca951-132">Verwenden Sie den Parameter, um weitere Details zu Parametern wie Description, Type und anderen möglichen Werten anzugeben.</span><span class="sxs-lookup"><span data-stu-id="ca951-132">Use the parameter to give more details on parameters such as description, type, and other possible values.</span></span>

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

### <span data-ttu-id="ca951-133">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="ca951-133">-UrlTemplate</span></span>
<span data-ttu-id="ca951-134">Gibt die URL-Vorlage an.</span><span class="sxs-lookup"><span data-stu-id="ca951-134">Specifies the URL template.</span></span>
<span data-ttu-id="ca951-135">Beispiel: Kunden/{CID}/Orders/{OID}/? date = {date}.</span><span class="sxs-lookup"><span data-stu-id="ca951-135">For instance: customers/{cid}/orders/{oid}/?date={date}.</span></span>

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

### <span data-ttu-id="ca951-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca951-136">-DefaultProfile</span></span>
<span data-ttu-id="ca951-137">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ca951-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca951-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca951-138">CommonParameters</span></span>
<span data-ttu-id="ca951-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca951-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca951-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca951-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca951-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ca951-141">INPUTS</span></span>

## <span data-ttu-id="ca951-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ca951-142">OUTPUTS</span></span>

### <span data-ttu-id="ca951-143">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ca951-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="ca951-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="ca951-144">NOTES</span></span>

## <span data-ttu-id="ca951-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ca951-145">RELATED LINKS</span></span>

[<span data-ttu-id="ca951-146">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ca951-146">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="ca951-147">Neu – AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ca951-147">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="ca951-148">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ca951-148">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)


