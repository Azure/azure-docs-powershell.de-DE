---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementLogger.md
ms.openlocfilehash: 48033c250286c59e2cadfadc1a5b5d28f869a66c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500978"
---
# <span data-ttu-id="64f24-101">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="64f24-101">Get-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="64f24-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="64f24-102">SYNOPSIS</span></span>
<span data-ttu-id="64f24-103">Ruft API-Verwaltungs Protokollierungs Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="64f24-103">Gets API Management Logger objects.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64f24-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="64f24-104">SYNTAX</span></span>

### <span data-ttu-id="64f24-105">Abrufen aller Protokollierungen (Standard)</span><span class="sxs-lookup"><span data-stu-id="64f24-105">Get all loggers (Default)</span></span>
```
Get-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="64f24-106">Abrufen nach Protokollierungs-ID</span><span class="sxs-lookup"><span data-stu-id="64f24-106">Get by logger ID</span></span>
```
Get-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64f24-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="64f24-107">DESCRIPTION</span></span>
<span data-ttu-id="64f24-108">Das Cmdlet " **Get-AzureRmApiManagementLogger** " Ruft eine Azure API-Verwaltungs **Protokollierung** oder alle Protokollierungen ab.</span><span class="sxs-lookup"><span data-stu-id="64f24-108">The **Get-AzureRmApiManagementLogger** cmdlet gets an Azure API Management **Logger** or all the loggers.</span></span>

## <span data-ttu-id="64f24-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="64f24-109">EXAMPLES</span></span>

### <span data-ttu-id="64f24-110">Beispiel 1: Abrufen aller Protokollierungen</span><span class="sxs-lookup"><span data-stu-id="64f24-110">Example 1: Get all loggers</span></span>
```
PS C:\>Get-AzureRmApiManagementLogger -Context $ApimContext
```

<span data-ttu-id="64f24-111">Dieser Befehl ruft alle Protokollierungen für den angegebenen Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="64f24-111">This command gets all the loggers for the specified context.</span></span>

### <span data-ttu-id="64f24-112">Beispiel 2: Abrufen einer bestimmten Protokollierung</span><span class="sxs-lookup"><span data-stu-id="64f24-112">Example 2: Get a specific logger</span></span>
```
PS C:\>Get-AzureRmApiManagementLogger -Context $ApimContext -LoggerId "Logger123"
```

<span data-ttu-id="64f24-113">Dieser Befehl entfernt eine Protokollierung mit der ID Logger123.</span><span class="sxs-lookup"><span data-stu-id="64f24-113">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="64f24-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="64f24-114">PARAMETERS</span></span>

### <span data-ttu-id="64f24-115">-Context</span><span class="sxs-lookup"><span data-stu-id="64f24-115">-Context</span></span>
<span data-ttu-id="64f24-116">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="64f24-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="64f24-117">-Protokollierungs-Nr</span><span class="sxs-lookup"><span data-stu-id="64f24-117">-LoggerId</span></span>
<span data-ttu-id="64f24-118">Gibt die ID der bestimmten Protokollierung an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="64f24-118">Specifies the ID of the specific logger to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by logger ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64f24-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64f24-119">-DefaultProfile</span></span>
<span data-ttu-id="64f24-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="64f24-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64f24-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64f24-121">CommonParameters</span></span>
<span data-ttu-id="64f24-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64f24-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64f24-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64f24-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64f24-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="64f24-124">INPUTS</span></span>

## <span data-ttu-id="64f24-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="64f24-125">OUTPUTS</span></span>

### <span data-ttu-id="64f24-126">IList<Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementLogger></span><span class="sxs-lookup"><span data-stu-id="64f24-126">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger></span></span>

## <span data-ttu-id="64f24-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="64f24-127">NOTES</span></span>

## <span data-ttu-id="64f24-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="64f24-128">RELATED LINKS</span></span>

[<span data-ttu-id="64f24-129">Neu – AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="64f24-129">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="64f24-130">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="64f24-130">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)

[<span data-ttu-id="64f24-131">Satz-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="64f24-131">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


