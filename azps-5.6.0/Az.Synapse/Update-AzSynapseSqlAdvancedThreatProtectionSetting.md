---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 5766c93ba1fa7434b6ebd41f0c414f5e8a9a5073
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939112"
---
# <span data-ttu-id="ec398-101">Update-AzSynapseSqlAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="ec398-101">Update-AzSynapseSqlAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="ec398-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec398-102">SYNOPSIS</span></span>
<span data-ttu-id="ec398-103">Aktualisiert erweiterte Einstellungen für den Bedrohungsschutz in einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="ec398-103">Updates an advanced threat protection settings on a workspace.</span></span>

## <span data-ttu-id="ec398-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ec398-104">SYNTAX</span></span>

### <span data-ttu-id="ec398-105">UpdateByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ec398-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec398-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec398-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec398-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec398-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-NotificationRecipientsEmail <String>]
 [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ec398-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ec398-108">DESCRIPTION</span></span>
<span data-ttu-id="ec398-109">Das **Update-AzSynapseSqlAdvancedThreatProtectionSetting-Cmdlet** aktualisiert erweiterte Bedrohungsschutzeinstellungen in einem Azure Synapse Analytics Workspace.</span><span class="sxs-lookup"><span data-stu-id="ec398-109">The **Update-AzSynapseSqlAdvancedThreatProtectionSetting** cmdlet updates an advanced threat protection settings on an Azure Synapse Analytics Workspace.</span></span> <span data-ttu-id="ec398-110">Um erweiterten Bedrohungsschutz für einen Arbeitsbereich zu aktivieren, müssen überwachungseinstellungen für diesen Arbeitsbereich aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="ec398-110">In order to enable advanced threat protection on a workspace an auditing settings must be enabled on that workspace.</span></span>

## <span data-ttu-id="ec398-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ec398-111">EXAMPLES</span></span>

### <span data-ttu-id="ec398-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ec398-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -NotificationRecipientsEmail "admin01@contoso.com;secadmin@contoso.com" -EmailAdmin $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="ec398-113">Mit diesem Befehl werden die erweiterten Bedrohungsschutzeinstellungen für einen Arbeitsbereich namens ContosoWorkspace aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="ec398-113">This command updates the advanced threat protection settings for a workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="ec398-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ec398-114">PARAMETERS</span></span>

### <span data-ttu-id="ec398-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ec398-115">-AsJob</span></span>
<span data-ttu-id="ec398-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ec398-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ec398-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec398-117">-DefaultProfile</span></span>
<span data-ttu-id="ec398-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ec398-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec398-119">-EmailAdmin</span><span class="sxs-lookup"><span data-stu-id="ec398-119">-EmailAdmin</span></span>
<span data-ttu-id="ec398-120">Definiert, ob Administratoren per E-Mail benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="ec398-120">Defines whether to email administrators.</span></span>

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

### <span data-ttu-id="ec398-121">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="ec398-121">-ExcludedDetectionType</span></span>
<span data-ttu-id="ec398-122">Erkennungstypen, die ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="ec398-122">Detection types to exclude.</span></span>

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

### <span data-ttu-id="ec398-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec398-123">-InputObject</span></span>
<span data-ttu-id="ec398-124">Arbeitsbereichseingabeobjekt, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="ec398-124">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="ec398-125">-NotificationRecipientsEmail</span><span class="sxs-lookup"><span data-stu-id="ec398-125">-NotificationRecipientsEmail</span></span>
<span data-ttu-id="ec398-126">Eine semikolon getrennte Liste der E-Mail-Adressen, an die die Benachrichtigungen gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ec398-126">A semicolon separated list of email addresses to send the alerts to.</span></span>

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

### <span data-ttu-id="ec398-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec398-127">-ResourceGroupName</span></span>
<span data-ttu-id="ec398-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ec398-128">Resource group name.</span></span>

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

### <span data-ttu-id="ec398-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec398-129">-ResourceId</span></span>
<span data-ttu-id="ec398-130">Ressourcenbezeichner des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="ec398-130">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="ec398-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="ec398-131">-RetentionInDays</span></span>
<span data-ttu-id="ec398-132">Die Anzahl der Aufbewahrungstage für die Überwachungsprotokolle.</span><span class="sxs-lookup"><span data-stu-id="ec398-132">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="ec398-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ec398-133">-StorageAccountName</span></span>
<span data-ttu-id="ec398-134">Der Name des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="ec398-134">The name of the storage account.</span></span>

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

### <span data-ttu-id="ec398-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ec398-135">-WorkspaceName</span></span>
<span data-ttu-id="ec398-136">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="ec398-136">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="ec398-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ec398-137">-Confirm</span></span>
<span data-ttu-id="ec398-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ec398-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec398-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec398-139">-WhatIf</span></span>
<span data-ttu-id="ec398-140">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ec398-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec398-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ec398-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec398-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec398-142">CommonParameters</span></span>
<span data-ttu-id="ec398-143">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec398-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec398-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec398-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec398-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ec398-145">INPUTS</span></span>

### <span data-ttu-id="ec398-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ec398-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="ec398-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ec398-147">OUTPUTS</span></span>

### <span data-ttu-id="ec398-148">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span><span class="sxs-lookup"><span data-stu-id="ec398-148">Microsoft.Azure.Commands.Synapse.Models.PSServerSecurityAlertPolicy</span></span>

## <span data-ttu-id="ec398-149">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ec398-149">NOTES</span></span>

## <span data-ttu-id="ec398-150">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ec398-150">RELATED LINKS</span></span>
