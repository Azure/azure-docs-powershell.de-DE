---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: bd2a157a1fb05baf0fa6e02b061462718ffad314
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98301867"
---
# <span data-ttu-id="89377-101">Get-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="89377-101">Get-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="89377-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89377-102">SYNOPSIS</span></span>
<span data-ttu-id="89377-103">Ruft Instanz failovergruppen ab oder listet sie auf.</span><span class="sxs-lookup"><span data-stu-id="89377-103">Gets or lists Instance Failover Groups.</span></span>

## <span data-ttu-id="89377-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="89377-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseInstanceFailoverGroup [[-Name] <String>] [-ResourceGroupName] <String> [-Location] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89377-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="89377-105">DESCRIPTION</span></span>
<span data-ttu-id="89377-106">Ruft eine bestimmte Instanz failovergruppe ab oder listet die Instanz failovergruppen in einer Region unter dem Abonnement des Benutzers auf.</span><span class="sxs-lookup"><span data-stu-id="89377-106">Gets a specific Instance Failover Group or lists the Instance Failover Groups in a region under the user's subscription.</span></span>

<span data-ttu-id="89377-107">Beide Regionen in der Instanz failovergruppe können zum Ausführen des Befehls verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="89377-107">Either region in the Instance Failover Group may be used to execute the command.</span></span> <span data-ttu-id="89377-108">Die zurückgegebenen Werte geben den Status der verwalteten Instanzen in dieser Region im Hinblick auf die Instanz failovergruppe wieder.</span><span class="sxs-lookup"><span data-stu-id="89377-108">The returned values will reflect the state of the Managed Instances in that region with respect to the Instance Failover Group.</span></span>

## <span data-ttu-id="89377-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="89377-109">EXAMPLES</span></span>

### <span data-ttu-id="89377-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="89377-110">Example 1</span></span>
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

<span data-ttu-id="89377-111">Listet alle Failovergruppen in der Region auf.</span><span class="sxs-lookup"><span data-stu-id="89377-111">Lists all Failover Groups in the region</span></span>

### <span data-ttu-id="89377-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="89377-112">Example 2</span></span>
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

<span data-ttu-id="89377-113">Sie erhalten eine bestimmte Instanz-Failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="89377-113">Get a specific Instance Failover Group.</span></span>

## <span data-ttu-id="89377-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89377-114">PARAMETERS</span></span>

### <span data-ttu-id="89377-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89377-115">-DefaultProfile</span></span>
<span data-ttu-id="89377-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="89377-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89377-117">-Location</span><span class="sxs-lookup"><span data-stu-id="89377-117">-Location</span></span>
<span data-ttu-id="89377-118">Der Name der lokalen Region, aus der die Instanz failovergruppe abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="89377-118">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="89377-119">-Name</span><span class="sxs-lookup"><span data-stu-id="89377-119">-Name</span></span>
<span data-ttu-id="89377-120">Der Name der abzurufende Instanz failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="89377-120">The name of the Instance Failover Group to retrieve.</span></span>

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

### <span data-ttu-id="89377-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89377-121">-ResourceGroupName</span></span>
<span data-ttu-id="89377-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="89377-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="89377-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89377-123">CommonParameters</span></span>
<span data-ttu-id="89377-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89377-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89377-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89377-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89377-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="89377-126">INPUTS</span></span>

### <span data-ttu-id="89377-127">System.String</span><span class="sxs-lookup"><span data-stu-id="89377-127">System.String</span></span>

## <span data-ttu-id="89377-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="89377-128">OUTPUTS</span></span>

### <span data-ttu-id="89377-129">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="89377-129">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="89377-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="89377-130">NOTES</span></span>

## <span data-ttu-id="89377-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="89377-131">RELATED LINKS</span></span>
