---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
ms.openlocfilehash: a8985d77ba1bbf33e49f353ad39d287f7bd3979b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920192"
---
# <span data-ttu-id="9b4b8-101">Remove-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="9b4b8-101">Remove-AzSqlInstance</span></span>

## <span data-ttu-id="9b4b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b4b8-102">SYNOPSIS</span></span>
<span data-ttu-id="9b4b8-103">Entfernt eine Azure SQL Verwaltete Datenbankinstanz.</span><span class="sxs-lookup"><span data-stu-id="9b4b8-103">Removes an Azure SQL Managed Database Instance.</span></span>

## <span data-ttu-id="9b4b8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9b4b8-104">SYNTAX</span></span>

### <span data-ttu-id="9b4b8-105">RemoveInstanceFromInputParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="9b4b8-105">RemoveInstanceFromInputParameters (Default)</span></span>
```
Remove-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b4b8-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="9b4b8-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Remove-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b4b8-107">RemoveInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="9b4b8-107">RemoveInstanceFromAzureResourceId</span></span>
```
Remove-AzSqlInstance [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b4b8-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b4b8-108">DESCRIPTION</span></span>
<span data-ttu-id="9b4b8-109">Das **Cmdlet Remove-AzSqlInstance** entfernt eine Azure SQL Datenbank verwaltete Instanz.</span><span class="sxs-lookup"><span data-stu-id="9b4b8-109">The **Remove-AzSqlInstance** cmdlet removes an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="9b4b8-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9b4b8-110">EXAMPLES</span></span>

### <span data-ttu-id="9b4b8-111">Beispiel 1: Entfernen der Instanz</span><span class="sxs-lookup"><span data-stu-id="9b4b8-111">Example 1: Remove instance</span></span>
```
PS C:\>Remove-AzSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="9b4b8-112">Mit diesem Befehl wird die Instanz mit dem Namen "managedInstance1" entfernt.</span><span class="sxs-lookup"><span data-stu-id="9b4b8-112">This command removes the instance named managedInstance1.</span></span>

## <span data-ttu-id="9b4b8-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9b4b8-113">PARAMETERS</span></span>

### <span data-ttu-id="9b4b8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b4b8-114">-DefaultProfile</span></span>
<span data-ttu-id="9b4b8-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9b4b8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b4b8-116">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="9b4b8-116">-Force</span></span>
<span data-ttu-id="9b4b8-117">Bestätigungsmeldung überspringen zum Ausführen der Aktion</span><span class="sxs-lookup"><span data-stu-id="9b4b8-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="9b4b8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b4b8-118">-InputObject</span></span>
<span data-ttu-id="9b4b8-119">Das zu entfernende AzureSqlManagedInstanceModel-Objekt</span><span class="sxs-lookup"><span data-stu-id="9b4b8-119">The AzureSqlManagedInstanceModel object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: SqlInstance

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b4b8-120">-Name</span><span class="sxs-lookup"><span data-stu-id="9b4b8-120">-Name</span></span>
<span data-ttu-id="9b4b8-121">SQL -Instanzname.</span><span class="sxs-lookup"><span data-stu-id="9b4b8-121">SQL instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b4b8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b4b8-122">-ResourceGroupName</span></span>
<span data-ttu-id="9b4b8-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9b4b8-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b4b8-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b4b8-124">-ResourceId</span></span>
<span data-ttu-id="9b4b8-125">Die Ressourcen-ID des zu entfernende Instanzobjekts</span><span class="sxs-lookup"><span data-stu-id="9b4b8-125">The resource id of instance object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b4b8-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9b4b8-126">-Confirm</span></span>
<span data-ttu-id="9b4b8-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9b4b8-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b4b8-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b4b8-128">-WhatIf</span></span>
<span data-ttu-id="9b4b8-129">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9b4b8-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b4b8-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9b4b8-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b4b8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b4b8-131">CommonParameters</span></span>
<span data-ttu-id="9b4b8-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b4b8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b4b8-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9b4b8-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b4b8-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9b4b8-134">INPUTS</span></span>

### <span data-ttu-id="9b4b8-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="9b4b8-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="9b4b8-136">System.String</span><span class="sxs-lookup"><span data-stu-id="9b4b8-136">System.String</span></span>

## <span data-ttu-id="9b4b8-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9b4b8-137">OUTPUTS</span></span>

### <span data-ttu-id="9b4b8-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="9b4b8-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="9b4b8-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9b4b8-139">NOTES</span></span>

## <span data-ttu-id="9b4b8-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9b4b8-140">RELATED LINKS</span></span>
