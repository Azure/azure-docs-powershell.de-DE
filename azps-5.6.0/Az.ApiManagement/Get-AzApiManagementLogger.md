---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
ms.openlocfilehash: aafe70a476dbf983e8ae68b0f1fadf021b2990f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929120"
---
# <span data-ttu-id="80f67-101">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="80f67-101">Get-AzApiManagementLogger</span></span>

## <span data-ttu-id="80f67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80f67-102">SYNOPSIS</span></span>
<span data-ttu-id="80f67-103">Ruft API-Verwaltungsprotokollierungsobjekte ab.</span><span class="sxs-lookup"><span data-stu-id="80f67-103">Gets API Management Logger objects.</span></span>

## <span data-ttu-id="80f67-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="80f67-104">SYNTAX</span></span>

### <span data-ttu-id="80f67-105">GetAllLoggers (Standard)</span><span class="sxs-lookup"><span data-stu-id="80f67-105">GetAllLoggers (Default)</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="80f67-106">GetByLoggerId</span><span class="sxs-lookup"><span data-stu-id="80f67-106">GetByLoggerId</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80f67-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="80f67-107">DESCRIPTION</span></span>
<span data-ttu-id="80f67-108">Das **Get-AzApiManagementLogger-Cmdlet** ruft einen Azure API-Verwaltungslogger oder alle **Logger** ab.</span><span class="sxs-lookup"><span data-stu-id="80f67-108">The **Get-AzApiManagementLogger** cmdlet gets an Azure API Management **Logger** or all the loggers.</span></span>

## <span data-ttu-id="80f67-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="80f67-109">EXAMPLES</span></span>

### <span data-ttu-id="80f67-110">Beispiel 1: Alle Protokollierungsdateien erhalten</span><span class="sxs-lookup"><span data-stu-id="80f67-110">Example 1: Get all loggers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext
```

<span data-ttu-id="80f67-111">Dieser Befehl ruft alle Logger für den angegebenen Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="80f67-111">This command gets all the loggers for the specified context.</span></span>

### <span data-ttu-id="80f67-112">Beispiel 2: Erhalten eines bestimmten Loggers</span><span class="sxs-lookup"><span data-stu-id="80f67-112">Example 2: Get a specific logger</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123"
```

<span data-ttu-id="80f67-113">Mit diesem Befehl wird ein Logger entfernt, der über die ID Logger123 verfügt.</span><span class="sxs-lookup"><span data-stu-id="80f67-113">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="80f67-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="80f67-114">PARAMETERS</span></span>

### <span data-ttu-id="80f67-115">-Context</span><span class="sxs-lookup"><span data-stu-id="80f67-115">-Context</span></span>
<span data-ttu-id="80f67-116">Gibt ein **PsApiManagementContext-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="80f67-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="80f67-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80f67-117">-DefaultProfile</span></span>
<span data-ttu-id="80f67-118">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="80f67-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80f67-119">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="80f67-119">-LoggerId</span></span>
<span data-ttu-id="80f67-120">Gibt die ID des bestimmten Zu erhaltenden Loggers an.</span><span class="sxs-lookup"><span data-stu-id="80f67-120">Specifies the ID of the specific logger to get.</span></span>

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

### <span data-ttu-id="80f67-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80f67-121">CommonParameters</span></span>
<span data-ttu-id="80f67-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80f67-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80f67-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80f67-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80f67-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="80f67-124">INPUTS</span></span>

### <span data-ttu-id="80f67-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="80f67-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="80f67-126">System.String</span><span class="sxs-lookup"><span data-stu-id="80f67-126">System.String</span></span>

## <span data-ttu-id="80f67-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="80f67-127">OUTPUTS</span></span>

### <span data-ttu-id="80f67-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="80f67-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="80f67-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="80f67-129">NOTES</span></span>

## <span data-ttu-id="80f67-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="80f67-130">RELATED LINKS</span></span>

[<span data-ttu-id="80f67-131">New-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="80f67-131">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="80f67-132">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="80f67-132">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)

[<span data-ttu-id="80f67-133">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="80f67-133">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


