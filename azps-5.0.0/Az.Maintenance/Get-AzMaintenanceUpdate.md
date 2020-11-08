---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azmaintenanceupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceUpdate.md
ms.openlocfilehash: d8d3e4df3349acb1340a24362043d32d528fc284
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177559"
---
# <span data-ttu-id="bc389-101">Get-AzMaintenanceUpdate</span><span class="sxs-lookup"><span data-stu-id="bc389-101">Get-AzMaintenanceUpdate</span></span>

## <span data-ttu-id="bc389-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bc389-102">SYNOPSIS</span></span>
<span data-ttu-id="bc389-103">Erhalten Sie ausstehende Wartungsaktualisierungen für die Ressource.</span><span class="sxs-lookup"><span data-stu-id="bc389-103">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="bc389-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc389-104">SYNTAX</span></span>

```
Get-AzMaintenanceUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc389-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bc389-105">DESCRIPTION</span></span>
<span data-ttu-id="bc389-106">Erhalten Sie ausstehende Wartungsaktualisierungen für die Ressource.</span><span class="sxs-lookup"><span data-stu-id="bc389-106">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="bc389-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bc389-107">EXAMPLES</span></span>

### <span data-ttu-id="bc389-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bc389-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMaintenanceUpdate -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute

MaintenanceScope    : Host
ImpactType          : Freeze
Status              : Pending
ImpactDurationInSec : 9
NotBefore           : 1/24/2020 5:11:41 AM
ResourceId          : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
```

<span data-ttu-id="bc389-109">Erhalten Sie ausstehende Wartungsaktualisierungen für die Ressource.</span><span class="sxs-lookup"><span data-stu-id="bc389-109">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="bc389-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc389-110">PARAMETERS</span></span>

### <span data-ttu-id="bc389-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc389-111">-DefaultProfile</span></span>
<span data-ttu-id="bc389-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bc389-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc389-113">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="bc389-113">-ProviderName</span></span>
<span data-ttu-id="bc389-114">Der Name des Ressourcenanbieters.</span><span class="sxs-lookup"><span data-stu-id="bc389-114">The resource provider Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc389-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc389-115">-ResourceGroupName</span></span>
<span data-ttu-id="bc389-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bc389-116">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc389-117">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="bc389-117">-ResourceName</span></span>
<span data-ttu-id="bc389-118">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="bc389-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc389-119">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="bc389-119">-ResourceParentName</span></span>
<span data-ttu-id="bc389-120">Der Name der übergeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="bc389-120">The parent resource name.</span></span>

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

### <span data-ttu-id="bc389-121">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="bc389-121">-ResourceParentType</span></span>
<span data-ttu-id="bc389-122">Der übergeordnete Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="bc389-122">The parent resource type.</span></span>

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

### <span data-ttu-id="bc389-123">-</span><span class="sxs-lookup"><span data-stu-id="bc389-123">-ResourceType</span></span>
<span data-ttu-id="bc389-124">Der Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="bc389-124">The resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc389-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc389-125">CommonParameters</span></span>
<span data-ttu-id="bc389-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc389-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc389-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc389-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc389-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bc389-128">INPUTS</span></span>

### <span data-ttu-id="bc389-129">System. String</span><span class="sxs-lookup"><span data-stu-id="bc389-129">System.String</span></span>

## <span data-ttu-id="bc389-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bc389-130">OUTPUTS</span></span>

### <span data-ttu-id="bc389-131">Microsoft. Azure. Management. Maintenance. Models. Update</span><span class="sxs-lookup"><span data-stu-id="bc389-131">Microsoft.Azure.Management.Maintenance.Models.Update</span></span>

## <span data-ttu-id="bc389-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="bc389-132">NOTES</span></span>

## <span data-ttu-id="bc389-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bc389-133">RELATED LINKS</span></span>
