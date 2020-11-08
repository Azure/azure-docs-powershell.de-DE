---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementhttpmessagediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
ms.openlocfilehash: 10c84654bb5d074ee9f668062d1fa7a18d92f8b0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177144"
---
# <span data-ttu-id="4c151-101">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="4c151-101">New-AzApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="4c151-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4c151-102">SYNOPSIS</span></span>
<span data-ttu-id="4c151-103">Erstellt eine Instanz von **PsApiManagementHttpMessageDiagnostic** , bei der es sich um eine HTTP-Nachrichten Diagnose Einstellung der Diagnose handelt.</span><span class="sxs-lookup"><span data-stu-id="4c151-103">Creates an instance of **PsApiManagementHttpMessageDiagnostic** which is an Http Message diagnostic setting of the Diagnostic</span></span>

## <span data-ttu-id="4c151-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c151-104">SYNTAX</span></span>

```
New-AzApiManagementHttpMessageDiagnostic [-HeadersToLog <String[]>] [-BodyBytesToLog <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c151-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4c151-105">DESCRIPTION</span></span>
<span data-ttu-id="4c151-106">Das Cmdlet **New-AzApiManagementHttpMessageDiagnostic** erstellt die Diagnose Einstellung für HTTP-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="4c151-106">The cmdlet **New-AzApiManagementHttpMessageDiagnostic** creates the Http Message diagnostic setting.</span></span>

## <span data-ttu-id="4c151-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4c151-107">EXAMPLES</span></span>

### <span data-ttu-id="4c151-108">Beispiel 1: Erstellen einer einfachen Diagnose Einstellung für HTTP-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="4c151-108">Example 1: Create a Basic Http Message diagnostic Setting</span></span>
```powershell
PS C:\>  New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100

Headers                   Body
-------                   ----
{Content-Type, UserAgent} Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBodyDiagnosticSetting
```

<span data-ttu-id="4c151-109">Erstellen einer Diagnose Einstellung für HTTP-Nachrichten für die Protokollierung `Content-Type` und über `User-Agent` Schriften zusammen mit 100 Byte `body`</span><span class="sxs-lookup"><span data-stu-id="4c151-109">Create a http message diagnostic setting to log `Content-Type` and `User-Agent` headers along with 100 bytes of `body`</span></span>

## <span data-ttu-id="4c151-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4c151-110">PARAMETERS</span></span>

### <span data-ttu-id="4c151-111">-BodyBytesToLog</span><span class="sxs-lookup"><span data-stu-id="4c151-111">-BodyBytesToLog</span></span>
<span data-ttu-id="4c151-112">Die Anzahl der anzumeldenden Bytes des Anforderungstexts.</span><span class="sxs-lookup"><span data-stu-id="4c151-112">Number of request body bytes to log.</span></span> <span data-ttu-id="4c151-113">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="4c151-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="4c151-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c151-114">-DefaultProfile</span></span>
<span data-ttu-id="4c151-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4c151-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c151-116">-HeadersToLog</span><span class="sxs-lookup"><span data-stu-id="4c151-116">-HeadersToLog</span></span>
<span data-ttu-id="4c151-117">Das Array der zu protokollierenden Kopfzeilen.</span><span class="sxs-lookup"><span data-stu-id="4c151-117">The array of headers to log.</span></span> <span data-ttu-id="4c151-118">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="4c151-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="4c151-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c151-119">CommonParameters</span></span>
<span data-ttu-id="4c151-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c151-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c151-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4c151-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c151-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4c151-122">INPUTS</span></span>

### <span data-ttu-id="4c151-123">Keine</span><span class="sxs-lookup"><span data-stu-id="4c151-123">None</span></span>

## <span data-ttu-id="4c151-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4c151-124">OUTPUTS</span></span>

### <span data-ttu-id="4c151-125">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="4c151-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="4c151-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="4c151-126">NOTES</span></span>

## <span data-ttu-id="4c151-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4c151-127">RELATED LINKS</span></span>

[<span data-ttu-id="4c151-128">Neu – AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="4c151-128">New-AzApiManagementDiagnostic</span></span>](./New-AzApiManagementDiagnostic.md)

[<span data-ttu-id="4c151-129">Neu – AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="4c151-129">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)