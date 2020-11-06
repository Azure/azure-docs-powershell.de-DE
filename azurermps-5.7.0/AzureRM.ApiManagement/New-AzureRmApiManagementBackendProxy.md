---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackendproxy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
ms.openlocfilehash: 890f169c3fd497f7045522133e1e9e1f1d509aca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504634"
---
# <span data-ttu-id="6cb6a-101">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="6cb6a-101">New-AzureRmApiManagementBackendProxy</span></span>

## <span data-ttu-id="6cb6a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6cb6a-102">SYNOPSIS</span></span>
<span data-ttu-id="6cb6a-103">Erstellt ein neues Back-End-Proxy Objekt.</span><span class="sxs-lookup"><span data-stu-id="6cb6a-103">Creates a new Backend Proxy Object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6cb6a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6cb6a-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendProxy -Url <String> [-ProxyCredential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6cb6a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6cb6a-105">DESCRIPTION</span></span>
<span data-ttu-id="6cb6a-106">Erstellt ein neues Back-End-Proxy Objekt, das beim Erstellen einer neuen Back-End-Entität umgeleitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="6cb6a-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="6cb6a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6cb6a-107">EXAMPLES</span></span>

### <span data-ttu-id="6cb6a-108">Erstellen eines Back-End-Proxys In-Memory Objekt</span><span class="sxs-lookup"><span data-stu-id="6cb6a-108">Create a Backend Proxy In-Memory Object</span></span>
```
PS C:\>$secpassword = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\>$proxyCreds = New-Object System.Management.Automation.PSCredential ("foo", $secpassword)
PS C:\>$credential = New-AzureRmApiManagementBackendProxy -Url "http://12.168.1.1:8080" -ProxyCredential $proxyCreds
```

<span data-ttu-id="6cb6a-109">Erstellt ein Back-End-Proxy Objekt</span><span class="sxs-lookup"><span data-stu-id="6cb6a-109">Creates a Backend Proxy Object</span></span>

## <span data-ttu-id="6cb6a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6cb6a-110">PARAMETERS</span></span>

### <span data-ttu-id="6cb6a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cb6a-111">-DefaultProfile</span></span>
<span data-ttu-id="6cb6a-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6cb6a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cb6a-113">-ProxyCredential</span><span class="sxs-lookup"><span data-stu-id="6cb6a-113">-ProxyCredential</span></span>
<span data-ttu-id="6cb6a-114">Zum Herstellen einer Verbindung mit dem Back-End-Proxy verwendete Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="6cb6a-114">Credentials used to connect to Backend Proxy.</span></span> <span data-ttu-id="6cb6a-115">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="6cb6a-115">This parameter is optional.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cb6a-116">-URL</span><span class="sxs-lookup"><span data-stu-id="6cb6a-116">-Url</span></span>
<span data-ttu-id="6cb6a-117">Die URL des Proxy Servers, der beim Weiterleiten von Anrufen an das Back-End verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6cb6a-117">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="6cb6a-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6cb6a-118">This parameter is required.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cb6a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cb6a-119">CommonParameters</span></span>
<span data-ttu-id="6cb6a-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cb6a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cb6a-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cb6a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cb6a-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6cb6a-122">INPUTS</span></span>

### <span data-ttu-id="6cb6a-123">Keine</span><span class="sxs-lookup"><span data-stu-id="6cb6a-123">None</span></span>
<span data-ttu-id="6cb6a-124">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="6cb6a-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6cb6a-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6cb6a-125">OUTPUTS</span></span>

### <span data-ttu-id="6cb6a-126">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="6cb6a-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="6cb6a-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="6cb6a-127">NOTES</span></span>

## <span data-ttu-id="6cb6a-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6cb6a-128">RELATED LINKS</span></span>

[<span data-ttu-id="6cb6a-129">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="6cb6a-129">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="6cb6a-130">Neu – AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="6cb6a-130">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="6cb6a-131">Neu – AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="6cb6a-131">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="6cb6a-132">Satz-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="6cb6a-132">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="6cb6a-133">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="6cb6a-133">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
