---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
ms.openlocfilehash: b5e51891f82b2a12f42fac3a1535f974912ca1dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496686"
---
# <span data-ttu-id="45cac-101">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="45cac-101">Set-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="45cac-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="45cac-102">SYNOPSIS</span></span>
<span data-ttu-id="45cac-103">Aktualisiert ein Back-End.</span><span class="sxs-lookup"><span data-stu-id="45cac-103">Updates a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45cac-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="45cac-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45cac-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="45cac-105">DESCRIPTION</span></span>
<span data-ttu-id="45cac-106">Aktualisiert ein vorhandenes Back-End in der API-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="45cac-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="45cac-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="45cac-107">EXAMPLES</span></span>

### <span data-ttu-id="45cac-108">Aktualisiert die Beschreibung des Back-End-123</span><span class="sxs-lookup"><span data-stu-id="45cac-108">Updates the Description of the Backend 123</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="45cac-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="45cac-109">PARAMETERS</span></span>

### <span data-ttu-id="45cac-110">-Back-End-Nr</span><span class="sxs-lookup"><span data-stu-id="45cac-110">-BackendId</span></span>
<span data-ttu-id="45cac-111">Bezeichner des neuen Back-Ends.</span><span class="sxs-lookup"><span data-stu-id="45cac-111">Identifier of new backend.</span></span>
<span data-ttu-id="45cac-112">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="45cac-112">This parameter is required.</span></span>

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

### <span data-ttu-id="45cac-113">-Context</span><span class="sxs-lookup"><span data-stu-id="45cac-113">-Context</span></span>
<span data-ttu-id="45cac-114">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="45cac-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="45cac-115">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="45cac-115">This parameter is required.</span></span>

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

### <span data-ttu-id="45cac-116">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="45cac-116">-Credential</span></span>
<span data-ttu-id="45cac-117">Anmeldeinformationen, die beim Gespräch mit dem Back-End verwendet werden sollten.</span><span class="sxs-lookup"><span data-stu-id="45cac-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="45cac-118">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="45cac-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="45cac-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45cac-119">-DefaultProfile</span></span>
<span data-ttu-id="45cac-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="45cac-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="45cac-121">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="45cac-121">-Description</span></span>
<span data-ttu-id="45cac-122">Back-End-Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="45cac-122">Backend Description.</span></span>
<span data-ttu-id="45cac-123">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="45cac-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="45cac-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="45cac-124">-PassThru</span></span>
<span data-ttu-id="45cac-125">Gibt an, dass dieses Cmdlet die  **PsApiManagementBackend** zurückgibt, die von diesem Cmdlet geändert werden.</span><span class="sxs-lookup"><span data-stu-id="45cac-125">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45cac-126">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="45cac-126">-Protocol</span></span>
<span data-ttu-id="45cac-127">Back-End-Kommunikationsprotokoll (http oder SOAP).</span><span class="sxs-lookup"><span data-stu-id="45cac-127">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="45cac-128">Dieser Parameter ist optional</span><span class="sxs-lookup"><span data-stu-id="45cac-128">This parameter is optional</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: http, soap

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45cac-129">-Proxy</span><span class="sxs-lookup"><span data-stu-id="45cac-129">-Proxy</span></span>
<span data-ttu-id="45cac-130">Proxy Server-Details, die beim Senden einer Anforderung an das Back-End verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="45cac-130">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="45cac-131">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="45cac-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="45cac-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="45cac-132">-ResourceId</span></span>
<span data-ttu-id="45cac-133">Verwaltungs-URI der Ressource im externen System.</span><span class="sxs-lookup"><span data-stu-id="45cac-133">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="45cac-134">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="45cac-134">This parameter is optional.</span></span>
<span data-ttu-id="45cac-135">Diese URL kann die Arm-Ressourcen-ID von Logik-apps, Funktions-Apps oder API-apps sein.</span><span class="sxs-lookup"><span data-stu-id="45cac-135">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="45cac-136">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="45cac-136">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="45cac-137">Gibt an, ob die Zertifikatkettenüberprüfung beim Gespräch mit dem Back-End übersprungen werden soll.</span><span class="sxs-lookup"><span data-stu-id="45cac-137">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="45cac-138">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="45cac-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="45cac-139">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="45cac-139">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="45cac-140">Gibt an, ob die Zertifikatnamen Überprüfung beim Gespräch mit dem Back-End übersprungen werden soll.</span><span class="sxs-lookup"><span data-stu-id="45cac-140">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="45cac-141">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="45cac-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="45cac-142">-Title</span><span class="sxs-lookup"><span data-stu-id="45cac-142">-Title</span></span>
<span data-ttu-id="45cac-143">Back-End-Titel.</span><span class="sxs-lookup"><span data-stu-id="45cac-143">Backend Title.</span></span>
<span data-ttu-id="45cac-144">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="45cac-144">This parameter is optional.</span></span>

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

### <span data-ttu-id="45cac-145">-URL</span><span class="sxs-lookup"><span data-stu-id="45cac-145">-Url</span></span>
<span data-ttu-id="45cac-146">Laufzeit-URL für das Back-End.</span><span class="sxs-lookup"><span data-stu-id="45cac-146">Runtime Url for the Backend.</span></span>
<span data-ttu-id="45cac-147">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="45cac-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="45cac-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="45cac-148">-Confirm</span></span>
<span data-ttu-id="45cac-149">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="45cac-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45cac-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45cac-150">-WhatIf</span></span>
<span data-ttu-id="45cac-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="45cac-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45cac-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="45cac-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45cac-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45cac-153">CommonParameters</span></span>
<span data-ttu-id="45cac-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45cac-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45cac-155">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45cac-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45cac-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="45cac-156">INPUTS</span></span>

### <span data-ttu-id="45cac-157">Keine</span><span class="sxs-lookup"><span data-stu-id="45cac-157">None</span></span>
<span data-ttu-id="45cac-158">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="45cac-158">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="45cac-159">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="45cac-159">OUTPUTS</span></span>

### <span data-ttu-id="45cac-160">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="45cac-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="45cac-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="45cac-161">NOTES</span></span>

## <span data-ttu-id="45cac-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="45cac-162">RELATED LINKS</span></span>

[<span data-ttu-id="45cac-163">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="45cac-163">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="45cac-164">Neu – AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="45cac-164">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="45cac-165">Neu – AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="45cac-165">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="45cac-166">Neu – AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="45cac-166">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="45cac-167">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="45cac-167">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
