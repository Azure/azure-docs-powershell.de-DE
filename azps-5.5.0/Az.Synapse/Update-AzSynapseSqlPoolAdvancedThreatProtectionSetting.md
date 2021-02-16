---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqlpooladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 87c3f0e2e86f2867d659b26b5acc9df5a6dfe8c7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100173497"
---
# <span data-ttu-id="3b3a4-101">Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="3b3a4-101">Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="3b3a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b3a4-102">SYNOPSIS</span></span>
<span data-ttu-id="3b3a4-103">Legt eine erweiterte Threat Protection-Einstellung für einen SQL fest.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-103">Sets a advanced threat protection settings on a SQL pool.</span></span>

## <span data-ttu-id="3b3a4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3b3a4-104">SYNTAX</span></span>

### <span data-ttu-id="3b3a4-105">UpdateByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3b3a4-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>]
 [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b3a4-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b3a4-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b3a4-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b3a4-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -InputObject <PSSynapseSqlPool>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b3a4-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b3a4-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -ResourceId <String>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b3a4-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3b3a4-109">DESCRIPTION</span></span>
<span data-ttu-id="3b3a4-110">Das **Cmdlet "Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting"** legt eine erweiterte Threat Protection-Einstellung für einen Azure Synapse Analytics SQL fest.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-110">The **Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure Synapse Analytics SQL pool.</span></span>
<span data-ttu-id="3b3a4-111">Um erweiterten Bedrohungsschutz für einen SQL müssen für diesen Pool Überwachungseinstellungen SQL werden.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-111">In order to enable advanced threat protection on a SQL pool an auditing settings must be enabled on that SQL pool.</span></span>

## <span data-ttu-id="3b3a4-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3b3a4-112">EXAMPLES</span></span>

### <span data-ttu-id="3b3a4-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3b3a4-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="3b3a4-114">Dieser Befehl legt die erweiterten Threat Protection-Einstellungen für einen SQL "ContosoSqlPool" unter dem Arbeitsbereich "ContosoWorkspace" fest.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-114">This command sets the advanced threat protection settings for a SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="3b3a4-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b3a4-115">PARAMETERS</span></span>

### <span data-ttu-id="3b3a4-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3b3a4-116">-AsJob</span></span>
<span data-ttu-id="3b3a4-117">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3b3a4-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3b3a4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b3a4-118">-DefaultProfile</span></span>
<span data-ttu-id="3b3a4-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b3a4-120">-EmailAdmin</span><span class="sxs-lookup"><span data-stu-id="3b3a4-120">-EmailAdmin</span></span>
<span data-ttu-id="3b3a4-121">Definiert, ob Administratoren eine E-Mail senden möchten.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-121">Defines whether to email administrators.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: EmailAdmins

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3a4-122">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="3b3a4-122">-ExcludedDetectionType</span></span>
<span data-ttu-id="3b3a4-123">Auszuschließende Erkennungstypen.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-123">Detection types to exclude.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3a4-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b3a4-124">-InputObject</span></span>
<span data-ttu-id="3b3a4-125">SQL pool-Eingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-125">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b3a4-126">-Name</span><span class="sxs-lookup"><span data-stu-id="3b3a4-126">-Name</span></span>
<span data-ttu-id="3b3a4-127">Name des Synapse SQL Pools.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-127">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3a4-128">-NotificationRecipientsEmail</span><span class="sxs-lookup"><span data-stu-id="3b3a4-128">-NotificationRecipientsEmail</span></span>
<span data-ttu-id="3b3a4-129">Eine durch Semikolons getrennte Liste der E-Mail-Adressen, an die die Benachrichtigungen gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-129">A semicolon separated list of email addresses to send the alerts to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NotificationRecipientsEmails

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3a4-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b3a4-130">-ResourceGroupName</span></span>
<span data-ttu-id="3b3a4-131">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-131">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3a4-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b3a4-132">-ResourceId</span></span>
<span data-ttu-id="3b3a4-133">Ressourcenbezeichner von Synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-133">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3a4-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="3b3a4-134">-RetentionInDays</span></span>
<span data-ttu-id="3b3a4-135">Die Anzahl der Aufbewahrungstage für die Überwachungsprotokolle.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-135">The number of retention days for the audit logs.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3a4-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3b3a4-136">-StorageAccountName</span></span>
<span data-ttu-id="3b3a4-137">Der Name des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-137">The name of the storage account.</span></span>

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

### <span data-ttu-id="3b3a4-138">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3b3a4-138">-WorkspaceName</span></span>
<span data-ttu-id="3b3a4-139">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-139">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3a4-140">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3b3a4-140">-WorkspaceObject</span></span>
<span data-ttu-id="3b3a4-141">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-141">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b3a4-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3b3a4-142">-Confirm</span></span>
<span data-ttu-id="3b3a4-143">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b3a4-144">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3b3a4-144">-WhatIf</span></span>
<span data-ttu-id="3b3a4-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b3a4-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b3a4-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b3a4-147">CommonParameters</span></span>
<span data-ttu-id="3b3a4-148">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b3a4-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b3a4-149">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3b3a4-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b3a4-150">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3b3a4-150">INPUTS</span></span>

### <span data-ttu-id="3b3a4-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3b3a4-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="3b3a4-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="3b3a4-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="3b3a4-153">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3b3a4-153">OUTPUTS</span></span>

### <span data-ttu-id="3b3a4-154">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="3b3a4-154">Microsoft.Azure.Commands.Synapse.Models.PSSqlPoolSecurityAlertPolicy</span></span>

## <span data-ttu-id="3b3a4-155">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3b3a4-155">NOTES</span></span>

## <span data-ttu-id="3b3a4-156">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3b3a4-156">RELATED LINKS</span></span>
