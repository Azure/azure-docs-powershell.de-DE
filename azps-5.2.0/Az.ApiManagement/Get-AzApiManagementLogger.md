---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
ms.openlocfilehash: c4b7246a2b600c1ed0d9f8a01ea3fd69cd4af33d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98301136"
---
# <span data-ttu-id="e9e9a-101">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="e9e9a-101">Get-AzApiManagementLogger</span></span>

## <span data-ttu-id="e9e9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9e9a-102">SYNOPSIS</span></span>
<span data-ttu-id="e9e9a-103">Ruft APIs-Verwaltungsprotokollierungsobjekte ab.</span><span class="sxs-lookup"><span data-stu-id="e9e9a-103">Gets API Management Logger objects.</span></span>

## <span data-ttu-id="e9e9a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e9e9a-104">SYNTAX</span></span>

### <span data-ttu-id="e9e9a-105">GetAllLoggers (Standard)</span><span class="sxs-lookup"><span data-stu-id="e9e9a-105">GetAllLoggers (Default)</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e9e9a-106">GetByLoggerId</span><span class="sxs-lookup"><span data-stu-id="e9e9a-106">GetByLoggerId</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9e9a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e9e9a-107">DESCRIPTION</span></span>
<span data-ttu-id="e9e9a-108">Das **Cmdlet "Get-AzApiManagementLogger"** ruft einen Azure API Management **Logger** oder alle Logger ab.</span><span class="sxs-lookup"><span data-stu-id="e9e9a-108">The **Get-AzApiManagementLogger** cmdlet gets an Azure API Management **Logger** or all the loggers.</span></span>

## <span data-ttu-id="e9e9a-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e9e9a-109">EXAMPLES</span></span>

### <span data-ttu-id="e9e9a-110">Beispiel 1: Alle Protokoller erhalten</span><span class="sxs-lookup"><span data-stu-id="e9e9a-110">Example 1: Get all loggers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext
```

<span data-ttu-id="e9e9a-111">Dieser Befehl ruft alle Logger für den angegebenen Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="e9e9a-111">This command gets all the loggers for the specified context.</span></span>

### <span data-ttu-id="e9e9a-112">Beispiel 2: Einen bestimmten Protokollger erhalten</span><span class="sxs-lookup"><span data-stu-id="e9e9a-112">Example 2: Get a specific logger</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123"
```

<span data-ttu-id="e9e9a-113">Mit diesem Befehl wird ein Protokoller entfernt, der den ID Logger123 enthält.</span><span class="sxs-lookup"><span data-stu-id="e9e9a-113">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="e9e9a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9e9a-114">PARAMETERS</span></span>

### <span data-ttu-id="e9e9a-115">-Context</span><span class="sxs-lookup"><span data-stu-id="e9e9a-115">-Context</span></span>
<span data-ttu-id="e9e9a-116">Gibt ein **"PsApiManagementContext"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="e9e9a-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e9e9a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9e9a-117">-DefaultProfile</span></span>
<span data-ttu-id="e9e9a-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e9e9a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9e9a-119">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="e9e9a-119">-LoggerId</span></span>
<span data-ttu-id="e9e9a-120">Gibt die ID des zu erhaltenden Loggers an.</span><span class="sxs-lookup"><span data-stu-id="e9e9a-120">Specifies the ID of the specific logger to get.</span></span>

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

### <span data-ttu-id="e9e9a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9e9a-121">CommonParameters</span></span>
<span data-ttu-id="e9e9a-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9e9a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9e9a-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e9e9a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9e9a-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e9e9a-124">INPUTS</span></span>

### <span data-ttu-id="e9e9a-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e9e9a-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e9e9a-126">System.String</span><span class="sxs-lookup"><span data-stu-id="e9e9a-126">System.String</span></span>

## <span data-ttu-id="e9e9a-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e9e9a-127">OUTPUTS</span></span>

### <span data-ttu-id="e9e9a-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="e9e9a-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="e9e9a-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e9e9a-129">NOTES</span></span>

## <span data-ttu-id="e9e9a-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e9e9a-130">RELATED LINKS</span></span>

[<span data-ttu-id="e9e9a-131">New-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="e9e9a-131">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="e9e9a-132">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="e9e9a-132">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)

[<span data-ttu-id="e9e9a-133">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="e9e9a-133">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


