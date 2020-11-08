---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/remove-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Remove-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Remove-AzPolicyRemediation.md
ms.openlocfilehash: 969b764be302231f33dda00b32afb79ec04a324e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003179"
---
# <span data-ttu-id="20edb-101">Remove-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="20edb-101">Remove-AzPolicyRemediation</span></span>

## <span data-ttu-id="20edb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="20edb-102">SYNOPSIS</span></span>
<span data-ttu-id="20edb-103">Löscht eine Richtlinien Bereinigung.</span><span class="sxs-lookup"><span data-stu-id="20edb-103">Deletes a policy remediation.</span></span>

## <span data-ttu-id="20edb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="20edb-104">SYNTAX</span></span>

### <span data-ttu-id="20edb-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="20edb-105">ByName (Default)</span></span>
```
Remove-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AllowStop] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20edb-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="20edb-106">ByResourceId</span></span>
```
Remove-AzPolicyRemediation -ResourceId <String> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20edb-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="20edb-107">ByInputObject</span></span>
```
Remove-AzPolicyRemediation -InputObject <PSRemediation> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20edb-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20edb-108">DESCRIPTION</span></span>
<span data-ttu-id="20edb-109">Das Cmdlet **Remove-AzPolicyRemediation** löscht eine Richtlinien Bereinigung.</span><span class="sxs-lookup"><span data-stu-id="20edb-109">The **Remove-AzPolicyRemediation** cmdlet deletes a policy remediation.</span></span>

## <span data-ttu-id="20edb-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="20edb-110">EXAMPLES</span></span>

### <span data-ttu-id="20edb-111">Beispiel 1: Löschen einer Richtlinien Bereinigung im Bereich der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="20edb-111">Example 1: Delete a policy remediation at resource group scope</span></span>
```
PS C:\> Remove-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="20edb-112">Dieser Befehl löscht die Bereinigung mit dem Namen "remediation1" in der Ressourcengruppe "myRG".</span><span class="sxs-lookup"><span data-stu-id="20edb-112">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="20edb-113">Beispiel 2: Löschen einer Verwaltungsgruppen Bereinigung über Rohre</span><span class="sxs-lookup"><span data-stu-id="20edb-113">Example 2: Delete a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Remove-AzPolicyRemediation -Confirm
```

<span data-ttu-id="20edb-114">Dieser Befehl löscht die Bereinigung mit dem Namen "remediation1" aus der Verwaltungsgruppe "mg1".</span><span class="sxs-lookup"><span data-stu-id="20edb-114">This command deletes the remediation named 'remediation1' from management group 'mg1'.</span></span> <span data-ttu-id="20edb-115">Vor dem Löschen der Ressource wird eine Bestätigungsaufforderung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="20edb-115">A confirmation prompt will be presented before deleting the resource.</span></span>

### <span data-ttu-id="20edb-116">Beispiel 3: Abbrechen und Löschen einer Richtlinien Bereinigung</span><span class="sxs-lookup"><span data-stu-id="20edb-116">Example 3: Cancel and delete a policy remediation</span></span>
```
PS C:\> Remove-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1" -AllowStop
```

<span data-ttu-id="20edb-117">Dieser Befehl löscht die Bereinigung mit dem Namen "remediation1" in der Ressourcengruppe "myRG".</span><span class="sxs-lookup"><span data-stu-id="20edb-117">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span> <span data-ttu-id="20edb-118">Wenn die Bereinigung in Bearbeitung ist, wird Sie vor dem Löschen abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="20edb-118">If the remediation is in-progress it will be canceled before being deleted.</span></span>

## <span data-ttu-id="20edb-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="20edb-119">PARAMETERS</span></span>

### <span data-ttu-id="20edb-120">-AllowStop</span><span class="sxs-lookup"><span data-stu-id="20edb-120">-AllowStop</span></span>
<span data-ttu-id="20edb-121">Zulassen, dass die Behebung abgebrochen wird, wenn Sie in Bearbeitung ist.</span><span class="sxs-lookup"><span data-stu-id="20edb-121">Allow the remediation to be canceled if it is in-progress.</span></span>

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

### <span data-ttu-id="20edb-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20edb-122">-AsJob</span></span>
<span data-ttu-id="20edb-123">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="20edb-123">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="20edb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20edb-124">-DefaultProfile</span></span>
<span data-ttu-id="20edb-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="20edb-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20edb-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="20edb-126">-InputObject</span></span>
<span data-ttu-id="20edb-127">Das Behebungs Objekt.</span><span class="sxs-lookup"><span data-stu-id="20edb-127">The Remediation object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20edb-128">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="20edb-128">-ManagementGroupName</span></span>
<span data-ttu-id="20edb-129">Verwaltungsgruppen-ID.</span><span class="sxs-lookup"><span data-stu-id="20edb-129">Management group ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20edb-130">-Name</span><span class="sxs-lookup"><span data-stu-id="20edb-130">-Name</span></span>
<span data-ttu-id="20edb-131">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="20edb-131">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20edb-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20edb-132">-PassThru</span></span>
<span data-ttu-id="20edb-133">Gibt "true" zurück, wenn der Befehl erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="20edb-133">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="20edb-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20edb-134">-ResourceGroupName</span></span>
<span data-ttu-id="20edb-135">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="20edb-135">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20edb-136">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="20edb-136">-ResourceId</span></span>
<span data-ttu-id="20edb-137">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="20edb-137">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20edb-138">-Scope</span><span class="sxs-lookup"><span data-stu-id="20edb-138">-Scope</span></span>
<span data-ttu-id="20edb-139">Der Bereich der Ressource.</span><span class="sxs-lookup"><span data-stu-id="20edb-139">Scope of the resource.</span></span>
<span data-ttu-id="20edb-140">Z.b..</span><span class="sxs-lookup"><span data-stu-id="20edb-140">E.g.</span></span>
<span data-ttu-id="20edb-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="20edb-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20edb-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="20edb-142">-Confirm</span></span>
<span data-ttu-id="20edb-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="20edb-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20edb-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20edb-144">-WhatIf</span></span>
<span data-ttu-id="20edb-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="20edb-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20edb-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="20edb-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20edb-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20edb-147">CommonParameters</span></span>
<span data-ttu-id="20edb-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20edb-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20edb-149">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20edb-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20edb-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="20edb-150">INPUTS</span></span>

### <span data-ttu-id="20edb-151">System. String</span><span class="sxs-lookup"><span data-stu-id="20edb-151">System.String</span></span>

### <span data-ttu-id="20edb-152">Microsoft. Azure. Commands. PolicyInsights. Models. Remediation. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="20edb-152">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="20edb-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="20edb-153">OUTPUTS</span></span>

### <span data-ttu-id="20edb-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="20edb-154">System.Boolean</span></span>

## <span data-ttu-id="20edb-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="20edb-155">NOTES</span></span>

## <span data-ttu-id="20edb-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="20edb-156">RELATED LINKS</span></span>
