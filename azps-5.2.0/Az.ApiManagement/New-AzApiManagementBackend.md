---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
ms.openlocfilehash: 4ed63d0e3b801572698b123038a2022e89672a88
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358404"
---
# <span data-ttu-id="dbfb8-101">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="dbfb8-101">New-AzApiManagementBackend</span></span>

## <span data-ttu-id="dbfb8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbfb8-102">SYNOPSIS</span></span>
<span data-ttu-id="dbfb8-103">Erstellt eine neue Back-End-Entität.</span><span class="sxs-lookup"><span data-stu-id="dbfb8-103">Creates a new backend entity.</span></span>

## <span data-ttu-id="dbfb8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dbfb8-104">SYNTAX</span></span>

```
New-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbfb8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dbfb8-105">DESCRIPTION</span></span>
<span data-ttu-id="dbfb8-106">Erstellt eine neue Back-End-Entität in Api Management.</span><span class="sxs-lookup"><span data-stu-id="dbfb8-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="dbfb8-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dbfb8-107">EXAMPLES</span></span>

### <span data-ttu-id="dbfb8-108">Beispiel 1: Erstellen von Back-End 123 mit einem grundlegenden Autorisierungsschema</span><span class="sxs-lookup"><span data-stu-id="dbfb8-108">Example 1: Create Backend 123 with a Basic Authorization Scheme</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="dbfb8-109">Erstellt ein neues Back-End</span><span class="sxs-lookup"><span data-stu-id="dbfb8-109">Creates a new Backend</span></span>

## <span data-ttu-id="dbfb8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dbfb8-110">PARAMETERS</span></span>

### <span data-ttu-id="dbfb8-111">-BackendId</span><span class="sxs-lookup"><span data-stu-id="dbfb8-111">-BackendId</span></span>
<span data-ttu-id="dbfb8-112">Bezeichner des neuen Backends.</span><span class="sxs-lookup"><span data-stu-id="dbfb8-112">Identifier of new backend.</span></span>
<span data-ttu-id="dbfb8-113">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="dbfb8-113">This parameter is optional.</span></span>
<span data-ttu-id="dbfb8-114">Wenn keine Angabe angegeben wird, wird ein Code generiert.</span><span class="sxs-lookup"><span data-stu-id="dbfb8-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="dbfb8-115">-Context</span><span class="sxs-lookup"><span data-stu-id="dbfb8-115">-Context</span></span>
<span data-ttu-id="dbfb8-116">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="dbfb8-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="dbfb8-117">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="dbfb8-117">This parameter is required.</span></span>

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

### <span data-ttu-id="dbfb8-118">-Credential</span><span class="sxs-lookup"><span data-stu-id="dbfb8-118">-Credential</span></span>
<span data-ttu-id="dbfb8-119">Anmeldeinformationen, die verwendet werden sollten, wenn Sie mit dem Back-End sprechen.</span><span class="sxs-lookup"><span data-stu-id="dbfb8-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="dbfb8-120">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="dbfb8-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="dbfb8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbfb8-121">-DefaultProfile</span></span>
<span data-ttu-id="dbfb8-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dbfb8-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbfb8-123">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dbfb8-123">-Description</span></span>
<span data-ttu-id="dbfb8-124">Back-End-Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="dbfb8-124">Backend Description.</span></span>
<span data-ttu-id="dbfb8-125">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="dbfb8-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="dbfb8-126">-Protocol</span><span class="sxs-lookup"><span data-stu-id="dbfb8-126">-Protocol</span></span>
<span data-ttu-id="dbfb8-127">Back-End-Kommunikationsprotokoll.</span><span class="sxs-lookup"><span data-stu-id="dbfb8-127">Backend Communication protocol.</span></span>
<span data-ttu-id="dbfb8-128">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="dbfb8-128">This parameter is required.</span></span>
<span data-ttu-id="dbfb8-129">Gültige Werte sind "http" und "soap".</span><span class="sxs-lookup"><span data-stu-id="dbfb8-129">Valid values are 'http' and 'soap'.</span></span>

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

### <span data-ttu-id="dbfb8-130">-Proxy</span><span class="sxs-lookup"><span data-stu-id="dbfb8-130">-Proxy</span></span>
<span data-ttu-id="dbfb8-131">Proxyserverdetails, die beim Senden einer Anforderung an das Back-End verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dbfb8-131">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="dbfb8-132">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="dbfb8-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="dbfb8-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dbfb8-133">-ResourceId</span></span>
<span data-ttu-id="dbfb8-134">Verwaltungs-URI der Ressource im externen System.</span><span class="sxs-lookup"><span data-stu-id="dbfb8-134">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="dbfb8-135">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="dbfb8-135">This parameter is optional.</span></span>
<span data-ttu-id="dbfb8-136">Diese URL kann die Arm-Ressourcen-ID von Logik-Apps, Funktions- oder Api-Apps sein.</span><span class="sxs-lookup"><span data-stu-id="dbfb8-136">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="dbfb8-137">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="dbfb8-137">-ServiceFabricCluster</span></span>
<span data-ttu-id="dbfb8-138">Service Fabric Cluster Back-End-Details.</span><span class="sxs-lookup"><span data-stu-id="dbfb8-138">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="dbfb8-139">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="dbfb8-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="dbfb8-140">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="dbfb8-140">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="dbfb8-141">Gibt an, ob die Zertifikatkettenüberprüfung beim Sprechen mit dem Back-End übersprungen werden soll.</span><span class="sxs-lookup"><span data-stu-id="dbfb8-141">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="dbfb8-142">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="dbfb8-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="dbfb8-143">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="dbfb8-143">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="dbfb8-144">Gibt an, ob die Zertifikatnamenüberprüfung beim Gespräch mit dem Backend übersprungen werden soll.</span><span class="sxs-lookup"><span data-stu-id="dbfb8-144">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="dbfb8-145">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="dbfb8-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="dbfb8-146">-Title</span><span class="sxs-lookup"><span data-stu-id="dbfb8-146">-Title</span></span>
<span data-ttu-id="dbfb8-147">Back-End-Titel.</span><span class="sxs-lookup"><span data-stu-id="dbfb8-147">Backend Title.</span></span>
<span data-ttu-id="dbfb8-148">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="dbfb8-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="dbfb8-149">-URL</span><span class="sxs-lookup"><span data-stu-id="dbfb8-149">-Url</span></span>
<span data-ttu-id="dbfb8-150">Laufzeit-URL für das Back-End.</span><span class="sxs-lookup"><span data-stu-id="dbfb8-150">Runtime Url for the Backend.</span></span>
<span data-ttu-id="dbfb8-151">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="dbfb8-151">This parameter is required.</span></span>

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

### <span data-ttu-id="dbfb8-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dbfb8-152">-Confirm</span></span>
<span data-ttu-id="dbfb8-153">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dbfb8-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbfb8-154">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="dbfb8-154">-WhatIf</span></span>
<span data-ttu-id="dbfb8-155">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dbfb8-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dbfb8-156">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dbfb8-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbfb8-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbfb8-157">CommonParameters</span></span>
<span data-ttu-id="dbfb8-158">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbfb8-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbfb8-159">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dbfb8-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbfb8-160">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dbfb8-160">INPUTS</span></span>

### <span data-ttu-id="dbfb8-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="dbfb8-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="dbfb8-162">System.String</span><span class="sxs-lookup"><span data-stu-id="dbfb8-162">System.String</span></span>

### <span data-ttu-id="dbfb8-163">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="dbfb8-163">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="dbfb8-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="dbfb8-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="dbfb8-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="dbfb8-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="dbfb8-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="dbfb8-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="dbfb8-167">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dbfb8-167">OUTPUTS</span></span>

### <span data-ttu-id="dbfb8-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="dbfb8-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="dbfb8-169">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="dbfb8-169">NOTES</span></span>

## <span data-ttu-id="dbfb8-170">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="dbfb8-170">RELATED LINKS</span></span>

[<span data-ttu-id="dbfb8-171">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="dbfb8-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="dbfb8-172">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="dbfb8-172">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="dbfb8-173">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="dbfb8-173">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="dbfb8-174">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="dbfb8-174">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="dbfb8-175">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="dbfb8-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)

