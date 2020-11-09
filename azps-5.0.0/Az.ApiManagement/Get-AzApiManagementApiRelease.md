---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRelease.md
ms.openlocfilehash: 7a3c418c5f55aa70b23972e5cd51065557335866
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302265"
---
# <span data-ttu-id="aeccc-101">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="aeccc-101">Get-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="aeccc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aeccc-102">SYNOPSIS</span></span>
<span data-ttu-id="aeccc-103">Rufen Sie die API-Version ab.</span><span class="sxs-lookup"><span data-stu-id="aeccc-103">Get the API Release.</span></span>

## <span data-ttu-id="aeccc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aeccc-104">SYNTAX</span></span>

### <span data-ttu-id="aeccc-105">ContextParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="aeccc-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> [-ReleaseId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aeccc-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aeccc-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementApiRelease -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aeccc-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aeccc-107">DESCRIPTION</span></span>
<span data-ttu-id="aeccc-108">Das Cmdlet " **Get-AzApiManagementApiRelease** " ruft mindestens eine Version der Azure API-Verwaltungs-API ab.</span><span class="sxs-lookup"><span data-stu-id="aeccc-108">The **Get-AzApiManagementApiRelease** cmdlet gets one or more releases of the Azure API Management API.</span></span>

## <span data-ttu-id="aeccc-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aeccc-109">EXAMPLES</span></span>

### <span data-ttu-id="aeccc-110">Beispiel 1: Abrufen aller Versionen der API</span><span class="sxs-lookup"><span data-stu-id="aeccc-110">Example 1: Get all releases of the API</span></span>
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
ServiceName       : contoso
```

<span data-ttu-id="aeccc-111">Dieser Befehl ruft alle Versionen der `echo-api` API für den angegebenen Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="aeccc-111">This command gets all of the releases of the `echo-api` API for the specified context.</span></span>

### <span data-ttu-id="aeccc-112">Beispiel 2: Abrufen der Veröffentlichungsinformationen der jeweiligen API-Version</span><span class="sxs-lookup"><span data-stu-id="aeccc-112">Example 2: Get the release information of the particular API release</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId 5adf6fbf0faadf3ad8558065 -ReleaseId 5afccaf6b89fd067426d402e
ReleaseId         : 5afccaf6b89fd067426d402e
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 12:21:12 AM
UpdatedDateTime   : 5/17/2018 12:21:12 AM
Notes             : creating a new release
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Mi
                    crosoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065/releases/5afccaf6b89fd067426d402
                    e
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="aeccc-113">Dieser Befehl ruft die Freigabe Informationen einer bestimmten API mit der angegebenen Veröffentlichungs-Nr ab.</span><span class="sxs-lookup"><span data-stu-id="aeccc-113">This command gets the releases information of a particular API with the specified releaseId.</span></span>

## <span data-ttu-id="aeccc-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="aeccc-114">PARAMETERS</span></span>

### <span data-ttu-id="aeccc-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="aeccc-115">-ApiId</span></span>
<span data-ttu-id="aeccc-116">Der API-Bezeichner, nach dem gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="aeccc-116">API identifier to look for.</span></span>
<span data-ttu-id="aeccc-117">Wenn angegeben, wird versucht, die API mithilfe der ID abzurufen.</span><span class="sxs-lookup"><span data-stu-id="aeccc-117">If specified will try to get the API by the Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeccc-118">-Context</span><span class="sxs-lookup"><span data-stu-id="aeccc-118">-Context</span></span>
<span data-ttu-id="aeccc-119">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="aeccc-119">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="aeccc-120">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="aeccc-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aeccc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aeccc-121">-DefaultProfile</span></span>
<span data-ttu-id="aeccc-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="aeccc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aeccc-123">-Veröffentlichungs-Nr</span><span class="sxs-lookup"><span data-stu-id="aeccc-123">-ReleaseId</span></span>
<span data-ttu-id="aeccc-124">Der Bezeichner der Freigabe.</span><span class="sxs-lookup"><span data-stu-id="aeccc-124">The identifier of the Release.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeccc-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="aeccc-125">-ResourceId</span></span>
<span data-ttu-id="aeccc-126">Arm-Ressourcenbezeichner einer API-Version.</span><span class="sxs-lookup"><span data-stu-id="aeccc-126">Arm Resource Identifier of a Api Release.</span></span> <span data-ttu-id="aeccc-127">Wenn angegeben, wird versucht, die API-Version durch den Bezeichner zu finden.</span><span class="sxs-lookup"><span data-stu-id="aeccc-127">If specified will try to find api release by the identifier.</span></span> <span data-ttu-id="aeccc-128">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="aeccc-128">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeccc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeccc-129">CommonParameters</span></span>
<span data-ttu-id="aeccc-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aeccc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeccc-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aeccc-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeccc-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aeccc-132">INPUTS</span></span>

### <span data-ttu-id="aeccc-133">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="aeccc-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="aeccc-134">System. String</span><span class="sxs-lookup"><span data-stu-id="aeccc-134">System.String</span></span>

## <span data-ttu-id="aeccc-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aeccc-135">OUTPUTS</span></span>

### <span data-ttu-id="aeccc-136">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="aeccc-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="aeccc-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="aeccc-137">NOTES</span></span>

## <span data-ttu-id="aeccc-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aeccc-138">RELATED LINKS</span></span>

[<span data-ttu-id="aeccc-139">Neu – AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="aeccc-139">New-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="aeccc-140">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="aeccc-140">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="aeccc-141">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="aeccc-141">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)