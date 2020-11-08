---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringreceivedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringReceivedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringReceivedRoute.md
ms.openlocfilehash: 14557809041fc6f4268dbe28ad9d8f13a70e4054
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178141"
---
# <span data-ttu-id="7f653-101">Get-AzPeeringReceivedRoute</span><span class="sxs-lookup"><span data-stu-id="7f653-101">Get-AzPeeringReceivedRoute</span></span>

## <span data-ttu-id="7f653-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7f653-102">SYNOPSIS</span></span>
<span data-ttu-id="7f653-103">Listet die empfangenen Routen für ein Peering auf.</span><span class="sxs-lookup"><span data-stu-id="7f653-103">Lists the received routes for a Peering.</span></span>

## <span data-ttu-id="7f653-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f653-104">SYNTAX</span></span>

### <span data-ttu-id="7f653-105">ByResourceGroupAndName (Standard)</span><span class="sxs-lookup"><span data-stu-id="7f653-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringReceivedRoute [-ResourceGroupName] <String> -Name <String> [-Prefix <String>] [-AsPath <String>]
 [-OriginAsValidationState <String>] [-RPKIValidationState <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7f653-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7f653-106">ByResourceId</span></span>
```
Get-AzPeeringReceivedRoute [-ResourceId] <String> [-Prefix <String>] [-AsPath <String>]
 [-OriginAsValidationState <String>] [-RPKIValidationState <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7f653-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f653-107">DESCRIPTION</span></span>
<span data-ttu-id="7f653-108">Listen empfangene Routen von einem Peering</span><span class="sxs-lookup"><span data-stu-id="7f653-108">Lists recieved routes from a Peering</span></span>

## <span data-ttu-id="7f653-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7f653-109">EXAMPLES</span></span>

### <span data-ttu-id="7f653-110">Auflisten der obersten 100-empfangenen Routen für ein Peering</span><span class="sxs-lookup"><span data-stu-id="7f653-110">List top 100 received routes for a peering</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName
```

<span data-ttu-id="7f653-111">Listet alle empfangenen Routen für ein Peering auf</span><span class="sxs-lookup"><span data-stu-id="7f653-111">Lists all of the received routes for a peering</span></span>

### <span data-ttu-id="7f653-112">Als Pfad filtern</span><span class="sxs-lookup"><span data-stu-id="7f653-112">Filter by AS Path</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -AsPath "1234 5674 9834"
```

<span data-ttu-id="7f653-113">Listet alle empfangenen Routen für ein Peering mit einem Filter auf AS auf</span><span class="sxs-lookup"><span data-stu-id="7f653-113">Lists all of the received routes for a peering with a filter on AS</span></span> 

### <span data-ttu-id="7f653-114">Filtern nach RPKIValidationState</span><span class="sxs-lookup"><span data-stu-id="7f653-114">Filter by RPKIValidationState</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -RPKIValidationState "Valid"
```

<span data-ttu-id="7f653-115">Listet alle empfangenen Routen für ein Peering mit einem Filter auf RPKIValidationState auf.</span><span class="sxs-lookup"><span data-stu-id="7f653-115">Lists all of the received routes for a peering with a filter on RPKIValidationState</span></span>

### <span data-ttu-id="7f653-116">Filtern nach OriginAsValidationState</span><span class="sxs-lookup"><span data-stu-id="7f653-116">Filter by OriginAsValidationState</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -OriginAsValidationState "Valid"
```

<span data-ttu-id="7f653-117">Listet alle empfangenen Routen für ein Peering mit einem Filter auf OriginAsValidationState auf.</span><span class="sxs-lookup"><span data-stu-id="7f653-117">Lists all of the received routes for a peering with a filter on OriginAsValidationState</span></span>

## <span data-ttu-id="7f653-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f653-118">PARAMETERS</span></span>

### <span data-ttu-id="7f653-119">-Ablängen</span><span class="sxs-lookup"><span data-stu-id="7f653-119">-AsPath</span></span>
<span data-ttu-id="7f653-120">Als Pfad filtern</span><span class="sxs-lookup"><span data-stu-id="7f653-120">Filter by AS Path.</span></span>
<span data-ttu-id="7f653-121">Beispiel: "9342 1234 4567"</span><span class="sxs-lookup"><span data-stu-id="7f653-121">Example: '9342 1234 4567'</span></span>

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

### <span data-ttu-id="7f653-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f653-122">-DefaultProfile</span></span>
<span data-ttu-id="7f653-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7f653-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f653-124">-Name</span><span class="sxs-lookup"><span data-stu-id="7f653-124">-Name</span></span>
<span data-ttu-id="7f653-125">Der eindeutige Name des PSPeering.</span><span class="sxs-lookup"><span data-stu-id="7f653-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="7f653-126">-OriginAsValidationState</span><span class="sxs-lookup"><span data-stu-id="7f653-126">-OriginAsValidationState</span></span>
<span data-ttu-id="7f653-127">Nach Ursprung als Überprüfungsstatus Filtern</span><span class="sxs-lookup"><span data-stu-id="7f653-127">Filter by origin AS validation state.</span></span>

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

### <span data-ttu-id="7f653-128">-Prefix</span><span class="sxs-lookup"><span data-stu-id="7f653-128">-Prefix</span></span>
<span data-ttu-id="7f653-129">Nach Präfix Filtern</span><span class="sxs-lookup"><span data-stu-id="7f653-129">Filter by prefix.</span></span>

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

### <span data-ttu-id="7f653-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f653-130">-ResourceGroupName</span></span>
<span data-ttu-id="7f653-131">Der Name der vorhandenen Ressourcengruppe erstellen oder verwenden</span><span class="sxs-lookup"><span data-stu-id="7f653-131">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="7f653-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="7f653-132">-ResourceId</span></span>
<span data-ttu-id="7f653-133">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="7f653-133">The resource id string name.</span></span>

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

### <span data-ttu-id="7f653-134">-RPKIValidationState</span><span class="sxs-lookup"><span data-stu-id="7f653-134">-RPKIValidationState</span></span>
<span data-ttu-id="7f653-135">Filtern nach RPKI-Überprüfungsstatus</span><span class="sxs-lookup"><span data-stu-id="7f653-135">Filter by RPKI validation state.</span></span>

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

### <span data-ttu-id="7f653-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f653-136">CommonParameters</span></span>
<span data-ttu-id="7f653-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f653-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f653-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f653-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f653-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7f653-139">INPUTS</span></span>

### <span data-ttu-id="7f653-140">System. String</span><span class="sxs-lookup"><span data-stu-id="7f653-140">System.String</span></span>

## <span data-ttu-id="7f653-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7f653-141">OUTPUTS</span></span>

### <span data-ttu-id="7f653-142">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSPeeringReceivedRoute</span><span class="sxs-lookup"><span data-stu-id="7f653-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringReceivedRoute</span></span>

## <span data-ttu-id="7f653-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="7f653-143">NOTES</span></span>

## <span data-ttu-id="7f653-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7f653-144">RELATED LINKS</span></span>
