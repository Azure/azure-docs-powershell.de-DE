---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
ms.openlocfilehash: 85545777f5a76f3f75e81648a009ffcdcad8ab30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664485"
---
# <span data-ttu-id="e7032-101">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e7032-101">Set-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="e7032-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e7032-102">SYNOPSIS</span></span>
<span data-ttu-id="e7032-103">Aktualisiert ein Back-End.</span><span class="sxs-lookup"><span data-stu-id="e7032-103">Updates a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7032-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7032-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7032-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e7032-105">DESCRIPTION</span></span>
<span data-ttu-id="e7032-106">Aktualisiert ein vorhandenes Back-End in der API-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="e7032-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="e7032-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e7032-107">EXAMPLES</span></span>

### <span data-ttu-id="e7032-108">Aktualisiert die Beschreibung des Back-End-123</span><span class="sxs-lookup"><span data-stu-id="e7032-108">Updates the Description of the Backend 123</span></span>
```
Set-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="e7032-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7032-109">PARAMETERS</span></span>

### <span data-ttu-id="e7032-110">-Back-End-Nr</span><span class="sxs-lookup"><span data-stu-id="e7032-110">-BackendId</span></span>
<span data-ttu-id="e7032-111">Bezeichner des neuen Back-Ends.</span><span class="sxs-lookup"><span data-stu-id="e7032-111">Identifier of new backend.</span></span>
<span data-ttu-id="e7032-112">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e7032-112">This parameter is required.</span></span>

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

### <span data-ttu-id="e7032-113">-Context</span><span class="sxs-lookup"><span data-stu-id="e7032-113">-Context</span></span>
<span data-ttu-id="e7032-114">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="e7032-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e7032-115">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e7032-115">This parameter is required.</span></span>

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

### <span data-ttu-id="e7032-116">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="e7032-116">-Credential</span></span>
<span data-ttu-id="e7032-117">Anmeldeinformationen, die beim Gespräch mit dem Back-End verwendet werden sollten.</span><span class="sxs-lookup"><span data-stu-id="e7032-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="e7032-118">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="e7032-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="e7032-119">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e7032-119">-Description</span></span>
<span data-ttu-id="e7032-120">Back-End-Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="e7032-120">Backend Description.</span></span>
<span data-ttu-id="e7032-121">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="e7032-121">This parameter is optional.</span></span>

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

### <span data-ttu-id="e7032-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7032-122">-PassThru</span></span>
<span data-ttu-id="e7032-123">Gibt an, dass dieses Cmdlet die  **PsApiManagementBackend** zurückgibt, die von diesem Cmdlet geändert werden.</span><span class="sxs-lookup"><span data-stu-id="e7032-123">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7032-124">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="e7032-124">-Protocol</span></span>
<span data-ttu-id="e7032-125">Back-End-Kommunikationsprotokoll (http oder SOAP).</span><span class="sxs-lookup"><span data-stu-id="e7032-125">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="e7032-126">Dieser Parameter ist optional</span><span class="sxs-lookup"><span data-stu-id="e7032-126">This parameter is optional</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: http, soap

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7032-127">-Proxy</span><span class="sxs-lookup"><span data-stu-id="e7032-127">-Proxy</span></span>
<span data-ttu-id="e7032-128">Proxy Server-Details, die beim Senden einer Anforderung an das Back-End verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e7032-128">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="e7032-129">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="e7032-129">This parameter is optional.</span></span>

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

### <span data-ttu-id="e7032-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e7032-130">-ResourceId</span></span>
<span data-ttu-id="e7032-131">Verwaltungs-URI der Ressource im externen System.</span><span class="sxs-lookup"><span data-stu-id="e7032-131">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="e7032-132">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="e7032-132">This parameter is optional.</span></span>
<span data-ttu-id="e7032-133">Diese URL kann die Arm-Ressourcen-ID von Logik-apps, Funktions-Apps oder API-apps sein.</span><span class="sxs-lookup"><span data-stu-id="e7032-133">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="e7032-134">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="e7032-134">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="e7032-135">Gibt an, ob die Zertifikatkettenüberprüfung beim Gespräch mit dem Back-End übersprungen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e7032-135">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="e7032-136">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="e7032-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="e7032-137">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="e7032-137">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="e7032-138">Gibt an, ob die Zertifikatnamen Überprüfung beim Gespräch mit dem Back-End übersprungen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e7032-138">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="e7032-139">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="e7032-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="e7032-140">-Title</span><span class="sxs-lookup"><span data-stu-id="e7032-140">-Title</span></span>
<span data-ttu-id="e7032-141">Back-End-Titel.</span><span class="sxs-lookup"><span data-stu-id="e7032-141">Backend Title.</span></span>
<span data-ttu-id="e7032-142">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="e7032-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="e7032-143">-URL</span><span class="sxs-lookup"><span data-stu-id="e7032-143">-Url</span></span>
<span data-ttu-id="e7032-144">Laufzeit-URL für das Back-End.</span><span class="sxs-lookup"><span data-stu-id="e7032-144">Runtime Url for the Backend.</span></span>
<span data-ttu-id="e7032-145">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="e7032-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="e7032-146">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e7032-146">-Confirm</span></span>
<span data-ttu-id="e7032-147">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e7032-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7032-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7032-148">-WhatIf</span></span>
<span data-ttu-id="e7032-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e7032-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e7032-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e7032-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7032-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7032-151">-DefaultProfile</span></span>
<span data-ttu-id="e7032-152">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e7032-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7032-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7032-153">CommonParameters</span></span>
<span data-ttu-id="e7032-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7032-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7032-155">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7032-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7032-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e7032-156">INPUTS</span></span>

## <span data-ttu-id="e7032-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e7032-157">OUTPUTS</span></span>

### <span data-ttu-id="e7032-158">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e7032-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="e7032-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="e7032-159">NOTES</span></span>

## <span data-ttu-id="e7032-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e7032-160">RELATED LINKS</span></span>

[<span data-ttu-id="e7032-161">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e7032-161">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="e7032-162">Neu – AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e7032-162">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="e7032-163">Neu – AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="e7032-163">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="e7032-164">Neu – AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="e7032-164">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="e7032-165">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e7032-165">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
