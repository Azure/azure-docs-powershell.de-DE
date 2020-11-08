---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
ms.openlocfilehash: 4ed63d0e3b801572698b123038a2022e89672a88
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010099"
---
# <span data-ttu-id="83f11-101">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="83f11-101">New-AzApiManagementBackend</span></span>

## <span data-ttu-id="83f11-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="83f11-102">SYNOPSIS</span></span>
<span data-ttu-id="83f11-103">Erstellt eine neue Back-End-Entität.</span><span class="sxs-lookup"><span data-stu-id="83f11-103">Creates a new backend entity.</span></span>

## <span data-ttu-id="83f11-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="83f11-104">SYNTAX</span></span>

```
New-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83f11-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="83f11-105">DESCRIPTION</span></span>
<span data-ttu-id="83f11-106">Erstellt eine neue Back-End-Entität in der API-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="83f11-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="83f11-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="83f11-107">EXAMPLES</span></span>

### <span data-ttu-id="83f11-108">Beispiel 1: Erstellen von Back-End-123 mit einem einfachen Autorisierungsschema</span><span class="sxs-lookup"><span data-stu-id="83f11-108">Example 1: Create Backend 123 with a Basic Authorization Scheme</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="83f11-109">Erstellt ein neues Back-End</span><span class="sxs-lookup"><span data-stu-id="83f11-109">Creates a new Backend</span></span>

## <span data-ttu-id="83f11-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="83f11-110">PARAMETERS</span></span>

### <span data-ttu-id="83f11-111">-Back-End-Nr</span><span class="sxs-lookup"><span data-stu-id="83f11-111">-BackendId</span></span>
<span data-ttu-id="83f11-112">Bezeichner des neuen Back-Ends.</span><span class="sxs-lookup"><span data-stu-id="83f11-112">Identifier of new backend.</span></span>
<span data-ttu-id="83f11-113">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="83f11-113">This parameter is optional.</span></span>
<span data-ttu-id="83f11-114">Wenn nicht angegeben, wird generiert.</span><span class="sxs-lookup"><span data-stu-id="83f11-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="83f11-115">-Context</span><span class="sxs-lookup"><span data-stu-id="83f11-115">-Context</span></span>
<span data-ttu-id="83f11-116">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="83f11-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="83f11-117">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="83f11-117">This parameter is required.</span></span>

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

### <span data-ttu-id="83f11-118">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="83f11-118">-Credential</span></span>
<span data-ttu-id="83f11-119">Anmeldeinformationen, die beim Gespräch mit dem Back-End verwendet werden sollten.</span><span class="sxs-lookup"><span data-stu-id="83f11-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="83f11-120">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="83f11-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="83f11-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83f11-121">-DefaultProfile</span></span>
<span data-ttu-id="83f11-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="83f11-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83f11-123">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="83f11-123">-Description</span></span>
<span data-ttu-id="83f11-124">Back-End-Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="83f11-124">Backend Description.</span></span>
<span data-ttu-id="83f11-125">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="83f11-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="83f11-126">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="83f11-126">-Protocol</span></span>
<span data-ttu-id="83f11-127">Back-End-Kommunikationsprotokoll.</span><span class="sxs-lookup"><span data-stu-id="83f11-127">Backend Communication protocol.</span></span>
<span data-ttu-id="83f11-128">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="83f11-128">This parameter is required.</span></span>
<span data-ttu-id="83f11-129">Gültige Werte sind "http" und "SOAP".</span><span class="sxs-lookup"><span data-stu-id="83f11-129">Valid values are 'http' and 'soap'.</span></span>

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

### <span data-ttu-id="83f11-130">-Proxy</span><span class="sxs-lookup"><span data-stu-id="83f11-130">-Proxy</span></span>
<span data-ttu-id="83f11-131">Proxy Server-Details, die beim Senden einer Anforderung an das Back-End verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="83f11-131">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="83f11-132">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="83f11-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="83f11-133">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="83f11-133">-ResourceId</span></span>
<span data-ttu-id="83f11-134">Verwaltungs-URI der Ressource im externen System.</span><span class="sxs-lookup"><span data-stu-id="83f11-134">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="83f11-135">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="83f11-135">This parameter is optional.</span></span>
<span data-ttu-id="83f11-136">Diese URL kann die Arm-Ressourcen-ID von Logik-apps, Funktions-Apps oder API-apps sein.</span><span class="sxs-lookup"><span data-stu-id="83f11-136">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="83f11-137">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="83f11-137">-ServiceFabricCluster</span></span>
<span data-ttu-id="83f11-138">Details zum Back-Fabric-Cluster-Back-End</span><span class="sxs-lookup"><span data-stu-id="83f11-138">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="83f11-139">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="83f11-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="83f11-140">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="83f11-140">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="83f11-141">Gibt an, ob die Zertifikatkettenüberprüfung beim Gespräch mit dem Back-End übersprungen werden soll.</span><span class="sxs-lookup"><span data-stu-id="83f11-141">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="83f11-142">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="83f11-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="83f11-143">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="83f11-143">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="83f11-144">Gibt an, ob die Zertifikatnamen Überprüfung beim Gespräch mit dem Back-End übersprungen werden soll.</span><span class="sxs-lookup"><span data-stu-id="83f11-144">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="83f11-145">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="83f11-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="83f11-146">-Title</span><span class="sxs-lookup"><span data-stu-id="83f11-146">-Title</span></span>
<span data-ttu-id="83f11-147">Back-End-Titel.</span><span class="sxs-lookup"><span data-stu-id="83f11-147">Backend Title.</span></span>
<span data-ttu-id="83f11-148">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="83f11-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="83f11-149">-URL</span><span class="sxs-lookup"><span data-stu-id="83f11-149">-Url</span></span>
<span data-ttu-id="83f11-150">Laufzeit-URL für das Back-End.</span><span class="sxs-lookup"><span data-stu-id="83f11-150">Runtime Url for the Backend.</span></span>
<span data-ttu-id="83f11-151">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="83f11-151">This parameter is required.</span></span>

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

### <span data-ttu-id="83f11-152">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="83f11-152">-Confirm</span></span>
<span data-ttu-id="83f11-153">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="83f11-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83f11-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83f11-154">-WhatIf</span></span>
<span data-ttu-id="83f11-155">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="83f11-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="83f11-156">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="83f11-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83f11-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83f11-157">CommonParameters</span></span>
<span data-ttu-id="83f11-158">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83f11-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83f11-159">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83f11-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83f11-160">Eingaben</span><span class="sxs-lookup"><span data-stu-id="83f11-160">INPUTS</span></span>

### <span data-ttu-id="83f11-161">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="83f11-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="83f11-162">System. String</span><span class="sxs-lookup"><span data-stu-id="83f11-162">System.String</span></span>

### <span data-ttu-id="83f11-163">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="83f11-163">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="83f11-164">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="83f11-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="83f11-165">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="83f11-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="83f11-166">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="83f11-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="83f11-167">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="83f11-167">OUTPUTS</span></span>

### <span data-ttu-id="83f11-168">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="83f11-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="83f11-169">Notizen</span><span class="sxs-lookup"><span data-stu-id="83f11-169">NOTES</span></span>

## <span data-ttu-id="83f11-170">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="83f11-170">RELATED LINKS</span></span>

[<span data-ttu-id="83f11-171">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="83f11-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="83f11-172">Neu – AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="83f11-172">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="83f11-173">Neu – AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="83f11-173">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="83f11-174">Satz-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="83f11-174">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="83f11-175">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="83f11-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)

