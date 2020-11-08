---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementhttpmessagediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
ms.openlocfilehash: d3706168a23a32d4338069cb593ef8dd71242896
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996942"
---
# <span data-ttu-id="20ce2-101">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="20ce2-101">New-AzApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="20ce2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="20ce2-102">SYNOPSIS</span></span>
<span data-ttu-id="20ce2-103">Erstellt eine Instanz von **PsApiManagementHttpMessageDiagnostic** , bei der es sich um eine HTTP-Nachrichten Diagnose Einstellung der Diagnose handelt.</span><span class="sxs-lookup"><span data-stu-id="20ce2-103">Creates an instance of **PsApiManagementHttpMessageDiagnostic** which is an Http Message diagnostic setting of the Diagnostic</span></span>

## <span data-ttu-id="20ce2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="20ce2-104">SYNTAX</span></span>

```
New-AzApiManagementHttpMessageDiagnostic [-HeadersToLog <String[]>] [-BodyBytesToLog <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20ce2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20ce2-105">DESCRIPTION</span></span>
<span data-ttu-id="20ce2-106">Das Cmdlet **New-AzApiManagementHttpMessageDiagnostic** erstellt die Diagnose Einstellung für HTTP-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="20ce2-106">The cmdlet **New-AzApiManagementHttpMessageDiagnostic** creates the Http Message diagnostic setting.</span></span>

## <span data-ttu-id="20ce2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="20ce2-107">EXAMPLES</span></span>

### <span data-ttu-id="20ce2-108">Beispiel 1: Erstellen einer einfachen Diagnose Einstellung für HTTP-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="20ce2-108">Example 1 : Create a Basic Http Message diagnostic Setting</span></span>
```powershell
PS C:\>  New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100

Headers                   Body
-------                   ----
{Content-Type, UserAgent} Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBodyDiagnosticSetting
```

<span data-ttu-id="20ce2-109">Erstellen einer Diagnose Einstellung für HTTP-Nachrichten für die Protokollierung `Content-Type` und über `User-Agent` Schriften zusammen mit 100 Byte `body`</span><span class="sxs-lookup"><span data-stu-id="20ce2-109">Create a http message diagnostic setting to log `Content-Type` and `User-Agent` headers along with 100 bytes of `body`</span></span>

## <span data-ttu-id="20ce2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="20ce2-110">PARAMETERS</span></span>

### <span data-ttu-id="20ce2-111">-BodyBytesToLog</span><span class="sxs-lookup"><span data-stu-id="20ce2-111">-BodyBytesToLog</span></span>
<span data-ttu-id="20ce2-112">Die Anzahl der anzumeldenden Bytes des Anforderungstexts.</span><span class="sxs-lookup"><span data-stu-id="20ce2-112">Number of request body bytes to log.</span></span> <span data-ttu-id="20ce2-113">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="20ce2-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="20ce2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20ce2-114">-DefaultProfile</span></span>
<span data-ttu-id="20ce2-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="20ce2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20ce2-116">-HeadersToLog</span><span class="sxs-lookup"><span data-stu-id="20ce2-116">-HeadersToLog</span></span>
<span data-ttu-id="20ce2-117">Das Array der zu protokollierenden Kopfzeilen.</span><span class="sxs-lookup"><span data-stu-id="20ce2-117">The array of headers to log.</span></span> <span data-ttu-id="20ce2-118">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="20ce2-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="20ce2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20ce2-119">CommonParameters</span></span>
<span data-ttu-id="20ce2-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20ce2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20ce2-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20ce2-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20ce2-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="20ce2-122">INPUTS</span></span>

### <span data-ttu-id="20ce2-123">Keine</span><span class="sxs-lookup"><span data-stu-id="20ce2-123">None</span></span>

## <span data-ttu-id="20ce2-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="20ce2-124">OUTPUTS</span></span>

### <span data-ttu-id="20ce2-125">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="20ce2-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="20ce2-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="20ce2-126">NOTES</span></span>

## <span data-ttu-id="20ce2-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="20ce2-127">RELATED LINKS</span></span>

[<span data-ttu-id="20ce2-128">Neu – AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="20ce2-128">New-AzApiManagementDiagnostic</span></span>](./New-AzApiManagementDiagnostic.md)

[<span data-ttu-id="20ce2-129">Neu – AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="20ce2-129">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)