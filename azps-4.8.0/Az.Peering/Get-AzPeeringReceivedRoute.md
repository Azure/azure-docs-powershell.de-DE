---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringreceivedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringReceivedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringReceivedRoute.md
ms.openlocfilehash: 14557809041fc6f4268dbe28ad9d8f13a70e4054
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174505"
---
# <span data-ttu-id="bf0c5-101">Get-AzPeeringReceivedRoute</span><span class="sxs-lookup"><span data-stu-id="bf0c5-101">Get-AzPeeringReceivedRoute</span></span>

## <span data-ttu-id="bf0c5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bf0c5-102">SYNOPSIS</span></span>
<span data-ttu-id="bf0c5-103">Listet die empfangenen Routen für ein Peering auf.</span><span class="sxs-lookup"><span data-stu-id="bf0c5-103">Lists the received routes for a Peering.</span></span>

## <span data-ttu-id="bf0c5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf0c5-104">SYNTAX</span></span>

### <span data-ttu-id="bf0c5-105">ByResourceGroupAndName (Standard)</span><span class="sxs-lookup"><span data-stu-id="bf0c5-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringReceivedRoute [-ResourceGroupName] <String> -Name <String> [-Prefix <String>] [-AsPath <String>]
 [-OriginAsValidationState <String>] [-RPKIValidationState <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bf0c5-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bf0c5-106">ByResourceId</span></span>
```
Get-AzPeeringReceivedRoute [-ResourceId] <String> [-Prefix <String>] [-AsPath <String>]
 [-OriginAsValidationState <String>] [-RPKIValidationState <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bf0c5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf0c5-107">DESCRIPTION</span></span>
<span data-ttu-id="bf0c5-108">Listen empfangene Routen von einem Peering</span><span class="sxs-lookup"><span data-stu-id="bf0c5-108">Lists recieved routes from a Peering</span></span>

## <span data-ttu-id="bf0c5-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bf0c5-109">EXAMPLES</span></span>

### <span data-ttu-id="bf0c5-110">Auflisten der obersten 100-empfangenen Routen für ein Peering</span><span class="sxs-lookup"><span data-stu-id="bf0c5-110">List top 100 received routes for a peering</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName
```

<span data-ttu-id="bf0c5-111">Listet alle empfangenen Routen für ein Peering auf</span><span class="sxs-lookup"><span data-stu-id="bf0c5-111">Lists all of the received routes for a peering</span></span>

### <span data-ttu-id="bf0c5-112">Als Pfad filtern</span><span class="sxs-lookup"><span data-stu-id="bf0c5-112">Filter by AS Path</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -AsPath "1234 5674 9834"
```

<span data-ttu-id="bf0c5-113">Listet alle empfangenen Routen für ein Peering mit einem Filter auf AS auf</span><span class="sxs-lookup"><span data-stu-id="bf0c5-113">Lists all of the received routes for a peering with a filter on AS</span></span> 

### <span data-ttu-id="bf0c5-114">Filtern nach RPKIValidationState</span><span class="sxs-lookup"><span data-stu-id="bf0c5-114">Filter by RPKIValidationState</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -RPKIValidationState "Valid"
```

<span data-ttu-id="bf0c5-115">Listet alle empfangenen Routen für ein Peering mit einem Filter auf RPKIValidationState auf.</span><span class="sxs-lookup"><span data-stu-id="bf0c5-115">Lists all of the received routes for a peering with a filter on RPKIValidationState</span></span>

### <span data-ttu-id="bf0c5-116">Filtern nach OriginAsValidationState</span><span class="sxs-lookup"><span data-stu-id="bf0c5-116">Filter by OriginAsValidationState</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -OriginAsValidationState "Valid"
```

<span data-ttu-id="bf0c5-117">Listet alle empfangenen Routen für ein Peering mit einem Filter auf OriginAsValidationState auf.</span><span class="sxs-lookup"><span data-stu-id="bf0c5-117">Lists all of the received routes for a peering with a filter on OriginAsValidationState</span></span>

## <span data-ttu-id="bf0c5-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf0c5-118">PARAMETERS</span></span>

### <span data-ttu-id="bf0c5-119">-Ablängen</span><span class="sxs-lookup"><span data-stu-id="bf0c5-119">-AsPath</span></span>
<span data-ttu-id="bf0c5-120">Als Pfad filtern</span><span class="sxs-lookup"><span data-stu-id="bf0c5-120">Filter by AS Path.</span></span>
<span data-ttu-id="bf0c5-121">Beispiel: "9342 1234 4567"</span><span class="sxs-lookup"><span data-stu-id="bf0c5-121">Example: '9342 1234 4567'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf0c5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf0c5-122">-DefaultProfile</span></span>
<span data-ttu-id="bf0c5-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bf0c5-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf0c5-124">-Name</span><span class="sxs-lookup"><span data-stu-id="bf0c5-124">-Name</span></span>
<span data-ttu-id="bf0c5-125">Der eindeutige Name des PSPeering.</span><span class="sxs-lookup"><span data-stu-id="bf0c5-125">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf0c5-126">-OriginAsValidationState</span><span class="sxs-lookup"><span data-stu-id="bf0c5-126">-OriginAsValidationState</span></span>
<span data-ttu-id="bf0c5-127">Nach Ursprung als Überprüfungsstatus Filtern</span><span class="sxs-lookup"><span data-stu-id="bf0c5-127">Filter by origin AS validation state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf0c5-128">-Prefix</span><span class="sxs-lookup"><span data-stu-id="bf0c5-128">-Prefix</span></span>
<span data-ttu-id="bf0c5-129">Nach Präfix Filtern</span><span class="sxs-lookup"><span data-stu-id="bf0c5-129">Filter by prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf0c5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf0c5-130">-ResourceGroupName</span></span>
<span data-ttu-id="bf0c5-131">Der Name der vorhandenen Ressourcengruppe erstellen oder verwenden</span><span class="sxs-lookup"><span data-stu-id="bf0c5-131">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf0c5-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="bf0c5-132">-ResourceId</span></span>
<span data-ttu-id="bf0c5-133">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="bf0c5-133">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf0c5-134">-RPKIValidationState</span><span class="sxs-lookup"><span data-stu-id="bf0c5-134">-RPKIValidationState</span></span>
<span data-ttu-id="bf0c5-135">Filtern nach RPKI-Überprüfungsstatus</span><span class="sxs-lookup"><span data-stu-id="bf0c5-135">Filter by RPKI validation state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf0c5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf0c5-136">CommonParameters</span></span>
<span data-ttu-id="bf0c5-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf0c5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf0c5-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bf0c5-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf0c5-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bf0c5-139">INPUTS</span></span>

### <span data-ttu-id="bf0c5-140">System. String</span><span class="sxs-lookup"><span data-stu-id="bf0c5-140">System.String</span></span>

## <span data-ttu-id="bf0c5-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bf0c5-141">OUTPUTS</span></span>

### <span data-ttu-id="bf0c5-142">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSPeeringReceivedRoute</span><span class="sxs-lookup"><span data-stu-id="bf0c5-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringReceivedRoute</span></span>

## <span data-ttu-id="bf0c5-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="bf0c5-143">NOTES</span></span>

## <span data-ttu-id="bf0c5-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bf0c5-144">RELATED LINKS</span></span>
