---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 95444b74b3d62dd187a701e2305df2e241ff236f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658273"
---
# <span data-ttu-id="039c7-101">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="039c7-101">New-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="039c7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="039c7-102">SYNOPSIS</span></span>
<span data-ttu-id="039c7-103">Erstellt eine API-Versionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="039c7-103">Creates an API Version Set.</span></span>

## <span data-ttu-id="039c7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="039c7-104">SYNTAX</span></span>

```
New-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>] -Name <String>
 -Scheme <PsApiManagementVersioningScheme> [-HeaderName <String>] [-QueryName <String>] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="039c7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="039c7-105">DESCRIPTION</span></span>
<span data-ttu-id="039c7-106">Das Cmdlet **New-AzApiManagementApiVersionSet** erstellt im Azure API-Verwaltungskontext eine API-Versions Satz Entität.</span><span class="sxs-lookup"><span data-stu-id="039c7-106">The **New-AzApiManagementApiVersionSet** cmdlet creates an API Version set entity in the Azure API Management context.</span></span>

## <span data-ttu-id="039c7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="039c7-107">EXAMPLES</span></span>

### <span data-ttu-id="039c7-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="039c7-108">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> New-AzApiManagementApiVersionSet -Context $ApiMgmtContext  -Name "newversion" -Scheme Header -HeaderName "x-ms-version" -Description "version by xmsversion"

ApiVersionSetId   : ea9a87cd-a699-4a75-bf7d-909846b91268
Description       : version by xmsversion
VersionQueryName  :
VersionHeaderName : x-ms-version
DisplayName       : newversion
VersioningScheme  : Header
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/ea9a87cd-a699-4a75-bf7d-909846b91268
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="039c7-109">Mit diesem Befehl wird eine API-Version erstellt, die das Versionsschema `Query` und den Abfrageparameter definiert `api-version` .</span><span class="sxs-lookup"><span data-stu-id="039c7-109">This command creates an API Version Set which versioning scheme `Query` and Query parameter `api-version`.</span></span>

## <span data-ttu-id="039c7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="039c7-110">PARAMETERS</span></span>

### <span data-ttu-id="039c7-111">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="039c7-111">-ApiVersionSetId</span></span>
<span data-ttu-id="039c7-112">Bezeichner für die neue API-Versionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="039c7-112">Identifier for new API Version Set.</span></span>
<span data-ttu-id="039c7-113">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="039c7-113">This parameter is optional.</span></span>
<span data-ttu-id="039c7-114">Wenn nicht angegeben, wird ein Bezeichner generiert.</span><span class="sxs-lookup"><span data-stu-id="039c7-114">If not specified an identifier will be generated.</span></span>

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

### <span data-ttu-id="039c7-115">-Context</span><span class="sxs-lookup"><span data-stu-id="039c7-115">-Context</span></span>
<span data-ttu-id="039c7-116">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="039c7-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="039c7-117">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="039c7-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="039c7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="039c7-118">-DefaultProfile</span></span>
<span data-ttu-id="039c7-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="039c7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="039c7-120">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="039c7-120">-Description</span></span>
<span data-ttu-id="039c7-121">Beschreibung der API-Versionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="039c7-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="039c7-122">-Headername</span><span class="sxs-lookup"><span data-stu-id="039c7-122">-HeaderName</span></span>
<span data-ttu-id="039c7-123">Der Header Wert, der die Versionsinformationen enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="039c7-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="039c7-124">Wenn die Kopfzeile des Versionsschemas ausgewählt ist, muss dieser Wert angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="039c7-124">If versioning Scheme HEADER is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="039c7-125">-Name</span><span class="sxs-lookup"><span data-stu-id="039c7-125">-Name</span></span>
<span data-ttu-id="039c7-126">Der Name des ApiVersion-Satzes.</span><span class="sxs-lookup"><span data-stu-id="039c7-126">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="039c7-127">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="039c7-127">This parameter is required.</span></span>

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

### <span data-ttu-id="039c7-128">-QueryName</span><span class="sxs-lookup"><span data-stu-id="039c7-128">-QueryName</span></span>
<span data-ttu-id="039c7-129">Der Abfragewert, der die Versionsinformationen enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="039c7-129">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="039c7-130">Wenn die Abfrage für das Versionsschema ausgewählt ist, muss dieser Wert angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="039c7-130">If versioning Scheme Query is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="039c7-131">-Scheme</span><span class="sxs-lookup"><span data-stu-id="039c7-131">-Scheme</span></span>
<span data-ttu-id="039c7-132">Versions Verwaltungsschema, das für den API-Versions Verwaltungssatz ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="039c7-132">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="039c7-133">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="039c7-133">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme
Parameter Sets: (All)
Aliases:
Accepted values: Segment, Query, Header

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="039c7-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="039c7-134">-Confirm</span></span>
<span data-ttu-id="039c7-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="039c7-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="039c7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="039c7-136">-WhatIf</span></span>
<span data-ttu-id="039c7-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="039c7-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="039c7-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="039c7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="039c7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="039c7-139">CommonParameters</span></span>
<span data-ttu-id="039c7-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="039c7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="039c7-141">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="039c7-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="039c7-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="039c7-142">INPUTS</span></span>

### <span data-ttu-id="039c7-143">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="039c7-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="039c7-144">System. String</span><span class="sxs-lookup"><span data-stu-id="039c7-144">System.String</span></span>

### <span data-ttu-id="039c7-145">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="039c7-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="039c7-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="039c7-146">OUTPUTS</span></span>

### <span data-ttu-id="039c7-147">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="039c7-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="039c7-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="039c7-148">NOTES</span></span>

## <span data-ttu-id="039c7-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="039c7-149">RELATED LINKS</span></span>

[<span data-ttu-id="039c7-150">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="039c7-150">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="039c7-151">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="039c7-151">Remove-AzApiManagementApiVersionSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="039c7-152">Satz-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="039c7-152">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)