---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/remove-azurermpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Remove-AzureRmPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Remove-AzureRmPolicyRemediation.md
ms.openlocfilehash: ec5becd714b034789aeeb8449a63012232c99d5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662507"
---
# <span data-ttu-id="78778-101">Remove-AzureRmPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="78778-101">Remove-AzureRmPolicyRemediation</span></span>

## <span data-ttu-id="78778-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="78778-102">SYNOPSIS</span></span>
<span data-ttu-id="78778-103">Löscht eine Richtlinien Bereinigung.</span><span class="sxs-lookup"><span data-stu-id="78778-103">Deletes a policy remediation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78778-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="78778-104">SYNTAX</span></span>

### <span data-ttu-id="78778-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="78778-105">ByName (Default)</span></span>
```
Remove-AzureRmPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AllowStop] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78778-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="78778-106">ByResourceId</span></span>
```
Remove-AzureRmPolicyRemediation -ResourceId <String> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78778-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="78778-107">ByInputObject</span></span>
```
Remove-AzureRmPolicyRemediation -InputObject <PSRemediation> [-AllowStop] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78778-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="78778-108">DESCRIPTION</span></span>
<span data-ttu-id="78778-109">Das Cmdlet **Remove-AzureRmPolicyRemediation** löscht eine Richtlinien Bereinigung.</span><span class="sxs-lookup"><span data-stu-id="78778-109">The **Remove-AzureRmPolicyRemediation** cmdlet deletes a policy remediation.</span></span>

## <span data-ttu-id="78778-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="78778-110">EXAMPLES</span></span>

### <span data-ttu-id="78778-111">Beispiel 1: Löschen einer Richtlinien Bereinigung im Bereich der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="78778-111">Example 1: Delete a policy remediation at resource group scope</span></span>
```
PS C:\> Remove-AzureRmPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="78778-112">Dieser Befehl löscht die Bereinigung mit dem Namen "remediation1" in der Ressourcengruppe "myRG".</span><span class="sxs-lookup"><span data-stu-id="78778-112">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="78778-113">Beispiel 2: Löschen einer Verwaltungsgruppen Bereinigung über Rohre</span><span class="sxs-lookup"><span data-stu-id="78778-113">Example 2: Delete a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzureRmPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Remove-AzureRmPolicyRemediation -Confirm
```

<span data-ttu-id="78778-114">Dieser Befehl löscht die Bereinigung mit dem Namen "remediation1" aus der Verwaltungsgruppe "mg1".</span><span class="sxs-lookup"><span data-stu-id="78778-114">This command deletes the remediation named 'remediation1' from management group 'mg1'.</span></span> <span data-ttu-id="78778-115">Vor dem Löschen der Ressource wird eine Bestätigungsaufforderung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="78778-115">A confirmation prompt will be presented before deleting the resource.</span></span>

### <span data-ttu-id="78778-116">Beispiel 3: Abbrechen und Löschen einer Richtlinien Bereinigung</span><span class="sxs-lookup"><span data-stu-id="78778-116">Example 3: Cancel and delete a policy remediation</span></span>
```
PS C:\> Remove-AzureRmPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1" -AllowStop
```

<span data-ttu-id="78778-117">Dieser Befehl löscht die Bereinigung mit dem Namen "remediation1" in der Ressourcengruppe "myRG".</span><span class="sxs-lookup"><span data-stu-id="78778-117">This command deletes the remediation named 'remediation1' in resource group 'myRG'.</span></span> <span data-ttu-id="78778-118">Wenn die Bereinigung in Bearbeitung ist, wird Sie vor dem Löschen abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="78778-118">If the remediation is in-progress it will be canceled before being deleted.</span></span>

## <span data-ttu-id="78778-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="78778-119">PARAMETERS</span></span>

### <span data-ttu-id="78778-120">-AllowStop</span><span class="sxs-lookup"><span data-stu-id="78778-120">-AllowStop</span></span>
<span data-ttu-id="78778-121">Zulassen, dass die Behebung abgebrochen wird, wenn Sie in Bearbeitung ist.</span><span class="sxs-lookup"><span data-stu-id="78778-121">Allow the remediation to be canceled if it is in-progress.</span></span>

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

### <span data-ttu-id="78778-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="78778-122">-AsJob</span></span>
<span data-ttu-id="78778-123">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="78778-123">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="78778-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78778-124">-DefaultProfile</span></span>
<span data-ttu-id="78778-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="78778-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78778-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="78778-126">-InputObject</span></span>
<span data-ttu-id="78778-127">Das Behebungs Objekt.</span><span class="sxs-lookup"><span data-stu-id="78778-127">The Remediation object.</span></span>

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

### <span data-ttu-id="78778-128">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="78778-128">-ManagementGroupName</span></span>
<span data-ttu-id="78778-129">Verwaltungsgruppen-ID.</span><span class="sxs-lookup"><span data-stu-id="78778-129">Management group ID.</span></span>

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

### <span data-ttu-id="78778-130">-Name</span><span class="sxs-lookup"><span data-stu-id="78778-130">-Name</span></span>
<span data-ttu-id="78778-131">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="78778-131">Resource name.</span></span>

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

### <span data-ttu-id="78778-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78778-132">-PassThru</span></span>
<span data-ttu-id="78778-133">Gibt "true" zurück, wenn der Befehl erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="78778-133">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="78778-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78778-134">-ResourceGroupName</span></span>
<span data-ttu-id="78778-135">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="78778-135">Resource group name.</span></span>

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

### <span data-ttu-id="78778-136">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="78778-136">-ResourceId</span></span>
<span data-ttu-id="78778-137">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="78778-137">Resource ID.</span></span>

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

### <span data-ttu-id="78778-138">-Scope</span><span class="sxs-lookup"><span data-stu-id="78778-138">-Scope</span></span>
<span data-ttu-id="78778-139">Der Bereich der Ressource.</span><span class="sxs-lookup"><span data-stu-id="78778-139">Scope of the resource.</span></span>
<span data-ttu-id="78778-140">Z.b..</span><span class="sxs-lookup"><span data-stu-id="78778-140">E.g.</span></span>
<span data-ttu-id="78778-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="78778-141">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="78778-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="78778-142">-Confirm</span></span>
<span data-ttu-id="78778-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="78778-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78778-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78778-144">-WhatIf</span></span>
<span data-ttu-id="78778-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="78778-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78778-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="78778-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78778-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78778-147">CommonParameters</span></span>
<span data-ttu-id="78778-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78778-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78778-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78778-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78778-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="78778-150">INPUTS</span></span>

### <span data-ttu-id="78778-151">System. String</span><span class="sxs-lookup"><span data-stu-id="78778-151">System.String</span></span>

### <span data-ttu-id="78778-152">Microsoft. Azure. Commands. PolicyInsights. Models. Remediation. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="78778-152">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="78778-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="78778-153">OUTPUTS</span></span>

### <span data-ttu-id="78778-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="78778-154">System.Boolean</span></span>

## <span data-ttu-id="78778-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="78778-155">NOTES</span></span>

## <span data-ttu-id="78778-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="78778-156">RELATED LINKS</span></span>
