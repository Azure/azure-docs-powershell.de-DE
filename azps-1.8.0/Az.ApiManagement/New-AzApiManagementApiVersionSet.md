---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 58f9fda87bc24b22a68e98d60092b80002e74e4a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650346"
---
# <span data-ttu-id="83319-101">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="83319-101">New-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="83319-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="83319-102">SYNOPSIS</span></span>
<span data-ttu-id="83319-103">Erstellt eine API-Versionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="83319-103">Creates an API Version Set.</span></span>

## <span data-ttu-id="83319-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="83319-104">SYNTAX</span></span>

```
New-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>] -Name <String>
 -Scheme <PsApiManagementVersioningScheme> [-HeaderName <String>] [-QueryName <String>] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83319-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="83319-105">DESCRIPTION</span></span>
<span data-ttu-id="83319-106">Das Cmdlet **New-AzApiManagementApiVersionSet** erstellt im Azure API-Verwaltungskontext eine API-Versions Satz Entität.</span><span class="sxs-lookup"><span data-stu-id="83319-106">The **New-AzApiManagementApiVersionSet** cmdlet creates an API Version set entity in the Azure API Management context.</span></span>

## <span data-ttu-id="83319-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="83319-107">EXAMPLES</span></span>

### <span data-ttu-id="83319-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="83319-108">Example 1</span></span>
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

<span data-ttu-id="83319-109">Mit diesem Befehl wird eine API-Version erstellt, die das Versionsschema `Query` und den Abfrageparameter definiert `api-version` .</span><span class="sxs-lookup"><span data-stu-id="83319-109">This command creates an API Version Set which versioning scheme `Query` and Query parameter `api-version`.</span></span>

## <span data-ttu-id="83319-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="83319-110">PARAMETERS</span></span>

### <span data-ttu-id="83319-111">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="83319-111">-ApiVersionSetId</span></span>
<span data-ttu-id="83319-112">Bezeichner für die neue API-Versionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="83319-112">Identifier for new API Version Set.</span></span>
<span data-ttu-id="83319-113">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="83319-113">This parameter is optional.</span></span>
<span data-ttu-id="83319-114">Wenn nicht angegeben, wird ein Bezeichner generiert.</span><span class="sxs-lookup"><span data-stu-id="83319-114">If not specified an identifier will be generated.</span></span>

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

### <span data-ttu-id="83319-115">-Context</span><span class="sxs-lookup"><span data-stu-id="83319-115">-Context</span></span>
<span data-ttu-id="83319-116">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="83319-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="83319-117">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="83319-117">This parameter is required.</span></span>

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

### <span data-ttu-id="83319-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83319-118">-DefaultProfile</span></span>
<span data-ttu-id="83319-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="83319-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83319-120">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="83319-120">-Description</span></span>
<span data-ttu-id="83319-121">Beschreibung der API-Versionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="83319-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="83319-122">-Headername</span><span class="sxs-lookup"><span data-stu-id="83319-122">-HeaderName</span></span>
<span data-ttu-id="83319-123">Der Header Wert, der die Versionsinformationen enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="83319-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="83319-124">Wenn die Kopfzeile des Versionsschemas ausgewählt ist, muss dieser Wert angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="83319-124">If versioning Scheme HEADER is choosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="83319-125">-Name</span><span class="sxs-lookup"><span data-stu-id="83319-125">-Name</span></span>
<span data-ttu-id="83319-126">Der Name des ApiVersion-Satzes.</span><span class="sxs-lookup"><span data-stu-id="83319-126">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="83319-127">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="83319-127">This parameter is required.</span></span>

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

### <span data-ttu-id="83319-128">-QueryName</span><span class="sxs-lookup"><span data-stu-id="83319-128">-QueryName</span></span>
<span data-ttu-id="83319-129">Der Abfragewert, der die Versionsinformationen enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="83319-129">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="83319-130">Wenn die Abfrage für das Versionsschema ausgewählt ist, muss dieser Wert angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="83319-130">If versioning Scheme Query is choosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="83319-131">-Scheme</span><span class="sxs-lookup"><span data-stu-id="83319-131">-Scheme</span></span>
<span data-ttu-id="83319-132">Versions Verwaltungsschema, das für den API-Versions Verwaltungssatz ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="83319-132">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="83319-133">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="83319-133">This parameter is required.</span></span>

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

### <span data-ttu-id="83319-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="83319-134">-Confirm</span></span>
<span data-ttu-id="83319-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="83319-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83319-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83319-136">-WhatIf</span></span>
<span data-ttu-id="83319-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="83319-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="83319-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="83319-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83319-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83319-139">CommonParameters</span></span>
<span data-ttu-id="83319-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83319-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83319-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83319-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83319-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="83319-142">INPUTS</span></span>

### <span data-ttu-id="83319-143">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="83319-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="83319-144">System. String</span><span class="sxs-lookup"><span data-stu-id="83319-144">System.String</span></span>

### <span data-ttu-id="83319-145">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="83319-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="83319-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="83319-146">OUTPUTS</span></span>

### <span data-ttu-id="83319-147">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="83319-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="83319-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="83319-148">NOTES</span></span>

## <span data-ttu-id="83319-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="83319-149">RELATED LINKS</span></span>

[<span data-ttu-id="83319-150">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="83319-150">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="83319-151">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="83319-151">Remove-AzApiManagementApiVersionSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="83319-152">Satz-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="83319-152">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)