---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
ms.openlocfilehash: f5cf0d9f80b15f178cb701b4474fa5dc13d957eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658150"
---
# <span data-ttu-id="d5cc6-101">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d5cc6-101">Set-AzApiManagementBackend</span></span>

## <span data-ttu-id="d5cc6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d5cc6-102">SYNOPSIS</span></span>
<span data-ttu-id="d5cc6-103">Aktualisiert ein Back-End.</span><span class="sxs-lookup"><span data-stu-id="d5cc6-103">Updates a Backend.</span></span>

## <span data-ttu-id="d5cc6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5cc6-104">SYNTAX</span></span>

### <span data-ttu-id="d5cc6-105">ContextParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d5cc6-105">ContextParameterSet (Default)</span></span>
```
Set-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5cc6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d5cc6-106">ByInputObject</span></span>
```
Set-AzApiManagementBackend -InputObject <PsApiManagementBackend> [-Protocol <String>] [-Url <String>]
 [-ResourceId <String>] [-Title <String>] [-Description <String>] [-SkipCertificateChainValidation <Boolean>]
 [-SkipCertificateNameValidation <Boolean>] [-Credential <PsApiManagementBackendCredential>]
 [-Proxy <PsApiManagementBackendProxy>] [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5cc6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d5cc6-107">DESCRIPTION</span></span>
<span data-ttu-id="d5cc6-108">Aktualisiert ein vorhandenes Back-End in der API-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="d5cc6-108">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="d5cc6-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d5cc6-109">EXAMPLES</span></span>

### <span data-ttu-id="d5cc6-110">Aktualisiert die Beschreibung des Back-End-123</span><span class="sxs-lookup"><span data-stu-id="d5cc6-110">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="d5cc6-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5cc6-111">PARAMETERS</span></span>

### <span data-ttu-id="d5cc6-112">-Back-End-Nr</span><span class="sxs-lookup"><span data-stu-id="d5cc6-112">-BackendId</span></span>
<span data-ttu-id="d5cc6-113">Bezeichner des neuen Back-Ends.</span><span class="sxs-lookup"><span data-stu-id="d5cc6-113">Identifier of new backend.</span></span>
<span data-ttu-id="d5cc6-114">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d5cc6-114">This parameter is required.</span></span>

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

### <span data-ttu-id="d5cc6-115">-Context</span><span class="sxs-lookup"><span data-stu-id="d5cc6-115">-Context</span></span>
<span data-ttu-id="d5cc6-116">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d5cc6-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d5cc6-117">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d5cc6-117">This parameter is required.</span></span>

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

### <span data-ttu-id="d5cc6-118">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="d5cc6-118">-Credential</span></span>
<span data-ttu-id="d5cc6-119">Anmeldeinformationen, die beim Gespräch mit dem Back-End verwendet werden sollten.</span><span class="sxs-lookup"><span data-stu-id="d5cc6-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="d5cc6-120">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="d5cc6-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="d5cc6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5cc6-121">-DefaultProfile</span></span>
<span data-ttu-id="d5cc6-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d5cc6-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5cc6-123">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d5cc6-123">-Description</span></span>
<span data-ttu-id="d5cc6-124">Back-End-Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="d5cc6-124">Backend Description.</span></span>
<span data-ttu-id="d5cc6-125">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="d5cc6-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="d5cc6-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d5cc6-126">-InputObject</span></span>
<span data-ttu-id="d5cc6-127">Instanz von PsApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="d5cc6-127">Instance of PsApiManagementBackend.</span></span> <span data-ttu-id="d5cc6-128">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d5cc6-128">This parameter is required.</span></span>

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

### <span data-ttu-id="d5cc6-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d5cc6-129">-PassThru</span></span>
<span data-ttu-id="d5cc6-130">Gibt an, dass dieses Cmdlet die  **PsApiManagementBackend** zurückgibt, die von diesem Cmdlet geändert werden.</span><span class="sxs-lookup"><span data-stu-id="d5cc6-130">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d5cc6-131">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="d5cc6-131">-Protocol</span></span>
<span data-ttu-id="d5cc6-132">Back-End-Kommunikationsprotokoll (http oder SOAP).</span><span class="sxs-lookup"><span data-stu-id="d5cc6-132">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="d5cc6-133">Dieser Parameter ist optional</span><span class="sxs-lookup"><span data-stu-id="d5cc6-133">This parameter is optional</span></span>

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

### <span data-ttu-id="d5cc6-134">-Proxy</span><span class="sxs-lookup"><span data-stu-id="d5cc6-134">-Proxy</span></span>
<span data-ttu-id="d5cc6-135">Proxy Server-Details, die beim Senden einer Anforderung an das Back-End verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d5cc6-135">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="d5cc6-136">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="d5cc6-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="d5cc6-137">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d5cc6-137">-ResourceId</span></span>
<span data-ttu-id="d5cc6-138">Verwaltungs-URI der Ressource im externen System.</span><span class="sxs-lookup"><span data-stu-id="d5cc6-138">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="d5cc6-139">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="d5cc6-139">This parameter is optional.</span></span>
<span data-ttu-id="d5cc6-140">Diese URL kann die Arm-Ressourcen-ID von Logik-apps, Funktions-Apps oder API-apps sein.</span><span class="sxs-lookup"><span data-stu-id="d5cc6-140">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="d5cc6-141">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="d5cc6-141">-ServiceFabricCluster</span></span>
<span data-ttu-id="d5cc6-142">Details zum Back-Fabric-Cluster-Back-End</span><span class="sxs-lookup"><span data-stu-id="d5cc6-142">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="d5cc6-143">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="d5cc6-143">This parameter is optional.</span></span>

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

### <span data-ttu-id="d5cc6-144">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="d5cc6-144">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="d5cc6-145">Gibt an, ob die Zertifikatkettenüberprüfung beim Gespräch mit dem Back-End übersprungen werden soll.</span><span class="sxs-lookup"><span data-stu-id="d5cc6-145">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="d5cc6-146">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="d5cc6-146">This parameter is optional.</span></span>

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

### <span data-ttu-id="d5cc6-147">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="d5cc6-147">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="d5cc6-148">Gibt an, ob die Zertifikatnamen Überprüfung beim Gespräch mit dem Back-End übersprungen werden soll.</span><span class="sxs-lookup"><span data-stu-id="d5cc6-148">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="d5cc6-149">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="d5cc6-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="d5cc6-150">-Title</span><span class="sxs-lookup"><span data-stu-id="d5cc6-150">-Title</span></span>
<span data-ttu-id="d5cc6-151">Back-End-Titel.</span><span class="sxs-lookup"><span data-stu-id="d5cc6-151">Backend Title.</span></span>
<span data-ttu-id="d5cc6-152">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="d5cc6-152">This parameter is optional.</span></span>

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

### <span data-ttu-id="d5cc6-153">-URL</span><span class="sxs-lookup"><span data-stu-id="d5cc6-153">-Url</span></span>
<span data-ttu-id="d5cc6-154">Laufzeit-URL für das Back-End.</span><span class="sxs-lookup"><span data-stu-id="d5cc6-154">Runtime Url for the Backend.</span></span>
<span data-ttu-id="d5cc6-155">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="d5cc6-155">This parameter is optional.</span></span>

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

### <span data-ttu-id="d5cc6-156">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d5cc6-156">-Confirm</span></span>
<span data-ttu-id="d5cc6-157">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d5cc6-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5cc6-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5cc6-158">-WhatIf</span></span>
<span data-ttu-id="d5cc6-159">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d5cc6-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d5cc6-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d5cc6-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5cc6-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5cc6-161">CommonParameters</span></span>
<span data-ttu-id="d5cc6-162">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5cc6-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5cc6-163">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d5cc6-163">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5cc6-164">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d5cc6-164">INPUTS</span></span>

### <span data-ttu-id="d5cc6-165">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d5cc6-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d5cc6-166">System. String</span><span class="sxs-lookup"><span data-stu-id="d5cc6-166">System.String</span></span>

### <span data-ttu-id="d5cc6-167">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d5cc6-167">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d5cc6-168">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="d5cc6-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="d5cc6-169">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="d5cc6-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="d5cc6-170">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="d5cc6-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="d5cc6-171">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="d5cc6-171">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d5cc6-172">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d5cc6-172">OUTPUTS</span></span>

### <span data-ttu-id="d5cc6-173">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d5cc6-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="d5cc6-174">Notizen</span><span class="sxs-lookup"><span data-stu-id="d5cc6-174">NOTES</span></span>

## <span data-ttu-id="d5cc6-175">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d5cc6-175">RELATED LINKS</span></span>

[<span data-ttu-id="d5cc6-176">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d5cc6-176">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="d5cc6-177">Neu – AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d5cc6-177">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="d5cc6-178">Neu – AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="d5cc6-178">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="d5cc6-179">Neu – AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="d5cc6-179">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="d5cc6-180">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d5cc6-180">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
