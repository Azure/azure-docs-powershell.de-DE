---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlvirtualcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlVirtualCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlVirtualCluster.md
ms.openlocfilehash: ef0ad91d0294f0ac1a4a466a79ce436a7719af5a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177176"
---
# <span data-ttu-id="f4a16-101">Remove-AzSqlVirtualCluster</span><span class="sxs-lookup"><span data-stu-id="f4a16-101">Remove-AzSqlVirtualCluster</span></span>

## <span data-ttu-id="f4a16-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f4a16-102">SYNOPSIS</span></span>
<span data-ttu-id="f4a16-103">Entfernt einen virtuellen Azure SQL-Cluster.</span><span class="sxs-lookup"><span data-stu-id="f4a16-103">Removes an Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="f4a16-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4a16-104">SYNTAX</span></span>

### <span data-ttu-id="f4a16-105">RemoveVirtualClusterFromInputParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="f4a16-105">RemoveVirtualClusterFromInputParameters (Default)</span></span>
```
Remove-AzSqlVirtualCluster [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4a16-106">RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition</span><span class="sxs-lookup"><span data-stu-id="f4a16-106">RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition</span></span>
```
Remove-AzSqlVirtualCluster [-InputObject] <AzureSqlVirtualClusterModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4a16-107">RemoveVirtualClusterFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="f4a16-107">RemoveVirtualClusterFromAzureResourceId</span></span>
```
Remove-AzSqlVirtualCluster -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4a16-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f4a16-108">DESCRIPTION</span></span>
<span data-ttu-id="f4a16-109">Das Cmdlet **Remove-AzSqlVirtualCluster** entfernt einen virtuellen Azure SQL-Cluster.</span><span class="sxs-lookup"><span data-stu-id="f4a16-109">The **Remove-AzSqlVirtualCluster** cmdlet removes an Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="f4a16-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f4a16-110">EXAMPLES</span></span>

### <span data-ttu-id="f4a16-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f4a16-111">Example 1</span></span>
```powershell
PS C:> Remove-AzSqlVirtualCluster -Name VirtualCluster1 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="f4a16-112">Dieser Befehl entfernt den virtuellen Cluster mit dem Namen VirtualCluster1, der der Ressourcengruppe ResourceGroup01 zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="f4a16-112">This command removes the virtual cluster named VirtualCluster1 assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="f4a16-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4a16-113">PARAMETERS</span></span>

### <span data-ttu-id="f4a16-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4a16-114">-AsJob</span></span>
<span data-ttu-id="f4a16-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f4a16-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f4a16-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4a16-116">-DefaultProfile</span></span>
<span data-ttu-id="f4a16-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f4a16-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4a16-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f4a16-118">-InputObject</span></span>
<span data-ttu-id="f4a16-119">Das zu entfernende Instanzen Objekt</span><span class="sxs-lookup"><span data-stu-id="f4a16-119">The instance object to remove</span></span>

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

### <span data-ttu-id="f4a16-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f4a16-120">-Name</span></span>
<span data-ttu-id="f4a16-121">Der Name des virtuellen Clusters.</span><span class="sxs-lookup"><span data-stu-id="f4a16-121">The name of the virtual cluster.</span></span>

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

### <span data-ttu-id="f4a16-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4a16-122">-ResourceGroupName</span></span>
<span data-ttu-id="f4a16-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f4a16-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="f4a16-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f4a16-124">-ResourceId</span></span>
<span data-ttu-id="f4a16-125">Die Ressourcen-ID des zu entfernenden Instance-Objekts</span><span class="sxs-lookup"><span data-stu-id="f4a16-125">The resource id of instance object to remove</span></span>

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

### <span data-ttu-id="f4a16-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f4a16-126">-Confirm</span></span>
<span data-ttu-id="f4a16-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f4a16-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4a16-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4a16-128">-WhatIf</span></span>
<span data-ttu-id="f4a16-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f4a16-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4a16-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f4a16-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4a16-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4a16-131">CommonParameters</span></span>
<span data-ttu-id="f4a16-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4a16-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4a16-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4a16-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4a16-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f4a16-134">INPUTS</span></span>

### <span data-ttu-id="f4a16-135">Microsoft. Azure. Commands. SQL. VirtualCluster. Model. AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="f4a16-135">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

### <span data-ttu-id="f4a16-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f4a16-136">System.String</span></span>

## <span data-ttu-id="f4a16-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f4a16-137">OUTPUTS</span></span>

### <span data-ttu-id="f4a16-138">Microsoft. Azure. Commands. SQL. VirtualCluster. Model. AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="f4a16-138">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

## <span data-ttu-id="f4a16-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="f4a16-139">NOTES</span></span>

## <span data-ttu-id="f4a16-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f4a16-140">RELATED LINKS</span></span>
