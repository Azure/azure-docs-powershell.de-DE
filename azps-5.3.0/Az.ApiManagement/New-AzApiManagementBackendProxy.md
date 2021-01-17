---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendproxy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
ms.openlocfilehash: fe4d94bb438d3180ed0a77bb7129b46c65d5edbc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471417"
---
# <span data-ttu-id="a0fde-101">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="a0fde-101">New-AzApiManagementBackendProxy</span></span>

## <span data-ttu-id="a0fde-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0fde-102">SYNOPSIS</span></span>
<span data-ttu-id="a0fde-103">Erstellt ein neues Back-End-Proxyobjekt.</span><span class="sxs-lookup"><span data-stu-id="a0fde-103">Creates a new Backend Proxy Object.</span></span>

## <span data-ttu-id="a0fde-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a0fde-104">SYNTAX</span></span>

```
New-AzApiManagementBackendProxy -Url <String> [-ProxyCredential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0fde-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0fde-105">DESCRIPTION</span></span>
<span data-ttu-id="a0fde-106">Erstellt ein neues Back-End-Proxyobjekt, das beim Erstellen einer neuen Backendentität weitergeleitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a0fde-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="a0fde-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a0fde-107">EXAMPLES</span></span>

### <span data-ttu-id="a0fde-108">Beispiel 1: Erstellen eines Back-End-Proxy-In-Memory Objekts</span><span class="sxs-lookup"><span data-stu-id="a0fde-108">Example 1: Create a Backend Proxy In-Memory Object</span></span>
```powershell
PS C:\>$secpassword = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\>$proxyCreds = New-Object System.Management.Automation.PSCredential ("foo", $secpassword)
PS C:\>$credential = New-AzApiManagementBackendProxy -Url "http://12.168.1.1:8080" -ProxyCredential $proxyCreds

PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Proxy $credential -Description "backend with proxy server"
```

<span data-ttu-id="a0fde-109">Erstellt ein Back-End-Proxyobjekt und richtet das Back-End ein.</span><span class="sxs-lookup"><span data-stu-id="a0fde-109">Creates a Backend Proxy Object and sets up Backend</span></span>

## <span data-ttu-id="a0fde-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0fde-110">PARAMETERS</span></span>

### <span data-ttu-id="a0fde-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0fde-111">-DefaultProfile</span></span>
<span data-ttu-id="a0fde-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a0fde-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0fde-113">-ProxyCredential</span><span class="sxs-lookup"><span data-stu-id="a0fde-113">-ProxyCredential</span></span>
<span data-ttu-id="a0fde-114">Anmeldeinformationen, die zum Herstellen einer Verbindung mit dem Back-End-Proxy verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a0fde-114">Credentials used to connect to Backend Proxy.</span></span> <span data-ttu-id="a0fde-115">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="a0fde-115">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0fde-116">-URL</span><span class="sxs-lookup"><span data-stu-id="a0fde-116">-Url</span></span>
<span data-ttu-id="a0fde-117">DIE URL des Proxyservers, der beim Weiterleiten von Anrufen an das Back-End verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a0fde-117">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="a0fde-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a0fde-118">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0fde-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0fde-119">CommonParameters</span></span>
<span data-ttu-id="a0fde-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0fde-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0fde-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a0fde-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0fde-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a0fde-122">INPUTS</span></span>

### <span data-ttu-id="a0fde-123">Keine</span><span class="sxs-lookup"><span data-stu-id="a0fde-123">None</span></span>

## <span data-ttu-id="a0fde-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a0fde-124">OUTPUTS</span></span>

### <span data-ttu-id="a0fde-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="a0fde-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="a0fde-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a0fde-126">NOTES</span></span>

## <span data-ttu-id="a0fde-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a0fde-127">RELATED LINKS</span></span>

[<span data-ttu-id="a0fde-128">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a0fde-128">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="a0fde-129">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a0fde-129">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="a0fde-130">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="a0fde-130">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="a0fde-131">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a0fde-131">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="a0fde-132">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="a0fde-132">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
