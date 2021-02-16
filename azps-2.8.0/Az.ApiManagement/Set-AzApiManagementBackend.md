---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
ms.openlocfilehash: cb7348e31ca80834836b27c97aa7f68e4207ed24
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404325"
---
# <span data-ttu-id="c65e2-101">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="c65e2-101">Set-AzApiManagementBackend</span></span>

## <span data-ttu-id="c65e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c65e2-102">SYNOPSIS</span></span>
<span data-ttu-id="c65e2-103">Aktualisiert ein Back-End.</span><span class="sxs-lookup"><span data-stu-id="c65e2-103">Updates a Backend.</span></span>

## <span data-ttu-id="c65e2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c65e2-104">SYNTAX</span></span>

### <span data-ttu-id="c65e2-105">ContextParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c65e2-105">ContextParameterSet (Default)</span></span>
```
Set-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c65e2-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c65e2-106">ByInputObject</span></span>
```
Set-AzApiManagementBackend -InputObject <PsApiManagementBackend> [-Protocol <String>] [-Url <String>]
 [-ResourceId <String>] [-Title <String>] [-Description <String>] [-SkipCertificateChainValidation <Boolean>]
 [-SkipCertificateNameValidation <Boolean>] [-Credential <PsApiManagementBackendCredential>]
 [-Proxy <PsApiManagementBackendProxy>] [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c65e2-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c65e2-107">DESCRIPTION</span></span>
<span data-ttu-id="c65e2-108">Aktualisiert ein vorhandenes Back-End in der Api-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="c65e2-108">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="c65e2-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c65e2-109">EXAMPLES</span></span>

### <span data-ttu-id="c65e2-110">Aktualisiert die Beschreibung von Back-End 123</span><span class="sxs-lookup"><span data-stu-id="c65e2-110">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="c65e2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c65e2-111">PARAMETERS</span></span>

### <span data-ttu-id="c65e2-112">-BackendId</span><span class="sxs-lookup"><span data-stu-id="c65e2-112">-BackendId</span></span>
<span data-ttu-id="c65e2-113">Bezeichner des neuen Backends.</span><span class="sxs-lookup"><span data-stu-id="c65e2-113">Identifier of new backend.</span></span>
<span data-ttu-id="c65e2-114">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c65e2-114">This parameter is required.</span></span>

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

### <span data-ttu-id="c65e2-115">-Context</span><span class="sxs-lookup"><span data-stu-id="c65e2-115">-Context</span></span>
<span data-ttu-id="c65e2-116">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c65e2-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c65e2-117">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c65e2-117">This parameter is required.</span></span>

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

### <span data-ttu-id="c65e2-118">-Credential</span><span class="sxs-lookup"><span data-stu-id="c65e2-118">-Credential</span></span>
<span data-ttu-id="c65e2-119">Anmeldeinformationen, die verwendet werden sollten, wenn Sie mit dem Back-End sprechen.</span><span class="sxs-lookup"><span data-stu-id="c65e2-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="c65e2-120">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="c65e2-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="c65e2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c65e2-121">-DefaultProfile</span></span>
<span data-ttu-id="c65e2-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c65e2-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c65e2-123">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c65e2-123">-Description</span></span>
<span data-ttu-id="c65e2-124">Back-End-Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="c65e2-124">Backend Description.</span></span>
<span data-ttu-id="c65e2-125">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="c65e2-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="c65e2-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c65e2-126">-InputObject</span></span>
<span data-ttu-id="c65e2-127">Instanz von PsApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="c65e2-127">Instance of PsApiManagementBackend.</span></span> <span data-ttu-id="c65e2-128">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c65e2-128">This parameter is required.</span></span>

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

### <span data-ttu-id="c65e2-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c65e2-129">-PassThru</span></span>
<span data-ttu-id="c65e2-130">Gibt an, dass dieses Cmdlet den  **PsApiManagementBackend zurückgibt,** den dieses Cmdlet ändert.</span><span class="sxs-lookup"><span data-stu-id="c65e2-130">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c65e2-131">-Protocol</span><span class="sxs-lookup"><span data-stu-id="c65e2-131">-Protocol</span></span>
<span data-ttu-id="c65e2-132">Back-End-Kommunikationsprotokoll (http oder soap).</span><span class="sxs-lookup"><span data-stu-id="c65e2-132">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="c65e2-133">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="c65e2-133">This parameter is optional</span></span>

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

### <span data-ttu-id="c65e2-134">-Proxy</span><span class="sxs-lookup"><span data-stu-id="c65e2-134">-Proxy</span></span>
<span data-ttu-id="c65e2-135">Proxyserverdetails, die beim Senden einer Anforderung an das Back-End verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c65e2-135">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="c65e2-136">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="c65e2-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="c65e2-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c65e2-137">-ResourceId</span></span>
<span data-ttu-id="c65e2-138">Verwaltungs-URI der Ressource im externen System.</span><span class="sxs-lookup"><span data-stu-id="c65e2-138">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="c65e2-139">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="c65e2-139">This parameter is optional.</span></span>
<span data-ttu-id="c65e2-140">Diese URL kann die Arm-Ressourcen-ID von Logik-Apps, Funktions- oder Api-Apps sein.</span><span class="sxs-lookup"><span data-stu-id="c65e2-140">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="c65e2-141">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="c65e2-141">-ServiceFabricCluster</span></span>
<span data-ttu-id="c65e2-142">Service Fabric Cluster Back-End-Details.</span><span class="sxs-lookup"><span data-stu-id="c65e2-142">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="c65e2-143">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="c65e2-143">This parameter is optional.</span></span>

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

### <span data-ttu-id="c65e2-144">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="c65e2-144">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="c65e2-145">Gibt an, ob die Zertifikatkettenüberprüfung beim Sprechen mit dem Back-End übersprungen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c65e2-145">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="c65e2-146">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="c65e2-146">This parameter is optional.</span></span>

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

### <span data-ttu-id="c65e2-147">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="c65e2-147">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="c65e2-148">Gibt an, ob die Zertifikatnamenüberprüfung beim Gespräch mit dem Backend übersprungen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c65e2-148">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="c65e2-149">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="c65e2-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="c65e2-150">-Title</span><span class="sxs-lookup"><span data-stu-id="c65e2-150">-Title</span></span>
<span data-ttu-id="c65e2-151">Back-End-Titel.</span><span class="sxs-lookup"><span data-stu-id="c65e2-151">Backend Title.</span></span>
<span data-ttu-id="c65e2-152">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="c65e2-152">This parameter is optional.</span></span>

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

### <span data-ttu-id="c65e2-153">-URL</span><span class="sxs-lookup"><span data-stu-id="c65e2-153">-Url</span></span>
<span data-ttu-id="c65e2-154">Laufzeit-URL für das Back-End.</span><span class="sxs-lookup"><span data-stu-id="c65e2-154">Runtime Url for the Backend.</span></span>
<span data-ttu-id="c65e2-155">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="c65e2-155">This parameter is optional.</span></span>

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

### <span data-ttu-id="c65e2-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c65e2-156">-Confirm</span></span>
<span data-ttu-id="c65e2-157">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c65e2-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c65e2-158">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c65e2-158">-WhatIf</span></span>
<span data-ttu-id="c65e2-159">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c65e2-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c65e2-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c65e2-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c65e2-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c65e2-161">CommonParameters</span></span>
<span data-ttu-id="c65e2-162">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c65e2-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c65e2-163">Weitere Informationen finden Sie unter [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c65e2-163">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c65e2-164">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c65e2-164">INPUTS</span></span>

### <span data-ttu-id="c65e2-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c65e2-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c65e2-166">System.String</span><span class="sxs-lookup"><span data-stu-id="c65e2-166">System.String</span></span>

### <span data-ttu-id="c65e2-167">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c65e2-167">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c65e2-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="c65e2-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="c65e2-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="c65e2-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="c65e2-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c65e2-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="c65e2-171">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c65e2-171">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c65e2-172">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c65e2-172">OUTPUTS</span></span>

### <span data-ttu-id="c65e2-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="c65e2-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="c65e2-174">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c65e2-174">NOTES</span></span>

## <span data-ttu-id="c65e2-175">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c65e2-175">RELATED LINKS</span></span>

[<span data-ttu-id="c65e2-176">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="c65e2-176">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="c65e2-177">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="c65e2-177">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="c65e2-178">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="c65e2-178">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="c65e2-179">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="c65e2-179">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="c65e2-180">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="c65e2-180">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
