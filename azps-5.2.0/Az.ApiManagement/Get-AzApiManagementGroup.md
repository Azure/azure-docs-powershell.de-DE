---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
ms.openlocfilehash: c7f88f204bbb6d4999e6ddb1f0f3e2942500daf7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365418"
---
# <span data-ttu-id="0d531-101">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="0d531-101">Get-AzApiManagementGroup</span></span>

## <span data-ttu-id="0d531-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d531-102">SYNOPSIS</span></span>
<span data-ttu-id="0d531-103">Ruft alle oder bestimmte API-Verwaltungsgruppen ab.</span><span class="sxs-lookup"><span data-stu-id="0d531-103">Gets all or specific API management groups.</span></span>

## <span data-ttu-id="0d531-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0d531-104">SYNTAX</span></span>

### <span data-ttu-id="0d531-105">GetAllGroups (Standard)</span><span class="sxs-lookup"><span data-stu-id="0d531-105">GetAllGroups (Default)</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d531-106">GetByGroupId</span><span class="sxs-lookup"><span data-stu-id="0d531-106">GetByGroupId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d531-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="0d531-107">GetByUserId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d531-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="0d531-108">GetByProductId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d531-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0d531-109">DESCRIPTION</span></span>
<span data-ttu-id="0d531-110">Das **Cmdlet "Get-AzApiManagementGroup"** ruft alle oder bestimmte API-Verwaltungsgruppen ab.</span><span class="sxs-lookup"><span data-stu-id="0d531-110">The **Get-AzApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="0d531-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0d531-111">EXAMPLES</span></span>

### <span data-ttu-id="0d531-112">Beispiel 1: Alle Gruppen erhalten</span><span class="sxs-lookup"><span data-stu-id="0d531-112">Example 1: Get all groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext
```

<span data-ttu-id="0d531-113">Dieser Befehl ruft alle Gruppen ab.</span><span class="sxs-lookup"><span data-stu-id="0d531-113">This command gets all groups.</span></span>

### <span data-ttu-id="0d531-114">Beispiel 2: Erhalten einer Gruppe nach ID</span><span class="sxs-lookup"><span data-stu-id="0d531-114">Example 2: Get a group by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -GroupId "0123456789"
```

<span data-ttu-id="0d531-115">Dieser Befehl ruft die Gruppen-ID mit dem Namen 0123456789 ab.</span><span class="sxs-lookup"><span data-stu-id="0d531-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="0d531-116">Beispiel 3: Erhalten einer Gruppe nach Name</span><span class="sxs-lookup"><span data-stu-id="0d531-116">Example 3: Get a group by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -Name "Group0002"
```

<span data-ttu-id="0d531-117">Dieser Befehl ruft die Gruppe mit dem Namen "Group0002" ab.</span><span class="sxs-lookup"><span data-stu-id="0d531-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="0d531-118">Beispiel 4: Alle Benutzergruppen erhalten</span><span class="sxs-lookup"><span data-stu-id="0d531-118">Example 4: Get all user groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="0d531-119">Dieser Befehl ruft alle Benutzergruppen mit der Benutzer-ID "0123456789" ab.</span><span class="sxs-lookup"><span data-stu-id="0d531-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="0d531-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0d531-120">PARAMETERS</span></span>

### <span data-ttu-id="0d531-121">-Context</span><span class="sxs-lookup"><span data-stu-id="0d531-121">-Context</span></span>
<span data-ttu-id="0d531-122">Gibt eine Instanz von "PsApiManagementContext" an.</span><span class="sxs-lookup"><span data-stu-id="0d531-122">Specifies an instance of PsApiManagementContext.</span></span>

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

### <span data-ttu-id="0d531-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d531-123">-DefaultProfile</span></span>
<span data-ttu-id="0d531-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0d531-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d531-125">-GroupId</span><span class="sxs-lookup"><span data-stu-id="0d531-125">-GroupId</span></span>
<span data-ttu-id="0d531-126">Gibt die Gruppen-ID an.</span><span class="sxs-lookup"><span data-stu-id="0d531-126">Specifies the group ID.</span></span>
<span data-ttu-id="0d531-127">Falls angegeben, versucht das Cmdlet, die Gruppe nach dem Bezeichner zu finden.</span><span class="sxs-lookup"><span data-stu-id="0d531-127">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByGroupId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d531-128">-Name</span><span class="sxs-lookup"><span data-stu-id="0d531-128">-Name</span></span>
<span data-ttu-id="0d531-129">Gibt den Namen der Verwaltungsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="0d531-129">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="0d531-130">-ProductId</span><span class="sxs-lookup"><span data-stu-id="0d531-130">-ProductId</span></span>
<span data-ttu-id="0d531-131">Id eines vorhandenen Produkts.</span><span class="sxs-lookup"><span data-stu-id="0d531-131">Identifier of existing product.</span></span>
<span data-ttu-id="0d531-132">Wenn diese Angabe angegeben wird, werden alle Gruppen, denen das Produkt zugewiesen ist, zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="0d531-132">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="0d531-133">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="0d531-133">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d531-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="0d531-134">-UserId</span></span>
<span data-ttu-id="0d531-135">Gibt den Bezeichner eines vorhandenen Produkts an.</span><span class="sxs-lookup"><span data-stu-id="0d531-135">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="0d531-136">Wenn diese Angabe angegeben ist, gibt das Cmdlet alle Gruppen zurück, denen das Produkt zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="0d531-136">If specified the cmdlet will return all groups the product assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUserId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d531-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d531-137">CommonParameters</span></span>
<span data-ttu-id="0d531-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d531-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d531-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0d531-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d531-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0d531-140">INPUTS</span></span>

### <span data-ttu-id="0d531-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0d531-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0d531-142">System.String</span><span class="sxs-lookup"><span data-stu-id="0d531-142">System.String</span></span>

## <span data-ttu-id="0d531-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0d531-143">OUTPUTS</span></span>

### <span data-ttu-id="0d531-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="0d531-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="0d531-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0d531-145">NOTES</span></span>

## <span data-ttu-id="0d531-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0d531-146">RELATED LINKS</span></span>

[<span data-ttu-id="0d531-147">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="0d531-147">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="0d531-148">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="0d531-148">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)

[<span data-ttu-id="0d531-149">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="0d531-149">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


