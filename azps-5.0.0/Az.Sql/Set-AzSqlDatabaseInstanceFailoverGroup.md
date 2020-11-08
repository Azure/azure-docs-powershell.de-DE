---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 79d7482d51ffc7c03703dbf62e00fd9230f9976d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179986"
---
# <span data-ttu-id="1b6d0-101">Set-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="1b6d0-101">Set-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="1b6d0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1b6d0-102">SYNOPSIS</span></span>
<span data-ttu-id="1b6d0-103">Ändert die Konfiguration einer Instanz-Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="1b6d0-103">Modifies the configuration of an Instance Failover Group.</span></span>

## <span data-ttu-id="1b6d0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b6d0-104">SYNTAX</span></span>

### <span data-ttu-id="1b6d0-105">SetInstanceFailoverGroupDefaultSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1b6d0-105">SetInstanceFailoverGroupDefaultSet (Default)</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b6d0-106">SetInstanceFailoverGroupByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1b6d0-106">SetInstanceFailoverGroupByResourceIdSet</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-FailoverPolicy <String>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b6d0-107">SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span><span class="sxs-lookup"><span data-stu-id="1b6d0-107">SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel>
 [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b6d0-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1b6d0-108">DESCRIPTION</span></span>
<span data-ttu-id="1b6d0-109">Mit diesem Befehl wird die Konfiguration einer Instanz-failovergruppe geändert.</span><span class="sxs-lookup"><span data-stu-id="1b6d0-109">This command modifies the configuration of an Instance Failover Group.</span></span>

<span data-ttu-id="1b6d0-110">Der primäre Bereich der Instanz-Failover-Gruppe sollte zum Ausführen des Befehls verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1b6d0-110">The Instance Failover Group's primary region should be used to execute the command.</span></span>

<span data-ttu-id="1b6d0-111">Während der Vorschau des Features "Instanzen-failovergruppen" werden nur Werte, die größer oder gleich 1 Stunde sind, für den "-GracePeriodWithDataLossHours"-Parameter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1b6d0-111">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="1b6d0-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1b6d0-112">EXAMPLES</span></span>

### <span data-ttu-id="1b6d0-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1b6d0-113">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Set-AzSqlDatabaseInstanceFailoverGroup -FailoverPolicy Manual
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
ReadWriteFailoverPolicy               : Manual
FailoverWithDataLossGracePeriodHours  : 
ReadOnlyFailoverPolicy                : Disabled
Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
```

<span data-ttu-id="1b6d0-114">Legt die Failover-Richtlinie einer Instanzen-failovergruppe auf "manuell" durch Verrohrung in der Gruppe Failover fest.</span><span class="sxs-lookup"><span data-stu-id="1b6d0-114">Sets a Instance Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="1b6d0-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b6d0-115">PARAMETERS</span></span>

### <span data-ttu-id="1b6d0-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="1b6d0-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="1b6d0-117">Ob Ausfälle auf dem sekundären Server ein automatisches Failover des schreibgeschützten Endpunkts auslösen sollten.</span><span class="sxs-lookup"><span data-stu-id="1b6d0-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>
<span data-ttu-id="1b6d0-118">Dieses Feature wird noch nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1b6d0-118">This feature is not yet supported.</span></span>

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

### <span data-ttu-id="1b6d0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b6d0-119">-DefaultProfile</span></span>
<span data-ttu-id="1b6d0-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1b6d0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b6d0-121">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="1b6d0-121">-FailoverPolicy</span></span>
<span data-ttu-id="1b6d0-122">Die Failover-Richtlinie der Instanz-Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="1b6d0-122">The failover policy of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="1b6d0-123">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="1b6d0-123">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="1b6d0-124">Das Intervall vor dem automatischen Failover wird initiiert, wenn ein Ausfall auf dem primären Server auftritt und ein Failover ohne Datenverlust nicht abgeschlossen werden kann.</span><span class="sxs-lookup"><span data-stu-id="1b6d0-124">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b6d0-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1b6d0-125">-InputObject</span></span>
<span data-ttu-id="1b6d0-126">Das zu bestimmende Instanzen-Failover-Gruppenobjekt</span><span class="sxs-lookup"><span data-stu-id="1b6d0-126">The Instance Failover Group object to set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel
Parameter Sets: SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b6d0-127">-Standort</span><span class="sxs-lookup"><span data-stu-id="1b6d0-127">-Location</span></span>
<span data-ttu-id="1b6d0-128">Der Name des lokalen Bereichs, aus dem die Gruppe der Instanz-Failover abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="1b6d0-128">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupDefaultSet, SetInstanceFailoverGroupByResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b6d0-129">-Name</span><span class="sxs-lookup"><span data-stu-id="1b6d0-129">-Name</span></span>
<span data-ttu-id="1b6d0-130">Der Name der Instanz-Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="1b6d0-130">The name of the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupDefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b6d0-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b6d0-131">-ResourceGroupName</span></span>
<span data-ttu-id="1b6d0-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1b6d0-132">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b6d0-133">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="1b6d0-133">-ResourceId</span></span>
<span data-ttu-id="1b6d0-134">Die Ressourcen-ID der zu bestimmenden Instanz-failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="1b6d0-134">The Resource ID of the Instance Failover Group to set.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupByResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b6d0-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1b6d0-135">-Confirm</span></span>
<span data-ttu-id="1b6d0-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1b6d0-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b6d0-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b6d0-137">-WhatIf</span></span>
<span data-ttu-id="1b6d0-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1b6d0-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b6d0-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1b6d0-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b6d0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b6d0-140">CommonParameters</span></span>
<span data-ttu-id="1b6d0-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b6d0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b6d0-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1b6d0-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b6d0-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1b6d0-143">INPUTS</span></span>

### <span data-ttu-id="1b6d0-144">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="1b6d0-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="1b6d0-145">System. String</span><span class="sxs-lookup"><span data-stu-id="1b6d0-145">System.String</span></span>

## <span data-ttu-id="1b6d0-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1b6d0-146">OUTPUTS</span></span>

### <span data-ttu-id="1b6d0-147">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="1b6d0-147">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="1b6d0-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="1b6d0-148">NOTES</span></span>

## <span data-ttu-id="1b6d0-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1b6d0-149">RELATED LINKS</span></span>
