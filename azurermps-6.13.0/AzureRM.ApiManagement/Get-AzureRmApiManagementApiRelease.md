---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiRelease.md
ms.openlocfilehash: 880d96ba0e9eff053084517452c03ffb018b72a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662334"
---
# <span data-ttu-id="00f06-101">Get-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="00f06-101">Get-AzureRmApiManagementApiRelease</span></span>

## <span data-ttu-id="00f06-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="00f06-102">SYNOPSIS</span></span>
<span data-ttu-id="00f06-103">Rufen Sie die API-Version ab.</span><span class="sxs-lookup"><span data-stu-id="00f06-103">Get the API Release.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00f06-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="00f06-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> [-ReleaseId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00f06-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="00f06-105">DESCRIPTION</span></span>
<span data-ttu-id="00f06-106">Das Cmdlet " **Get-AzureRmApiManagementApiRelease** " ruft mindestens eine Version der Azure API-Verwaltungs-API ab.</span><span class="sxs-lookup"><span data-stu-id="00f06-106">The **Get-AzureRmApiManagementApiRelease** cmdlet gets one or more releases of the Azure API Management API.</span></span>

## <span data-ttu-id="00f06-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="00f06-107">EXAMPLES</span></span>

### <span data-ttu-id="00f06-108">Beispiel 1: Abrufen aller Versionen der API</span><span class="sxs-lookup"><span data-stu-id="00f06-108">Example 1: Get all releases of the API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065
ReleaseId         : 5afccaf6b89fd067426d402e
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 12:21:12 AM
UpdatedDateTime   : 5/17/2018 12:21:12 AM
Notes             : creating a new release
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065/releases/5afccaf6b89fd067426d402e
ResourceGroupName : Api-Default-WestUS
ServiceName       : contos
```

<span data-ttu-id="00f06-109">Dieser Befehl ruft alle Versionen der `echo-api` API für den angegebenen Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="00f06-109">This command gets all of the releases of the `echo-api` API for the specified context.</span></span>

### <span data-ttu-id="00f06-110">Beispiel 2: Abrufen der Veröffentlichungsinformationen der jeweiligen API-Version</span><span class="sxs-lookup"><span data-stu-id="00f06-110">Example 2: Get the release information of the particular API release</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065 -ReleaseId 5afccaf6b89fd067426d402e
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

<span data-ttu-id="00f06-111">Dieser Befehl ruft die Freigabe Informationen einer bestimmten API mit der angegebenen Veröffentlichungs-Nr ab.</span><span class="sxs-lookup"><span data-stu-id="00f06-111">This command gets the releases information of a particular API with the specified releaseId.</span></span>

## <span data-ttu-id="00f06-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="00f06-112">PARAMETERS</span></span>

### <span data-ttu-id="00f06-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="00f06-113">-ApiId</span></span>
<span data-ttu-id="00f06-114">Der API-Bezeichner, nach dem gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="00f06-114">API identifier to look for.</span></span>
<span data-ttu-id="00f06-115">Wenn angegeben, wird versucht, die API mithilfe der ID abzurufen.</span><span class="sxs-lookup"><span data-stu-id="00f06-115">If specified will try to get the API by the Id.</span></span>

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

### <span data-ttu-id="00f06-116">-Context</span><span class="sxs-lookup"><span data-stu-id="00f06-116">-Context</span></span>
<span data-ttu-id="00f06-117">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="00f06-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="00f06-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="00f06-118">This parameter is required.</span></span>

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

### <span data-ttu-id="00f06-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00f06-119">-DefaultProfile</span></span>
<span data-ttu-id="00f06-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="00f06-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00f06-121">-Veröffentlichungs-Nr</span><span class="sxs-lookup"><span data-stu-id="00f06-121">-ReleaseId</span></span>
<span data-ttu-id="00f06-122">Der Bezeichner der Freigabe.</span><span class="sxs-lookup"><span data-stu-id="00f06-122">The identifier of the Release.</span></span>

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

### <span data-ttu-id="00f06-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00f06-123">CommonParameters</span></span>
<span data-ttu-id="00f06-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00f06-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00f06-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00f06-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00f06-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="00f06-126">INPUTS</span></span>

### <span data-ttu-id="00f06-127">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="00f06-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="00f06-128">System. String</span><span class="sxs-lookup"><span data-stu-id="00f06-128">System.String</span></span>

## <span data-ttu-id="00f06-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="00f06-129">OUTPUTS</span></span>

### <span data-ttu-id="00f06-130">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="00f06-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="00f06-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="00f06-131">NOTES</span></span>

## <span data-ttu-id="00f06-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="00f06-132">RELATED LINKS</span></span>

[<span data-ttu-id="00f06-133">Neu – AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="00f06-133">New-AzureRmApiManagementApiRelease</span></span>](./Get-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="00f06-134">Remove-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="00f06-134">Remove-AzureRmApiManagementApiRelease</span></span>](./Remove-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="00f06-135">Satz-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="00f06-135">Set-AzureRmApiManagementApiRelease</span></span>](./Set-AzureRmApiManagementApiRelease.md)
