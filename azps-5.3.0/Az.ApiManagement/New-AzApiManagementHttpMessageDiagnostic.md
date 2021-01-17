---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementhttpmessagediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
ms.openlocfilehash: 10c84654bb5d074ee9f668062d1fa7a18d92f8b0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471398"
---
# <span data-ttu-id="d5258-101">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d5258-101">New-AzApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="d5258-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5258-102">SYNOPSIS</span></span>
<span data-ttu-id="d5258-103">Erstellt eine Instanz von **"PsApiManagementHttpMessageDiagnostic",** bei der es sich um eine Http-Nachrichtendiagnoseeinstellung des Diagnosetools handelt.</span><span class="sxs-lookup"><span data-stu-id="d5258-103">Creates an instance of **PsApiManagementHttpMessageDiagnostic** which is an Http Message diagnostic setting of the Diagnostic</span></span>

## <span data-ttu-id="d5258-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5258-104">SYNTAX</span></span>

```
New-AzApiManagementHttpMessageDiagnostic [-HeadersToLog <String[]>] [-BodyBytesToLog <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5258-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d5258-105">DESCRIPTION</span></span>
<span data-ttu-id="d5258-106">Das Cmdlet **"New-AzApiManagementHttpMessageDiagnostic"** erstellt die Diagnoseeinstellung "Http Message".</span><span class="sxs-lookup"><span data-stu-id="d5258-106">The cmdlet **New-AzApiManagementHttpMessageDiagnostic** creates the Http Message diagnostic setting.</span></span>

## <span data-ttu-id="d5258-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d5258-107">EXAMPLES</span></span>

### <span data-ttu-id="d5258-108">Beispiel 1: Erstellen einer grundlegenden Einstellung für die Http-Nachricht-Diagnose</span><span class="sxs-lookup"><span data-stu-id="d5258-108">Example 1: Create a Basic Http Message diagnostic Setting</span></span>
```powershell
PS C:\>  New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100

Headers                   Body
-------                   ----
{Content-Type, UserAgent} Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBodyDiagnosticSetting
```

<span data-ttu-id="d5258-109">Erstellen einer Http-Nachrichtendiagnoseeinstellung zum Protokollieren und Erstellen von Headern zusammen mit `Content-Type` `User-Agent` 100 Bytes `body`</span><span class="sxs-lookup"><span data-stu-id="d5258-109">Create a http message diagnostic setting to log `Content-Type` and `User-Agent` headers along with 100 bytes of `body`</span></span>

## <span data-ttu-id="d5258-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5258-110">PARAMETERS</span></span>

### <span data-ttu-id="d5258-111">-BodyBytesToLog</span><span class="sxs-lookup"><span data-stu-id="d5258-111">-BodyBytesToLog</span></span>
<span data-ttu-id="d5258-112">Anzahl der zu protokollierende Anforderungstextbytes.</span><span class="sxs-lookup"><span data-stu-id="d5258-112">Number of request body bytes to log.</span></span> <span data-ttu-id="d5258-113">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="d5258-113">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5258-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5258-114">-DefaultProfile</span></span>
<span data-ttu-id="d5258-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d5258-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5258-116">-HeadersToLog</span><span class="sxs-lookup"><span data-stu-id="d5258-116">-HeadersToLog</span></span>
<span data-ttu-id="d5258-117">Das Array der zu protokollierenden Überschriften.</span><span class="sxs-lookup"><span data-stu-id="d5258-117">The array of headers to log.</span></span> <span data-ttu-id="d5258-118">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="d5258-118">This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5258-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5258-119">CommonParameters</span></span>
<span data-ttu-id="d5258-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5258-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5258-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d5258-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5258-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d5258-122">INPUTS</span></span>

### <span data-ttu-id="d5258-123">Keine</span><span class="sxs-lookup"><span data-stu-id="d5258-123">None</span></span>

## <span data-ttu-id="d5258-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d5258-124">OUTPUTS</span></span>

### <span data-ttu-id="d5258-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d5258-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="d5258-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d5258-126">NOTES</span></span>

## <span data-ttu-id="d5258-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d5258-127">RELATED LINKS</span></span>

[<span data-ttu-id="d5258-128">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d5258-128">New-AzApiManagementDiagnostic</span></span>](./New-AzApiManagementDiagnostic.md)

[<span data-ttu-id="d5258-129">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="d5258-129">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)