---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagement.md
ms.openlocfilehash: 99b98bd402d6ac22da4f05ce07a08a2c5980359b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658339"
---
# <span data-ttu-id="bb63c-101">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="bb63c-101">Get-AzApiManagement</span></span>

## <span data-ttu-id="bb63c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bb63c-102">SYNOPSIS</span></span>
<span data-ttu-id="bb63c-103">Ruft eine Liste oder eine bestimmte API-Verwaltungsdienst Beschreibung ab.</span><span class="sxs-lookup"><span data-stu-id="bb63c-103">Gets a list or a particular API Management Service description.</span></span>

## <span data-ttu-id="bb63c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb63c-104">SYNTAX</span></span>

### <span data-ttu-id="bb63c-105">GetBySubscription (Standard)</span><span class="sxs-lookup"><span data-stu-id="bb63c-105">GetBySubscription (Default)</span></span>
```
Get-AzApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb63c-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bb63c-106">GetByResourceGroup</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb63c-107">GetByResource</span><span class="sxs-lookup"><span data-stu-id="bb63c-107">GetByResource</span></span>
```
Get-AzApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bb63c-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bb63c-108">ByResourceId</span></span>
```
Get-AzApiManagement -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb63c-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bb63c-109">DESCRIPTION</span></span>
<span data-ttu-id="bb63c-110">Das Cmdlet " **Get-AzApiManagement** " Ruft eine Liste aller API-Verwaltungsdienste unter Abonnement oder angegebene Ressourcengruppe oder eine bestimmte API-Verwaltung ab.</span><span class="sxs-lookup"><span data-stu-id="bb63c-110">The **Get-AzApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="bb63c-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bb63c-111">EXAMPLES</span></span>

### <span data-ttu-id="bb63c-112">Beispiel 1: Abrufen aller API-Verwaltungsdienste</span><span class="sxs-lookup"><span data-stu-id="bb63c-112">Example 1: Get all API Management services</span></span>
```powershell
PS C:\>Get-AzApiManagement
```

<span data-ttu-id="bb63c-113">Dieser Befehl ruft alle API-Verwaltungsdienste innerhalb eines Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="bb63c-113">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="bb63c-114">Beispiel 2: Abrufen aller API-Verwaltungsdienste nach einem bestimmten Namen</span><span class="sxs-lookup"><span data-stu-id="bb63c-114">Example 2: Get all API Management services by a specific name</span></span>
```powershell
PS C:\>Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="bb63c-115">Mit diesem Befehl wird der gesamte API-Verwaltungsdienst nach Namen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="bb63c-115">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="bb63c-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb63c-116">PARAMETERS</span></span>

### <span data-ttu-id="bb63c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb63c-117">-DefaultProfile</span></span>
<span data-ttu-id="bb63c-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bb63c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb63c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="bb63c-119">-Name</span></span>
<span data-ttu-id="bb63c-120">Gibt den Namen des API-Verwaltungsdiensts an.</span><span class="sxs-lookup"><span data-stu-id="bb63c-120">Specifies the name of API Management service.</span></span>

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

### <span data-ttu-id="bb63c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb63c-121">-ResourceGroupName</span></span>
<span data-ttu-id="bb63c-122">Gibt den Namen der Ressourcengruppe an, unter der dieses Cmdlet den API-Verwaltungsdienst erhält.</span><span class="sxs-lookup"><span data-stu-id="bb63c-122">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

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

### <span data-ttu-id="bb63c-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="bb63c-123">-ResourceId</span></span>
<span data-ttu-id="bb63c-124">Arm-resourcecode des API-Verwaltungsdiensts.</span><span class="sxs-lookup"><span data-stu-id="bb63c-124">Arm ResourceId of the API Management service.</span></span>

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

### <span data-ttu-id="bb63c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb63c-125">CommonParameters</span></span>
<span data-ttu-id="bb63c-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb63c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb63c-127">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb63c-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb63c-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bb63c-128">INPUTS</span></span>

### <span data-ttu-id="bb63c-129">System. String</span><span class="sxs-lookup"><span data-stu-id="bb63c-129">System.String</span></span>

## <span data-ttu-id="bb63c-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bb63c-130">OUTPUTS</span></span>

### <span data-ttu-id="bb63c-131">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="bb63c-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="bb63c-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="bb63c-132">NOTES</span></span>

## <span data-ttu-id="bb63c-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bb63c-133">RELATED LINKS</span></span>

[<span data-ttu-id="bb63c-134">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="bb63c-134">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="bb63c-135">Neu – AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="bb63c-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="bb63c-136">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="bb63c-136">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="bb63c-137">Wiederherstellen – AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="bb63c-137">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


