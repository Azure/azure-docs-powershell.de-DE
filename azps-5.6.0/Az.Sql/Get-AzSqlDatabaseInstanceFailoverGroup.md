---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 2b8ddc8b15ca9fa7322de231f9688548c4073708
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950003"
---
# <span data-ttu-id="fdca2-101">Get-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="fdca2-101">Get-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="fdca2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdca2-102">SYNOPSIS</span></span>
<span data-ttu-id="fdca2-103">Ruft Instanz-Failovergruppen ab oder listet diese auf.</span><span class="sxs-lookup"><span data-stu-id="fdca2-103">Gets or lists Instance Failover Groups.</span></span>

## <span data-ttu-id="fdca2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fdca2-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseInstanceFailoverGroup [[-Name] <String>] [-ResourceGroupName] <String> [-Location] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdca2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fdca2-105">DESCRIPTION</span></span>
<span data-ttu-id="fdca2-106">Ruft eine bestimmte Instanz-Failovergruppe ab oder listet die Instanz-Failovergruppen in einer Region unter dem Abonnement des Benutzers auf.</span><span class="sxs-lookup"><span data-stu-id="fdca2-106">Gets a specific Instance Failover Group or lists the Instance Failover Groups in a region under the user's subscription.</span></span>

<span data-ttu-id="fdca2-107">Jeder Bereich in der Instanz-Failover-Gruppe kann zum Ausführen des Befehls verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fdca2-107">Either region in the Instance Failover Group may be used to execute the command.</span></span> <span data-ttu-id="fdca2-108">Die zurückgegebenen Werte geben den Zustand der verwalteten Instanzen in dieser Region in Bezug auf die Instanz-Failover-Gruppe wieder.</span><span class="sxs-lookup"><span data-stu-id="fdca2-108">The returned values will reflect the state of the Managed Instances in that region with respect to the Instance Failover Group.</span></span>

## <span data-ttu-id="fdca2-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fdca2-109">EXAMPLES</span></span>

### <span data-ttu-id="fdca2-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fdca2-110">Example 1</span></span>
```
PS C:\> $failoverGroups = Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location
Output:
{
    ResourceGroupName                     : rg
    Location                              : East US
    Name                                  : fg
    PartnerResourceGroupName              : rg
    PartnerRegion                         : West US
    PrimaryManagedInstanceName            : managedInstance1
    PartnerManagedInstanceName            : managedInstance2
    ReplicationRole                       : Primary
    ReplicationState                      : CATCH_UP
    ReadWriteFailoverPolicy               : Automatic
    FailoverWithDataLossGracePeriodHours  : 1
    ReadOnlyFailoverPolicy                : Disabled
    Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
}
```

<span data-ttu-id="fdca2-111">Liste aller Failovergruppen in der Region</span><span class="sxs-lookup"><span data-stu-id="fdca2-111">Lists all Failover Groups in the region</span></span>

### <span data-ttu-id="fdca2-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fdca2-112">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg
Output:
ResourceGroupName                     : rg
Location                              : East US
Name                                  : fg
PartnerResourceGroupName              : rg
PartnerRegion                         : West US
PrimaryManagedInstanceName            : managedInstance1
PartnerManagedInstanceName            : managedInstance2
ReplicationRole                       : Primary
ReplicationState                      : CATCH_UP
ReadWriteFailoverPolicy               : Automatic
FailoverWithDataLossGracePeriodHours  : 1
ReadOnlyFailoverPolicy                : Disabled
Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
```

<span data-ttu-id="fdca2-113">Holen Sie sich eine bestimmte Instanz-Failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="fdca2-113">Get a specific Instance Failover Group.</span></span>

## <span data-ttu-id="fdca2-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fdca2-114">PARAMETERS</span></span>

### <span data-ttu-id="fdca2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdca2-115">-DefaultProfile</span></span>
<span data-ttu-id="fdca2-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fdca2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdca2-117">-Location</span><span class="sxs-lookup"><span data-stu-id="fdca2-117">-Location</span></span>
<span data-ttu-id="fdca2-118">Der Name der lokalen Region, aus der die Instanz-Failovergruppe abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="fdca2-118">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdca2-119">-Name</span><span class="sxs-lookup"><span data-stu-id="fdca2-119">-Name</span></span>
<span data-ttu-id="fdca2-120">Der Name der abzurufende Instanz-Failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="fdca2-120">The name of the Instance Failover Group to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdca2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdca2-121">-ResourceGroupName</span></span>
<span data-ttu-id="fdca2-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fdca2-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdca2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdca2-123">CommonParameters</span></span>
<span data-ttu-id="fdca2-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdca2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdca2-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fdca2-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdca2-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fdca2-126">INPUTS</span></span>

### <span data-ttu-id="fdca2-127">System.String</span><span class="sxs-lookup"><span data-stu-id="fdca2-127">System.String</span></span>

## <span data-ttu-id="fdca2-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fdca2-128">OUTPUTS</span></span>

### <span data-ttu-id="fdca2-129">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="fdca2-129">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="fdca2-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fdca2-130">NOTES</span></span>

## <span data-ttu-id="fdca2-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fdca2-131">RELATED LINKS</span></span>
