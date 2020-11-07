---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 8027af33b9ea4f4184c10963da69e8be3b4e3961
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825960"
---
# <span data-ttu-id="1db3b-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="1db3b-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="1db3b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1db3b-102">SYNOPSIS</span></span>
<span data-ttu-id="1db3b-103">Entfernt eine Instanz-Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="1db3b-103">Removes an Instance Failover Group.</span></span>

## <span data-ttu-id="1db3b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1db3b-104">SYNTAX</span></span>

### <span data-ttu-id="1db3b-105">RemoveIFGDefault (Standard)</span><span class="sxs-lookup"><span data-stu-id="1db3b-105">RemoveIFGDefault (Default)</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1db3b-106">Entfernen einer Instanz-Failover-Gruppe aus der Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="1db3b-106">Remove a Instance Failover Group from Resource Id</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1db3b-107">Entfernen einer Instanz-Failover-Gruppe aus der AzureSqlInstanceFailoverGroupModel-Instanzen Definition</span><span class="sxs-lookup"><span data-stu-id="1db3b-107">Remove a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup -InputObject <AzureSqlInstanceFailoverGroupModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1db3b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1db3b-108">DESCRIPTION</span></span>
<span data-ttu-id="1db3b-109">Mit diesem Befehl wird die Failoverclusterinstanz mit dem angegebenen Namen entfernt, sodass alle Datenbanken intakt bleiben.</span><span class="sxs-lookup"><span data-stu-id="1db3b-109">This command removes the Instance Failover Group with the specified name, leaving all databases intact.</span></span> <span data-ttu-id="1db3b-110">Der Listener-Endpunkt wird aus DNS aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="1db3b-110">The listener endpoint will be unregistered from DNS.</span></span>

<span data-ttu-id="1db3b-111">Der primäre Bereich der Instanz-Failover-Gruppe sollte zum Ausführen des Befehls verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1db3b-111">The Instance Failover Group's primary region should be used to execute the command.</span></span>

## <span data-ttu-id="1db3b-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1db3b-112">EXAMPLES</span></span>

### <span data-ttu-id="1db3b-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1db3b-113">Example 1</span></span>
```
PS C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Remove-AzSqlDatabaseInstanceFailoverGroup
```

<span data-ttu-id="1db3b-114">Entfernen Sie eine Instanz-Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="1db3b-114">Remove a Instance Failover Group.</span></span>

## <span data-ttu-id="1db3b-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="1db3b-115">PARAMETERS</span></span>

### <span data-ttu-id="1db3b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1db3b-116">-DefaultProfile</span></span>
<span data-ttu-id="1db3b-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1db3b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1db3b-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1db3b-118">-Force</span></span>
<span data-ttu-id="1db3b-119">Bestätigungsmeldung zum Durchführen der Aktion überspringen.</span><span class="sxs-lookup"><span data-stu-id="1db3b-119">Skip confirmation message for performing the action.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1db3b-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1db3b-120">-InputObject</span></span>
<span data-ttu-id="1db3b-121">Das zu entfernende Instanzen-Failover-Gruppenobjekt</span><span class="sxs-lookup"><span data-stu-id="1db3b-121">The Instance Failover Group object to remove</span></span>

```yaml
Type: AzureSqlInstanceFailoverGroupModel
Parameter Sets: Remove a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1db3b-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="1db3b-122">-Location</span></span>
<span data-ttu-id="1db3b-123">Der Name des lokalen Bereichs, aus dem die Gruppe der Instanz-Failover abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="1db3b-123">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveIFGDefault, Remove a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1db3b-124">-Name</span><span class="sxs-lookup"><span data-stu-id="1db3b-124">-Name</span></span>
<span data-ttu-id="1db3b-125">Der Name der zu entfernenden Instanz-Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="1db3b-125">The name of the Instance Failover Group to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveIFGDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1db3b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1db3b-126">-ResourceGroupName</span></span>
<span data-ttu-id="1db3b-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1db3b-127">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveIFGDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1db3b-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="1db3b-128">-ResourceId</span></span>
<span data-ttu-id="1db3b-129">Die Ressourcen-ID der zu entfernenden Instanz-Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="1db3b-129">The Resource ID of the Instance Failover Group to remove.</span></span>

```yaml
Type: String
Parameter Sets: Remove a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1db3b-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1db3b-130">-Confirm</span></span>
<span data-ttu-id="1db3b-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1db3b-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1db3b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1db3b-132">-WhatIf</span></span>
<span data-ttu-id="1db3b-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1db3b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1db3b-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1db3b-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1db3b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1db3b-135">CommonParameters</span></span>
<span data-ttu-id="1db3b-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1db3b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1db3b-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1db3b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1db3b-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1db3b-138">INPUTS</span></span>

### <span data-ttu-id="1db3b-139">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="1db3b-139">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="1db3b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="1db3b-140">System.String</span></span>

## <span data-ttu-id="1db3b-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1db3b-141">OUTPUTS</span></span>

### <span data-ttu-id="1db3b-142">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="1db3b-142">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="1db3b-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="1db3b-143">NOTES</span></span>

## <span data-ttu-id="1db3b-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1db3b-144">RELATED LINKS</span></span>
