---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlvirtualcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlVirtualCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlVirtualCluster.md
ms.openlocfilehash: d4c69457b9932f76d002e3941af3015225345c8f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659023"
---
# <span data-ttu-id="a0082-101">Remove-AzSqlVirtualCluster</span><span class="sxs-lookup"><span data-stu-id="a0082-101">Remove-AzSqlVirtualCluster</span></span>

## <span data-ttu-id="a0082-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a0082-102">SYNOPSIS</span></span>
<span data-ttu-id="a0082-103">Entfernt einen virtuellen Azure SQL-Cluster.</span><span class="sxs-lookup"><span data-stu-id="a0082-103">Removes an Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="a0082-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0082-104">SYNTAX</span></span>

### <span data-ttu-id="a0082-105">RemoveVirtualClusterFromInputParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="a0082-105">RemoveVirtualClusterFromInputParameters (Default)</span></span>
```
Remove-AzSqlVirtualCluster [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0082-106">RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition</span><span class="sxs-lookup"><span data-stu-id="a0082-106">RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition</span></span>
```
Remove-AzSqlVirtualCluster [-InputObject] <AzureSqlVirtualClusterModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0082-107">RemoveVirtualClusterFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="a0082-107">RemoveVirtualClusterFromAzureResourceId</span></span>
```
Remove-AzSqlVirtualCluster -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0082-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a0082-108">DESCRIPTION</span></span>
<span data-ttu-id="a0082-109">Das Cmdlet **Remove-AzSqlVirtualCluster** entfernt einen virtuellen Azure SQL-Cluster.</span><span class="sxs-lookup"><span data-stu-id="a0082-109">The **Remove-AzSqlVirtualCluster** cmdlet removes an Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="a0082-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a0082-110">EXAMPLES</span></span>

### <span data-ttu-id="a0082-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a0082-111">Example 1</span></span>
```powershell
PS C:> Remove-AzSqlVirtualCluster -Name VirtualCluster1 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="a0082-112">Dieser Befehl entfernt den virtuellen Cluster mit dem Namen VirtualCluster1, der der Ressourcengruppe ResourceGroup01 zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="a0082-112">This command removes the virtual cluster named VirtualCluster1 assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="a0082-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0082-113">PARAMETERS</span></span>

### <span data-ttu-id="a0082-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a0082-114">-AsJob</span></span>
<span data-ttu-id="a0082-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a0082-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0082-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0082-116">-DefaultProfile</span></span>
<span data-ttu-id="a0082-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a0082-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0082-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a0082-118">-InputObject</span></span>
<span data-ttu-id="a0082-119">Das zu entfernende Instanzen Objekt</span><span class="sxs-lookup"><span data-stu-id="a0082-119">The instance object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel
Parameter Sets: RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition
Aliases: VirtualCluster

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0082-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a0082-120">-Name</span></span>
<span data-ttu-id="a0082-121">Der Name des virtuellen Clusters.</span><span class="sxs-lookup"><span data-stu-id="a0082-121">The name of the virtual cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveVirtualClusterFromInputParameters
Aliases: VirtualClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0082-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0082-122">-ResourceGroupName</span></span>
<span data-ttu-id="a0082-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a0082-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveVirtualClusterFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0082-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a0082-124">-ResourceId</span></span>
<span data-ttu-id="a0082-125">Die Ressourcen-ID des zu entfernenden Instance-Objekts</span><span class="sxs-lookup"><span data-stu-id="a0082-125">The resource id of instance object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveVirtualClusterFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0082-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a0082-126">-Confirm</span></span>
<span data-ttu-id="a0082-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a0082-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0082-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0082-128">-WhatIf</span></span>
<span data-ttu-id="a0082-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a0082-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0082-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a0082-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0082-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0082-131">CommonParameters</span></span>
<span data-ttu-id="a0082-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0082-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0082-133">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0082-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0082-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a0082-134">INPUTS</span></span>

### <span data-ttu-id="a0082-135">Microsoft. Azure. Commands. SQL. VirtualCluster. Model. AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="a0082-135">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

### <span data-ttu-id="a0082-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a0082-136">System.String</span></span>

## <span data-ttu-id="a0082-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a0082-137">OUTPUTS</span></span>

### <span data-ttu-id="a0082-138">Microsoft. Azure. Commands. SQL. VirtualCluster. Model. AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="a0082-138">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

## <span data-ttu-id="a0082-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="a0082-139">NOTES</span></span>

## <span data-ttu-id="a0082-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a0082-140">RELATED LINKS</span></span>
