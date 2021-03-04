---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
ms.openlocfilehash: a4a6cf459c253c26f5d550492f8b756d59fcdf44
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940656"
---
# <span data-ttu-id="30ea7-101">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="30ea7-101">Get-AzApiManagement</span></span>

## <span data-ttu-id="30ea7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30ea7-102">SYNOPSIS</span></span>
<span data-ttu-id="30ea7-103">Ruft eine Liste oder eine bestimmte API-Verwaltungsdienstbeschreibung ab.</span><span class="sxs-lookup"><span data-stu-id="30ea7-103">Gets a list or a particular API Management Service description.</span></span>

## <span data-ttu-id="30ea7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="30ea7-104">SYNTAX</span></span>

### <span data-ttu-id="30ea7-105">GetBySubscription (Standard)</span><span class="sxs-lookup"><span data-stu-id="30ea7-105">GetBySubscription (Default)</span></span>
```
Get-AzApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30ea7-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="30ea7-106">GetByResourceGroup</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30ea7-107">GetByResource</span><span class="sxs-lookup"><span data-stu-id="30ea7-107">GetByResource</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="30ea7-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="30ea7-108">ByResourceId</span></span>
```
Get-AzApiManagement -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30ea7-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="30ea7-109">DESCRIPTION</span></span>
<span data-ttu-id="30ea7-110">Das **Get-AzApiManagement-Cmdlet** ruft eine Liste aller API-Verwaltungsdienste unter Abonnement oder einer angegebenen Ressourcengruppe oder einer bestimmten API-Verwaltung ab.</span><span class="sxs-lookup"><span data-stu-id="30ea7-110">The **Get-AzApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="30ea7-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="30ea7-111">EXAMPLES</span></span>

### <span data-ttu-id="30ea7-112">Beispiel 1: Abrufen aller API-Verwaltungsdienste</span><span class="sxs-lookup"><span data-stu-id="30ea7-112">Example 1: Get all API Management services</span></span>
```powershell
PS C:\>Get-AzApiManagement
```

<span data-ttu-id="30ea7-113">Dieser Befehl ruft alle API-Verwaltungsdienste innerhalb eines Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="30ea7-113">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="30ea7-114">Beispiel 2: Abrufen aller API-Verwaltungsdienste unter einem bestimmten Namen</span><span class="sxs-lookup"><span data-stu-id="30ea7-114">Example 2: Get all API Management services by a specific name</span></span>
```powershell
PS C:\>Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="30ea7-115">Dieser Befehl ruft alle API-Verwaltungsdienste nach Namen ab.</span><span class="sxs-lookup"><span data-stu-id="30ea7-115">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="30ea7-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="30ea7-116">PARAMETERS</span></span>

### <span data-ttu-id="30ea7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30ea7-117">-DefaultProfile</span></span>
<span data-ttu-id="30ea7-118">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="30ea7-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30ea7-119">-Name</span><span class="sxs-lookup"><span data-stu-id="30ea7-119">-Name</span></span>
<span data-ttu-id="30ea7-120">Gibt den Namen des API-Verwaltungsdiensts an.</span><span class="sxs-lookup"><span data-stu-id="30ea7-120">Specifies the name of API Management service.</span></span>

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

### <span data-ttu-id="30ea7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30ea7-121">-ResourceGroupName</span></span>
<span data-ttu-id="30ea7-122">Gibt den Namen der Ressourcengruppe an, unter der dieses Cmdlet den API-Verwaltungsdienst erhält.</span><span class="sxs-lookup"><span data-stu-id="30ea7-122">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

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

### <span data-ttu-id="30ea7-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="30ea7-123">-ResourceId</span></span>
<span data-ttu-id="30ea7-124">Arm ResourceId des API-Verwaltungsdiensts.</span><span class="sxs-lookup"><span data-stu-id="30ea7-124">Arm ResourceId of the API Management service.</span></span>

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

### <span data-ttu-id="30ea7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30ea7-125">CommonParameters</span></span>
<span data-ttu-id="30ea7-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30ea7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30ea7-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30ea7-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30ea7-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="30ea7-128">INPUTS</span></span>

### <span data-ttu-id="30ea7-129">System.String</span><span class="sxs-lookup"><span data-stu-id="30ea7-129">System.String</span></span>

## <span data-ttu-id="30ea7-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="30ea7-130">OUTPUTS</span></span>

### <span data-ttu-id="30ea7-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="30ea7-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="30ea7-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="30ea7-132">NOTES</span></span>

## <span data-ttu-id="30ea7-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="30ea7-133">RELATED LINKS</span></span>

[<span data-ttu-id="30ea7-134">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="30ea7-134">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="30ea7-135">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="30ea7-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="30ea7-136">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="30ea7-136">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="30ea7-137">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="30ea7-137">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


