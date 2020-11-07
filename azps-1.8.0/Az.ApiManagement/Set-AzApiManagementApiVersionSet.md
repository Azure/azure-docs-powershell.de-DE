---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 32279f3f87ec3653fe4d9aab25a98c90f7642b3b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821015"
---
# <span data-ttu-id="7092b-101">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="7092b-101">Set-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="7092b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7092b-102">SYNOPSIS</span></span>
<span data-ttu-id="7092b-103">Aktualisiert eine API-Version, die im API-Verwaltungskontext gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="7092b-103">Updates an API Version Set in the API Management Context.</span></span>

## <span data-ttu-id="7092b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7092b-104">SYNTAX</span></span>

### <span data-ttu-id="7092b-105">Expanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="7092b-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7092b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7092b-106">ByInputObject</span></span>
```
Set-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7092b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7092b-107">DESCRIPTION</span></span>

<span data-ttu-id="7092b-108">Das Cmdlet " **Satz-AzApiManagementApiVersionSet** " ändert eine Azure API Management API-Versionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="7092b-108">The **Set-AzApiManagementApiVersionSet** cmdlet modifies an Azure API Management API Version Set.</span></span>

## <span data-ttu-id="7092b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7092b-109">EXAMPLES</span></span>

### <span data-ttu-id="7092b-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7092b-110">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId "query-verion-set" -Scheme Header -HeaderName "api-version" -Description "Azure version header string"
```

<span data-ttu-id="7092b-111">Mit diesem Befehl wird eine vorhandene API-Versionsgruppe mit Versionsschema `Header` und dem Header Parameter aktualisiert `api-version` .</span><span class="sxs-lookup"><span data-stu-id="7092b-111">This command updates an existing API Version Set with versioning scheme `Header` and Header parameter `api-version`.</span></span>

## <span data-ttu-id="7092b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7092b-112">PARAMETERS</span></span>

### <span data-ttu-id="7092b-113">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="7092b-113">-ApiVersionSetId</span></span>
<span data-ttu-id="7092b-114">Bezeichner für die neue API-Versionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="7092b-114">Identifier for new API Version Set.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7092b-115">-Context</span><span class="sxs-lookup"><span data-stu-id="7092b-115">-Context</span></span>
<span data-ttu-id="7092b-116">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="7092b-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="7092b-117">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7092b-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7092b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7092b-118">-DefaultProfile</span></span>
<span data-ttu-id="7092b-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7092b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7092b-120">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7092b-120">-Description</span></span>
<span data-ttu-id="7092b-121">Beschreibung der API-Versionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="7092b-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="7092b-122">-Headername</span><span class="sxs-lookup"><span data-stu-id="7092b-122">-HeaderName</span></span>
<span data-ttu-id="7092b-123">Der Header Wert, der die Versionsinformationen enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="7092b-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="7092b-124">Wenn die Kopfzeile des Versionsschemas ausgewählt ist, muss dieser Wert angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7092b-124">If versioning Scheme HEADER is choosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="7092b-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7092b-125">-InputObject</span></span>
<span data-ttu-id="7092b-126">Instanz von PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="7092b-126">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="7092b-127">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7092b-127">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7092b-128">-Name</span><span class="sxs-lookup"><span data-stu-id="7092b-128">-Name</span></span>
<span data-ttu-id="7092b-129">Der Name des ApiVersion-Satzes.</span><span class="sxs-lookup"><span data-stu-id="7092b-129">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="7092b-130">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="7092b-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="7092b-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7092b-131">-PassThru</span></span>
<span data-ttu-id="7092b-132">Wenn angegeben, wird Instanz des Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApiVersionSet-Typs, der die geänderte apiVersionSet darstellt, in die Ausgabe geschrieben.</span><span class="sxs-lookup"><span data-stu-id="7092b-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet type  representing the modified apiVersionSet will be written to output.</span></span>

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

### <span data-ttu-id="7092b-133">-QueryName</span><span class="sxs-lookup"><span data-stu-id="7092b-133">-QueryName</span></span>
<span data-ttu-id="7092b-134">Der Abfragewert, der die Versionsinformationen enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="7092b-134">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="7092b-135">Wenn die Abfrage für das Versionsschema ausgewählt ist, muss dieser Wert angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7092b-135">If versioning Scheme Query is choosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="7092b-136">-Scheme</span><span class="sxs-lookup"><span data-stu-id="7092b-136">-Scheme</span></span>
<span data-ttu-id="7092b-137">Versions Verwaltungsschema, das für den API-Versions Verwaltungssatz ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="7092b-137">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="7092b-138">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="7092b-138">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme
Parameter Sets: (All)
Aliases:
Accepted values: Segment, Query, Header

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7092b-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7092b-139">-Confirm</span></span>
<span data-ttu-id="7092b-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7092b-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7092b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7092b-141">-WhatIf</span></span>
<span data-ttu-id="7092b-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7092b-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7092b-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7092b-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7092b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7092b-144">CommonParameters</span></span>
<span data-ttu-id="7092b-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7092b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7092b-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7092b-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7092b-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7092b-147">INPUTS</span></span>

### <span data-ttu-id="7092b-148">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7092b-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7092b-149">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="7092b-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="7092b-150">System. String</span><span class="sxs-lookup"><span data-stu-id="7092b-150">System.String</span></span>

### <span data-ttu-id="7092b-151">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="7092b-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="7092b-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7092b-152">OUTPUTS</span></span>

### <span data-ttu-id="7092b-153">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="7092b-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="7092b-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="7092b-154">NOTES</span></span>

## <span data-ttu-id="7092b-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7092b-155">RELATED LINKS</span></span>

[<span data-ttu-id="7092b-156">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="7092b-156">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="7092b-157">Neu – AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="7092b-157">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="7092b-158">Satz-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="7092b-158">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)
