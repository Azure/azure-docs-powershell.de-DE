---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
ms.openlocfilehash: 46e0a864bcedd8ac0c23761545f5480eaa4a093a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480658"
---
# <span data-ttu-id="aeefd-101">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="aeefd-101">New-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="aeefd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aeefd-102">SYNOPSIS</span></span>
<span data-ttu-id="aeefd-103">Erstellt eine neue Back-End-Entität.</span><span class="sxs-lookup"><span data-stu-id="aeefd-103">Creates a new backend entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aeefd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aeefd-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aeefd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aeefd-105">DESCRIPTION</span></span>
<span data-ttu-id="aeefd-106">Erstellt eine neue Back-End-Entität in der API-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="aeefd-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="aeefd-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aeefd-107">EXAMPLES</span></span>

### <span data-ttu-id="aeefd-108">Erstellen von Back-End-123 mit einem einfachen Autorisierungsschema</span><span class="sxs-lookup"><span data-stu-id="aeefd-108">Create Backend 123 with a Basic Authorization Scheme</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="aeefd-109">Erstellt ein neues Back-End</span><span class="sxs-lookup"><span data-stu-id="aeefd-109">Creates a new Backend</span></span>

## <span data-ttu-id="aeefd-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="aeefd-110">PARAMETERS</span></span>

### <span data-ttu-id="aeefd-111">-Back-End-Nr</span><span class="sxs-lookup"><span data-stu-id="aeefd-111">-BackendId</span></span>
<span data-ttu-id="aeefd-112">Bezeichner des neuen Back-Ends.</span><span class="sxs-lookup"><span data-stu-id="aeefd-112">Identifier of new backend.</span></span>
<span data-ttu-id="aeefd-113">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="aeefd-113">This parameter is optional.</span></span>
<span data-ttu-id="aeefd-114">Wenn nicht angegeben, wird generiert.</span><span class="sxs-lookup"><span data-stu-id="aeefd-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="aeefd-115">-Context</span><span class="sxs-lookup"><span data-stu-id="aeefd-115">-Context</span></span>
<span data-ttu-id="aeefd-116">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="aeefd-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="aeefd-117">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="aeefd-117">This parameter is required.</span></span>

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

### <span data-ttu-id="aeefd-118">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="aeefd-118">-Credential</span></span>
<span data-ttu-id="aeefd-119">Anmeldeinformationen, die beim Gespräch mit dem Back-End verwendet werden sollten.</span><span class="sxs-lookup"><span data-stu-id="aeefd-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="aeefd-120">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="aeefd-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="aeefd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aeefd-121">-DefaultProfile</span></span>
<span data-ttu-id="aeefd-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="aeefd-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aeefd-123">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aeefd-123">-Description</span></span>
<span data-ttu-id="aeefd-124">Back-End-Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="aeefd-124">Backend Description.</span></span>
<span data-ttu-id="aeefd-125">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="aeefd-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="aeefd-126">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="aeefd-126">-Protocol</span></span>
<span data-ttu-id="aeefd-127">Back-End-Kommunikationsprotokoll.</span><span class="sxs-lookup"><span data-stu-id="aeefd-127">Backend Communication protocol.</span></span>
<span data-ttu-id="aeefd-128">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="aeefd-128">This parameter is required.</span></span>
<span data-ttu-id="aeefd-129">Gültige Werte sind "http" und "SOAP".</span><span class="sxs-lookup"><span data-stu-id="aeefd-129">Valid values are 'http' and 'soap'.</span></span>

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

### <span data-ttu-id="aeefd-130">-Proxy</span><span class="sxs-lookup"><span data-stu-id="aeefd-130">-Proxy</span></span>
<span data-ttu-id="aeefd-131">Proxy Server-Details, die beim Senden einer Anforderung an das Back-End verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aeefd-131">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="aeefd-132">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="aeefd-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="aeefd-133">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="aeefd-133">-ResourceId</span></span>
<span data-ttu-id="aeefd-134">Verwaltungs-URI der Ressource im externen System.</span><span class="sxs-lookup"><span data-stu-id="aeefd-134">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="aeefd-135">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="aeefd-135">This parameter is optional.</span></span>
<span data-ttu-id="aeefd-136">Diese URL kann die Arm-Ressourcen-ID von Logik-apps, Funktions-Apps oder API-apps sein.</span><span class="sxs-lookup"><span data-stu-id="aeefd-136">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="aeefd-137">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="aeefd-137">-ServiceFabricCluster</span></span>
<span data-ttu-id="aeefd-138">Details zum Back-Fabric-Cluster-Back-End</span><span class="sxs-lookup"><span data-stu-id="aeefd-138">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="aeefd-139">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="aeefd-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="aeefd-140">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="aeefd-140">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="aeefd-141">Gibt an, ob die Zertifikatkettenüberprüfung beim Gespräch mit dem Back-End übersprungen werden soll.</span><span class="sxs-lookup"><span data-stu-id="aeefd-141">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="aeefd-142">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="aeefd-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="aeefd-143">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="aeefd-143">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="aeefd-144">Gibt an, ob die Zertifikatnamen Überprüfung beim Gespräch mit dem Back-End übersprungen werden soll.</span><span class="sxs-lookup"><span data-stu-id="aeefd-144">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="aeefd-145">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="aeefd-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="aeefd-146">-Title</span><span class="sxs-lookup"><span data-stu-id="aeefd-146">-Title</span></span>
<span data-ttu-id="aeefd-147">Back-End-Titel.</span><span class="sxs-lookup"><span data-stu-id="aeefd-147">Backend Title.</span></span>
<span data-ttu-id="aeefd-148">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="aeefd-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="aeefd-149">-URL</span><span class="sxs-lookup"><span data-stu-id="aeefd-149">-Url</span></span>
<span data-ttu-id="aeefd-150">Laufzeit-URL für das Back-End.</span><span class="sxs-lookup"><span data-stu-id="aeefd-150">Runtime Url for the Backend.</span></span>
<span data-ttu-id="aeefd-151">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="aeefd-151">This parameter is required.</span></span>

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

### <span data-ttu-id="aeefd-152">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="aeefd-152">-Confirm</span></span>
<span data-ttu-id="aeefd-153">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aeefd-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aeefd-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aeefd-154">-WhatIf</span></span>
<span data-ttu-id="aeefd-155">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aeefd-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aeefd-156">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aeefd-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aeefd-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeefd-157">CommonParameters</span></span>
<span data-ttu-id="aeefd-158">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aeefd-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeefd-159">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aeefd-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeefd-160">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aeefd-160">INPUTS</span></span>

### <span data-ttu-id="aeefd-161">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="aeefd-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="aeefd-162">System. String</span><span class="sxs-lookup"><span data-stu-id="aeefd-162">System.String</span></span>

### <span data-ttu-id="aeefd-163">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="aeefd-163">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="aeefd-164">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="aeefd-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="aeefd-165">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="aeefd-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="aeefd-166">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="aeefd-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="aeefd-167">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aeefd-167">OUTPUTS</span></span>

### <span data-ttu-id="aeefd-168">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="aeefd-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="aeefd-169">Notizen</span><span class="sxs-lookup"><span data-stu-id="aeefd-169">NOTES</span></span>

## <span data-ttu-id="aeefd-170">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aeefd-170">RELATED LINKS</span></span>

[<span data-ttu-id="aeefd-171">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="aeefd-171">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="aeefd-172">Neu – AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="aeefd-172">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="aeefd-173">Neu – AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="aeefd-173">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="aeefd-174">Satz-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="aeefd-174">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="aeefd-175">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="aeefd-175">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)

