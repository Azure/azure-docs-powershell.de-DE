---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRevision.md
ms.openlocfilehash: 16c108d4f62d9bcc44176fce7ede9a7e56d98687
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302259"
---
# <span data-ttu-id="4854e-101">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="4854e-101">Get-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="4854e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4854e-102">SYNOPSIS</span></span>
<span data-ttu-id="4854e-103">Ruft Details aller API-Überarbeitungen einer API ab</span><span class="sxs-lookup"><span data-stu-id="4854e-103">Gets details of all the API Revisions of an API</span></span>

## <span data-ttu-id="4854e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4854e-104">SYNTAX</span></span>

```
Get-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4854e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4854e-105">DESCRIPTION</span></span>
<span data-ttu-id="4854e-106">Das Cmdlet " **Get-AzApiManagementApiRevision** " Ruft die Details aller Überarbeitungen einer API ab.</span><span class="sxs-lookup"><span data-stu-id="4854e-106">The **Get-AzApiManagementApiRevision** cmdlet gets the details of all revisions of an API</span></span>

## <span data-ttu-id="4854e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4854e-107">EXAMPLES</span></span>

### <span data-ttu-id="4854e-108">Beispiel 1: Abrufen aller API-Überarbeitungen einer API</span><span class="sxs-lookup"><span data-stu-id="4854e-108">Example 1: Get all API Revisions of an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRevision -Context $ApiMgmtContext -ApiId "5adf6fbf0faadf3ad8558065"

ApiId           : /apis/5adf6fbf0faadf3ad8558065;rev=3
ApiRevision     : 3
CreatedDateTime : 4/26/2018 10:57:42 PM
UpdatedDateTime : 4/26/2018 10:57:42 PM
Description     : ddsds
PrivateUrl      : /httpbin/v1;rev=3
IsOnline        : True
IsCurrent       : False

ApiId           : /apis/5adf6fbf0faadf3ad8558065;rev=2
ApiRevision     : 2
CreatedDateTime : 4/26/2018 10:57:33 PM
UpdatedDateTime : 4/26/2018 10:57:33 PM
Description     : AA
PrivateUrl      : /httpbin/v1
IsOnline        : True
IsCurrent       : True

ApiId           : /apis/5adf6fbf0faadf3ad8558065;rev=1
ApiRevision     : 1
CreatedDateTime : 4/24/2018 5:56:17 PM
UpdatedDateTime : 5/9/2018 9:29:06 PM
Description     :
PrivateUrl      : /httpbin/v1;rev=1
IsOnline        : True
IsCurrent       : False
```

<span data-ttu-id="4854e-109">Dieser Befehl ruft alle API-Revision der angegebenen API für einen bestimmten ApiManagement-Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="4854e-109">This command gets all of the API revision of specified API for particular ApiManagement Context.</span></span>

## <span data-ttu-id="4854e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4854e-110">PARAMETERS</span></span>

### <span data-ttu-id="4854e-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="4854e-111">-ApiId</span></span>
<span data-ttu-id="4854e-112">API-Bezeichner, dessen Überarbeitungen wir auflisten möchten.</span><span class="sxs-lookup"><span data-stu-id="4854e-112">API identifier whose revisions we want to list.</span></span>
<span data-ttu-id="4854e-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4854e-113">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4854e-114">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="4854e-114">-ApiRevision</span></span>
<span data-ttu-id="4854e-115">Revisions-ID der jeweiligen API-Revision.</span><span class="sxs-lookup"><span data-stu-id="4854e-115">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="4854e-116">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="4854e-116">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4854e-117">-Context</span><span class="sxs-lookup"><span data-stu-id="4854e-117">-Context</span></span>
<span data-ttu-id="4854e-118">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="4854e-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="4854e-119">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4854e-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4854e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4854e-120">-DefaultProfile</span></span>
<span data-ttu-id="4854e-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4854e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4854e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4854e-122">CommonParameters</span></span>
<span data-ttu-id="4854e-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4854e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4854e-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4854e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4854e-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4854e-125">INPUTS</span></span>

### <span data-ttu-id="4854e-126">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4854e-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4854e-127">System. String</span><span class="sxs-lookup"><span data-stu-id="4854e-127">System.String</span></span>

## <span data-ttu-id="4854e-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4854e-128">OUTPUTS</span></span>

### <span data-ttu-id="4854e-129">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="4854e-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRevision</span></span>

## <span data-ttu-id="4854e-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="4854e-130">NOTES</span></span>

## <span data-ttu-id="4854e-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4854e-131">RELATED LINKS</span></span>
