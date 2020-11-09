---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
ms.openlocfilehash: 41f7b921cb1977d7410c511be224b7e24623597b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299925"
---
# <span data-ttu-id="68146-101">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="68146-101">Get-AzApiManagement</span></span>

## <span data-ttu-id="68146-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="68146-102">SYNOPSIS</span></span>
<span data-ttu-id="68146-103">Ruft eine Liste oder eine bestimmte API-Verwaltungsdienst Beschreibung ab.</span><span class="sxs-lookup"><span data-stu-id="68146-103">Gets a list or a particular API Management Service description.</span></span>

## <span data-ttu-id="68146-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="68146-104">SYNTAX</span></span>

### <span data-ttu-id="68146-105">GetBySubscription (Standard)</span><span class="sxs-lookup"><span data-stu-id="68146-105">GetBySubscription (Default)</span></span>
```
Get-AzApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68146-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="68146-106">GetByResourceGroup</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68146-107">GetByResource</span><span class="sxs-lookup"><span data-stu-id="68146-107">GetByResource</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="68146-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="68146-108">ByResourceId</span></span>
```
Get-AzApiManagement -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68146-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="68146-109">DESCRIPTION</span></span>
<span data-ttu-id="68146-110">Das Cmdlet " **Get-AzApiManagement** " Ruft eine Liste aller API-Verwaltungsdienste unter Abonnement oder angegebene Ressourcengruppe oder eine bestimmte API-Verwaltung ab.</span><span class="sxs-lookup"><span data-stu-id="68146-110">The **Get-AzApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="68146-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="68146-111">EXAMPLES</span></span>

### <span data-ttu-id="68146-112">Beispiel 1: Abrufen aller API-Verwaltungsdienste</span><span class="sxs-lookup"><span data-stu-id="68146-112">Example 1: Get all API Management services</span></span>
```powershell
PS C:\>Get-AzApiManagement
```

<span data-ttu-id="68146-113">Dieser Befehl ruft alle API-Verwaltungsdienste innerhalb eines Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="68146-113">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="68146-114">Beispiel 2: Abrufen aller API-Verwaltungsdienste nach einem bestimmten Namen</span><span class="sxs-lookup"><span data-stu-id="68146-114">Example 2: Get all API Management services by a specific name</span></span>
```powershell
PS C:\>Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="68146-115">Mit diesem Befehl wird der gesamte API-Verwaltungsdienst nach Namen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="68146-115">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="68146-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="68146-116">PARAMETERS</span></span>

### <span data-ttu-id="68146-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68146-117">-DefaultProfile</span></span>
<span data-ttu-id="68146-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="68146-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68146-119">-Name</span><span class="sxs-lookup"><span data-stu-id="68146-119">-Name</span></span>
<span data-ttu-id="68146-120">Gibt den Namen des API-Verwaltungsdiensts an.</span><span class="sxs-lookup"><span data-stu-id="68146-120">Specifies the name of API Management service.</span></span>

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

### <span data-ttu-id="68146-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68146-121">-ResourceGroupName</span></span>
<span data-ttu-id="68146-122">Gibt den Namen der Ressourcengruppe an, unter der dieses Cmdlet den API-Verwaltungsdienst erhält.</span><span class="sxs-lookup"><span data-stu-id="68146-122">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

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

### <span data-ttu-id="68146-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="68146-123">-ResourceId</span></span>
<span data-ttu-id="68146-124">Arm-resourcecode des API-Verwaltungsdiensts.</span><span class="sxs-lookup"><span data-stu-id="68146-124">Arm ResourceId of the API Management service.</span></span>

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

### <span data-ttu-id="68146-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68146-125">CommonParameters</span></span>
<span data-ttu-id="68146-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68146-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68146-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68146-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68146-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="68146-128">INPUTS</span></span>

### <span data-ttu-id="68146-129">System. String</span><span class="sxs-lookup"><span data-stu-id="68146-129">System.String</span></span>

## <span data-ttu-id="68146-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="68146-130">OUTPUTS</span></span>

### <span data-ttu-id="68146-131">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="68146-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="68146-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="68146-132">NOTES</span></span>

## <span data-ttu-id="68146-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="68146-133">RELATED LINKS</span></span>

[<span data-ttu-id="68146-134">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="68146-134">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="68146-135">Neu – AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="68146-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="68146-136">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="68146-136">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="68146-137">Wiederherstellen – AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="68146-137">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


