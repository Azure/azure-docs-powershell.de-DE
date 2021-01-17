---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlvirtualcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlVirtualCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlVirtualCluster.md
ms.openlocfilehash: ef0ad91d0294f0ac1a4a466a79ce436a7719af5a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458419"
---
# <span data-ttu-id="638ae-101">Remove-AzSqlVirtualCluster</span><span class="sxs-lookup"><span data-stu-id="638ae-101">Remove-AzSqlVirtualCluster</span></span>

## <span data-ttu-id="638ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="638ae-102">SYNOPSIS</span></span>
<span data-ttu-id="638ae-103">Entfernt einen virtuellen Azure SQL Cluster.</span><span class="sxs-lookup"><span data-stu-id="638ae-103">Removes an Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="638ae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="638ae-104">SYNTAX</span></span>

### <span data-ttu-id="638ae-105">RemoveVirtualClusterFromInputParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="638ae-105">RemoveVirtualClusterFromInputParameters (Default)</span></span>
```
Remove-AzSqlVirtualCluster [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="638ae-106">RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition</span><span class="sxs-lookup"><span data-stu-id="638ae-106">RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition</span></span>
```
Remove-AzSqlVirtualCluster [-InputObject] <AzureSqlVirtualClusterModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="638ae-107">RemoveVirtualClusterFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="638ae-107">RemoveVirtualClusterFromAzureResourceId</span></span>
```
Remove-AzSqlVirtualCluster -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="638ae-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="638ae-108">DESCRIPTION</span></span>
<span data-ttu-id="638ae-109">Das **Cmdlet "Remove-AzSqlVirtualCluster"** entfernt einen virtuellen Azure SQL Cluster.</span><span class="sxs-lookup"><span data-stu-id="638ae-109">The **Remove-AzSqlVirtualCluster** cmdlet removes an Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="638ae-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="638ae-110">EXAMPLES</span></span>

### <span data-ttu-id="638ae-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="638ae-111">Example 1</span></span>
```powershell
PS C:> Remove-AzSqlVirtualCluster -Name VirtualCluster1 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="638ae-112">Mit diesem Befehl wird der virtuelle Cluster "VirtualCluster1" entfernt, der der Ressourcengruppe "ResourceGroup01" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="638ae-112">This command removes the virtual cluster named VirtualCluster1 assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="638ae-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="638ae-113">PARAMETERS</span></span>

### <span data-ttu-id="638ae-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="638ae-114">-AsJob</span></span>
<span data-ttu-id="638ae-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="638ae-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="638ae-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="638ae-116">-DefaultProfile</span></span>
<span data-ttu-id="638ae-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="638ae-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="638ae-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="638ae-118">-InputObject</span></span>
<span data-ttu-id="638ae-119">Das zu entfernende Instanzobjekt</span><span class="sxs-lookup"><span data-stu-id="638ae-119">The instance object to remove</span></span>

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

### <span data-ttu-id="638ae-120">-Name</span><span class="sxs-lookup"><span data-stu-id="638ae-120">-Name</span></span>
<span data-ttu-id="638ae-121">Der Name des virtuellen Cluster.</span><span class="sxs-lookup"><span data-stu-id="638ae-121">The name of the virtual cluster.</span></span>

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

### <span data-ttu-id="638ae-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="638ae-122">-ResourceGroupName</span></span>
<span data-ttu-id="638ae-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="638ae-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="638ae-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="638ae-124">-ResourceId</span></span>
<span data-ttu-id="638ae-125">Die Ressourcen-ID des zu entfernende Instanzobjekts</span><span class="sxs-lookup"><span data-stu-id="638ae-125">The resource id of instance object to remove</span></span>

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

### <span data-ttu-id="638ae-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="638ae-126">-Confirm</span></span>
<span data-ttu-id="638ae-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="638ae-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="638ae-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="638ae-128">-WhatIf</span></span>
<span data-ttu-id="638ae-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="638ae-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="638ae-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="638ae-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="638ae-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="638ae-131">CommonParameters</span></span>
<span data-ttu-id="638ae-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="638ae-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="638ae-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="638ae-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="638ae-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="638ae-134">INPUTS</span></span>

### <span data-ttu-id="638ae-135">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="638ae-135">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

### <span data-ttu-id="638ae-136">System.String</span><span class="sxs-lookup"><span data-stu-id="638ae-136">System.String</span></span>

## <span data-ttu-id="638ae-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="638ae-137">OUTPUTS</span></span>

### <span data-ttu-id="638ae-138">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="638ae-138">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

## <span data-ttu-id="638ae-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="638ae-139">NOTES</span></span>

## <span data-ttu-id="638ae-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="638ae-140">RELATED LINKS</span></span>
