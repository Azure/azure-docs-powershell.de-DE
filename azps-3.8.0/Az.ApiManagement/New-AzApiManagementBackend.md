---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
ms.openlocfilehash: fc6346bc87b5bc69fdcd06474227afec7de55dee
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996969"
---
# <span data-ttu-id="dd34a-101">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="dd34a-101">New-AzApiManagementBackend</span></span>

## <span data-ttu-id="dd34a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dd34a-102">SYNOPSIS</span></span>
<span data-ttu-id="dd34a-103">Erstellt eine neue Back-End-Entität.</span><span class="sxs-lookup"><span data-stu-id="dd34a-103">Creates a new backend entity.</span></span>

## <span data-ttu-id="dd34a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd34a-104">SYNTAX</span></span>

```
New-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd34a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dd34a-105">DESCRIPTION</span></span>
<span data-ttu-id="dd34a-106">Erstellt eine neue Back-End-Entität in der API-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="dd34a-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="dd34a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dd34a-107">EXAMPLES</span></span>

### <span data-ttu-id="dd34a-108">Erstellen von Back-End-123 mit einem einfachen Autorisierungsschema</span><span class="sxs-lookup"><span data-stu-id="dd34a-108">Create Backend 123 with a Basic Authorization Scheme</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="dd34a-109">Erstellt ein neues Back-End</span><span class="sxs-lookup"><span data-stu-id="dd34a-109">Creates a new Backend</span></span>

## <span data-ttu-id="dd34a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd34a-110">PARAMETERS</span></span>

### <span data-ttu-id="dd34a-111">-Back-End-Nr</span><span class="sxs-lookup"><span data-stu-id="dd34a-111">-BackendId</span></span>
<span data-ttu-id="dd34a-112">Bezeichner des neuen Back-Ends.</span><span class="sxs-lookup"><span data-stu-id="dd34a-112">Identifier of new backend.</span></span>
<span data-ttu-id="dd34a-113">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="dd34a-113">This parameter is optional.</span></span>
<span data-ttu-id="dd34a-114">Wenn nicht angegeben, wird generiert.</span><span class="sxs-lookup"><span data-stu-id="dd34a-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="dd34a-115">-Context</span><span class="sxs-lookup"><span data-stu-id="dd34a-115">-Context</span></span>
<span data-ttu-id="dd34a-116">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="dd34a-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="dd34a-117">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="dd34a-117">This parameter is required.</span></span>

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

### <span data-ttu-id="dd34a-118">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="dd34a-118">-Credential</span></span>
<span data-ttu-id="dd34a-119">Anmeldeinformationen, die beim Gespräch mit dem Back-End verwendet werden sollten.</span><span class="sxs-lookup"><span data-stu-id="dd34a-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="dd34a-120">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="dd34a-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="dd34a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd34a-121">-DefaultProfile</span></span>
<span data-ttu-id="dd34a-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dd34a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd34a-123">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dd34a-123">-Description</span></span>
<span data-ttu-id="dd34a-124">Back-End-Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="dd34a-124">Backend Description.</span></span>
<span data-ttu-id="dd34a-125">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="dd34a-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="dd34a-126">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="dd34a-126">-Protocol</span></span>
<span data-ttu-id="dd34a-127">Back-End-Kommunikationsprotokoll.</span><span class="sxs-lookup"><span data-stu-id="dd34a-127">Backend Communication protocol.</span></span>
<span data-ttu-id="dd34a-128">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="dd34a-128">This parameter is required.</span></span>
<span data-ttu-id="dd34a-129">Gültige Werte sind "http" und "SOAP".</span><span class="sxs-lookup"><span data-stu-id="dd34a-129">Valid values are 'http' and 'soap'.</span></span>

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

### <span data-ttu-id="dd34a-130">-Proxy</span><span class="sxs-lookup"><span data-stu-id="dd34a-130">-Proxy</span></span>
<span data-ttu-id="dd34a-131">Proxy Server-Details, die beim Senden einer Anforderung an das Back-End verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dd34a-131">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="dd34a-132">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="dd34a-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="dd34a-133">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="dd34a-133">-ResourceId</span></span>
<span data-ttu-id="dd34a-134">Verwaltungs-URI der Ressource im externen System.</span><span class="sxs-lookup"><span data-stu-id="dd34a-134">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="dd34a-135">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="dd34a-135">This parameter is optional.</span></span>
<span data-ttu-id="dd34a-136">Diese URL kann die Arm-Ressourcen-ID von Logik-apps, Funktions-Apps oder API-apps sein.</span><span class="sxs-lookup"><span data-stu-id="dd34a-136">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="dd34a-137">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="dd34a-137">-ServiceFabricCluster</span></span>
<span data-ttu-id="dd34a-138">Details zum Back-Fabric-Cluster-Back-End</span><span class="sxs-lookup"><span data-stu-id="dd34a-138">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="dd34a-139">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="dd34a-139">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd34a-140">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="dd34a-140">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="dd34a-141">Gibt an, ob die Zertifikatkettenüberprüfung beim Gespräch mit dem Back-End übersprungen werden soll.</span><span class="sxs-lookup"><span data-stu-id="dd34a-141">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="dd34a-142">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="dd34a-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="dd34a-143">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="dd34a-143">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="dd34a-144">Gibt an, ob die Zertifikatnamen Überprüfung beim Gespräch mit dem Back-End übersprungen werden soll.</span><span class="sxs-lookup"><span data-stu-id="dd34a-144">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="dd34a-145">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="dd34a-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="dd34a-146">-Title</span><span class="sxs-lookup"><span data-stu-id="dd34a-146">-Title</span></span>
<span data-ttu-id="dd34a-147">Back-End-Titel.</span><span class="sxs-lookup"><span data-stu-id="dd34a-147">Backend Title.</span></span>
<span data-ttu-id="dd34a-148">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="dd34a-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="dd34a-149">-URL</span><span class="sxs-lookup"><span data-stu-id="dd34a-149">-Url</span></span>
<span data-ttu-id="dd34a-150">Laufzeit-URL für das Back-End.</span><span class="sxs-lookup"><span data-stu-id="dd34a-150">Runtime Url for the Backend.</span></span>
<span data-ttu-id="dd34a-151">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="dd34a-151">This parameter is required.</span></span>

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

### <span data-ttu-id="dd34a-152">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dd34a-152">-Confirm</span></span>
<span data-ttu-id="dd34a-153">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dd34a-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd34a-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd34a-154">-WhatIf</span></span>
<span data-ttu-id="dd34a-155">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dd34a-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dd34a-156">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dd34a-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd34a-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd34a-157">CommonParameters</span></span>
<span data-ttu-id="dd34a-158">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd34a-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd34a-159">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd34a-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd34a-160">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dd34a-160">INPUTS</span></span>

### <span data-ttu-id="dd34a-161">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="dd34a-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="dd34a-162">System. String</span><span class="sxs-lookup"><span data-stu-id="dd34a-162">System.String</span></span>

### <span data-ttu-id="dd34a-163">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="dd34a-163">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="dd34a-164">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="dd34a-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="dd34a-165">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="dd34a-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="dd34a-166">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dd34a-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="dd34a-167">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dd34a-167">OUTPUTS</span></span>

### <span data-ttu-id="dd34a-168">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="dd34a-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="dd34a-169">Notizen</span><span class="sxs-lookup"><span data-stu-id="dd34a-169">NOTES</span></span>

## <span data-ttu-id="dd34a-170">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dd34a-170">RELATED LINKS</span></span>

[<span data-ttu-id="dd34a-171">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="dd34a-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="dd34a-172">Neu – AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="dd34a-172">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="dd34a-173">Neu – AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="dd34a-173">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="dd34a-174">Satz-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="dd34a-174">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="dd34a-175">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="dd34a-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)

