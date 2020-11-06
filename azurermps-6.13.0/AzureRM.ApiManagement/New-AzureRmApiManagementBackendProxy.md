---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackendproxy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
ms.openlocfilehash: d5ff2fd4f9bd3360974d93c457e541cb2f96dc5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480654"
---
# <span data-ttu-id="519d1-101">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="519d1-101">New-AzureRmApiManagementBackendProxy</span></span>

## <span data-ttu-id="519d1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="519d1-102">SYNOPSIS</span></span>
<span data-ttu-id="519d1-103">Erstellt ein neues Back-End-Proxy Objekt.</span><span class="sxs-lookup"><span data-stu-id="519d1-103">Creates a new Backend Proxy Object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="519d1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="519d1-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendProxy -Url <String> [-ProxyCredential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="519d1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="519d1-105">DESCRIPTION</span></span>
<span data-ttu-id="519d1-106">Erstellt ein neues Back-End-Proxy Objekt, das beim Erstellen einer neuen Back-End-Entität umgeleitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="519d1-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="519d1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="519d1-107">EXAMPLES</span></span>

### <span data-ttu-id="519d1-108">Erstellen eines Back-End-Proxys In-Memory Objekt</span><span class="sxs-lookup"><span data-stu-id="519d1-108">Create a Backend Proxy In-Memory Object</span></span>
```powershell
PS C:\>$secpassword = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\>$proxyCreds = New-Object System.Management.Automation.PSCredential ("foo", $secpassword)
PS C:\>$credential = New-AzureRmApiManagementBackendProxy -Url "http://12.168.1.1:8080" -ProxyCredential $proxyCreds

PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"

PS C:\>$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Proxy $credential -Description "backend with proxy server"
```

<span data-ttu-id="519d1-109">Erstellt ein Back-End-Proxy Objekt und richtet das Back-End ein.</span><span class="sxs-lookup"><span data-stu-id="519d1-109">Creates a Backend Proxy Object and sets up Backend</span></span>

## <span data-ttu-id="519d1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="519d1-110">PARAMETERS</span></span>

### <span data-ttu-id="519d1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="519d1-111">-DefaultProfile</span></span>
<span data-ttu-id="519d1-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="519d1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="519d1-113">-ProxyCredential</span><span class="sxs-lookup"><span data-stu-id="519d1-113">-ProxyCredential</span></span>
<span data-ttu-id="519d1-114">Zum Herstellen einer Verbindung mit dem Back-End-Proxy verwendete Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="519d1-114">Credentials used to connect to Backend Proxy.</span></span> <span data-ttu-id="519d1-115">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="519d1-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="519d1-116">-URL</span><span class="sxs-lookup"><span data-stu-id="519d1-116">-Url</span></span>
<span data-ttu-id="519d1-117">Die URL des Proxy Servers, der beim Weiterleiten von Anrufen an das Back-End verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="519d1-117">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="519d1-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="519d1-118">This parameter is required.</span></span>

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

### <span data-ttu-id="519d1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="519d1-119">CommonParameters</span></span>
<span data-ttu-id="519d1-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="519d1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="519d1-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="519d1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="519d1-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="519d1-122">INPUTS</span></span>

### <span data-ttu-id="519d1-123">Keine</span><span class="sxs-lookup"><span data-stu-id="519d1-123">None</span></span>

## <span data-ttu-id="519d1-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="519d1-124">OUTPUTS</span></span>

### <span data-ttu-id="519d1-125">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="519d1-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="519d1-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="519d1-126">NOTES</span></span>

## <span data-ttu-id="519d1-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="519d1-127">RELATED LINKS</span></span>

[<span data-ttu-id="519d1-128">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="519d1-128">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="519d1-129">Neu – AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="519d1-129">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="519d1-130">Neu – AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="519d1-130">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="519d1-131">Satz-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="519d1-131">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="519d1-132">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="519d1-132">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
