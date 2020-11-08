---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
ms.openlocfilehash: c7f88f204bbb6d4999e6ddb1f0f3e2942500daf7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173973"
---
# <span data-ttu-id="83ba9-101">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="83ba9-101">Get-AzApiManagementGroup</span></span>

## <span data-ttu-id="83ba9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="83ba9-102">SYNOPSIS</span></span>
<span data-ttu-id="83ba9-103">Ruft alle oder bestimmte API-Verwaltungsgruppen ab.</span><span class="sxs-lookup"><span data-stu-id="83ba9-103">Gets all or specific API management groups.</span></span>

## <span data-ttu-id="83ba9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="83ba9-104">SYNTAX</span></span>

### <span data-ttu-id="83ba9-105">GetAllGroups (Standard)</span><span class="sxs-lookup"><span data-stu-id="83ba9-105">GetAllGroups (Default)</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83ba9-106">GetByGroupId</span><span class="sxs-lookup"><span data-stu-id="83ba9-106">GetByGroupId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83ba9-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="83ba9-107">GetByUserId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83ba9-108">Getneben-Nr</span><span class="sxs-lookup"><span data-stu-id="83ba9-108">GetByProductId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83ba9-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="83ba9-109">DESCRIPTION</span></span>
<span data-ttu-id="83ba9-110">Das Cmdlet " **Get-AzApiManagementGroup** " ruft alle oder bestimmte API-Verwaltungsgruppen ab.</span><span class="sxs-lookup"><span data-stu-id="83ba9-110">The **Get-AzApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="83ba9-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="83ba9-111">EXAMPLES</span></span>

### <span data-ttu-id="83ba9-112">Beispiel 1: Abrufen aller Gruppen</span><span class="sxs-lookup"><span data-stu-id="83ba9-112">Example 1: Get all groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext
```

<span data-ttu-id="83ba9-113">Dieser Befehl ruft alle Gruppen ab.</span><span class="sxs-lookup"><span data-stu-id="83ba9-113">This command gets all groups.</span></span>

### <span data-ttu-id="83ba9-114">Beispiel 2: Abrufen einer Group by-ID</span><span class="sxs-lookup"><span data-stu-id="83ba9-114">Example 2: Get a group by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -GroupId "0123456789"
```

<span data-ttu-id="83ba9-115">Mit diesem Befehl wird die Gruppen-ID mit dem Namen 0123456789 abgerufen.</span><span class="sxs-lookup"><span data-stu-id="83ba9-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="83ba9-116">Beispiel 3: Abrufen einer Gruppe nach Name</span><span class="sxs-lookup"><span data-stu-id="83ba9-116">Example 3: Get a group by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -Name "Group0002"
```

<span data-ttu-id="83ba9-117">Dieser Befehl ruft die Gruppe mit dem Namen Group0002 ab.</span><span class="sxs-lookup"><span data-stu-id="83ba9-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="83ba9-118">Beispiel 4: Abrufen aller Benutzergruppen</span><span class="sxs-lookup"><span data-stu-id="83ba9-118">Example 4: Get all user groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="83ba9-119">Mit diesem Befehl werden alle Benutzergruppen mit der Benutzer-ID namens 0123456789 abgerufen.</span><span class="sxs-lookup"><span data-stu-id="83ba9-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="83ba9-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="83ba9-120">PARAMETERS</span></span>

### <span data-ttu-id="83ba9-121">-Context</span><span class="sxs-lookup"><span data-stu-id="83ba9-121">-Context</span></span>
<span data-ttu-id="83ba9-122">Gibt eine Instanz von PsApiManagementContext an.</span><span class="sxs-lookup"><span data-stu-id="83ba9-122">Specifies an instance of PsApiManagementContext.</span></span>

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

### <span data-ttu-id="83ba9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83ba9-123">-DefaultProfile</span></span>
<span data-ttu-id="83ba9-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="83ba9-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83ba9-125">-Gruppen-Nr</span><span class="sxs-lookup"><span data-stu-id="83ba9-125">-GroupId</span></span>
<span data-ttu-id="83ba9-126">Gibt die Gruppen-ID an.</span><span class="sxs-lookup"><span data-stu-id="83ba9-126">Specifies the group ID.</span></span>
<span data-ttu-id="83ba9-127">Wenn angegeben, versucht das Cmdlet, die Gruppe nach dem Bezeichner zu finden.</span><span class="sxs-lookup"><span data-stu-id="83ba9-127">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

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

### <span data-ttu-id="83ba9-128">-Name</span><span class="sxs-lookup"><span data-stu-id="83ba9-128">-Name</span></span>
<span data-ttu-id="83ba9-129">Gibt den Namen der Verwaltungsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="83ba9-129">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="83ba9-130">-ProductID</span><span class="sxs-lookup"><span data-stu-id="83ba9-130">-ProductId</span></span>
<span data-ttu-id="83ba9-131">Bezeichner des vorhandenen Produkts.</span><span class="sxs-lookup"><span data-stu-id="83ba9-131">Identifier of existing product.</span></span>
<span data-ttu-id="83ba9-132">Wenn angegeben, werden alle Gruppen zurückgegeben, denen das Produkt zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="83ba9-132">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="83ba9-133">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="83ba9-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="83ba9-134">-UserID</span><span class="sxs-lookup"><span data-stu-id="83ba9-134">-UserId</span></span>
<span data-ttu-id="83ba9-135">Gibt den Bezeichner des vorhandenen Produkts an.</span><span class="sxs-lookup"><span data-stu-id="83ba9-135">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="83ba9-136">Wenn angegeben, gibt das Cmdlet alle Gruppen zurück, denen das Produkt zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="83ba9-136">If specified the cmdlet will return all groups the product assigned to.</span></span>

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

### <span data-ttu-id="83ba9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83ba9-137">CommonParameters</span></span>
<span data-ttu-id="83ba9-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83ba9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83ba9-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83ba9-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83ba9-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="83ba9-140">INPUTS</span></span>

### <span data-ttu-id="83ba9-141">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="83ba9-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="83ba9-142">System. String</span><span class="sxs-lookup"><span data-stu-id="83ba9-142">System.String</span></span>

## <span data-ttu-id="83ba9-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="83ba9-143">OUTPUTS</span></span>

### <span data-ttu-id="83ba9-144">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="83ba9-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="83ba9-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="83ba9-145">NOTES</span></span>

## <span data-ttu-id="83ba9-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="83ba9-146">RELATED LINKS</span></span>

[<span data-ttu-id="83ba9-147">Neu – AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="83ba9-147">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="83ba9-148">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="83ba9-148">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)

[<span data-ttu-id="83ba9-149">Satz-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="83ba9-149">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


