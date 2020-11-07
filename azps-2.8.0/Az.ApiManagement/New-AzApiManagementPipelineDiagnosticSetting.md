---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementpipelinediagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
ms.openlocfilehash: f2d9c12cb3795d23144fa5296cba992a25383819
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658240"
---
# <span data-ttu-id="92f58-101">New-AzApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="92f58-101">New-AzApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="92f58-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="92f58-102">SYNOPSIS</span></span>
<span data-ttu-id="92f58-103">Erstellen Sie Diagnoseeinstellungen für eingehende/ausgehende HTTP-Nachrichten an das Gateway.</span><span class="sxs-lookup"><span data-stu-id="92f58-103">Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="92f58-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="92f58-104">SYNTAX</span></span>

```
New-AzApiManagementPipelineDiagnosticSetting [-Request <PsApiManagementHttpMessageDiagnostic>]
 [-Response <PsApiManagementHttpMessageDiagnostic>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="92f58-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="92f58-105">DESCRIPTION</span></span>
<span data-ttu-id="92f58-106">Das Cmdlet **New-AzApiManagementPipelineDiagnosticSetting** erstellt die Diagnoseeinstellungen für eingehende/ausgehende HTTP-Nachrichten an das Gateway.</span><span class="sxs-lookup"><span data-stu-id="92f58-106">The cmdlet **New-AzApiManagementPipelineDiagnosticSetting** creates the Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="92f58-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="92f58-107">EXAMPLES</span></span>

### <span data-ttu-id="92f58-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="92f58-108">Example 1</span></span>
```powershell
PS c:\> $httpMessageDiagnostic = New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100
PS c:\> New-AzApiManagementPipelineDiagnosticSetting -Request $httpMessageDiagnostic -Response $httpMessageDiagnostic

Request                                                                                              Response
-------                                                                                              --------
Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
```

<span data-ttu-id="92f58-109">Erstellen Sie eine Pipeline Diagnose, die entweder in der Frontend-oder Back-End-Anwendung in der diagnostischen Entität verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="92f58-109">Create a pipeline diagnostic to be used in either FrontEnd or Backend in the Diagnostic Entity.</span></span>

## <span data-ttu-id="92f58-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="92f58-110">PARAMETERS</span></span>

### <span data-ttu-id="92f58-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92f58-111">-DefaultProfile</span></span>
<span data-ttu-id="92f58-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="92f58-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92f58-113">-Anfrage</span><span class="sxs-lookup"><span data-stu-id="92f58-113">-Request</span></span>
<span data-ttu-id="92f58-114">Diagnose Einstellung für Anforderung.</span><span class="sxs-lookup"><span data-stu-id="92f58-114">Diagnostic setting for Request.</span></span>
<span data-ttu-id="92f58-115">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="92f58-115">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92f58-116">-Response</span><span class="sxs-lookup"><span data-stu-id="92f58-116">-Response</span></span>
<span data-ttu-id="92f58-117">Diagnose Einstellung für Antwort.</span><span class="sxs-lookup"><span data-stu-id="92f58-117">Diagnostic setting for Response.</span></span>
<span data-ttu-id="92f58-118">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="92f58-118">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92f58-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92f58-119">CommonParameters</span></span>
<span data-ttu-id="92f58-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92f58-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92f58-121">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92f58-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92f58-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="92f58-122">INPUTS</span></span>

### <span data-ttu-id="92f58-123">Keine</span><span class="sxs-lookup"><span data-stu-id="92f58-123">None</span></span>

## <span data-ttu-id="92f58-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="92f58-124">OUTPUTS</span></span>

### <span data-ttu-id="92f58-125">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="92f58-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="92f58-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="92f58-126">NOTES</span></span>

## <span data-ttu-id="92f58-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="92f58-127">RELATED LINKS</span></span>

[<span data-ttu-id="92f58-128">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="92f58-128">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="92f58-129">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="92f58-129">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="92f58-130">Satz-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="92f58-130">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="92f58-131">Neu – AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="92f58-131">New-AzApiManagementHttpMessageDiagnostic</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)


