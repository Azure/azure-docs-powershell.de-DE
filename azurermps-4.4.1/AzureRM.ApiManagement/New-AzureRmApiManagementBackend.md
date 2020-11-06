---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
ms.openlocfilehash: 144830c2155379683c8568eda6e0d1bc021b38fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498078"
---
# <span data-ttu-id="068ff-101">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="068ff-101">New-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="068ff-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="068ff-102">SYNOPSIS</span></span>
<span data-ttu-id="068ff-103">Erstellt eine neue Back-End-Entität.</span><span class="sxs-lookup"><span data-stu-id="068ff-103">Creates a new backend entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="068ff-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="068ff-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="068ff-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="068ff-105">DESCRIPTION</span></span>
<span data-ttu-id="068ff-106">Erstellt eine neue Back-End-Entität in der API-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="068ff-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="068ff-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="068ff-107">EXAMPLES</span></span>

### <span data-ttu-id="068ff-108">Erstellen von Back-End-123 mit einem einfachen Autorisierungsschema</span><span class="sxs-lookup"><span data-stu-id="068ff-108">Create Backend 123 with a Basic Authorization Scheme</span></span>
```
$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="068ff-109">Erstellt ein neues Back-End</span><span class="sxs-lookup"><span data-stu-id="068ff-109">Creates a new Backend</span></span>

## <span data-ttu-id="068ff-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="068ff-110">PARAMETERS</span></span>

### <span data-ttu-id="068ff-111">-Back-End-Nr</span><span class="sxs-lookup"><span data-stu-id="068ff-111">-BackendId</span></span>
<span data-ttu-id="068ff-112">Bezeichner des neuen Back-Ends.</span><span class="sxs-lookup"><span data-stu-id="068ff-112">Identifier of new backend.</span></span>
<span data-ttu-id="068ff-113">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="068ff-113">This parameter is optional.</span></span>
<span data-ttu-id="068ff-114">Wenn nicht angegeben, wird generiert.</span><span class="sxs-lookup"><span data-stu-id="068ff-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="068ff-115">-Context</span><span class="sxs-lookup"><span data-stu-id="068ff-115">-Context</span></span>
<span data-ttu-id="068ff-116">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="068ff-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="068ff-117">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="068ff-117">This parameter is required.</span></span>

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

### <span data-ttu-id="068ff-118">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="068ff-118">-Credential</span></span>
<span data-ttu-id="068ff-119">Anmeldeinformationen, die beim Gespräch mit dem Back-End verwendet werden sollten.</span><span class="sxs-lookup"><span data-stu-id="068ff-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="068ff-120">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="068ff-120">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="068ff-121">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="068ff-121">-Description</span></span>
<span data-ttu-id="068ff-122">Back-End-Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="068ff-122">Backend Description.</span></span>
<span data-ttu-id="068ff-123">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="068ff-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="068ff-124">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="068ff-124">-Protocol</span></span>
<span data-ttu-id="068ff-125">Back-End-Kommunikationsprotokoll.</span><span class="sxs-lookup"><span data-stu-id="068ff-125">Backend Communication protocol.</span></span>
<span data-ttu-id="068ff-126">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="068ff-126">This parameter is required.</span></span>
<span data-ttu-id="068ff-127">Gültige Werte sind "http" und "SOAP".</span><span class="sxs-lookup"><span data-stu-id="068ff-127">Valid values are 'http' and 'soap'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: http, soap

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="068ff-128">-Proxy</span><span class="sxs-lookup"><span data-stu-id="068ff-128">-Proxy</span></span>
<span data-ttu-id="068ff-129">Proxy Server-Details, die beim Senden einer Anforderung an das Back-End verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="068ff-129">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="068ff-130">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="068ff-130">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="068ff-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="068ff-131">-ResourceId</span></span>
<span data-ttu-id="068ff-132">Verwaltungs-URI der Ressource im externen System.</span><span class="sxs-lookup"><span data-stu-id="068ff-132">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="068ff-133">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="068ff-133">This parameter is optional.</span></span>
<span data-ttu-id="068ff-134">Diese URL kann die Arm-Ressourcen-ID von Logik-apps, Funktions-Apps oder API-apps sein.</span><span class="sxs-lookup"><span data-stu-id="068ff-134">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="068ff-135">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="068ff-135">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="068ff-136">Gibt an, ob die Zertifikatkettenüberprüfung beim Gespräch mit dem Back-End übersprungen werden soll.</span><span class="sxs-lookup"><span data-stu-id="068ff-136">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="068ff-137">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="068ff-137">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="068ff-138">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="068ff-138">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="068ff-139">Gibt an, ob die Zertifikatnamen Überprüfung beim Gespräch mit dem Back-End übersprungen werden soll.</span><span class="sxs-lookup"><span data-stu-id="068ff-139">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="068ff-140">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="068ff-140">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="068ff-141">-Title</span><span class="sxs-lookup"><span data-stu-id="068ff-141">-Title</span></span>
<span data-ttu-id="068ff-142">Back-End-Titel.</span><span class="sxs-lookup"><span data-stu-id="068ff-142">Backend Title.</span></span>
<span data-ttu-id="068ff-143">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="068ff-143">This parameter is optional.</span></span>

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

### <span data-ttu-id="068ff-144">-URL</span><span class="sxs-lookup"><span data-stu-id="068ff-144">-Url</span></span>
<span data-ttu-id="068ff-145">Laufzeit-URL für das Back-End.</span><span class="sxs-lookup"><span data-stu-id="068ff-145">Runtime Url for the Backend.</span></span>
<span data-ttu-id="068ff-146">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="068ff-146">This parameter is required.</span></span>

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

### <span data-ttu-id="068ff-147">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="068ff-147">-Confirm</span></span>
<span data-ttu-id="068ff-148">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="068ff-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="068ff-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="068ff-149">-WhatIf</span></span>
<span data-ttu-id="068ff-150">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="068ff-150">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="068ff-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="068ff-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="068ff-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="068ff-152">-DefaultProfile</span></span>
<span data-ttu-id="068ff-153">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="068ff-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="068ff-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="068ff-154">CommonParameters</span></span>
<span data-ttu-id="068ff-155">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="068ff-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="068ff-156">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="068ff-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="068ff-157">Eingaben</span><span class="sxs-lookup"><span data-stu-id="068ff-157">INPUTS</span></span>

## <span data-ttu-id="068ff-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="068ff-158">OUTPUTS</span></span>

### <span data-ttu-id="068ff-159">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="068ff-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="068ff-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="068ff-160">NOTES</span></span>

## <span data-ttu-id="068ff-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="068ff-161">RELATED LINKS</span></span>

[<span data-ttu-id="068ff-162">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="068ff-162">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="068ff-163">Neu – AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="068ff-163">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="068ff-164">Neu – AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="068ff-164">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="068ff-165">Satz-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="068ff-165">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="068ff-166">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="068ff-166">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)

