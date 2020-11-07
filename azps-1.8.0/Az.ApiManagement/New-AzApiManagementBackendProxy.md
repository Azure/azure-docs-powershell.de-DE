---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendproxy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendProxy.md
ms.openlocfilehash: aa681d48330755137b9c9687be6c40adc12295f2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650343"
---
# <span data-ttu-id="35a2d-101">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="35a2d-101">New-AzApiManagementBackendProxy</span></span>

## <span data-ttu-id="35a2d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="35a2d-102">SYNOPSIS</span></span>
<span data-ttu-id="35a2d-103">Erstellt ein neues Back-End-Proxy Objekt.</span><span class="sxs-lookup"><span data-stu-id="35a2d-103">Creates a new Backend Proxy Object.</span></span>

## <span data-ttu-id="35a2d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="35a2d-104">SYNTAX</span></span>

```
New-AzApiManagementBackendProxy -Url <String> [-ProxyCredential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35a2d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="35a2d-105">DESCRIPTION</span></span>
<span data-ttu-id="35a2d-106">Erstellt ein neues Back-End-Proxy Objekt, das beim Erstellen einer neuen Back-End-Entität umgeleitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="35a2d-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="35a2d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="35a2d-107">EXAMPLES</span></span>

### <span data-ttu-id="35a2d-108">Erstellen eines Back-End-Proxys In-Memory Objekt</span><span class="sxs-lookup"><span data-stu-id="35a2d-108">Create a Backend Proxy In-Memory Object</span></span>
```powershell
PS C:\>$secpassword = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\>$proxyCreds = New-Object System.Management.Automation.PSCredential ("foo", $secpassword)
PS C:\>$credential = New-AzApiManagementBackendProxy -Url "http://12.168.1.1:8080" -ProxyCredential $proxyCreds

PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Proxy $credential -Description "backend with proxy server"
```

<span data-ttu-id="35a2d-109">Erstellt ein Back-End-Proxy Objekt und richtet das Back-End ein.</span><span class="sxs-lookup"><span data-stu-id="35a2d-109">Creates a Backend Proxy Object and sets up Backend</span></span>

## <span data-ttu-id="35a2d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="35a2d-110">PARAMETERS</span></span>

### <span data-ttu-id="35a2d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35a2d-111">-DefaultProfile</span></span>
<span data-ttu-id="35a2d-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="35a2d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35a2d-113">-ProxyCredential</span><span class="sxs-lookup"><span data-stu-id="35a2d-113">-ProxyCredential</span></span>
<span data-ttu-id="35a2d-114">Zum Herstellen einer Verbindung mit dem Back-End-Proxy verwendete Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="35a2d-114">Credentials used to connect to Backend Proxy.</span></span> <span data-ttu-id="35a2d-115">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="35a2d-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="35a2d-116">-URL</span><span class="sxs-lookup"><span data-stu-id="35a2d-116">-Url</span></span>
<span data-ttu-id="35a2d-117">Die URL des Proxy Servers, der beim Weiterleiten von Anrufen an das Back-End verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="35a2d-117">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="35a2d-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="35a2d-118">This parameter is required.</span></span>

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

### <span data-ttu-id="35a2d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35a2d-119">CommonParameters</span></span>
<span data-ttu-id="35a2d-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35a2d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35a2d-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35a2d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35a2d-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="35a2d-122">INPUTS</span></span>

### <span data-ttu-id="35a2d-123">Keine</span><span class="sxs-lookup"><span data-stu-id="35a2d-123">None</span></span>

## <span data-ttu-id="35a2d-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="35a2d-124">OUTPUTS</span></span>

### <span data-ttu-id="35a2d-125">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="35a2d-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="35a2d-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="35a2d-126">NOTES</span></span>

## <span data-ttu-id="35a2d-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="35a2d-127">RELATED LINKS</span></span>

[<span data-ttu-id="35a2d-128">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="35a2d-128">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="35a2d-129">Neu – AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="35a2d-129">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="35a2d-130">Neu – AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="35a2d-130">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="35a2d-131">Satz-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="35a2d-131">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="35a2d-132">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="35a2d-132">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
