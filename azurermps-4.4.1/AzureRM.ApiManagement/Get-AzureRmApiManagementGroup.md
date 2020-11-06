---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementGroup.md
ms.openlocfilehash: 0c28742eb3c774adb8c7b6a8d920e91377bea35f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499281"
---
# <span data-ttu-id="f1cd8-101">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="f1cd8-101">Get-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="f1cd8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f1cd8-102">SYNOPSIS</span></span>
<span data-ttu-id="f1cd8-103">Ruft alle oder bestimmte API-Verwaltungsgruppen ab.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-103">Gets all or specific API management groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1cd8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1cd8-104">SYNTAX</span></span>

### <span data-ttu-id="f1cd8-105">Alle Gruppen abrufen (Standard)</span><span class="sxs-lookup"><span data-stu-id="f1cd8-105">Get all groups (Default)</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1cd8-106">Abrufen nach Gruppen-ID</span><span class="sxs-lookup"><span data-stu-id="f1cd8-106">Get by group ID</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1cd8-107">Suchen nach Gruppen nach Benutzer</span><span class="sxs-lookup"><span data-stu-id="f1cd8-107">Find groups by user</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1cd8-108">Suchen nach Gruppen nach Produkt</span><span class="sxs-lookup"><span data-stu-id="f1cd8-108">Find groups by product</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1cd8-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f1cd8-109">DESCRIPTION</span></span>
<span data-ttu-id="f1cd8-110">Das Cmdlet " **Get-AzureRmApiManagementGroup** " ruft alle oder bestimmte API-Verwaltungsgruppen ab.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-110">The **Get-AzureRmApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="f1cd8-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f1cd8-111">EXAMPLES</span></span>

### <span data-ttu-id="f1cd8-112">Beispiel 1: Abrufen aller Gruppen</span><span class="sxs-lookup"><span data-stu-id="f1cd8-112">Example 1: Get all groups</span></span>
```
PS C:\>Get-AzureRmApiManagementGroup -Context $APImContext
```

<span data-ttu-id="f1cd8-113">Dieser Befehl ruft alle Gruppen ab.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-113">This command gets all groups.</span></span>

### <span data-ttu-id="f1cd8-114">Beispiel 2: Abrufen einer Group by-ID</span><span class="sxs-lookup"><span data-stu-id="f1cd8-114">Example 2: Get a group by ID</span></span>
```
PS C:\>Get-AzureRmApiManagementGroup -Context $APImContext -GroupId "0123456789"
```

<span data-ttu-id="f1cd8-115">Mit diesem Befehl wird die Gruppen-ID mit dem Namen 0123456789 abgerufen.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="f1cd8-116">Beispiel 3: Abrufen einer Gruppe nach Name</span><span class="sxs-lookup"><span data-stu-id="f1cd8-116">Example 3: Get a group by name</span></span>
```
PS C:\>Get-AzureRmApiManagementGroup -Context $APImContext -Name "Group0002"
```

<span data-ttu-id="f1cd8-117">Dieser Befehl ruft die Gruppe mit dem Namen Group0002 ab.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="f1cd8-118">Beispiel 4: Abrufen aller Benutzergruppen</span><span class="sxs-lookup"><span data-stu-id="f1cd8-118">Example 4: Get all user groups</span></span>
```
PS C:\>Get-AzureRmApiManagementGroup -Context $APImContext -UserId "0123456789"
```

<span data-ttu-id="f1cd8-119">Mit diesem Befehl werden alle Benutzergruppen mit der Benutzer-ID namens 0123456789 abgerufen.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="f1cd8-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1cd8-120">PARAMETERS</span></span>

### <span data-ttu-id="f1cd8-121">-Context</span><span class="sxs-lookup"><span data-stu-id="f1cd8-121">-Context</span></span>
<span data-ttu-id="f1cd8-122">Gibt eine Instanz von PsApiManagementContext an.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-122">Specifies an instance of PsApiManagementContext.</span></span>

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

### <span data-ttu-id="f1cd8-123">-Gruppen-Nr</span><span class="sxs-lookup"><span data-stu-id="f1cd8-123">-GroupId</span></span>
<span data-ttu-id="f1cd8-124">Gibt die Gruppen-ID an.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-124">Specifies the group ID.</span></span>
<span data-ttu-id="f1cd8-125">Wenn angegeben, versucht das Cmdlet, die Gruppe nach dem Bezeichner zu finden.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-125">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by group ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1cd8-126">-Name</span><span class="sxs-lookup"><span data-stu-id="f1cd8-126">-Name</span></span>
<span data-ttu-id="f1cd8-127">Gibt den Namen der Verwaltungsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-127">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="f1cd8-128">-ProductID</span><span class="sxs-lookup"><span data-stu-id="f1cd8-128">-ProductId</span></span>
<span data-ttu-id="f1cd8-129">Bezeichner des vorhandenen Produkts.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-129">Identifier of existing product.</span></span>
<span data-ttu-id="f1cd8-130">Wenn angegeben, werden alle Gruppen zurückgegeben, denen das Produkt zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-130">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="f1cd8-131">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-131">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find groups by product
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1cd8-132">-UserID</span><span class="sxs-lookup"><span data-stu-id="f1cd8-132">-UserId</span></span>
<span data-ttu-id="f1cd8-133">Gibt den Bezeichner des vorhandenen Produkts an.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-133">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="f1cd8-134">Wenn angegeben, gibt das Cmdlet alle Gruppen zurück, denen das Produkt zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-134">If specified the cmdlet will return all groups the product assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: Find groups by user
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1cd8-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1cd8-135">-DefaultProfile</span></span>
<span data-ttu-id="f1cd8-136">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1cd8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1cd8-137">CommonParameters</span></span>
<span data-ttu-id="f1cd8-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1cd8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1cd8-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1cd8-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1cd8-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f1cd8-140">INPUTS</span></span>

## <span data-ttu-id="f1cd8-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f1cd8-141">OUTPUTS</span></span>

### <span data-ttu-id="f1cd8-142">IList<Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementGroup></span><span class="sxs-lookup"><span data-stu-id="f1cd8-142">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup></span></span>

## <span data-ttu-id="f1cd8-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="f1cd8-143">NOTES</span></span>

## <span data-ttu-id="f1cd8-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f1cd8-144">RELATED LINKS</span></span>

[<span data-ttu-id="f1cd8-145">Neu – AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="f1cd8-145">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="f1cd8-146">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="f1cd8-146">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)

[<span data-ttu-id="f1cd8-147">Satz-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="f1cd8-147">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)


