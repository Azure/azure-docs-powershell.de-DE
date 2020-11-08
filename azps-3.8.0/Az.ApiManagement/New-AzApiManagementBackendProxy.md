---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendproxy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
ms.openlocfilehash: d7afe10975003dcc8c82156d03adc1aa022b505c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996950"
---
# <span data-ttu-id="08b03-101">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="08b03-101">New-AzApiManagementBackendProxy</span></span>

## <span data-ttu-id="08b03-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="08b03-102">SYNOPSIS</span></span>
<span data-ttu-id="08b03-103">Erstellt ein neues Back-End-Proxy Objekt.</span><span class="sxs-lookup"><span data-stu-id="08b03-103">Creates a new Backend Proxy Object.</span></span>

## <span data-ttu-id="08b03-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="08b03-104">SYNTAX</span></span>

```
New-AzApiManagementBackendProxy -Url <String> [-ProxyCredential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08b03-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="08b03-105">DESCRIPTION</span></span>
<span data-ttu-id="08b03-106">Erstellt ein neues Back-End-Proxy Objekt, das beim Erstellen einer neuen Back-End-Entität umgeleitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="08b03-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="08b03-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="08b03-107">EXAMPLES</span></span>

### <span data-ttu-id="08b03-108">Erstellen eines Back-End-Proxys In-Memory Objekt</span><span class="sxs-lookup"><span data-stu-id="08b03-108">Create a Backend Proxy In-Memory Object</span></span>
```powershell
PS C:\>$secpassword = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\>$proxyCreds = New-Object System.Management.Automation.PSCredential ("foo", $secpassword)
PS C:\>$credential = New-AzApiManagementBackendProxy -Url "http://12.168.1.1:8080" -ProxyCredential $proxyCreds

PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Proxy $credential -Description "backend with proxy server"
```

<span data-ttu-id="08b03-109">Erstellt ein Back-End-Proxy Objekt und richtet das Back-End ein.</span><span class="sxs-lookup"><span data-stu-id="08b03-109">Creates a Backend Proxy Object and sets up Backend</span></span>

## <span data-ttu-id="08b03-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="08b03-110">PARAMETERS</span></span>

### <span data-ttu-id="08b03-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08b03-111">-DefaultProfile</span></span>
<span data-ttu-id="08b03-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="08b03-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08b03-113">-ProxyCredential</span><span class="sxs-lookup"><span data-stu-id="08b03-113">-ProxyCredential</span></span>
<span data-ttu-id="08b03-114">Zum Herstellen einer Verbindung mit dem Back-End-Proxy verwendete Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="08b03-114">Credentials used to connect to Backend Proxy.</span></span> <span data-ttu-id="08b03-115">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="08b03-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="08b03-116">-URL</span><span class="sxs-lookup"><span data-stu-id="08b03-116">-Url</span></span>
<span data-ttu-id="08b03-117">Die URL des Proxy Servers, der beim Weiterleiten von Anrufen an das Back-End verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="08b03-117">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="08b03-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="08b03-118">This parameter is required.</span></span>

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

### <span data-ttu-id="08b03-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08b03-119">CommonParameters</span></span>
<span data-ttu-id="08b03-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08b03-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08b03-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08b03-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08b03-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="08b03-122">INPUTS</span></span>

### <span data-ttu-id="08b03-123">Keine</span><span class="sxs-lookup"><span data-stu-id="08b03-123">None</span></span>

## <span data-ttu-id="08b03-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="08b03-124">OUTPUTS</span></span>

### <span data-ttu-id="08b03-125">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="08b03-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="08b03-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="08b03-126">NOTES</span></span>

## <span data-ttu-id="08b03-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="08b03-127">RELATED LINKS</span></span>

[<span data-ttu-id="08b03-128">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="08b03-128">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="08b03-129">Neu – AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="08b03-129">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="08b03-130">Neu – AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="08b03-130">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="08b03-131">Satz-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="08b03-131">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="08b03-132">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="08b03-132">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
