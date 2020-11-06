---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementLogger.md
ms.openlocfilehash: bcfcd052d2278fa39bc310a5c1927457a1b0fcd3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500629"
---
# <span data-ttu-id="3872a-101">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="3872a-101">Get-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="3872a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3872a-102">SYNOPSIS</span></span>
<span data-ttu-id="3872a-103">Ruft API-Verwaltungs Protokollierungs Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="3872a-103">Gets API Management Logger objects.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3872a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3872a-104">SYNTAX</span></span>

### <span data-ttu-id="3872a-105">GetAllLoggers (Standard)</span><span class="sxs-lookup"><span data-stu-id="3872a-105">GetAllLoggers (Default)</span></span>
```
Get-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3872a-106">GetByLoggerId</span><span class="sxs-lookup"><span data-stu-id="3872a-106">GetByLoggerId</span></span>
```
Get-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3872a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3872a-107">DESCRIPTION</span></span>
<span data-ttu-id="3872a-108">Das Cmdlet " **Get-AzureRmApiManagementLogger** " Ruft eine Azure API-Verwaltungs **Protokollierung** oder alle Protokollierungen ab.</span><span class="sxs-lookup"><span data-stu-id="3872a-108">The **Get-AzureRmApiManagementLogger** cmdlet gets an Azure API Management **Logger** or all the loggers.</span></span>

## <span data-ttu-id="3872a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3872a-109">EXAMPLES</span></span>

### <span data-ttu-id="3872a-110">Beispiel 1: Abrufen aller Protokollierungen</span><span class="sxs-lookup"><span data-stu-id="3872a-110">Example 1: Get all loggers</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementLogger -Context $apimContext
```

<span data-ttu-id="3872a-111">Dieser Befehl ruft alle Protokollierungen für den angegebenen Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="3872a-111">This command gets all the loggers for the specified context.</span></span>

### <span data-ttu-id="3872a-112">Beispiel 2: Abrufen einer bestimmten Protokollierung</span><span class="sxs-lookup"><span data-stu-id="3872a-112">Example 2: Get a specific logger</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123"
```

<span data-ttu-id="3872a-113">Dieser Befehl entfernt eine Protokollierung mit der ID Logger123.</span><span class="sxs-lookup"><span data-stu-id="3872a-113">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="3872a-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="3872a-114">PARAMETERS</span></span>

### <span data-ttu-id="3872a-115">-Context</span><span class="sxs-lookup"><span data-stu-id="3872a-115">-Context</span></span>
<span data-ttu-id="3872a-116">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="3872a-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3872a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3872a-117">-DefaultProfile</span></span>
<span data-ttu-id="3872a-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3872a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="3872a-119">-Protokollierungs-Nr</span><span class="sxs-lookup"><span data-stu-id="3872a-119">-LoggerId</span></span>
<span data-ttu-id="3872a-120">Gibt die ID der bestimmten Protokollierung an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="3872a-120">Specifies the ID of the specific logger to get.</span></span>

```yaml
Type: String
Parameter Sets: GetByLoggerId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3872a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3872a-121">CommonParameters</span></span>
<span data-ttu-id="3872a-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3872a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3872a-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3872a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3872a-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3872a-124">INPUTS</span></span>

### <span data-ttu-id="3872a-125">Keine</span><span class="sxs-lookup"><span data-stu-id="3872a-125">None</span></span>
<span data-ttu-id="3872a-126">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="3872a-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3872a-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3872a-127">OUTPUTS</span></span>

### <span data-ttu-id="3872a-128">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="3872a-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>
<span data-ttu-id="3872a-129">Die Details der Protokollierung, die im API-Verwaltungsdienst konfiguriert wurde.</span><span class="sxs-lookup"><span data-stu-id="3872a-129">The detail of the Logger configured in API Management service.</span></span>

### <span data-ttu-id="3872a-130">IList<Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementLogger></span><span class="sxs-lookup"><span data-stu-id="3872a-130">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger></span></span>
<span data-ttu-id="3872a-131">Die Liste der Protokollierungen, die im API-Verwaltungsdienst konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="3872a-131">The list of Loggers configured in API Management service.</span></span>

## <span data-ttu-id="3872a-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="3872a-132">NOTES</span></span>

## <span data-ttu-id="3872a-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3872a-133">RELATED LINKS</span></span>

[<span data-ttu-id="3872a-134">Neu – AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="3872a-134">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="3872a-135">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="3872a-135">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)

[<span data-ttu-id="3872a-136">Satz-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="3872a-136">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


