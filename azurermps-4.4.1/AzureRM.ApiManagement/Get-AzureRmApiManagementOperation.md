---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
ms.openlocfilehash: b2c623d46dcc2d84e2c90ae5f3d94cfb54f7224a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498110"
---
# <span data-ttu-id="dbdd3-101">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="dbdd3-101">Get-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="dbdd3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dbdd3-102">SYNOPSIS</span></span>
<span data-ttu-id="dbdd3-103">Ruft eine Liste oder einen angegebenen API-Vorgang ab.</span><span class="sxs-lookup"><span data-stu-id="dbdd3-103">Gets a list or a specified API Operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbdd3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dbdd3-104">SYNTAX</span></span>

### <span data-ttu-id="dbdd3-105">Alle API-Vorgänge (Standard)</span><span class="sxs-lookup"><span data-stu-id="dbdd3-105">All API Operations (Default)</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbdd3-106">Nach ID suchen</span><span class="sxs-lookup"><span data-stu-id="dbdd3-106">Find by ID</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbdd3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dbdd3-107">DESCRIPTION</span></span>
<span data-ttu-id="dbdd3-108">Die **Get-AzureRmApiManagementOperation** Ruft eine Liste oder einen angegebenen API-Vorgang ab.</span><span class="sxs-lookup"><span data-stu-id="dbdd3-108">The **Get-AzureRmApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="dbdd3-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dbdd3-109">EXAMPLES</span></span>

### <span data-ttu-id="dbdd3-110">Beispiel 1: Abrufen aller API-Verwaltungsvorgänge</span><span class="sxs-lookup"><span data-stu-id="dbdd3-110">Example 1: Get all API management operations</span></span>
```
PS C:\>Get-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIId
```

<span data-ttu-id="dbdd3-111">Dieser Befehl ruft alle API-Verwaltungsvorgänge ab.</span><span class="sxs-lookup"><span data-stu-id="dbdd3-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="dbdd3-112">Beispiel 2: Abrufen einer API-Verwaltungsoperation nach Vorgangs-ID</span><span class="sxs-lookup"><span data-stu-id="dbdd3-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>Get-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="dbdd3-113">Dieser Befehl ruft eine API-Verwaltungsoperation anhand der Vorgangs-ID mit dem Namen Operation0003 ab.</span><span class="sxs-lookup"><span data-stu-id="dbdd3-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="dbdd3-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="dbdd3-114">PARAMETERS</span></span>

### <span data-ttu-id="dbdd3-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="dbdd3-115">-ApiId</span></span>
<span data-ttu-id="dbdd3-116">Gibt den Bezeichner des API-Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="dbdd3-116">Specifies the identifier of the API Operation.</span></span>

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

### <span data-ttu-id="dbdd3-117">-Context</span><span class="sxs-lookup"><span data-stu-id="dbdd3-117">-Context</span></span>
<span data-ttu-id="dbdd3-118">Gibt die Instanz des **PsApiManagementContext** -Objekts an.</span><span class="sxs-lookup"><span data-stu-id="dbdd3-118">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="dbdd3-119">-Vorgangs-Nr</span><span class="sxs-lookup"><span data-stu-id="dbdd3-119">-OperationId</span></span>
<span data-ttu-id="dbdd3-120">Gibt die Vorgangs-ID an.</span><span class="sxs-lookup"><span data-stu-id="dbdd3-120">Specifies the operation identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbdd3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbdd3-121">-DefaultProfile</span></span>
<span data-ttu-id="dbdd3-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dbdd3-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbdd3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbdd3-123">CommonParameters</span></span>
<span data-ttu-id="dbdd3-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbdd3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbdd3-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbdd3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbdd3-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dbdd3-126">INPUTS</span></span>

## <span data-ttu-id="dbdd3-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dbdd3-127">OUTPUTS</span></span>

### <span data-ttu-id="dbdd3-128">IList<Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementOperation></span><span class="sxs-lookup"><span data-stu-id="dbdd3-128">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation></span></span>

## <span data-ttu-id="dbdd3-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="dbdd3-129">NOTES</span></span>

## <span data-ttu-id="dbdd3-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dbdd3-130">RELATED LINKS</span></span>

[<span data-ttu-id="dbdd3-131">Neu – AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="dbdd3-131">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="dbdd3-132">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="dbdd3-132">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)

[<span data-ttu-id="dbdd3-133">Satz-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="dbdd3-133">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


