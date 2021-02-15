---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
ms.openlocfilehash: 0ac89ed099029fbbabe90e07da7ba9c204449db9
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400738"
---
# <span data-ttu-id="704ba-101">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="704ba-101">Set-AzApiManagementBackend</span></span>

## <span data-ttu-id="704ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="704ba-102">SYNOPSIS</span></span>
<span data-ttu-id="704ba-103">Aktualisiert ein Back-End.</span><span class="sxs-lookup"><span data-stu-id="704ba-103">Updates a Backend.</span></span>

## <span data-ttu-id="704ba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="704ba-104">SYNTAX</span></span>

```
Set-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="704ba-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="704ba-105">DESCRIPTION</span></span>
<span data-ttu-id="704ba-106">Aktualisiert ein vorhandenes Back-End in der Api-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="704ba-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="704ba-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="704ba-107">EXAMPLES</span></span>

### <span data-ttu-id="704ba-108">Aktualisiert die Beschreibung von Back-End 123</span><span class="sxs-lookup"><span data-stu-id="704ba-108">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="704ba-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="704ba-109">PARAMETERS</span></span>

### <span data-ttu-id="704ba-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="704ba-110">-BackendId</span></span>
<span data-ttu-id="704ba-111">Bezeichner des neuen Backends.</span><span class="sxs-lookup"><span data-stu-id="704ba-111">Identifier of new backend.</span></span>
<span data-ttu-id="704ba-112">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="704ba-112">This parameter is required.</span></span>

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

### <span data-ttu-id="704ba-113">-Context</span><span class="sxs-lookup"><span data-stu-id="704ba-113">-Context</span></span>
<span data-ttu-id="704ba-114">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="704ba-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="704ba-115">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="704ba-115">This parameter is required.</span></span>

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

### <span data-ttu-id="704ba-116">-Credential</span><span class="sxs-lookup"><span data-stu-id="704ba-116">-Credential</span></span>
<span data-ttu-id="704ba-117">Anmeldeinformationen, die verwendet werden sollten, wenn Sie mit dem Back-End sprechen.</span><span class="sxs-lookup"><span data-stu-id="704ba-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="704ba-118">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="704ba-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="704ba-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="704ba-119">-DefaultProfile</span></span>
<span data-ttu-id="704ba-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="704ba-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="704ba-121">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="704ba-121">-Description</span></span>
<span data-ttu-id="704ba-122">Back-End-Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="704ba-122">Backend Description.</span></span>
<span data-ttu-id="704ba-123">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="704ba-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="704ba-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="704ba-124">-PassThru</span></span>
<span data-ttu-id="704ba-125">Gibt an, dass dieses Cmdlet den  **PsApiManagementBackend zurückgibt,** den dieses Cmdlet ändert.</span><span class="sxs-lookup"><span data-stu-id="704ba-125">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="704ba-126">-Protocol</span><span class="sxs-lookup"><span data-stu-id="704ba-126">-Protocol</span></span>
<span data-ttu-id="704ba-127">Back-End-Kommunikationsprotokoll (http oder soap).</span><span class="sxs-lookup"><span data-stu-id="704ba-127">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="704ba-128">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="704ba-128">This parameter is optional</span></span>

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

### <span data-ttu-id="704ba-129">-Proxy</span><span class="sxs-lookup"><span data-stu-id="704ba-129">-Proxy</span></span>
<span data-ttu-id="704ba-130">Proxyserverdetails, die beim Senden einer Anforderung an das Back-End verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="704ba-130">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="704ba-131">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="704ba-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="704ba-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="704ba-132">-ResourceId</span></span>
<span data-ttu-id="704ba-133">Verwaltungs-URI der Ressource im externen System.</span><span class="sxs-lookup"><span data-stu-id="704ba-133">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="704ba-134">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="704ba-134">This parameter is optional.</span></span>
<span data-ttu-id="704ba-135">Diese URL kann die Arm-Ressourcen-ID von Logik-Apps, Funktions- oder Api-Apps sein.</span><span class="sxs-lookup"><span data-stu-id="704ba-135">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="704ba-136">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="704ba-136">-ServiceFabricCluster</span></span>
<span data-ttu-id="704ba-137">Service Fabric Cluster Back-End-Details.</span><span class="sxs-lookup"><span data-stu-id="704ba-137">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="704ba-138">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="704ba-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="704ba-139">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="704ba-139">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="704ba-140">Gibt an, ob die Zertifikatkettenüberprüfung beim Sprechen mit dem Back-End übersprungen werden soll.</span><span class="sxs-lookup"><span data-stu-id="704ba-140">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="704ba-141">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="704ba-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="704ba-142">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="704ba-142">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="704ba-143">Gibt an, ob die Zertifikatnamenüberprüfung beim Gespräch mit dem Backend übersprungen werden soll.</span><span class="sxs-lookup"><span data-stu-id="704ba-143">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="704ba-144">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="704ba-144">This parameter is optional.</span></span>

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

### <span data-ttu-id="704ba-145">-Title</span><span class="sxs-lookup"><span data-stu-id="704ba-145">-Title</span></span>
<span data-ttu-id="704ba-146">Back-End-Titel.</span><span class="sxs-lookup"><span data-stu-id="704ba-146">Backend Title.</span></span>
<span data-ttu-id="704ba-147">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="704ba-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="704ba-148">-URL</span><span class="sxs-lookup"><span data-stu-id="704ba-148">-Url</span></span>
<span data-ttu-id="704ba-149">Laufzeit-URL für das Back-End.</span><span class="sxs-lookup"><span data-stu-id="704ba-149">Runtime Url for the Backend.</span></span>
<span data-ttu-id="704ba-150">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="704ba-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="704ba-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="704ba-151">-Confirm</span></span>
<span data-ttu-id="704ba-152">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="704ba-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="704ba-153">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="704ba-153">-WhatIf</span></span>
<span data-ttu-id="704ba-154">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="704ba-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="704ba-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="704ba-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="704ba-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="704ba-156">CommonParameters</span></span>
<span data-ttu-id="704ba-157">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="704ba-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="704ba-158">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="704ba-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="704ba-159">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="704ba-159">INPUTS</span></span>

### <span data-ttu-id="704ba-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="704ba-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="704ba-161">System.String</span><span class="sxs-lookup"><span data-stu-id="704ba-161">System.String</span></span>

### <span data-ttu-id="704ba-162">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="704ba-162">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="704ba-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="704ba-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="704ba-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="704ba-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="704ba-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="704ba-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="704ba-166">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="704ba-166">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="704ba-167">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="704ba-167">OUTPUTS</span></span>

### <span data-ttu-id="704ba-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="704ba-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="704ba-169">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="704ba-169">NOTES</span></span>

## <span data-ttu-id="704ba-170">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="704ba-170">RELATED LINKS</span></span>

[<span data-ttu-id="704ba-171">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="704ba-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="704ba-172">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="704ba-172">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="704ba-173">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="704ba-173">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="704ba-174">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="704ba-174">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="704ba-175">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="704ba-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
