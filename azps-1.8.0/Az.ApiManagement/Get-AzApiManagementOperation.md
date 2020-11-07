---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
ms.openlocfilehash: 8fdfa75e78d48fb582af869a240476bfff31f25d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650381"
---
# <span data-ttu-id="6171c-101">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="6171c-101">Get-AzApiManagementOperation</span></span>

## <span data-ttu-id="6171c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6171c-102">SYNOPSIS</span></span>
<span data-ttu-id="6171c-103">Ruft eine Liste oder einen angegebenen API-Vorgang ab.</span><span class="sxs-lookup"><span data-stu-id="6171c-103">Gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="6171c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6171c-104">SYNTAX</span></span>

### <span data-ttu-id="6171c-105">GetAllApiOperations (Standard)</span><span class="sxs-lookup"><span data-stu-id="6171c-105">GetAllApiOperations (Default)</span></span>
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6171c-106">GetById</span><span class="sxs-lookup"><span data-stu-id="6171c-106">GetById</span></span>
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6171c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6171c-107">DESCRIPTION</span></span>
<span data-ttu-id="6171c-108">Die **Get-AzApiManagementOperation** Ruft eine Liste oder einen angegebenen API-Vorgang ab.</span><span class="sxs-lookup"><span data-stu-id="6171c-108">The **Get-AzApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="6171c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6171c-109">EXAMPLES</span></span>

### <span data-ttu-id="6171c-110">Beispiel 1: Abrufen aller API-Verwaltungsvorgänge</span><span class="sxs-lookup"><span data-stu-id="6171c-110">Example 1: Get all API management operations</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId
```

<span data-ttu-id="6171c-111">Dieser Befehl ruft alle API-Verwaltungsvorgänge ab.</span><span class="sxs-lookup"><span data-stu-id="6171c-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="6171c-112">Beispiel 2: Abrufen einer API-Verwaltungsoperation nach Vorgangs-ID</span><span class="sxs-lookup"><span data-stu-id="6171c-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="6171c-113">Dieser Befehl ruft eine API-Verwaltungsoperation anhand der Vorgangs-ID mit dem Namen Operation0003 ab.</span><span class="sxs-lookup"><span data-stu-id="6171c-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="6171c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="6171c-114">PARAMETERS</span></span>

### <span data-ttu-id="6171c-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="6171c-115">-ApiId</span></span>
<span data-ttu-id="6171c-116">Gibt den Bezeichner des API-Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="6171c-116">Specifies the identifier of the API Operation.</span></span>

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

### <span data-ttu-id="6171c-117">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="6171c-117">-ApiRevision</span></span>
<span data-ttu-id="6171c-118">Bezeichner der API-Überarbeitung.</span><span class="sxs-lookup"><span data-stu-id="6171c-118">Identifier of API Revision.</span></span> <span data-ttu-id="6171c-119">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="6171c-119">This parameter is optional.</span></span> <span data-ttu-id="6171c-120">Wenn keine Angabe erfolgt, wird der Vorgang aus der aktuell aktiven API-Revision abgerufen.</span><span class="sxs-lookup"><span data-stu-id="6171c-120">If not specified, the operation will be retrieved from the currently active api revision.</span></span>

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

### <span data-ttu-id="6171c-121">-Context</span><span class="sxs-lookup"><span data-stu-id="6171c-121">-Context</span></span>
<span data-ttu-id="6171c-122">Gibt die Instanz des **PsApiManagementContext** -Objekts an.</span><span class="sxs-lookup"><span data-stu-id="6171c-122">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="6171c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6171c-123">-DefaultProfile</span></span>
<span data-ttu-id="6171c-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6171c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6171c-125">-Vorgangs-Nr</span><span class="sxs-lookup"><span data-stu-id="6171c-125">-OperationId</span></span>
<span data-ttu-id="6171c-126">Gibt die Vorgangs-ID an.</span><span class="sxs-lookup"><span data-stu-id="6171c-126">Specifies the operation identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6171c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6171c-127">CommonParameters</span></span>
<span data-ttu-id="6171c-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6171c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6171c-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6171c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6171c-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6171c-130">INPUTS</span></span>

### <span data-ttu-id="6171c-131">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6171c-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6171c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6171c-132">System.String</span></span>

## <span data-ttu-id="6171c-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6171c-133">OUTPUTS</span></span>

### <span data-ttu-id="6171c-134">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="6171c-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="6171c-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="6171c-135">NOTES</span></span>

## <span data-ttu-id="6171c-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6171c-136">RELATED LINKS</span></span>

[<span data-ttu-id="6171c-137">Neu – AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="6171c-137">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="6171c-138">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="6171c-138">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)

[<span data-ttu-id="6171c-139">Satz-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="6171c-139">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


