---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: bd2a157a1fb05baf0fa6e02b061462718ffad314
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008903"
---
# <span data-ttu-id="6434e-101">Get-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6434e-101">Get-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="6434e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6434e-102">SYNOPSIS</span></span>
<span data-ttu-id="6434e-103">Ruft Instanzen-failovergruppen ab oder listet Sie auf.</span><span class="sxs-lookup"><span data-stu-id="6434e-103">Gets or lists Instance Failover Groups.</span></span>

## <span data-ttu-id="6434e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6434e-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseInstanceFailoverGroup [[-Name] <String>] [-ResourceGroupName] <String> [-Location] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6434e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6434e-105">DESCRIPTION</span></span>
<span data-ttu-id="6434e-106">Ruft eine bestimmte Instanz-failovergruppe ab oder listet die Failoverclusterinstanz-Gruppen in einem Bereich unter dem Abonnement des Benutzers auf.</span><span class="sxs-lookup"><span data-stu-id="6434e-106">Gets a specific Instance Failover Group or lists the Instance Failover Groups in a region under the user's subscription.</span></span>

<span data-ttu-id="6434e-107">Eine der beiden Bereiche in der Gruppe "Instanzen-Failover" kann verwendet werden, um den Befehl auszuführen.</span><span class="sxs-lookup"><span data-stu-id="6434e-107">Either region in the Instance Failover Group may be used to execute the command.</span></span> <span data-ttu-id="6434e-108">Die zurückgegebenen Werte geben den Zustand der verwalteten Instanzen in diesem Bereich hinsichtlich der Instanz-failovergruppe wieder.</span><span class="sxs-lookup"><span data-stu-id="6434e-108">The returned values will reflect the state of the Managed Instances in that region with respect to the Instance Failover Group.</span></span>

## <span data-ttu-id="6434e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6434e-109">EXAMPLES</span></span>

### <span data-ttu-id="6434e-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6434e-110">Example 1</span></span>
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

<span data-ttu-id="6434e-111">Listet alle Failovercluster in der Region auf</span><span class="sxs-lookup"><span data-stu-id="6434e-111">Lists all Failover Groups in the region</span></span>

### <span data-ttu-id="6434e-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6434e-112">Example 2</span></span>
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

<span data-ttu-id="6434e-113">Abrufen einer bestimmten Instanz-Failover-Gruppe</span><span class="sxs-lookup"><span data-stu-id="6434e-113">Get a specific Instance Failover Group.</span></span>

## <span data-ttu-id="6434e-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="6434e-114">PARAMETERS</span></span>

### <span data-ttu-id="6434e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6434e-115">-DefaultProfile</span></span>
<span data-ttu-id="6434e-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6434e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6434e-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="6434e-117">-Location</span></span>
<span data-ttu-id="6434e-118">Der Name des lokalen Bereichs, aus dem die Gruppe der Instanz-Failover abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="6434e-118">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="6434e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="6434e-119">-Name</span></span>
<span data-ttu-id="6434e-120">Der Name der abzurufenden Instanzen-Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="6434e-120">The name of the Instance Failover Group to retrieve.</span></span>

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

### <span data-ttu-id="6434e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6434e-121">-ResourceGroupName</span></span>
<span data-ttu-id="6434e-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6434e-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="6434e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6434e-123">CommonParameters</span></span>
<span data-ttu-id="6434e-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6434e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6434e-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6434e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6434e-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6434e-126">INPUTS</span></span>

### <span data-ttu-id="6434e-127">System. String</span><span class="sxs-lookup"><span data-stu-id="6434e-127">System.String</span></span>

## <span data-ttu-id="6434e-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6434e-128">OUTPUTS</span></span>

### <span data-ttu-id="6434e-129">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="6434e-129">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="6434e-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="6434e-130">NOTES</span></span>

## <span data-ttu-id="6434e-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6434e-131">RELATED LINKS</span></span>
