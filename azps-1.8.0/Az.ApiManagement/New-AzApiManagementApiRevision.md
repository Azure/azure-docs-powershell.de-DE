---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
ms.openlocfilehash: 81a80acdfb89f30cc1add6b1cfc10bcd7d745dfd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650348"
---
# <span data-ttu-id="d6fc1-101">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="d6fc1-101">New-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="d6fc1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d6fc1-102">SYNOPSIS</span></span>
<span data-ttu-id="d6fc1-103">Erstellt eine neue Revision einer vorhandenen API.</span><span class="sxs-lookup"><span data-stu-id="d6fc1-103">Creates a new Revision of an Existing API.</span></span>

## <span data-ttu-id="d6fc1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6fc1-104">SYNTAX</span></span>

```
New-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6fc1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d6fc1-105">DESCRIPTION</span></span>

<span data-ttu-id="d6fc1-106">Das Cmdlet **New-AzApiManagementApiRevision** erstellt eine API-Revision für eine vorhandene API im API-Verwaltungskontext.</span><span class="sxs-lookup"><span data-stu-id="d6fc1-106">The **New-AzApiManagementApiRevision** cmdlet creates an API Revision for an existing an API in API Management context.</span></span>

## <span data-ttu-id="d6fc1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d6fc1-107">EXAMPLES</span></span>

### <span data-ttu-id="d6fc1-108">Beispiel 1: Erstellen einer API-Revision für eine API</span><span class="sxs-lookup"><span data-stu-id="d6fc1-108">Example 1: Create an API Revision for an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRevision -Context $ApiMgmtContext  -ApiId 5adf6fbf0faadf3ad8558065 -ApiRevision 6


ApiId                         : 5adf6fbf0faadf3ad8558065;rev=6
Name                          : httpbin.org
Description                   : API Management facade for a very handy and free online HTTP tool.
ServiceUrl                    : https://httpbin.org/
Path                          : httpbin
ApiType                       : http
Protocols                     : {Http, Https}
AuthorizationServerId         : contoso-oauth
AuthorizationScope            : contoso-oauth
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 6
ApiVersion                    : v1
IsCurrent                     : False
IsOnline                      : False
Id                            : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065;rev=6
ResourceGroupName             : Api-Default-WestUS
ServiceName                   : contoso
```

<span data-ttu-id="d6fc1-109">Dieser Befehl erstellt eine API-Revision `2` der `echo-api` API.</span><span class="sxs-lookup"><span data-stu-id="d6fc1-109">This command creates an API Revision `2` of the `echo-api` API.</span></span>

## <span data-ttu-id="d6fc1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6fc1-110">PARAMETERS</span></span>

### <span data-ttu-id="d6fc1-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="d6fc1-111">-ApiId</span></span>
<span data-ttu-id="d6fc1-112">Bezeichner für API, dessen Revision erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d6fc1-112">Identifier for API whose Revision is to be created.</span></span>

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

### <span data-ttu-id="d6fc1-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="d6fc1-113">-ApiRevision</span></span>
<span data-ttu-id="d6fc1-114">Überarbeitungs-ID der API.</span><span class="sxs-lookup"><span data-stu-id="d6fc1-114">Revision Identifier of the Api.</span></span>

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

### <span data-ttu-id="d6fc1-115">-Context</span><span class="sxs-lookup"><span data-stu-id="d6fc1-115">-Context</span></span>
<span data-ttu-id="d6fc1-116">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d6fc1-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d6fc1-117">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d6fc1-117">This parameter is required.</span></span>

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

### <span data-ttu-id="d6fc1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6fc1-118">-DefaultProfile</span></span>
<span data-ttu-id="d6fc1-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d6fc1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6fc1-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d6fc1-120">-Confirm</span></span>
<span data-ttu-id="d6fc1-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d6fc1-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6fc1-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6fc1-122">-WhatIf</span></span>
<span data-ttu-id="d6fc1-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d6fc1-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d6fc1-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d6fc1-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6fc1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6fc1-125">CommonParameters</span></span>
<span data-ttu-id="d6fc1-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6fc1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6fc1-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6fc1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6fc1-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d6fc1-128">INPUTS</span></span>

### <span data-ttu-id="d6fc1-129">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d6fc1-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d6fc1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d6fc1-130">System.String</span></span>

## <span data-ttu-id="d6fc1-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d6fc1-131">OUTPUTS</span></span>

### <span data-ttu-id="d6fc1-132">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d6fc1-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="d6fc1-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="d6fc1-133">NOTES</span></span>

## <span data-ttu-id="d6fc1-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d6fc1-134">RELATED LINKS</span></span>

[<span data-ttu-id="d6fc1-135">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d6fc1-135">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="d6fc1-136">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d6fc1-136">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="d6fc1-137">Satz-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d6fc1-137">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)
