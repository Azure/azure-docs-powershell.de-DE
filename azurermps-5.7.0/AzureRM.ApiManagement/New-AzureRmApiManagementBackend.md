---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
ms.openlocfilehash: c337e82c88c7fdbbc1f8a3663249126c9d92b19f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504638"
---
# <span data-ttu-id="1956e-101">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1956e-101">New-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="1956e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1956e-102">SYNOPSIS</span></span>
<span data-ttu-id="1956e-103">Erstellt eine neue Back-End-Entität.</span><span class="sxs-lookup"><span data-stu-id="1956e-103">Creates a new backend entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1956e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1956e-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1956e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1956e-105">DESCRIPTION</span></span>
<span data-ttu-id="1956e-106">Erstellt eine neue Back-End-Entität in der API-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="1956e-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="1956e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1956e-107">EXAMPLES</span></span>

### <span data-ttu-id="1956e-108">Erstellen von Back-End-123 mit einem einfachen Autorisierungsschema</span><span class="sxs-lookup"><span data-stu-id="1956e-108">Create Backend 123 with a Basic Authorization Scheme</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="1956e-109">Erstellt ein neues Back-End</span><span class="sxs-lookup"><span data-stu-id="1956e-109">Creates a new Backend</span></span>

## <span data-ttu-id="1956e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1956e-110">PARAMETERS</span></span>

### <span data-ttu-id="1956e-111">-Back-End-Nr</span><span class="sxs-lookup"><span data-stu-id="1956e-111">-BackendId</span></span>
<span data-ttu-id="1956e-112">Bezeichner des neuen Back-Ends.</span><span class="sxs-lookup"><span data-stu-id="1956e-112">Identifier of new backend.</span></span>
<span data-ttu-id="1956e-113">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="1956e-113">This parameter is optional.</span></span>
<span data-ttu-id="1956e-114">Wenn nicht angegeben, wird generiert.</span><span class="sxs-lookup"><span data-stu-id="1956e-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="1956e-115">-Context</span><span class="sxs-lookup"><span data-stu-id="1956e-115">-Context</span></span>
<span data-ttu-id="1956e-116">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="1956e-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="1956e-117">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1956e-117">This parameter is required.</span></span>

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

### <span data-ttu-id="1956e-118">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="1956e-118">-Credential</span></span>
<span data-ttu-id="1956e-119">Anmeldeinformationen, die beim Gespräch mit dem Back-End verwendet werden sollten.</span><span class="sxs-lookup"><span data-stu-id="1956e-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="1956e-120">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="1956e-120">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementBackendCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1956e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1956e-121">-DefaultProfile</span></span>
<span data-ttu-id="1956e-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1956e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="1956e-123">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1956e-123">-Description</span></span>
<span data-ttu-id="1956e-124">Back-End-Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="1956e-124">Backend Description.</span></span>
<span data-ttu-id="1956e-125">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="1956e-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="1956e-126">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="1956e-126">-Protocol</span></span>
<span data-ttu-id="1956e-127">Back-End-Kommunikationsprotokoll.</span><span class="sxs-lookup"><span data-stu-id="1956e-127">Backend Communication protocol.</span></span>
<span data-ttu-id="1956e-128">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1956e-128">This parameter is required.</span></span>
<span data-ttu-id="1956e-129">Gültige Werte sind "http" und "SOAP".</span><span class="sxs-lookup"><span data-stu-id="1956e-129">Valid values are 'http' and 'soap'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: http, soap

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1956e-130">-Proxy</span><span class="sxs-lookup"><span data-stu-id="1956e-130">-Proxy</span></span>
<span data-ttu-id="1956e-131">Proxy Server-Details, die beim Senden einer Anforderung an das Back-End verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1956e-131">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="1956e-132">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="1956e-132">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementBackendProxy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1956e-133">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="1956e-133">-ResourceId</span></span>
<span data-ttu-id="1956e-134">Verwaltungs-URI der Ressource im externen System.</span><span class="sxs-lookup"><span data-stu-id="1956e-134">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="1956e-135">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="1956e-135">This parameter is optional.</span></span>
<span data-ttu-id="1956e-136">Diese URL kann die Arm-Ressourcen-ID von Logik-apps, Funktions-Apps oder API-apps sein.</span><span class="sxs-lookup"><span data-stu-id="1956e-136">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="1956e-137">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="1956e-137">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="1956e-138">Gibt an, ob die Zertifikatkettenüberprüfung beim Gespräch mit dem Back-End übersprungen werden soll.</span><span class="sxs-lookup"><span data-stu-id="1956e-138">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="1956e-139">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="1956e-139">This parameter is optional.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1956e-140">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="1956e-140">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="1956e-141">Gibt an, ob die Zertifikatnamen Überprüfung beim Gespräch mit dem Back-End übersprungen werden soll.</span><span class="sxs-lookup"><span data-stu-id="1956e-141">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="1956e-142">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="1956e-142">This parameter is optional.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1956e-143">-Title</span><span class="sxs-lookup"><span data-stu-id="1956e-143">-Title</span></span>
<span data-ttu-id="1956e-144">Back-End-Titel.</span><span class="sxs-lookup"><span data-stu-id="1956e-144">Backend Title.</span></span>
<span data-ttu-id="1956e-145">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="1956e-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="1956e-146">-URL</span><span class="sxs-lookup"><span data-stu-id="1956e-146">-Url</span></span>
<span data-ttu-id="1956e-147">Laufzeit-URL für das Back-End.</span><span class="sxs-lookup"><span data-stu-id="1956e-147">Runtime Url for the Backend.</span></span>
<span data-ttu-id="1956e-148">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1956e-148">This parameter is required.</span></span>

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

### <span data-ttu-id="1956e-149">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1956e-149">-Confirm</span></span>
<span data-ttu-id="1956e-150">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1956e-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1956e-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1956e-151">-WhatIf</span></span>
<span data-ttu-id="1956e-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1956e-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1956e-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1956e-153">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1956e-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1956e-154">CommonParameters</span></span>
<span data-ttu-id="1956e-155">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1956e-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1956e-156">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1956e-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1956e-157">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1956e-157">INPUTS</span></span>

### <span data-ttu-id="1956e-158">Keine</span><span class="sxs-lookup"><span data-stu-id="1956e-158">None</span></span>
<span data-ttu-id="1956e-159">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="1956e-159">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1956e-160">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1956e-160">OUTPUTS</span></span>

### <span data-ttu-id="1956e-161">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1956e-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="1956e-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="1956e-162">NOTES</span></span>

## <span data-ttu-id="1956e-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1956e-163">RELATED LINKS</span></span>

[<span data-ttu-id="1956e-164">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1956e-164">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="1956e-165">Neu – AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="1956e-165">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="1956e-166">Neu – AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="1956e-166">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="1956e-167">Satz-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1956e-167">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="1956e-168">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1956e-168">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)

