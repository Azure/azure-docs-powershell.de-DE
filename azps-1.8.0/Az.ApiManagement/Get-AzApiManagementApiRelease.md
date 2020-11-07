---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
ms.openlocfilehash: 353fd6365f85ba71105f80324ba740b4d829a85a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650401"
---
# <span data-ttu-id="41b73-101">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="41b73-101">Get-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="41b73-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="41b73-102">SYNOPSIS</span></span>
<span data-ttu-id="41b73-103">Rufen Sie die API-Version ab.</span><span class="sxs-lookup"><span data-stu-id="41b73-103">Get the API Release.</span></span>

## <span data-ttu-id="41b73-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="41b73-104">SYNTAX</span></span>

```
Get-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> [-ReleaseId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41b73-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="41b73-105">DESCRIPTION</span></span>
<span data-ttu-id="41b73-106">Das Cmdlet " **Get-AzApiManagementApiRelease** " ruft mindestens eine Version der Azure API-Verwaltungs-API ab.</span><span class="sxs-lookup"><span data-stu-id="41b73-106">The **Get-AzApiManagementApiRelease** cmdlet gets one or more releases of the Azure API Management API.</span></span>

## <span data-ttu-id="41b73-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="41b73-107">EXAMPLES</span></span>

### <span data-ttu-id="41b73-108">Beispiel 1: Abrufen aller Versionen der API</span><span class="sxs-lookup"><span data-stu-id="41b73-108">Example 1: Get all releases of the API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065
ReleaseId         : 5afccaf6b89fd067426d402e
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 12:21:12 AM
UpdatedDateTime   : 5/17/2018 12:21:12 AM
Notes             : creating a new release
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065/releases/5afccaf6b89fd067426d402e
ResourceGroupName : Api-Default-WestUS
ServiceName       : contos
```

<span data-ttu-id="41b73-109">Dieser Befehl ruft alle Versionen der `echo-api` API für den angegebenen Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="41b73-109">This command gets all of the releases of the `echo-api` API for the specified context.</span></span>

### <span data-ttu-id="41b73-110">Beispiel 2: Abrufen der Veröffentlichungsinformationen der jeweiligen API-Version</span><span class="sxs-lookup"><span data-stu-id="41b73-110">Example 2: Get the release information of the particular API release</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065 -ReleaseId 5afccaf6b89fd067426d402e
ReleaseId         : 5afccaf6b89fd067426d402e
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 12:21:12 AM
UpdatedDateTime   : 5/17/2018 12:21:12 AM
Notes             : creating a new release
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Mi
                    crosoft.ApiManagement/service/contos/apis/5adf6fbf0faadf3ad8558065/releases/5afccaf6b89fd067426d402
                    e
ResourceGroupName : Api-Default-WestUS
ServiceName       : contos
```

<span data-ttu-id="41b73-111">Dieser Befehl ruft die Freigabe Informationen einer bestimmten API mit der angegebenen Veröffentlichungs-Nr ab.</span><span class="sxs-lookup"><span data-stu-id="41b73-111">This command gets the releases information of a particular API with the specified releaseId.</span></span>

## <span data-ttu-id="41b73-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="41b73-112">PARAMETERS</span></span>

### <span data-ttu-id="41b73-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="41b73-113">-ApiId</span></span>
<span data-ttu-id="41b73-114">Der API-Bezeichner, nach dem gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="41b73-114">API identifier to look for.</span></span>
<span data-ttu-id="41b73-115">Wenn angegeben, wird versucht, die API mithilfe der ID abzurufen.</span><span class="sxs-lookup"><span data-stu-id="41b73-115">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="41b73-116">-Context</span><span class="sxs-lookup"><span data-stu-id="41b73-116">-Context</span></span>
<span data-ttu-id="41b73-117">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="41b73-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="41b73-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="41b73-118">This parameter is required.</span></span>

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

### <span data-ttu-id="41b73-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41b73-119">-DefaultProfile</span></span>
<span data-ttu-id="41b73-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="41b73-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41b73-121">-Veröffentlichungs-Nr</span><span class="sxs-lookup"><span data-stu-id="41b73-121">-ReleaseId</span></span>
<span data-ttu-id="41b73-122">Der Bezeichner der Freigabe.</span><span class="sxs-lookup"><span data-stu-id="41b73-122">The identifier of the Release.</span></span>

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

### <span data-ttu-id="41b73-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41b73-123">CommonParameters</span></span>
<span data-ttu-id="41b73-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41b73-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41b73-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41b73-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41b73-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="41b73-126">INPUTS</span></span>

### <span data-ttu-id="41b73-127">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="41b73-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="41b73-128">System. String</span><span class="sxs-lookup"><span data-stu-id="41b73-128">System.String</span></span>

## <span data-ttu-id="41b73-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="41b73-129">OUTPUTS</span></span>

### <span data-ttu-id="41b73-130">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="41b73-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="41b73-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="41b73-131">NOTES</span></span>

## <span data-ttu-id="41b73-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="41b73-132">RELATED LINKS</span></span>

[<span data-ttu-id="41b73-133">Neu – AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="41b73-133">New-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="41b73-134">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="41b73-134">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="41b73-135">Satz-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="41b73-135">Set-AzApiManagementApiRelease</span></span>](./Set-AzApiManagementApiRelease.md)