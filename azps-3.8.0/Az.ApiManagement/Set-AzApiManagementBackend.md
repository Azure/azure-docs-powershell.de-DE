---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
ms.openlocfilehash: 30947e52e5a7afaa8bf2890b95f48f6bb6f36bce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004065"
---
# <span data-ttu-id="62808-101">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="62808-101">Set-AzApiManagementBackend</span></span>

## <span data-ttu-id="62808-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="62808-102">SYNOPSIS</span></span>
<span data-ttu-id="62808-103">Aktualisiert ein Back-End.</span><span class="sxs-lookup"><span data-stu-id="62808-103">Updates a Backend.</span></span>

## <span data-ttu-id="62808-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="62808-104">SYNTAX</span></span>

### <span data-ttu-id="62808-105">ContextParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="62808-105">ContextParameterSet (Default)</span></span>
```
Set-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62808-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="62808-106">ByInputObject</span></span>
```
Set-AzApiManagementBackend -InputObject <PsApiManagementBackend> [-Protocol <String>] [-Url <String>]
 [-ResourceId <String>] [-Title <String>] [-Description <String>] [-SkipCertificateChainValidation <Boolean>]
 [-SkipCertificateNameValidation <Boolean>] [-Credential <PsApiManagementBackendCredential>]
 [-Proxy <PsApiManagementBackendProxy>] [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62808-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="62808-107">DESCRIPTION</span></span>
<span data-ttu-id="62808-108">Aktualisiert ein vorhandenes Back-End in der API-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="62808-108">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="62808-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="62808-109">EXAMPLES</span></span>

### <span data-ttu-id="62808-110">Aktualisiert die Beschreibung des Back-End-123</span><span class="sxs-lookup"><span data-stu-id="62808-110">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="62808-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="62808-111">PARAMETERS</span></span>

### <span data-ttu-id="62808-112">-Back-End-Nr</span><span class="sxs-lookup"><span data-stu-id="62808-112">-BackendId</span></span>
<span data-ttu-id="62808-113">Bezeichner des neuen Back-Ends.</span><span class="sxs-lookup"><span data-stu-id="62808-113">Identifier of new backend.</span></span>
<span data-ttu-id="62808-114">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="62808-114">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62808-115">-Context</span><span class="sxs-lookup"><span data-stu-id="62808-115">-Context</span></span>
<span data-ttu-id="62808-116">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="62808-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="62808-117">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="62808-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62808-118">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="62808-118">-Credential</span></span>
<span data-ttu-id="62808-119">Anmeldeinformationen, die beim Gespräch mit dem Back-End verwendet werden sollten.</span><span class="sxs-lookup"><span data-stu-id="62808-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="62808-120">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="62808-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="62808-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62808-121">-DefaultProfile</span></span>
<span data-ttu-id="62808-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="62808-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62808-123">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="62808-123">-Description</span></span>
<span data-ttu-id="62808-124">Back-End-Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="62808-124">Backend Description.</span></span>
<span data-ttu-id="62808-125">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="62808-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="62808-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="62808-126">-InputObject</span></span>
<span data-ttu-id="62808-127">Instanz von PsApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="62808-127">Instance of PsApiManagementBackend.</span></span> <span data-ttu-id="62808-128">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="62808-128">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62808-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62808-129">-PassThru</span></span>
<span data-ttu-id="62808-130">Gibt an, dass dieses Cmdlet die  **PsApiManagementBackend** zurückgibt, die von diesem Cmdlet geändert werden.</span><span class="sxs-lookup"><span data-stu-id="62808-130">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="62808-131">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="62808-131">-Protocol</span></span>
<span data-ttu-id="62808-132">Back-End-Kommunikationsprotokoll (http oder SOAP).</span><span class="sxs-lookup"><span data-stu-id="62808-132">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="62808-133">Dieser Parameter ist optional</span><span class="sxs-lookup"><span data-stu-id="62808-133">This parameter is optional</span></span>

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

### <span data-ttu-id="62808-134">-Proxy</span><span class="sxs-lookup"><span data-stu-id="62808-134">-Proxy</span></span>
<span data-ttu-id="62808-135">Proxy Server-Details, die beim Senden einer Anforderung an das Back-End verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="62808-135">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="62808-136">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="62808-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="62808-137">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="62808-137">-ResourceId</span></span>
<span data-ttu-id="62808-138">Verwaltungs-URI der Ressource im externen System.</span><span class="sxs-lookup"><span data-stu-id="62808-138">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="62808-139">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="62808-139">This parameter is optional.</span></span>
<span data-ttu-id="62808-140">Diese URL kann die Arm-Ressourcen-ID von Logik-apps, Funktions-Apps oder API-apps sein.</span><span class="sxs-lookup"><span data-stu-id="62808-140">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="62808-141">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="62808-141">-ServiceFabricCluster</span></span>
<span data-ttu-id="62808-142">Details zum Back-Fabric-Cluster-Back-End</span><span class="sxs-lookup"><span data-stu-id="62808-142">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="62808-143">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="62808-143">This parameter is optional.</span></span>

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

### <span data-ttu-id="62808-144">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="62808-144">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="62808-145">Gibt an, ob die Zertifikatkettenüberprüfung beim Gespräch mit dem Back-End übersprungen werden soll.</span><span class="sxs-lookup"><span data-stu-id="62808-145">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="62808-146">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="62808-146">This parameter is optional.</span></span>

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

### <span data-ttu-id="62808-147">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="62808-147">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="62808-148">Gibt an, ob die Zertifikatnamen Überprüfung beim Gespräch mit dem Back-End übersprungen werden soll.</span><span class="sxs-lookup"><span data-stu-id="62808-148">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="62808-149">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="62808-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="62808-150">-Title</span><span class="sxs-lookup"><span data-stu-id="62808-150">-Title</span></span>
<span data-ttu-id="62808-151">Back-End-Titel.</span><span class="sxs-lookup"><span data-stu-id="62808-151">Backend Title.</span></span>
<span data-ttu-id="62808-152">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="62808-152">This parameter is optional.</span></span>

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

### <span data-ttu-id="62808-153">-URL</span><span class="sxs-lookup"><span data-stu-id="62808-153">-Url</span></span>
<span data-ttu-id="62808-154">Laufzeit-URL für das Back-End.</span><span class="sxs-lookup"><span data-stu-id="62808-154">Runtime Url for the Backend.</span></span>
<span data-ttu-id="62808-155">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="62808-155">This parameter is optional.</span></span>

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

### <span data-ttu-id="62808-156">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="62808-156">-Confirm</span></span>
<span data-ttu-id="62808-157">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="62808-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62808-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62808-158">-WhatIf</span></span>
<span data-ttu-id="62808-159">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="62808-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="62808-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="62808-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62808-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62808-161">CommonParameters</span></span>
<span data-ttu-id="62808-162">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62808-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62808-163">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="62808-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62808-164">Eingaben</span><span class="sxs-lookup"><span data-stu-id="62808-164">INPUTS</span></span>

### <span data-ttu-id="62808-165">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="62808-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="62808-166">System. String</span><span class="sxs-lookup"><span data-stu-id="62808-166">System.String</span></span>

### <span data-ttu-id="62808-167">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="62808-167">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="62808-168">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="62808-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="62808-169">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="62808-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="62808-170">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="62808-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="62808-171">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="62808-171">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="62808-172">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="62808-172">OUTPUTS</span></span>

### <span data-ttu-id="62808-173">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="62808-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="62808-174">Notizen</span><span class="sxs-lookup"><span data-stu-id="62808-174">NOTES</span></span>

## <span data-ttu-id="62808-175">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="62808-175">RELATED LINKS</span></span>

[<span data-ttu-id="62808-176">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="62808-176">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="62808-177">Neu – AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="62808-177">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="62808-178">Neu – AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="62808-178">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="62808-179">Neu – AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="62808-179">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="62808-180">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="62808-180">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
