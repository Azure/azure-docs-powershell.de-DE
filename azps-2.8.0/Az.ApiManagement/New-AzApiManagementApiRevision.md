---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
ms.openlocfilehash: 1a58c34aac272f6c8278833cd356de66774c5a4a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658278"
---
# <span data-ttu-id="09158-101">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="09158-101">New-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="09158-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="09158-102">SYNOPSIS</span></span>
<span data-ttu-id="09158-103">Erstellt eine neue Revision einer vorhandenen API.</span><span class="sxs-lookup"><span data-stu-id="09158-103">Creates a new Revision of an Existing API.</span></span>

## <span data-ttu-id="09158-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="09158-104">SYNTAX</span></span>

```
New-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ApiRevisionDescription <String>] [-SourceApiRevision <String>] [-ServiceUrl <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09158-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="09158-105">DESCRIPTION</span></span>

<span data-ttu-id="09158-106">Das Cmdlet **New-AzApiManagementApiRevision** erstellt eine API-Revision für eine vorhandene API im API-Verwaltungskontext.</span><span class="sxs-lookup"><span data-stu-id="09158-106">The **New-AzApiManagementApiRevision** cmdlet creates an API Revision for an existing an API in API Management context.</span></span>

## <span data-ttu-id="09158-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="09158-107">EXAMPLES</span></span>

### <span data-ttu-id="09158-108">Beispiel 1: Erstellen einer leeren API-Revision für eine API</span><span class="sxs-lookup"><span data-stu-id="09158-108">Example 1: Create an empty API Revision for an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5"


New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5"
```

<span data-ttu-id="09158-109">Dieser Befehl erstellt eine API-Revision `2` der `echo-api` API.</span><span class="sxs-lookup"><span data-stu-id="09158-109">This command creates an API Revision `2` of the `echo-api` API.</span></span>

### <span data-ttu-id="09158-110">Beispiel 2: Erstellen einer API-Revision aus einer vorhandenen API und Kopieren aller Vorgänge, Kategorien und Richtlinien</span><span class="sxs-lookup"><span data-stu-id="09158-110">Example 2: Create an API Revision from an Existing Api and copy All operations, tags and Policies</span></span>
```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRevision -Context $context -ApiId "echo-api" -ApiRevision "5" -SourceApiRevision "1" -ServiceUrl "https://echoapi.cloudapp.net/rev4"


ApiId                         : echo-api;rev=5
Name                          : Echo API
Description                   :
ServiceUrl                    : http://echoapi.cloudapp.net/api
Path                          : echo
ApiType                       : http
Protocols                     : {Https}
AuthorizationServerId         :
AuthorizationScope            :
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 5
ApiVersion                    :
IsCurrent                     : False
IsOnline                      : False
SubscriptionRequired          : True
ApiRevisionDescription        :
ApiVersionSetDescription      :
ApiVersionSetId               :
Id                            : /subscriptions/subid/resourceGroups/apimService1/providers/Microsoft.ApiManagement/service/sdktestapim4163/apis/echo-api;rev=5
ResourceGroupName             : apimService1
ServiceName                   : sdktestapim4163
```

<span data-ttu-id="09158-111">Dieser Befehl erstellt eine API-Revision `5` der `echo-api` API.</span><span class="sxs-lookup"><span data-stu-id="09158-111">This command creates an API Revision `5` of the `echo-api` API.</span></span>

## <span data-ttu-id="09158-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="09158-112">PARAMETERS</span></span>

### <span data-ttu-id="09158-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="09158-113">-ApiId</span></span>
<span data-ttu-id="09158-114">Bezeichner für API, dessen Revision erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="09158-114">Identifier for API whose Revision is to be created.</span></span>

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

### <span data-ttu-id="09158-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="09158-115">-ApiRevision</span></span>
<span data-ttu-id="09158-116">Überarbeitungs-ID der API.</span><span class="sxs-lookup"><span data-stu-id="09158-116">Revision Identifier of the Api.</span></span>

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

### <span data-ttu-id="09158-117">-ApiRevisionDescription</span><span class="sxs-lookup"><span data-stu-id="09158-117">-ApiRevisionDescription</span></span>
<span data-ttu-id="09158-118">API-Überarbeitungs Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="09158-118">Api Revision Description.</span></span> <span data-ttu-id="09158-119">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="09158-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="09158-120">-Context</span><span class="sxs-lookup"><span data-stu-id="09158-120">-Context</span></span>
<span data-ttu-id="09158-121">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="09158-121">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="09158-122">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="09158-122">This parameter is required.</span></span>

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

### <span data-ttu-id="09158-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09158-123">-DefaultProfile</span></span>
<span data-ttu-id="09158-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="09158-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09158-125">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="09158-125">-ServiceUrl</span></span>
<span data-ttu-id="09158-126">Eine URL des Webdiensts, der die API im Back-End-Dienst verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="09158-126">A URL of the web service exposing the API in the Backend service.</span></span> <span data-ttu-id="09158-127">Diese URL wird nur von der Azure-API-Verwaltung verwendet und wird nicht veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="09158-127">This URL will be used by Azure API Management only, and will not be made public.</span></span> <span data-ttu-id="09158-128">Muss 1 bis 2000 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="09158-128">Must be 1 to 2000 characters long.</span></span> <span data-ttu-id="09158-129">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="09158-129">This parameter is required.</span></span>

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

### <span data-ttu-id="09158-130">-SourceApiRevision</span><span class="sxs-lookup"><span data-stu-id="09158-130">-SourceApiRevision</span></span>
<span data-ttu-id="09158-131">API-Überarbeitungs-ID der Quell-API.</span><span class="sxs-lookup"><span data-stu-id="09158-131">Api Revision identifier of the source API.</span></span> <span data-ttu-id="09158-132">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="09158-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="09158-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="09158-133">-Confirm</span></span>
<span data-ttu-id="09158-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="09158-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09158-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09158-135">-WhatIf</span></span>
<span data-ttu-id="09158-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="09158-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="09158-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="09158-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09158-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09158-138">CommonParameters</span></span>
<span data-ttu-id="09158-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09158-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09158-140">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09158-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09158-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="09158-141">INPUTS</span></span>

### <span data-ttu-id="09158-142">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="09158-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="09158-143">System. String</span><span class="sxs-lookup"><span data-stu-id="09158-143">System.String</span></span>

## <span data-ttu-id="09158-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="09158-144">OUTPUTS</span></span>

### <span data-ttu-id="09158-145">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="09158-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="09158-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="09158-146">NOTES</span></span>

## <span data-ttu-id="09158-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="09158-147">RELATED LINKS</span></span>

[<span data-ttu-id="09158-148">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="09158-148">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="09158-149">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="09158-149">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="09158-150">Satz-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="09158-150">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)
