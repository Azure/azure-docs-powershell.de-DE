---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
ms.openlocfilehash: 5807925c302f951f9e48c89afcb62634bd774c89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949792"
---
# <span data-ttu-id="e9d99-101">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="e9d99-101">Get-AzApiManagementOperation</span></span>

## <span data-ttu-id="e9d99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9d99-102">SYNOPSIS</span></span>
<span data-ttu-id="e9d99-103">Ruft eine Liste oder einen angegebenen API-Vorgang ab.</span><span class="sxs-lookup"><span data-stu-id="e9d99-103">Gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="e9d99-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e9d99-104">SYNTAX</span></span>

### <span data-ttu-id="e9d99-105">GetAllApiOperations (Standard)</span><span class="sxs-lookup"><span data-stu-id="e9d99-105">GetAllApiOperations (Default)</span></span>
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9d99-106">GetById</span><span class="sxs-lookup"><span data-stu-id="e9d99-106">GetById</span></span>
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9d99-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e9d99-107">DESCRIPTION</span></span>
<span data-ttu-id="e9d99-108">Die **Get-AzApiManagementOperation** ruft eine Liste oder einen angegebenen API-Vorgang ab.</span><span class="sxs-lookup"><span data-stu-id="e9d99-108">The **Get-AzApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="e9d99-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e9d99-109">EXAMPLES</span></span>

### <span data-ttu-id="e9d99-110">Beispiel 1: Abrufen aller API-Verwaltungsvorgänge</span><span class="sxs-lookup"><span data-stu-id="e9d99-110">Example 1: Get all API management operations</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId
```

<span data-ttu-id="e9d99-111">Dieser Befehl ruft alle API-Verwaltungsvorgänge ab.</span><span class="sxs-lookup"><span data-stu-id="e9d99-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="e9d99-112">Beispiel 2: Abrufen eines API-Verwaltungsvorgangs nach Vorgangs-ID</span><span class="sxs-lookup"><span data-stu-id="e9d99-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="e9d99-113">Dieser Befehl ruft einen API-Verwaltungsvorgang nach Vorgangs-ID mit dem Namen Operation0003 ab.</span><span class="sxs-lookup"><span data-stu-id="e9d99-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="e9d99-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e9d99-114">PARAMETERS</span></span>

### <span data-ttu-id="e9d99-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="e9d99-115">-ApiId</span></span>
<span data-ttu-id="e9d99-116">Gibt den Bezeichner des API-Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="e9d99-116">Specifies the identifier of the API Operation.</span></span>

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

### <span data-ttu-id="e9d99-117">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="e9d99-117">-ApiRevision</span></span>
<span data-ttu-id="e9d99-118">Bezeichner der API-Überarbeitung.</span><span class="sxs-lookup"><span data-stu-id="e9d99-118">Identifier of API Revision.</span></span> <span data-ttu-id="e9d99-119">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="e9d99-119">This parameter is optional.</span></span> <span data-ttu-id="e9d99-120">Wenn nicht angegeben, wird der Vorgang aus der aktuell aktiven Apirevision abgerufen.</span><span class="sxs-lookup"><span data-stu-id="e9d99-120">If not specified, the operation will be retrieved from the currently active api revision.</span></span>

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

### <span data-ttu-id="e9d99-121">-Context</span><span class="sxs-lookup"><span data-stu-id="e9d99-121">-Context</span></span>
<span data-ttu-id="e9d99-122">Gibt die Instanz des **PsApiManagementContext-Objekts** an.</span><span class="sxs-lookup"><span data-stu-id="e9d99-122">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e9d99-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9d99-123">-DefaultProfile</span></span>
<span data-ttu-id="e9d99-124">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e9d99-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9d99-125">-OperationId</span><span class="sxs-lookup"><span data-stu-id="e9d99-125">-OperationId</span></span>
<span data-ttu-id="e9d99-126">Gibt den Vorgangsbezeichner an.</span><span class="sxs-lookup"><span data-stu-id="e9d99-126">Specifies the operation identifier.</span></span>

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

### <span data-ttu-id="e9d99-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9d99-127">CommonParameters</span></span>
<span data-ttu-id="e9d99-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9d99-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9d99-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e9d99-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9d99-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e9d99-130">INPUTS</span></span>

### <span data-ttu-id="e9d99-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e9d99-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e9d99-132">System.String</span><span class="sxs-lookup"><span data-stu-id="e9d99-132">System.String</span></span>

## <span data-ttu-id="e9d99-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e9d99-133">OUTPUTS</span></span>

### <span data-ttu-id="e9d99-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="e9d99-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="e9d99-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e9d99-135">NOTES</span></span>

## <span data-ttu-id="e9d99-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e9d99-136">RELATED LINKS</span></span>

[<span data-ttu-id="e9d99-137">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="e9d99-137">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="e9d99-138">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="e9d99-138">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)

[<span data-ttu-id="e9d99-139">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="e9d99-139">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


