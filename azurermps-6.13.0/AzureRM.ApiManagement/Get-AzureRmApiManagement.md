---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagement.md
ms.openlocfilehash: bff36b7bcb37dd099f9aa50a99bed9538111e8d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502286"
---
# <span data-ttu-id="0ec63-101">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="0ec63-101">Get-AzureRmApiManagement</span></span>

## <span data-ttu-id="0ec63-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0ec63-102">SYNOPSIS</span></span>
<span data-ttu-id="0ec63-103">Ruft eine Liste oder eine bestimmte API-Verwaltungsdienst Beschreibung ab.</span><span class="sxs-lookup"><span data-stu-id="0ec63-103">Gets a list or a particular API Management Service description.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ec63-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ec63-104">SYNTAX</span></span>

### <span data-ttu-id="0ec63-105">GetBySubscription (Standard)</span><span class="sxs-lookup"><span data-stu-id="0ec63-105">GetBySubscription (Default)</span></span>
```
Get-AzureRmApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ec63-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0ec63-106">GetByResourceGroup</span></span>
```
Get-AzureRmApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0ec63-107">GetByResource</span><span class="sxs-lookup"><span data-stu-id="0ec63-107">GetByResource</span></span>
```
Get-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0ec63-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0ec63-108">DESCRIPTION</span></span>
<span data-ttu-id="0ec63-109">Das Cmdlet " **Get-AzureRmApiManagement** " Ruft eine Liste aller API-Verwaltungsdienste unter Abonnement oder angegebene Ressourcengruppe oder eine bestimmte API-Verwaltung ab.</span><span class="sxs-lookup"><span data-stu-id="0ec63-109">The **Get-AzureRmApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="0ec63-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0ec63-110">EXAMPLES</span></span>

### <span data-ttu-id="0ec63-111">Beispiel 1: Abrufen aller API-Verwaltungsdienste</span><span class="sxs-lookup"><span data-stu-id="0ec63-111">Example 1: Get all API Management services</span></span>
```powershell
PS C:\>Get-AzureRmApiManagement
```

<span data-ttu-id="0ec63-112">Dieser Befehl ruft alle API-Verwaltungsdienste innerhalb eines Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="0ec63-112">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="0ec63-113">Beispiel 2: Abrufen aller API-Verwaltungsdienste nach einem bestimmten Namen</span><span class="sxs-lookup"><span data-stu-id="0ec63-113">Example 2: Get all API Management services by a specific name</span></span>
```powershell
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="0ec63-114">Mit diesem Befehl wird der gesamte API-Verwaltungsdienst nach Namen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="0ec63-114">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="0ec63-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ec63-115">PARAMETERS</span></span>

### <span data-ttu-id="0ec63-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ec63-116">-DefaultProfile</span></span>
<span data-ttu-id="0ec63-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0ec63-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ec63-118">-Name</span><span class="sxs-lookup"><span data-stu-id="0ec63-118">-Name</span></span>
<span data-ttu-id="0ec63-119">Gibt den Namen des API-Verwaltungsdiensts an.</span><span class="sxs-lookup"><span data-stu-id="0ec63-119">Specifies the name of API Management service.</span></span>

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

### <span data-ttu-id="0ec63-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ec63-120">-ResourceGroupName</span></span>
<span data-ttu-id="0ec63-121">Gibt den Namen der Ressourcengruppe an, unter der dieses Cmdlet den API-Verwaltungsdienst erhält.</span><span class="sxs-lookup"><span data-stu-id="0ec63-121">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

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

### <span data-ttu-id="0ec63-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ec63-122">CommonParameters</span></span>
<span data-ttu-id="0ec63-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ec63-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ec63-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ec63-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ec63-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0ec63-125">INPUTS</span></span>

### <span data-ttu-id="0ec63-126">System. String</span><span class="sxs-lookup"><span data-stu-id="0ec63-126">System.String</span></span>

## <span data-ttu-id="0ec63-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0ec63-127">OUTPUTS</span></span>

### <span data-ttu-id="0ec63-128">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="0ec63-128">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="0ec63-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="0ec63-129">NOTES</span></span>

## <span data-ttu-id="0ec63-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0ec63-130">RELATED LINKS</span></span>

[<span data-ttu-id="0ec63-131">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="0ec63-131">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="0ec63-132">Neu – AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="0ec63-132">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="0ec63-133">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="0ec63-133">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="0ec63-134">Wiederherstellen – AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="0ec63-134">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


