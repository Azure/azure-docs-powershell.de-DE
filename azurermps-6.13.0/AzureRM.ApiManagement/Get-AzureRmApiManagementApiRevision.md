---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApiRevision.md
ms.openlocfilehash: f57a95e97c0ec74e7e45338e15a028feab60849b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498557"
---
# <span data-ttu-id="523cc-101">Get-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="523cc-101">Get-AzureRmApiManagementApiRevision</span></span>

## <span data-ttu-id="523cc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="523cc-102">SYNOPSIS</span></span>
<span data-ttu-id="523cc-103">Ruft Details aller API-Überarbeitungen einer API ab</span><span class="sxs-lookup"><span data-stu-id="523cc-103">Gets details of all the API Revisions of an API</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="523cc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="523cc-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="523cc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="523cc-105">DESCRIPTION</span></span>
<span data-ttu-id="523cc-106">Das Cmdlet " **Get-AzureRmApiManagementApiRevision** " Ruft die Details aller Überarbeitungen einer API ab.</span><span class="sxs-lookup"><span data-stu-id="523cc-106">The **Get-AzureRmApiManagementApiRevision** cmdlet gets the details of all revisions of an API</span></span>

## <span data-ttu-id="523cc-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="523cc-107">EXAMPLES</span></span>

### <span data-ttu-id="523cc-108">Beispiel 1: Abrufen aller API-Überarbeitungen einer API</span><span class="sxs-lookup"><span data-stu-id="523cc-108">Example 1: Get all API Revisions of an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementApiRevision -Context $ApiMgmtContext -ApiId "5adf6fbf0faadf3ad8558065"

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

<span data-ttu-id="523cc-109">Dieser Befehl ruft alle API-Revision der angegebenen API für einen bestimmten ApiManagement-Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="523cc-109">This command gets all of the API revision of specified API for particular ApiManagement Context.</span></span>

## <span data-ttu-id="523cc-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="523cc-110">PARAMETERS</span></span>

### <span data-ttu-id="523cc-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="523cc-111">-ApiId</span></span>
<span data-ttu-id="523cc-112">API-Bezeichner, dessen Überarbeitungen wir auflisten möchten.</span><span class="sxs-lookup"><span data-stu-id="523cc-112">API identifier whose revisions we want to list.</span></span>
<span data-ttu-id="523cc-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="523cc-113">This parameter is required.</span></span>

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

### <span data-ttu-id="523cc-114">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="523cc-114">-ApiRevision</span></span>
<span data-ttu-id="523cc-115">Revisions-ID der jeweiligen API-Revision.</span><span class="sxs-lookup"><span data-stu-id="523cc-115">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="523cc-116">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="523cc-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="523cc-117">-Context</span><span class="sxs-lookup"><span data-stu-id="523cc-117">-Context</span></span>
<span data-ttu-id="523cc-118">Instanz von PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="523cc-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="523cc-119">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="523cc-119">This parameter is required.</span></span>

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

### <span data-ttu-id="523cc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="523cc-120">-DefaultProfile</span></span>
<span data-ttu-id="523cc-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="523cc-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="523cc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="523cc-122">CommonParameters</span></span>
<span data-ttu-id="523cc-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="523cc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="523cc-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="523cc-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="523cc-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="523cc-125">INPUTS</span></span>

### <span data-ttu-id="523cc-126">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="523cc-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="523cc-127">System. String</span><span class="sxs-lookup"><span data-stu-id="523cc-127">System.String</span></span>

## <span data-ttu-id="523cc-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="523cc-128">OUTPUTS</span></span>

### <span data-ttu-id="523cc-129">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="523cc-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRevision</span></span>

## <span data-ttu-id="523cc-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="523cc-130">NOTES</span></span>

## <span data-ttu-id="523cc-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="523cc-131">RELATED LINKS</span></span>
