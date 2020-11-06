---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementGroup.md
ms.openlocfilehash: b77452bff93a9b66f8ffe54fdff623d391749622
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500633"
---
# <span data-ttu-id="71047-101">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="71047-101">Get-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="71047-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="71047-102">SYNOPSIS</span></span>
<span data-ttu-id="71047-103">Ruft alle oder bestimmte API-Verwaltungsgruppen ab.</span><span class="sxs-lookup"><span data-stu-id="71047-103">Gets all or specific API management groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71047-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="71047-104">SYNTAX</span></span>

### <span data-ttu-id="71047-105">GetAllGroups (Standard)</span><span class="sxs-lookup"><span data-stu-id="71047-105">GetAllGroups (Default)</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71047-106">GetByGroupId</span><span class="sxs-lookup"><span data-stu-id="71047-106">GetByGroupId</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71047-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="71047-107">GetByUserId</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71047-108">Getneben-Nr</span><span class="sxs-lookup"><span data-stu-id="71047-108">GetByProductId</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71047-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="71047-109">DESCRIPTION</span></span>
<span data-ttu-id="71047-110">Das Cmdlet " **Get-AzureRmApiManagementGroup** " ruft alle oder bestimmte API-Verwaltungsgruppen ab.</span><span class="sxs-lookup"><span data-stu-id="71047-110">The **Get-AzureRmApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="71047-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="71047-111">EXAMPLES</span></span>

### <span data-ttu-id="71047-112">Beispiel 1: Abrufen aller Gruppen</span><span class="sxs-lookup"><span data-stu-id="71047-112">Example 1: Get all groups</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementGroup -Context $apimContext
```

<span data-ttu-id="71047-113">Dieser Befehl ruft alle Gruppen ab.</span><span class="sxs-lookup"><span data-stu-id="71047-113">This command gets all groups.</span></span>

### <span data-ttu-id="71047-114">Beispiel 2: Abrufen einer Group by-ID</span><span class="sxs-lookup"><span data-stu-id="71047-114">Example 2: Get a group by ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementGroup -Context $apimContext -GroupId "0123456789"
```

<span data-ttu-id="71047-115">Mit diesem Befehl wird die Gruppen-ID mit dem Namen 0123456789 abgerufen.</span><span class="sxs-lookup"><span data-stu-id="71047-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="71047-116">Beispiel 3: Abrufen einer Gruppe nach Name</span><span class="sxs-lookup"><span data-stu-id="71047-116">Example 3: Get a group by name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementGroup -Context $apimContext -Name "Group0002"
```

<span data-ttu-id="71047-117">Dieser Befehl ruft die Gruppe mit dem Namen Group0002 ab.</span><span class="sxs-lookup"><span data-stu-id="71047-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="71047-118">Beispiel 4: Abrufen aller Benutzergruppen</span><span class="sxs-lookup"><span data-stu-id="71047-118">Example 4: Get all user groups</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementGroup -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="71047-119">Mit diesem Befehl werden alle Benutzergruppen mit der Benutzer-ID namens 0123456789 abgerufen.</span><span class="sxs-lookup"><span data-stu-id="71047-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="71047-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="71047-120">PARAMETERS</span></span>

### <span data-ttu-id="71047-121">-Context</span><span class="sxs-lookup"><span data-stu-id="71047-121">-Context</span></span>
<span data-ttu-id="71047-122">Gibt eine Instanz von PsApiManagementContext an.</span><span class="sxs-lookup"><span data-stu-id="71047-122">Specifies an instance of PsApiManagementContext.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71047-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71047-123">-DefaultProfile</span></span>
<span data-ttu-id="71047-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="71047-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71047-125">-Gruppen-Nr</span><span class="sxs-lookup"><span data-stu-id="71047-125">-GroupId</span></span>
<span data-ttu-id="71047-126">Gibt die Gruppen-ID an.</span><span class="sxs-lookup"><span data-stu-id="71047-126">Specifies the group ID.</span></span>
<span data-ttu-id="71047-127">Wenn angegeben, versucht das Cmdlet, die Gruppe nach dem Bezeichner zu finden.</span><span class="sxs-lookup"><span data-stu-id="71047-127">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

```yaml
Type: String
Parameter Sets: GetByGroupId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71047-128">-Name</span><span class="sxs-lookup"><span data-stu-id="71047-128">-Name</span></span>
<span data-ttu-id="71047-129">Gibt den Namen der Verwaltungsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="71047-129">Specifies the name of the management group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71047-130">-ProductID</span><span class="sxs-lookup"><span data-stu-id="71047-130">-ProductId</span></span>
<span data-ttu-id="71047-131">Bezeichner des vorhandenen Produkts.</span><span class="sxs-lookup"><span data-stu-id="71047-131">Identifier of existing product.</span></span>
<span data-ttu-id="71047-132">Wenn angegeben, werden alle Gruppen zurückgegeben, denen das Produkt zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="71047-132">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="71047-133">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="71047-133">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByProductId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71047-134">-UserID</span><span class="sxs-lookup"><span data-stu-id="71047-134">-UserId</span></span>
<span data-ttu-id="71047-135">Gibt den Bezeichner des vorhandenen Produkts an.</span><span class="sxs-lookup"><span data-stu-id="71047-135">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="71047-136">Wenn angegeben, gibt das Cmdlet alle Gruppen zurück, denen das Produkt zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="71047-136">If specified the cmdlet will return all groups the product assigned to.</span></span>

```yaml
Type: String
Parameter Sets: GetByUserId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71047-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71047-137">CommonParameters</span></span>
<span data-ttu-id="71047-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71047-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71047-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71047-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71047-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="71047-140">INPUTS</span></span>

### <span data-ttu-id="71047-141">Keine</span><span class="sxs-lookup"><span data-stu-id="71047-141">None</span></span>
<span data-ttu-id="71047-142">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="71047-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="71047-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="71047-143">OUTPUTS</span></span>

### <span data-ttu-id="71047-144">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="71047-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>
<span data-ttu-id="71047-145">Die Details der im API-Verwaltungsdienst konfigurierten Gruppe.</span><span class="sxs-lookup"><span data-stu-id="71047-145">The details of the Group configured in API Management service.</span></span>

### <span data-ttu-id="71047-146">IList<Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementGroup></span><span class="sxs-lookup"><span data-stu-id="71047-146">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup></span></span>
<span data-ttu-id="71047-147">Die Liste der Gruppen, die im API-Verwaltungsdienst konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="71047-147">The list of Groups configured in API Management service.</span></span>

## <span data-ttu-id="71047-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="71047-148">NOTES</span></span>

## <span data-ttu-id="71047-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="71047-149">RELATED LINKS</span></span>

[<span data-ttu-id="71047-150">Neu – AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="71047-150">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="71047-151">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="71047-151">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)

[<span data-ttu-id="71047-152">Satz-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="71047-152">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)


