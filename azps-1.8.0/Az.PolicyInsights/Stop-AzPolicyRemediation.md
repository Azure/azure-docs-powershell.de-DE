---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/stop-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Stop-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Stop-AzPolicyRemediation.md
ms.openlocfilehash: 2630b438fa9c5aaa691422be2da2d32e08112fba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660028"
---
# <span data-ttu-id="3fecd-101">Stop-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="3fecd-101">Stop-AzPolicyRemediation</span></span>

## <span data-ttu-id="3fecd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3fecd-102">SYNOPSIS</span></span>
<span data-ttu-id="3fecd-103">Bricht eine in-Progress-Richtlinien Bereinigung ab.</span><span class="sxs-lookup"><span data-stu-id="3fecd-103">Cancels an in-progress policy remediation.</span></span>

## <span data-ttu-id="3fecd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3fecd-104">SYNTAX</span></span>

### <span data-ttu-id="3fecd-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="3fecd-105">ByName (Default)</span></span>
```
Stop-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fecd-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3fecd-106">ByResourceId</span></span>
```
Stop-AzPolicyRemediation -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fecd-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3fecd-107">ByInputObject</span></span>
```
Stop-AzPolicyRemediation -InputObject <PSRemediation> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fecd-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3fecd-108">DESCRIPTION</span></span>
<span data-ttu-id="3fecd-109">Das Cmdlet " **Stop-AzPolicyRemediation** " bricht eine in-Progress-Richtlinien Bereinigung ab.</span><span class="sxs-lookup"><span data-stu-id="3fecd-109">The **Stop-AzPolicyRemediation** cmdlet cancels an in-progress policy remediation.</span></span> <span data-ttu-id="3fecd-110">Aktive Bereitstellungen werden abgebrochen, und es werden keine neuen Bereitstellungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="3fecd-110">Active deployments will be canceled and no new deployments will be created.</span></span>

## <span data-ttu-id="3fecd-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3fecd-111">EXAMPLES</span></span>

### <span data-ttu-id="3fecd-112">Beispiel 1: Abbrechen einer Richtlinien Bereinigung im Bereich der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="3fecd-112">Example 1: Cancel a policy remediation at resource group scope</span></span>
```
PS C:\> Stop-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="3fecd-113">Mit diesem Befehl wird die Bereinigung mit dem Namen "remediation1" in der Ressourcengruppe "myRG" abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="3fecd-113">This command cancels the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="3fecd-114">Beispiel 2: Abbrechen einer Verwaltungsgruppen Bereinigung über Rohre</span><span class="sxs-lookup"><span data-stu-id="3fecd-114">Example 2: Cancel a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Stop-AzPolicyRemediation
```

<span data-ttu-id="3fecd-115">Mit diesem Befehl wird die Bereinigung mit dem Namen "remediation1" in der Verwaltungsgruppe "mg1" abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="3fecd-115">This command cancels the remediation named 'remediation1' in management group 'mg1'.</span></span>

## <span data-ttu-id="3fecd-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="3fecd-116">PARAMETERS</span></span>

### <span data-ttu-id="3fecd-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3fecd-117">-AsJob</span></span>
<span data-ttu-id="3fecd-118">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="3fecd-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="3fecd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fecd-119">-DefaultProfile</span></span>
<span data-ttu-id="3fecd-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3fecd-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fecd-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3fecd-121">-InputObject</span></span>
<span data-ttu-id="3fecd-122">Das Behebungs Objekt.</span><span class="sxs-lookup"><span data-stu-id="3fecd-122">The Remediation object.</span></span>

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

### <span data-ttu-id="3fecd-123">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="3fecd-123">-ManagementGroupName</span></span>
<span data-ttu-id="3fecd-124">Verwaltungsgruppen-ID.</span><span class="sxs-lookup"><span data-stu-id="3fecd-124">Management group ID.</span></span>

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

### <span data-ttu-id="3fecd-125">-Name</span><span class="sxs-lookup"><span data-stu-id="3fecd-125">-Name</span></span>
<span data-ttu-id="3fecd-126">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="3fecd-126">Resource name.</span></span>

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

### <span data-ttu-id="3fecd-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3fecd-127">-PassThru</span></span>
<span data-ttu-id="3fecd-128">Gibt "true" zurück, wenn der Befehl erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="3fecd-128">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="3fecd-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fecd-129">-ResourceGroupName</span></span>
<span data-ttu-id="3fecd-130">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3fecd-130">Resource group name.</span></span>

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

### <span data-ttu-id="3fecd-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3fecd-131">-ResourceId</span></span>
<span data-ttu-id="3fecd-132">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="3fecd-132">Resource ID.</span></span>

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

### <span data-ttu-id="3fecd-133">-Scope</span><span class="sxs-lookup"><span data-stu-id="3fecd-133">-Scope</span></span>
<span data-ttu-id="3fecd-134">Der Bereich der Ressource.</span><span class="sxs-lookup"><span data-stu-id="3fecd-134">Scope of the resource.</span></span>
<span data-ttu-id="3fecd-135">Z.b..</span><span class="sxs-lookup"><span data-stu-id="3fecd-135">E.g.</span></span>
<span data-ttu-id="3fecd-136">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="3fecd-136">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="3fecd-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3fecd-137">-Confirm</span></span>
<span data-ttu-id="3fecd-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3fecd-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fecd-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fecd-139">-WhatIf</span></span>
<span data-ttu-id="3fecd-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3fecd-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fecd-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3fecd-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fecd-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fecd-142">CommonParameters</span></span>
<span data-ttu-id="3fecd-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fecd-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fecd-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fecd-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fecd-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3fecd-145">INPUTS</span></span>

### <span data-ttu-id="3fecd-146">System. String</span><span class="sxs-lookup"><span data-stu-id="3fecd-146">System.String</span></span>

### <span data-ttu-id="3fecd-147">Microsoft. Azure. Commands. PolicyInsights. Models. Remediation. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="3fecd-147">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="3fecd-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3fecd-148">OUTPUTS</span></span>

### <span data-ttu-id="3fecd-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3fecd-149">System.Boolean</span></span>

## <span data-ttu-id="3fecd-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="3fecd-150">NOTES</span></span>

## <span data-ttu-id="3fecd-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3fecd-151">RELATED LINKS</span></span>
