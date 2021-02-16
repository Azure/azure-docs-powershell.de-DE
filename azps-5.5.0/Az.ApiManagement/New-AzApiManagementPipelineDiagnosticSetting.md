---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementpipelinediagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
ms.openlocfilehash: 7e6f6515b24a7cefabd40a6fdfaedfda430f69d0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166985"
---
# <span data-ttu-id="9484b-101">New-AzApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="9484b-101">New-AzApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="9484b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9484b-102">SYNOPSIS</span></span>
<span data-ttu-id="9484b-103">Erstellen Sie Diagnoseeinstellungen für eingehende/ausgehende HTTP-Nachrichten an das Gateway.</span><span class="sxs-lookup"><span data-stu-id="9484b-103">Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="9484b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9484b-104">SYNTAX</span></span>

```
New-AzApiManagementPipelineDiagnosticSetting [-Request <PsApiManagementHttpMessageDiagnostic>]
 [-Response <PsApiManagementHttpMessageDiagnostic>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9484b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9484b-105">DESCRIPTION</span></span>
<span data-ttu-id="9484b-106">Das Cmdlet **"New-AzApiManagementPipelineDiagnosticSetting"** erstellt die Diagnoseeinstellungen für eingehende/ausgehende HTTP-Nachrichten an das Gateway.</span><span class="sxs-lookup"><span data-stu-id="9484b-106">The cmdlet **New-AzApiManagementPipelineDiagnosticSetting** creates the Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="9484b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9484b-107">EXAMPLES</span></span>

### <span data-ttu-id="9484b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9484b-108">Example 1</span></span>
```powershell
PS c:\> $httpMessageDiagnostic = New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100
PS c:\> New-AzApiManagementPipelineDiagnosticSetting -Request $httpMessageDiagnostic -Response $httpMessageDiagnostic

Request                                                                                              Response
-------                                                                                              --------
Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
```

<span data-ttu-id="9484b-109">Erstellen Sie ein Pipelinediagnosetool, das in FrontEnd oder Back-End in der Diagnoseentität verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9484b-109">Create a pipeline diagnostic to be used in either FrontEnd or Backend in the Diagnostic Entity.</span></span>

## <span data-ttu-id="9484b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9484b-110">PARAMETERS</span></span>

### <span data-ttu-id="9484b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9484b-111">-DefaultProfile</span></span>
<span data-ttu-id="9484b-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9484b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9484b-113">-Request</span><span class="sxs-lookup"><span data-stu-id="9484b-113">-Request</span></span>
<span data-ttu-id="9484b-114">Diagnoseeinstellung für Anforderung.</span><span class="sxs-lookup"><span data-stu-id="9484b-114">Diagnostic setting for Request.</span></span>
<span data-ttu-id="9484b-115">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="9484b-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="9484b-116">-Response</span><span class="sxs-lookup"><span data-stu-id="9484b-116">-Response</span></span>
<span data-ttu-id="9484b-117">Diagnoseeinstellung für "Antwort".</span><span class="sxs-lookup"><span data-stu-id="9484b-117">Diagnostic setting for Response.</span></span>
<span data-ttu-id="9484b-118">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="9484b-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="9484b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9484b-119">CommonParameters</span></span>
<span data-ttu-id="9484b-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9484b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9484b-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9484b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9484b-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9484b-122">INPUTS</span></span>

### <span data-ttu-id="9484b-123">Keine</span><span class="sxs-lookup"><span data-stu-id="9484b-123">None</span></span>

## <span data-ttu-id="9484b-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9484b-124">OUTPUTS</span></span>

### <span data-ttu-id="9484b-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="9484b-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="9484b-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9484b-126">NOTES</span></span>

## <span data-ttu-id="9484b-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9484b-127">RELATED LINKS</span></span>

[<span data-ttu-id="9484b-128">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="9484b-128">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="9484b-129">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="9484b-129">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="9484b-130">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="9484b-130">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="9484b-131">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="9484b-131">New-AzApiManagementHttpMessageDiagnostic</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)


