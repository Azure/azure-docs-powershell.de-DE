---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
ms.openlocfilehash: 41f7b921cb1977d7410c511be224b7e24623597b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471518"
---
# <span data-ttu-id="ef7c1-101">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="ef7c1-101">Get-AzApiManagement</span></span>

## <span data-ttu-id="ef7c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef7c1-102">SYNOPSIS</span></span>
<span data-ttu-id="ef7c1-103">Ruft eine Liste oder eine bestimmte BESCHREIBUNG des API-Verwaltungsdiensts ab.</span><span class="sxs-lookup"><span data-stu-id="ef7c1-103">Gets a list or a particular API Management Service description.</span></span>

## <span data-ttu-id="ef7c1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ef7c1-104">SYNTAX</span></span>

### <span data-ttu-id="ef7c1-105">GetBySubscription (Standard)</span><span class="sxs-lookup"><span data-stu-id="ef7c1-105">GetBySubscription (Default)</span></span>
```
Get-AzApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef7c1-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ef7c1-106">GetByResourceGroup</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef7c1-107">GetByResource</span><span class="sxs-lookup"><span data-stu-id="ef7c1-107">GetByResource</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ef7c1-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ef7c1-108">ByResourceId</span></span>
```
Get-AzApiManagement -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef7c1-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ef7c1-109">DESCRIPTION</span></span>
<span data-ttu-id="ef7c1-110">Das **Cmdlet "Get-AzApiManagement"** ruft eine Liste aller API-Verwaltungsdienste im Abonnement oder einer angegebenen Ressourcengruppe oder einer bestimmten API-Verwaltung ab.</span><span class="sxs-lookup"><span data-stu-id="ef7c1-110">The **Get-AzApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="ef7c1-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ef7c1-111">EXAMPLES</span></span>

### <span data-ttu-id="ef7c1-112">Beispiel 1: Abrufen aller API-Verwaltungsdienste</span><span class="sxs-lookup"><span data-stu-id="ef7c1-112">Example 1: Get all API Management services</span></span>
```powershell
PS C:\>Get-AzApiManagement
```

<span data-ttu-id="ef7c1-113">Dieser Befehl ruft alle API-Verwaltungsdienste in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="ef7c1-113">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="ef7c1-114">Beispiel 2: Abrufen aller API-Verwaltungsdienste unter einem bestimmten Namen</span><span class="sxs-lookup"><span data-stu-id="ef7c1-114">Example 2: Get all API Management services by a specific name</span></span>
```powershell
PS C:\>Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="ef7c1-115">Dieser Befehl ruft den sämtlichen API-Verwaltungsdienst nach Name ab.</span><span class="sxs-lookup"><span data-stu-id="ef7c1-115">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="ef7c1-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef7c1-116">PARAMETERS</span></span>

### <span data-ttu-id="ef7c1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef7c1-117">-DefaultProfile</span></span>
<span data-ttu-id="ef7c1-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ef7c1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef7c1-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ef7c1-119">-Name</span></span>
<span data-ttu-id="ef7c1-120">Gibt den Namen des API-Verwaltungsdiensts an.</span><span class="sxs-lookup"><span data-stu-id="ef7c1-120">Specifies the name of API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef7c1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef7c1-121">-ResourceGroupName</span></span>
<span data-ttu-id="ef7c1-122">Gibt den Namen der Ressourcengruppe an, unter der dieses Cmdlet den API-Verwaltungsdienst erhält.</span><span class="sxs-lookup"><span data-stu-id="ef7c1-122">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup, GetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef7c1-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef7c1-123">-ResourceId</span></span>
<span data-ttu-id="ef7c1-124">Arm ResourceId des API-Verwaltungsdiensts.</span><span class="sxs-lookup"><span data-stu-id="ef7c1-124">Arm ResourceId of the API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef7c1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef7c1-125">CommonParameters</span></span>
<span data-ttu-id="ef7c1-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef7c1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef7c1-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef7c1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef7c1-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ef7c1-128">INPUTS</span></span>

### <span data-ttu-id="ef7c1-129">System.String</span><span class="sxs-lookup"><span data-stu-id="ef7c1-129">System.String</span></span>

## <span data-ttu-id="ef7c1-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ef7c1-130">OUTPUTS</span></span>

### <span data-ttu-id="ef7c1-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="ef7c1-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="ef7c1-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ef7c1-132">NOTES</span></span>

## <span data-ttu-id="ef7c1-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ef7c1-133">RELATED LINKS</span></span>

[<span data-ttu-id="ef7c1-134">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="ef7c1-134">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="ef7c1-135">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="ef7c1-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="ef7c1-136">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="ef7c1-136">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="ef7c1-137">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="ef7c1-137">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


