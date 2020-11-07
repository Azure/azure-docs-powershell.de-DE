---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
ms.openlocfilehash: 219c78dbcd39a922f98a185deb1e6ce6f0c3b652
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658313"
---
# <span data-ttu-id="0052a-101">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="0052a-101">Get-AzApiManagementLogger</span></span>

## <span data-ttu-id="0052a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0052a-102">SYNOPSIS</span></span>
<span data-ttu-id="0052a-103">Ruft API-Verwaltungs Protokollierungs Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="0052a-103">Gets API Management Logger objects.</span></span>

## <span data-ttu-id="0052a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0052a-104">SYNTAX</span></span>

### <span data-ttu-id="0052a-105">GetAllLoggers (Standard)</span><span class="sxs-lookup"><span data-stu-id="0052a-105">GetAllLoggers (Default)</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0052a-106">GetByLoggerId</span><span class="sxs-lookup"><span data-stu-id="0052a-106">GetByLoggerId</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0052a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0052a-107">DESCRIPTION</span></span>
<span data-ttu-id="0052a-108">Das Cmdlet " **Get-AzApiManagementLogger** " Ruft eine Azure API-Verwaltungs **Protokollierung** oder alle Protokollierungen ab.</span><span class="sxs-lookup"><span data-stu-id="0052a-108">The **Get-AzApiManagementLogger** cmdlet gets an Azure API Management **Logger** or all the loggers.</span></span>

## <span data-ttu-id="0052a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0052a-109">EXAMPLES</span></span>

### <span data-ttu-id="0052a-110">Beispiel 1: Abrufen aller Protokollierungen</span><span class="sxs-lookup"><span data-stu-id="0052a-110">Example 1: Get all loggers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext
```

<span data-ttu-id="0052a-111">Dieser Befehl ruft alle Protokollierungen für den angegebenen Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="0052a-111">This command gets all the loggers for the specified context.</span></span>

### <span data-ttu-id="0052a-112">Beispiel 2: Abrufen einer bestimmten Protokollierung</span><span class="sxs-lookup"><span data-stu-id="0052a-112">Example 2: Get a specific logger</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123"
```

<span data-ttu-id="0052a-113">Dieser Befehl entfernt eine Protokollierung mit der ID Logger123.</span><span class="sxs-lookup"><span data-stu-id="0052a-113">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="0052a-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="0052a-114">PARAMETERS</span></span>

### <span data-ttu-id="0052a-115">-Context</span><span class="sxs-lookup"><span data-stu-id="0052a-115">-Context</span></span>
<span data-ttu-id="0052a-116">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="0052a-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0052a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0052a-117">-DefaultProfile</span></span>
<span data-ttu-id="0052a-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0052a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0052a-119">-Protokollierungs-Nr</span><span class="sxs-lookup"><span data-stu-id="0052a-119">-LoggerId</span></span>
<span data-ttu-id="0052a-120">Gibt die ID der bestimmten Protokollierung an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="0052a-120">Specifies the ID of the specific logger to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByLoggerId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0052a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0052a-121">CommonParameters</span></span>
<span data-ttu-id="0052a-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0052a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0052a-123">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0052a-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0052a-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0052a-124">INPUTS</span></span>

### <span data-ttu-id="0052a-125">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0052a-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0052a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="0052a-126">System.String</span></span>

## <span data-ttu-id="0052a-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0052a-127">OUTPUTS</span></span>

### <span data-ttu-id="0052a-128">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="0052a-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="0052a-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="0052a-129">NOTES</span></span>

## <span data-ttu-id="0052a-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0052a-130">RELATED LINKS</span></span>

[<span data-ttu-id="0052a-131">Neu – AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="0052a-131">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="0052a-132">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="0052a-132">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)

[<span data-ttu-id="0052a-133">Satz-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="0052a-133">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


