---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
ms.openlocfilehash: c4b7246a2b600c1ed0d9f8a01ea3fd69cd4af33d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995876"
---
# <span data-ttu-id="6dbfa-101">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="6dbfa-101">Get-AzApiManagementLogger</span></span>

## <span data-ttu-id="6dbfa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6dbfa-102">SYNOPSIS</span></span>
<span data-ttu-id="6dbfa-103">Ruft API-Verwaltungs Protokollierungs Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="6dbfa-103">Gets API Management Logger objects.</span></span>

## <span data-ttu-id="6dbfa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6dbfa-104">SYNTAX</span></span>

### <span data-ttu-id="6dbfa-105">GetAllLoggers (Standard)</span><span class="sxs-lookup"><span data-stu-id="6dbfa-105">GetAllLoggers (Default)</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6dbfa-106">GetByLoggerId</span><span class="sxs-lookup"><span data-stu-id="6dbfa-106">GetByLoggerId</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6dbfa-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6dbfa-107">DESCRIPTION</span></span>
<span data-ttu-id="6dbfa-108">Das Cmdlet " **Get-AzApiManagementLogger** " Ruft eine Azure API-Verwaltungs **Protokollierung** oder alle Protokollierungen ab.</span><span class="sxs-lookup"><span data-stu-id="6dbfa-108">The **Get-AzApiManagementLogger** cmdlet gets an Azure API Management **Logger** or all the loggers.</span></span>

## <span data-ttu-id="6dbfa-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6dbfa-109">EXAMPLES</span></span>

### <span data-ttu-id="6dbfa-110">Beispiel 1: Abrufen aller Protokollierungen</span><span class="sxs-lookup"><span data-stu-id="6dbfa-110">Example 1: Get all loggers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext
```

<span data-ttu-id="6dbfa-111">Dieser Befehl ruft alle Protokollierungen für den angegebenen Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="6dbfa-111">This command gets all the loggers for the specified context.</span></span>

### <span data-ttu-id="6dbfa-112">Beispiel 2: Abrufen einer bestimmten Protokollierung</span><span class="sxs-lookup"><span data-stu-id="6dbfa-112">Example 2: Get a specific logger</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123"
```

<span data-ttu-id="6dbfa-113">Dieser Befehl entfernt eine Protokollierung mit der ID Logger123.</span><span class="sxs-lookup"><span data-stu-id="6dbfa-113">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="6dbfa-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="6dbfa-114">PARAMETERS</span></span>

### <span data-ttu-id="6dbfa-115">-Context</span><span class="sxs-lookup"><span data-stu-id="6dbfa-115">-Context</span></span>
<span data-ttu-id="6dbfa-116">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="6dbfa-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="6dbfa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dbfa-117">-DefaultProfile</span></span>
<span data-ttu-id="6dbfa-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6dbfa-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6dbfa-119">-Protokollierungs-Nr</span><span class="sxs-lookup"><span data-stu-id="6dbfa-119">-LoggerId</span></span>
<span data-ttu-id="6dbfa-120">Gibt die ID der bestimmten Protokollierung an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="6dbfa-120">Specifies the ID of the specific logger to get.</span></span>

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

### <span data-ttu-id="6dbfa-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dbfa-121">CommonParameters</span></span>
<span data-ttu-id="6dbfa-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dbfa-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dbfa-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6dbfa-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dbfa-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6dbfa-124">INPUTS</span></span>

### <span data-ttu-id="6dbfa-125">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6dbfa-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6dbfa-126">System. String</span><span class="sxs-lookup"><span data-stu-id="6dbfa-126">System.String</span></span>

## <span data-ttu-id="6dbfa-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6dbfa-127">OUTPUTS</span></span>

### <span data-ttu-id="6dbfa-128">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="6dbfa-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="6dbfa-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="6dbfa-129">NOTES</span></span>

## <span data-ttu-id="6dbfa-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6dbfa-130">RELATED LINKS</span></span>

[<span data-ttu-id="6dbfa-131">Neu – AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="6dbfa-131">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="6dbfa-132">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="6dbfa-132">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)

[<span data-ttu-id="6dbfa-133">Satz-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="6dbfa-133">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


