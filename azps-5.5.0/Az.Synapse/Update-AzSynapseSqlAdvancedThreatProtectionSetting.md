---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 4fb27d1d822d72de9564e9acc900122016940c6d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100174876"
---
# <span data-ttu-id="76d07-101">Update-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="76d07-101">Update-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="76d07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76d07-102">SYNOPSIS</span></span>
<span data-ttu-id="76d07-103">Aktualisiert eine erweiterte Threat Protection-Einstellung in einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="76d07-103">Updates an advanced threat protection settings on a workspace.</span></span>

## <span data-ttu-id="76d07-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76d07-104">SYNTAX</span></span>

### <span data-ttu-id="76d07-105">UpdateByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="76d07-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76d07-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="76d07-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76d07-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="76d07-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-NotificationRecipientsEmail <String>]
 [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="76d07-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="76d07-108">DESCRIPTION</span></span>
<span data-ttu-id="76d07-109">Das **Cmdlet "Update-AzSynapseSqlAdvancedThreatProtectionSetting"** aktualisiert eine erweiterte Threat Protection-Einstellung in einem Azure Synapse Analytics Workspace.</span><span class="sxs-lookup"><span data-stu-id="76d07-109">The **Update-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet updates an advanced threat protection settings on an Azure Synapse Analytics Workspace.</span></span> <span data-ttu-id="76d07-110">Um erweiterten Bedrohungsschutz für einen Arbeitsbereich zu aktivieren, müssen in diesem Arbeitsbereich Überwachungseinstellungen aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="76d07-110">In order to enable advanced threat protection on a workspace an auditing settings must be enabled on that workspace.</span></span>

## <span data-ttu-id="76d07-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="76d07-111">EXAMPLES</span></span>

### <span data-ttu-id="76d07-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="76d07-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -NotificationRecipientsEmail "admin01@contoso.com;secadmin@contoso.com" -EmailAdmin $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="76d07-113">Mit diesem Befehl werden die erweiterten Threat Protection-Einstellungen für einen Arbeitsbereich namens ContosoWorkspace aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="76d07-113">This command updates the advanced threat protection settings for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="76d07-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76d07-114">PARAMETERS</span></span>

### <span data-ttu-id="76d07-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76d07-115">-AsJob</span></span>
<span data-ttu-id="76d07-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="76d07-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="76d07-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76d07-117">-DefaultProfile</span></span>
<span data-ttu-id="76d07-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="76d07-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76d07-119">-EmailAdmin</span><span class="sxs-lookup"><span data-stu-id="76d07-119">-EmailAdmin</span></span>
<span data-ttu-id="76d07-120">Definiert, ob Administratoren eine E-Mail senden möchten.</span><span class="sxs-lookup"><span data-stu-id="76d07-120">Defines whether to email administrators.</span></span>

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

### <span data-ttu-id="76d07-121">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="76d07-121">-ExcludedDetectionType</span></span>
<span data-ttu-id="76d07-122">Auszuschließende Erkennungstypen.</span><span class="sxs-lookup"><span data-stu-id="76d07-122">Detection types to exclude.</span></span>

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

### <span data-ttu-id="76d07-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76d07-123">-InputObject</span></span>
<span data-ttu-id="76d07-124">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="76d07-124">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76d07-125">-NotificationRecipientsEmail</span><span class="sxs-lookup"><span data-stu-id="76d07-125">-NotificationRecipientsEmail</span></span>
<span data-ttu-id="76d07-126">Eine durch Semikolons getrennte Liste der E-Mail-Adressen, an die die Benachrichtigungen gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="76d07-126">A semicolon separated list of email addresses to send the alerts to.</span></span>

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

### <span data-ttu-id="76d07-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76d07-127">-ResourceGroupName</span></span>
<span data-ttu-id="76d07-128">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="76d07-128">Resource group name.</span></span>

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

### <span data-ttu-id="76d07-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76d07-129">-ResourceId</span></span>
<span data-ttu-id="76d07-130">Ressourcenbezeichner des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="76d07-130">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="76d07-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="76d07-131">-RetentionInDays</span></span>
<span data-ttu-id="76d07-132">Die Anzahl der Aufbewahrungstage für die Überwachungsprotokolle.</span><span class="sxs-lookup"><span data-stu-id="76d07-132">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="76d07-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="76d07-133">-StorageAccountName</span></span>
<span data-ttu-id="76d07-134">Der Name des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="76d07-134">The name of the storage account.</span></span>

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

### <span data-ttu-id="76d07-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="76d07-135">-WorkspaceName</span></span>
<span data-ttu-id="76d07-136">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="76d07-136">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="76d07-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76d07-137">-Confirm</span></span>
<span data-ttu-id="76d07-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="76d07-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76d07-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="76d07-139">-WhatIf</span></span>
<span data-ttu-id="76d07-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="76d07-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76d07-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="76d07-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76d07-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76d07-142">CommonParameters</span></span>
<span data-ttu-id="76d07-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76d07-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76d07-144">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76d07-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76d07-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="76d07-145">INPUTS</span></span>

### <span data-ttu-id="76d07-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="76d07-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="76d07-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="76d07-147">OUTPUTS</span></span>

### <span data-ttu-id="76d07-148">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="76d07-148">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span></span>

## <span data-ttu-id="76d07-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="76d07-149">NOTES</span></span>

## <span data-ttu-id="76d07-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="76d07-150">RELATED LINKS</span></span>
