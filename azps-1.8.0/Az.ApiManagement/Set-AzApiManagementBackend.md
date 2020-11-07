---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
ms.openlocfilehash: ce27a151ebb6d778ed647fb81909c44c11edbf8e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821007"
---
# <span data-ttu-id="e915b-101">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e915b-101">Set-AzApiManagementBackend</span></span>

## <span data-ttu-id="e915b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e915b-102">SYNOPSIS</span></span>
<span data-ttu-id="e915b-103">Aktualisiert ein Back-End.</span><span class="sxs-lookup"><span data-stu-id="e915b-103">Updates a Backend.</span></span>

## <span data-ttu-id="e915b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e915b-104">SYNTAX</span></span>

```
Set-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e915b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e915b-105">DESCRIPTION</span></span>
<span data-ttu-id="e915b-106">Aktualisiert ein vorhandenes Back-End in der API-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="e915b-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="e915b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e915b-107">EXAMPLES</span></span>

### <span data-ttu-id="e915b-108">Aktualisiert die Beschreibung des Back-End-123</span><span class="sxs-lookup"><span data-stu-id="e915b-108">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="e915b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e915b-109">PARAMETERS</span></span>

### <span data-ttu-id="e915b-110">-Back-End-Nr</span><span class="sxs-lookup"><span data-stu-id="e915b-110">-BackendId</span></span>
<span data-ttu-id="e915b-111">Bezeichner des neuen Back-Ends.</span><span class="sxs-lookup"><span data-stu-id="e915b-111">Identifier of new backend.</span></span>
<span data-ttu-id="e915b-112">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e915b-112">This parameter is required.</span></span>

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

### <span data-ttu-id="e915b-113">-Context</span><span class="sxs-lookup"><span data-stu-id="e915b-113">-Context</span></span>
<span data-ttu-id="e915b-114">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="e915b-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e915b-115">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e915b-115">This parameter is required.</span></span>

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

### <span data-ttu-id="e915b-116">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="e915b-116">-Credential</span></span>
<span data-ttu-id="e915b-117">Anmeldeinformationen, die beim Gespräch mit dem Back-End verwendet werden sollten.</span><span class="sxs-lookup"><span data-stu-id="e915b-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="e915b-118">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="e915b-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="e915b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e915b-119">-DefaultProfile</span></span>
<span data-ttu-id="e915b-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e915b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e915b-121">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e915b-121">-Description</span></span>
<span data-ttu-id="e915b-122">Back-End-Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="e915b-122">Backend Description.</span></span>
<span data-ttu-id="e915b-123">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="e915b-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="e915b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e915b-124">-PassThru</span></span>
<span data-ttu-id="e915b-125">Gibt an, dass dieses Cmdlet die  **PsApiManagementBackend** zurückgibt, die von diesem Cmdlet geändert werden.</span><span class="sxs-lookup"><span data-stu-id="e915b-125">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="e915b-126">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="e915b-126">-Protocol</span></span>
<span data-ttu-id="e915b-127">Back-End-Kommunikationsprotokoll (http oder SOAP).</span><span class="sxs-lookup"><span data-stu-id="e915b-127">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="e915b-128">Dieser Parameter ist optional</span><span class="sxs-lookup"><span data-stu-id="e915b-128">This parameter is optional</span></span>

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

### <span data-ttu-id="e915b-129">-Proxy</span><span class="sxs-lookup"><span data-stu-id="e915b-129">-Proxy</span></span>
<span data-ttu-id="e915b-130">Proxy Server-Details, die beim Senden einer Anforderung an das Back-End verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e915b-130">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="e915b-131">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="e915b-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="e915b-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e915b-132">-ResourceId</span></span>
<span data-ttu-id="e915b-133">Verwaltungs-URI der Ressource im externen System.</span><span class="sxs-lookup"><span data-stu-id="e915b-133">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="e915b-134">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="e915b-134">This parameter is optional.</span></span>
<span data-ttu-id="e915b-135">Diese URL kann die Arm-Ressourcen-ID von Logik-apps, Funktions-Apps oder API-apps sein.</span><span class="sxs-lookup"><span data-stu-id="e915b-135">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="e915b-136">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="e915b-136">-ServiceFabricCluster</span></span>
<span data-ttu-id="e915b-137">Details zum Back-Fabric-Cluster-Back-End</span><span class="sxs-lookup"><span data-stu-id="e915b-137">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="e915b-138">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="e915b-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="e915b-139">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="e915b-139">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="e915b-140">Gibt an, ob die Zertifikatkettenüberprüfung beim Gespräch mit dem Back-End übersprungen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e915b-140">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="e915b-141">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="e915b-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="e915b-142">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="e915b-142">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="e915b-143">Gibt an, ob die Zertifikatnamen Überprüfung beim Gespräch mit dem Back-End übersprungen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e915b-143">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="e915b-144">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="e915b-144">This parameter is optional.</span></span>

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

### <span data-ttu-id="e915b-145">-Title</span><span class="sxs-lookup"><span data-stu-id="e915b-145">-Title</span></span>
<span data-ttu-id="e915b-146">Back-End-Titel.</span><span class="sxs-lookup"><span data-stu-id="e915b-146">Backend Title.</span></span>
<span data-ttu-id="e915b-147">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="e915b-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="e915b-148">-URL</span><span class="sxs-lookup"><span data-stu-id="e915b-148">-Url</span></span>
<span data-ttu-id="e915b-149">Laufzeit-URL für das Back-End.</span><span class="sxs-lookup"><span data-stu-id="e915b-149">Runtime Url for the Backend.</span></span>
<span data-ttu-id="e915b-150">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="e915b-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="e915b-151">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e915b-151">-Confirm</span></span>
<span data-ttu-id="e915b-152">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e915b-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e915b-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e915b-153">-WhatIf</span></span>
<span data-ttu-id="e915b-154">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e915b-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e915b-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e915b-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e915b-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e915b-156">CommonParameters</span></span>
<span data-ttu-id="e915b-157">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e915b-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e915b-158">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e915b-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e915b-159">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e915b-159">INPUTS</span></span>

### <span data-ttu-id="e915b-160">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e915b-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e915b-161">System. String</span><span class="sxs-lookup"><span data-stu-id="e915b-161">System.String</span></span>

### <span data-ttu-id="e915b-162">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e915b-162">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e915b-163">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="e915b-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="e915b-164">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="e915b-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="e915b-165">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e915b-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="e915b-166">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="e915b-166">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e915b-167">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e915b-167">OUTPUTS</span></span>

### <span data-ttu-id="e915b-168">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e915b-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="e915b-169">Notizen</span><span class="sxs-lookup"><span data-stu-id="e915b-169">NOTES</span></span>

## <span data-ttu-id="e915b-170">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e915b-170">RELATED LINKS</span></span>

[<span data-ttu-id="e915b-171">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e915b-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="e915b-172">Neu – AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e915b-172">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="e915b-173">Neu – AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="e915b-173">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="e915b-174">Neu – AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="e915b-174">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="e915b-175">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e915b-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
