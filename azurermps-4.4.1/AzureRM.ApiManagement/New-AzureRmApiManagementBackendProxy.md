---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendProxy.md
ms.openlocfilehash: d3699347d21f17452d521afb3bc5524f8e68e40b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498061"
---
# <span data-ttu-id="ac944-101">New-AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="ac944-101">New-AzureRmApiManagementBackendProxy</span></span>

## <span data-ttu-id="ac944-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ac944-102">SYNOPSIS</span></span>
<span data-ttu-id="ac944-103">Erstellt ein neues Back-End-Proxy Objekt.</span><span class="sxs-lookup"><span data-stu-id="ac944-103">Creates a new Backend Proxy Object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac944-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac944-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendProxy -Url <String> [-UserName <String>] [-Password <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac944-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ac944-105">DESCRIPTION</span></span>
<span data-ttu-id="ac944-106">Erstellt ein neues Back-End-Proxy Objekt, das beim Erstellen einer neuen Back-End-Entität umgeleitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ac944-106">Creates a new Backend Proxy Object which can be piped when creating a new Backend entity.</span></span>

## <span data-ttu-id="ac944-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ac944-107">EXAMPLES</span></span>

### <span data-ttu-id="ac944-108">Erstellen eines Back-End-Proxys In-Memory Objekt</span><span class="sxs-lookup"><span data-stu-id="ac944-108">Create a Backend Proxy In-Memory Object</span></span>
```
$proxy= New-AzureRmApiManagementBackendProxy -Url "https://abbc.def.g" -UserName "apim" -Password "password"
```

<span data-ttu-id="ac944-109">Erstellt ein Back-End-Proxy Objekt</span><span class="sxs-lookup"><span data-stu-id="ac944-109">Creates a Backend Proxy Object</span></span>

## <span data-ttu-id="ac944-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac944-110">PARAMETERS</span></span>

### <span data-ttu-id="ac944-111">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="ac944-111">-Password</span></span>
<span data-ttu-id="ac944-112">Proxykennwort, das für die Verbindung mit dem Back-End-Proxy verwendet wird</span><span class="sxs-lookup"><span data-stu-id="ac944-112">Proxy Password used to connect to Backend Proxy.</span></span>
<span data-ttu-id="ac944-113">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="ac944-113">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac944-114">-URL</span><span class="sxs-lookup"><span data-stu-id="ac944-114">-Url</span></span>
<span data-ttu-id="ac944-115">Die URL des Proxy Servers, der beim Weiterleiten von Anrufen an das Back-End verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ac944-115">Url of the Proxy server to be used when forwarding calls to Backend.</span></span>
<span data-ttu-id="ac944-116">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ac944-116">This parameter is required.</span></span>

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

### <span data-ttu-id="ac944-117">-UserName</span><span class="sxs-lookup"><span data-stu-id="ac944-117">-UserName</span></span>
<span data-ttu-id="ac944-118">Proxy-Nutzername zum Herstellen einer Verbindung mit dem Back-End-Proxy</span><span class="sxs-lookup"><span data-stu-id="ac944-118">Proxy UserName used to connect to Backend Proxy.</span></span>
<span data-ttu-id="ac944-119">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="ac944-119">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac944-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac944-120">-DefaultProfile</span></span>
<span data-ttu-id="ac944-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ac944-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac944-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac944-122">CommonParameters</span></span>
<span data-ttu-id="ac944-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac944-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac944-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac944-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac944-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ac944-125">INPUTS</span></span>

## <span data-ttu-id="ac944-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ac944-126">OUTPUTS</span></span>

### <span data-ttu-id="ac944-127">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="ac944-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

## <span data-ttu-id="ac944-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="ac944-128">NOTES</span></span>

## <span data-ttu-id="ac944-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ac944-129">RELATED LINKS</span></span>

[<span data-ttu-id="ac944-130">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ac944-130">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="ac944-131">Neu – AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ac944-131">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="ac944-132">Neu – AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="ac944-132">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="ac944-133">Satz-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ac944-133">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="ac944-134">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ac944-134">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
